# PHP / SYMFONY Exceptions

## Docs

- https://gist.github.com/feyyazesat/c65ccfde12839c03c610 (Symfony Exception List)
- https://www.strangebuzz.com/en/blog/the-php-exceptions-cheatsheet (The PHP exceptions' cheat sheet )
- https://docs.w3cub.com/symfony~4.1/symfony/component/security/core/exception/accessdeniedexception (Exception details)

## Notes

- As of PHP 7, errors and exceptions extend the Throwable class

```
{
    Throwable: {
        Error: {
            ArithmeticError: [
                "DivisionByZeroError"
            ],
            AssertionError: [],
            CompileError: [
                "ParseError"
            ],
            TypeError: [
                "ArgumentCountError"
            ]
        },
        Exception: {
            ClosedGeneratorException: [],
            DOMException: [],
            ErrorException: [],
            IntlException: [],
            JsonException: [],
            LogicException: {
                BadFunctionCallException: [
                    "BadMethodCallException"
                ],
                DomainException: [],
                InvalidArgumentException: [],
                LengthException: [],
                OutOfRangeException: []
            },
            PharException: [],
            ReflectionException: [],
            RuntimeException: [
                "OutOfBoundsException",
                "OverflowException",
                "PDOException",
                "RangeException",
                "UnderflowException",
                "UnexpectedValueException"
            ],
            SoapFault: [],
            SodiumException: []
        }
    }
}
```

- **\Throwable** - Throwable is the base interface for any object that can be thrown via a throw statement, including Error and Exception.
<br>

- **\Error** - Error is the base class for all internal PHP errors.
<br>

- **\ArithmeticError** - Thrown when an error occurs while performing mathematical operations.
<br>

- **\DivisionByZeroError** - Thrown when an attempt is made to divide a number by zero.
<br>

- **\AssertionError** - Thrown when an assertion made via assert() fails.
<br>

- **\CompileError** - Thrown for some compilation errors, which formerly issued a fatal error.
<br>

- **\TypeError** 
    - The value being set for a class property does not match the property's corresponding declared type.
    - The argument type being passed to a function does not match its corresponding declared parameter type.
    - A value being returned from a function does not match the declared function return type.
<br>

- **\Exception** - Exception is the base class for all user exceptions.
<br>

- **\ClosedGeneratorException** - occurs when attempting to perform a traversal on a generator that has already been closed or terminated.
<br>

- **\DOMException** - DOM operations raise exceptions under particular circumstances, i.e., when an operation is impossible to perform for logical reasons.
<br>

- **\ErrorException** - ErrorException is mostly used to convert php error (raised by error_reporting) to Exception.
<br>

- **\IntlException** - This class is used for generating exceptions when errors occur inside intl functions. Such exceptions are only generated when intl.use_exceptions is enabled.
<br>


- **\JsonException** - Exception thrown if JSON_THROW_ON_ERROR option is set for json_encode() or json_decode(). code contains the error type, for possible values see json_last_error().
<br>


- **\LogicException** - Exception that represents error in the program logic. This kind of exception should lead directly to a fix in your code.
<br>

- **\BadFunctionCallException** - Exception thrown if a callback refers to an undefined function or if some arguments are missing.
<br>

- **\BadMethodCallException** - Exception thrown if a callback refers to an undefined method or if some arguments are missing.
<br>

- **\DomainException** - Exception thrown if a value does not adhere to a defined valid data domain.
<br>

- **\InvalidArgumentException** - Exception thrown if an argument is not of the expected type.
<br>

- **\LengthException** - Exception thrown if a length is invalid.
<br>

- **\OutOfRangeException** - Exception thrown when an illegal index was requested. This represents errors that should be detected at compile time.
<br>

- **\PharException** - The PharException class provides a phar-specific exception class for try/catch blocks.
<br>

- **\ReflectionException** - The ReflectionException class.
<br>

- **\RuntimeException** - Exception thrown if an error which can only be found on runtime occurs.
<br>

- **\OutOfBoundsException** - Exception thrown if a value is not a valid key. This represents errors that cannot be detected at compile time.
<br>

- **\OverflowException** - Exception thrown when adding an element to a full container.
<br>

- **\PDOException** - Represents an error raised by PDO. You should not throw a PDOException from your own code. See Exceptions for more information about Exceptions in PHP.
<br>

- **\RangeException** - Exception thrown to indicate range errors during program execution. Normally this means there was an arithmetic error other than under/overflow. This is the runtime version of DomainException.
<br>

- **\UnderflowException** - Exception thrown when performing an invalid operation on an empty container, such as removing an element.
<br>

- **\UnexpectedValueException** - Exception thrown if a value does not match with a set of values. Typically this happens when a function calls another function and expects the return value to be of a certain type or value not including arithmetic or buffer related errors.
<br>

- **\SoapFault** - 	This class is used to send SOAP fault responses from the PHP handler. faultcode, faultstring, faultactor and detail are standard elements of a SOAP Fault.
<br>

- **\SodiumException** - Exceptions thrown by the sodium functions.
<br>

---

### Symfony

- **MissingOptionsException** - Exception thrown when a required option is missing.
- **InvalidOptionsException** - Thrown when the value of an option does not match its validation rules.
- **MethodNotAllowedHttpException**
- **NotFoundHttpException**
- **HttpException**
- **AccessDeniedHttpException**