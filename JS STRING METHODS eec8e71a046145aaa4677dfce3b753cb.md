# JS STRING METHODS

### 1.JavaScript String Length

The `length` property returns the length of a string

### 2.**JavaScript String slice()**

`slice()` extracts a part of a string and returns the extracted part in a new string.

The method takes 2 parameters: start position, and end position (end not included).

# Note

JavaScript counts positions from zero.

First position is 0.

Second position is 1.

If a parameter is negative, the position is counted from the end of the string

If you omit the second parameter, the method will slice out the rest of the string

### 3.**JavaScript String substring()**

`substring()` is similar to `slice()`.

The difference is that start and end values less than 0 are treated as 0 in `substring()`.

### 4.**JavaScript String substr()**

`substr()` is similar to `slice()`.

The difference is that the second parameter specifies the **length** of the extracted part.

### 5.**Replacing String Content**

The `replace()` method replaces a specified value with another value in a string:

```html
let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");
```

By default, the `replace()` method is case sensitive. Writing MICROSOFT (with upper-case) will not work:

To replace case insensitive, use a **regular expression** with an `/i` flag (insensitive):

### 6.**JavaScript String ReplaceAll()**

The `replaceAll()` method allows you to specify a regular expression instead of a string to be replaced.

If the parameter is a regular expression, the global flag (g) must be set, otherwise a TypeError is thrown.

### 7.**Converting to Upper and Lower Case**

A string is converted to upper case with `toUpperCase()`:

A string is converted to lower case with `toLowerCase()`:

### 8.**JavaScript String concat()**

`concat()` joins two or more strings:

The `concat()` method can be used instead of the plus operator.

### 9.**JavaScript String trim()**

The `trim()` method removes whitespace from both sides of a string:

### 10.**JavaScript String trimStart() & trimEnd()**

The `trimStart()` method works like `trim()`, but removes whitespace only from the start of a string.

The `trimEnd()` method works like `trim()`, but removes whitespace only from the end of a string.

### 11.**JavaScript String Padding**

`padStart()` and `padEnd()` to support padding at the beginning and at the end of a string.

The `padStart()` method pads a string from the start.

It pads a string with another string (multiple times) until it reaches a given length.

The `padEnd()` method pads a string from the end.

It pads a string with another string (multiple times) until it reaches a given length.

### 12.**Extracting String Characters**

1. **JavaScript String charAt()**

The `charAt()` method returns the character at a specified index (position) in a string:

1. **JavaScript String charCodeAt()**

he `charCodeAt()` method returns the unicode of the character at a specified index in a string:

The method returns a UTF-16 code (an integer between 0 and 65535).

1. **Property Access**

allows property access on strings:

### 13.**Converting a String to an Array**

If you want to work with a string as an array, you can convert it to an array.

A string can be converted to an array with the `split()` method:

```html
text.split(",")    // Split on commas
text.split(" ")    // Split on spaces
text.split("|")    // Split on pipe
```

### **JavaScript Arrow Function**

Arrow functions allow us to write shorter function syntax:

You don't need the `function` keyword, the `return` keyword, and the **curly brackets**.

```html
let myFunction = (a, b) => a * b;
```

It gets shorter! If the function has only one statement, and the statement returns a value, you can remove the brackets *and* the `return` keyword:

### normal function declaration

```html
function functionName(parameters) {
  // code to be executed
}
```

```html
const x = function (a, b) {return a * b};
let z = x(4, 3);
```

The function above is actually an anonymous **function** (a function without a name).