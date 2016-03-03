# AssertJS

Assertion library written in ES6 for nodejs.

## Installation

```
npm install assert-js --save
```

> Keep dependencies like this one installed per project.

## Contributing

Clone repository and install dependencies

```
git clone git@github.com:Tiliqua/assert-js.git
cd assert-js
npm install
```

In order to execute tests run

```
npm test
```

Before commiting changes make sure that code is transpiled to ES5

```
npm run build
```

## Usage

```
var Assert = require('assert-js');

Assert.string("test"); // everything is fine
Assert.string(1); // Expected string but got "int[1]". - error thrown
```

## Available assertions:

```
Assert.instanceOf(objectValue, instance)

// example

var string = new String("this is string object");
Assert.instanceOf(string, String);
```

```
Assert.containsOnly(arrayValue, expectedInstance)

// example

var arrayOfStrings = [];
arrayOfStrings.push(new String("test 1"));
arrayOfStrings.push(new String("test 2"));
Assert.containsOnly(arrayOfStrings, String);
```

```
Assert.integer(integerValue)

// example

var integerValue = 1;
Assert.integer(integerValue);
```

```
Assert.number(numberValue)

// example

var integerValue = 1;
var floatValue = 0.5;
Assert.integer(integerValue);
Assert.integer(floatValue);
```

```
Assert.oddNumber(integerValue)

// example

var integerValue = 3;
Assert.oddNumber(integerValue);
```

```
Assert.greaterThan(requiredTreshold, integerValue)

// example

var integerValue = 0;
Assert.greaterThan(1, integerValue)
```

```
Assert.string(stringValue)

// example

var stringValue = "string";
Assert.integer(stringValue);
```

```
Assert.boolean(booleanValue)

// example

var boolValue = true;
Assert.integer(boolValue);
```

```
Assert.object(objectValue)

// example

var objectValue = {};
Assert.integer(objectValue);
```

```
Assert.isFunction(functionValue)

// example

var simpleFunction = function() {};
Assert.isFunction(simpleFunction);
```

```
Assert.array(arrayValue)

// example

var arrayValue = [];
Assert.integer(arrayValue);
```

```
Assert.count(expectedCount, arrayValue)

// example

var arrayValue = [];
Assert.count(0, arrayValue);
```

```
Assert.notEmpty(value)

// example

var arrayValue = [1, 2, 3];
Assert.notEmpty(0, arrayValue);
```

