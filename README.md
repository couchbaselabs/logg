A lightweight logging utility for Go.

![screnshot](http://cl.ly/image/2l0Q1M123D1c/Screen%20Shot%202013-09-14%20at%2012.28.07%20PM.png)

# Features

* Simple log levels (1 == regular logs, 2 == warnings, 3+ == panics)
* Keyword based log partitioning.  Eg, define a "REST" keyword for all REST related logs.
* Log Timestamp which includes microseconds
* Terminal color coded logs

# How to use Logg in your project

Import:

```
import "github.com/couchbaselabs/logg"
```

Log something:

```
logg.Log("hello")

```

Setup keyword based log partitioning:

```
logg.LogKeys["foo"] = true
```

Log something to the "foo" channel:

```
logg.LogTo("foo", "hello foo")

```

Increase log level to only include panics:

```
logg.LogLevel = logg.LOG_LEVEL_PANICS
```






