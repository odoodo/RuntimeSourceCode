Extracts the source code of a deployed channel component from the script cache of Mirth

**Purpose:**<br/>
This code template provides the source code with all attached code templates and internal logic that is added by Mirth. This can be used to understand the internal working, gain an overview of the complete transformer code and of course for debugging. Line numbers are identical to the ones indicated by mirth in case of an exception.

**How to use:**<br/>
simply import the code template attached below and call it in a transformer step.
To get the source code of the current component:
```js
var sourceCode = getSourceCode();
```
To get the source code with line numbers
```js
var sourceCodeWithLineNumbers = getSourceCode(true);
```

**How it works:**<br/>
The reference to the current script is not accessible. However, when a Rhino exception is thrown, it contains the reference to the current script. Thus, an exception is provoked, the reference is read from the exception and the source code is taken from the code cache.
