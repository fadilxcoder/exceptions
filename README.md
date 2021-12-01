# PHP / SYMFONY Exceptions

## Docs

- https://gist.github.com/feyyazesat/c65ccfde12839c03c610 (Symfony Exception List)
- https://www.strangebuzz.com/en/blog/the-php-exceptions-cheatsheet (The PHP exceptions' cheat sheet )
- https://docs.w3cub.com/symfony~4.1/symfony/component/security/core/exception/accessdeniedexception (Exception details)
- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/index.html (Symfony classes namespaces)

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

---

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/OptionsResolver/Exception.html
```
Symfony/Component/OptionsResolver/Exception/MissingOptionsException.php
Symfony/Component/OptionsResolver/Exception/OptionDefinitionException.php
Symfony/Component/OptionsResolver/Exception/InvalidOptionsException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Serializer/Exception.html
```
Symfony/Component/Serializer/Exception/InvalidArgumentException.php
Symfony/Component/Serializer/Exception/UnsupportedException.php
Symfony/Component/Serializer/Exception/UnexpectedValueException.php
Symfony/Component/Serializer/Exception/LogicException.php
Symfony/Component/Serializer/Exception/Exception.php
Symfony/Component/Serializer/Exception/RuntimeException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/HttpKernel/Exception.html
```
Symfony/Component/HttpKernel/Exception/MethodNotAllowedHttpException.php
Symfony/Component/HttpKernel/Exception/NotFoundHttpException.php
Symfony/Component/HttpKernel/Exception/HttpException.php
Symfony/Component/HttpKernel/Exception/AccessDeniedHttpException.php
Symfony/Component/HttpKernel/Exception/FlattenException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Form/Exception.html
```
Symfony/Component/Form/Exception/InvalidConfigurationException.php
Symfony/Component/Form/Exception/TransformationFailedException.php
Symfony/Component/Form/Exception/PropertyAccessDeniedException.php
Symfony/Component/Form/Exception/TypeLoaderException.php
Symfony/Component/Form/Exception/NotInitializedException.php
Symfony/Component/Form/Exception/NotValidException.php
Symfony/Component/Form/Exception/AlreadyBoundException.php
Symfony/Component/Form/Exception/InvalidPropertyPathException.php
Symfony/Component/Form/Exception/CreationException.php
Symfony/Component/Form/Exception/StringCastException.php
Symfony/Component/Form/Exception/FormException.php
Symfony/Component/Form/Exception/TypeDefinitionException.php
Symfony/Component/Form/Exception/UnexpectedTypeException.php
Symfony/Component/Form/Exception/ErrorMappingException.php
Symfony/Component/Form/Exception/InvalidPropertyException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Process/Exception.html
```
Symfony/Component/Process/Exception/ProcessFailedException.php
Symfony/Component/Process/Exception/RuntimeException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Yaml/Exception.html
```
Symfony/Component/Yaml/Exception/DumpException.php
Symfony/Component/Yaml/Exception/ParseException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Filesystem/Exception.html
```
Symfony/Component/Filesystem/Exception/IOException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/HttpFoundation/File/Exception.html
```
Symfony/Component/HttpFoundation/File/Exception/AccessDeniedException.php
Symfony/Component/HttpFoundation/File/Exception/FileNotFoundException.php
Symfony/Component/HttpFoundation/File/Exception/UnexpectedTypeException.php
Symfony/Component/HttpFoundation/File/Exception/UploadException.php
Symfony/Component/HttpFoundation/File/Exception/FileException.php
```

-http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/DependencyInjection/Exception.html
```
Symfony/Component/DependencyInjection/Exception/InvalidArgumentException.php
Symfony/Component/DependencyInjection/Exception/ParameterNotFoundException.php
Symfony/Component/DependencyInjection/Exception/LogicException.php
Symfony/Component/DependencyInjection/Exception/OutOfBoundsException.php
Symfony/Component/DependencyInjection/Exception/BadMethodCallException.php
Symfony/Component/DependencyInjection/Exception/ServiceNotFoundException.php
Symfony/Component/DependencyInjection/Exception/RuntimeException.php
Symfony/Component/DependencyInjection/Exception/ServiceCircularReferenceException.php
Symfony/Component/DependencyInjection/Exception/InactiveScopeException.php
Symfony/Component/DependencyInjection/Exception/ParameterCircularReferenceException.php
Symfony/Component/DependencyInjection/Exception/ScopeCrossingInjectionException.php
Symfony/Component/DependencyInjection/Exception/ScopeWideningInjectionException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Config/Exception.html
```
Symfony/Component/Config/Exception/FileLoaderImportCircularReferenceException.php
Symfony/Component/Config/Exception/FileLoaderLoadException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Config/Definition/Exception.html
```
Symfony/Component/Config/Definition/Exception/InvalidConfigurationException.php
Symfony/Component/Config/Definition/Exception/ForbiddenOverwriteException.php
Symfony/Component/Config/Definition/Exception/UnsetKeyException.php
Symfony/Component/Config/Definition/Exception/Exception.php
Symfony/Component/Config/Definition/Exception/InvalidDefinitionException.php
Symfony/Component/Config/Definition/Exception/InvalidTypeException.php
Symfony/Component/Config/Definition/Exception/DuplicateKeyException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Routing/Exception.html
```
Symfony/Component/Routing/Exception/InvalidParameterException.php
Symfony/Component/Routing/Exception/ResourceNotFoundException.php
Symfony/Component/Routing/Exception/MissingMandatoryParametersException.php
Symfony/Component/Routing/Exception/RouteNotFoundException.php
Symfony/Component/Routing/Exception/MethodNotAllowedException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Validator/Exception.html
```
Symfony/Component/Validator/Exception/MappingException.php
Symfony/Component/Validator/Exception/MissingOptionsException.php
Symfony/Component/Validator/Exception/GroupDefinitionException.php
Symfony/Component/Validator/Exception/ConstraintDefinitionException.php
Symfony/Component/Validator/Exception/UnexpectedTypeException.php
Symfony/Component/Validator/Exception/InvalidOptionsException.php
Symfony/Component/Validator/Exception/ValidatorException.php
```

```
Symfony/Component/Locale/Exception/MethodArgumentValueNotImplementedException.php
Symfony/Component/Locale/Exception/MethodArgumentNotImplementedException.php
Symfony/Component/Locale/Exception/MethodNotImplementedException.php
Symfony/Component/Locale/Exception/NotImplementedException.php
```

-http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/CssSelector/Exception.html
```
Symfony/Component/CssSelector/Exception/ParseException.php
```

- http://man.hubwiz.com/docset/Symfony.docset/Contents/Resources/Documents/packagist_docset/Symfony/Component/Security/Core/Exception.html
```
Symfony/Component/Security/Core/Exception/SessionUnavailableException.php
Symfony/Component/Security/Core/Exception/AuthenticationException.php
Symfony/Component/Security/Core/Exception/UnsupportedUserException.php
Symfony/Component/Security/Core/Exception/AccessDeniedException.php
Symfony/Component/Security/Core/Exception/CredentialsExpiredException.php
Symfony/Component/Security/Core/Exception/UsernameNotFoundException.php
Symfony/Component/Security/Core/Exception/LogoutException.php
Symfony/Component/Security/Core/Exception/CookieTheftException.php
Symfony/Component/Security/Core/Exception/InsufficientAuthenticationException.php
Symfony/Component/Security/Core/Exception/DisabledException.php
Symfony/Component/Security/Core/Exception/InvalidCsrfTokenException.php
Symfony/Component/Security/Core/Exception/LockedException.php
Symfony/Component/Security/Core/Exception/AuthenticationServiceException.php
Symfony/Component/Security/Core/Exception/AuthenticationCredentialsNotFoundException.php
Symfony/Component/Security/Core/Exception/TokenNotFoundException.php
Symfony/Component/Security/Core/Exception/AccountExpiredException.php
Symfony/Component/Security/Core/Exception/NonceExpiredException.php
Symfony/Component/Security/Core/Exception/AccountStatusException.php
Symfony/Component/Security/Core/Exception/ProviderNotFoundException.php
Symfony/Component/Security/Core/Exception/BadCredentialsException.php
```
```
Symfony/Component/Security/Acl/Exception/SidNotLoadedException.php
Symfony/Component/Security/Acl/Exception/AclNotFoundException.php
Symfony/Component/Security/Acl/Exception/NotAllAclsFoundException.php
Symfony/Component/Security/Acl/Exception/InvalidDomainObjectException.php
Symfony/Component/Security/Acl/Exception/NoAceFoundException.php
Symfony/Component/Security/Acl/Exception/Exception.php
Symfony/Component/Security/Acl/Exception/ConcurrentModificationException.php
Symfony/Component/Security/Acl/Exception/AclAlreadyExistsException.php
```
- Doctrine

```
Doctrine/Common/DataFixtures/Exception/CircularReferenceException.php
Doctrine/Common/Annotations/AnnotationException.php
Doctrine/Common/CommonException.php
Doctrine/Common/Persistence/Mapping/MappingException.php
---------------------------------------------------------------------------------------------

Doctrine/ORM/TransactionRequiredException.php
Doctrine/ORM/Query/QueryException.php
Doctrine/ORM/Query/AST/ASTException.php
Doctrine/ORM/Mapping/MappingException.php
Doctrine/ORM/UnexpectedResultException.php
Doctrine/ORM/PessimisticLockException.php
Doctrine/ORM/OptimisticLockException.php
Doctrine/ORM/Internal/Hydration/HydrationException.php
Doctrine/ORM/ORMException.php
Doctrine/ORM/NonUniqueResultException.php
Doctrine/ORM/EntityNotFoundException.php
Doctrine/ORM/Tools/ToolsException.php
Doctrine/ORM/Tools/Export/ExportException.php
Doctrine/ORM/Proxy/ProxyException.php
Doctrine/ORM/NoResultException.php
Doctrine/ORM/ORMInvalidArgumentException.php
---------------------------------------------------------------------------------------------

Doctrine/DBAL/Query/QueryException.php
Doctrine/DBAL/Types/ConversionException.php
Doctrine/DBAL/Schema/SchemaException.php
Doctrine/DBAL/Sharding/ShardingException.php
Doctrine/DBAL/ConnectionException.php
Doctrine/DBAL/Cache/CacheException.php
Doctrine/DBAL/Driver/OCI8/OCI8Exception.php
Doctrine/DBAL/Driver/SQLSrv/SQLSrvException.php
Doctrine/DBAL/Driver/Mysqli/MysqliException.php
Doctrine/DBAL/Driver/IBMDB2/DB2Exception.php
Doctrine/DBAL/DBALException.php
```