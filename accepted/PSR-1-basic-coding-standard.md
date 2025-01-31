# Basic Coding Standard

This section of the standard comprises what should be considered the standard
coding elements that are required to ensure a high level of technical
interoperability between shared PHP code.

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD",
"SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be
interpreted as described in [RFC 2119].

[RFC 2119]: http://www.ietf.org/rfc/rfc2119.txt
[PSR-0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[PSR-4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md

## 1. Overview

- [x] Files MUST use only `<?php` and `<?=` tags.

- [x] Files MUST use only UTF-8 without BOM for PHP code.

- [x] Files SHOULD *either* declare symbols (classes, functions, constants, etc.) *or* cause side-effects (e.g. generate output,
  change .ini settings, etc.) but SHOULD NOT do both.

- [x] Namespaces and classes MUST follow recommendations in [PSR4].

- [x] Class names MUST be declared in `StudlyCaps`.

- [x] Class constants MUST be declared in all upper case with underscore separators.

- [x] Method names MUST be declared either in `snake_case` or in `camelCase`.

## 2. Files

### 2.1. PHP Tags

- [x] PHP code MUST use the long `<?php ?>` tags or the short-echo `<?= ?>` tags; it MUST NOT use the other tag variations.

### 2.2. Character Encoding

- [x] PHP code MUST use only UTF-8 without BOM.

### 2.3. Side Effects

- [x] A file SHOULD declare new symbols (classes, functions, constants, etc.) and cause no other side effects, or it SHOULD
  execute logic with side effects, but SHOULD NOT do both.

*Note*: The term "side effects" means execution of logic not directly related to declaring classes, functions, constants, etc.,
*merely from including the file*.

Side effects include but are not limited to: generating output, explicit use of `require` or `include`, connecting to external
services, modifying ini settings, emitting errors or exceptions, modifying global or static variables, reading from or writing to
a file, and so on.

The following is an example of a file with both declarations and side effects;
i.e, an example of what to avoid:

``` {.php}
<?php
// side effect: change ini settings
ini_set('error_reporting', E_ALL);

// side effect: loads a file
include "file.php";

// side effect: generates output
echo "<html>\n";

// declaration
function foo() {
    // function body
}
```

The following example is of a file that contains declarations without side
effects; i.e., an example of what to emulate:

``` {.php}
<?php
// declaration
function foo() {
    // function body
}

// conditional declaration is *not* a side effect
if (! function_exists('bar')) function bar () {
    // function body
}
```

## 3. Namespace and Class Names

- [x] Namespaces and classes MUST follow "autoloading" PSR4.

    This means each class is in a file by itself, and is in a namespace of at least one level: a top-level vendor name.

- [x] Class names MUST be declared in `StudlyCaps`.

- [x] Code MUST use formal namespaces.

For example:

``` {.php}
<?php namespace Vendor\Model;

class Foo {
}
```

## 4. Class constants, properties, and methods

The term "class" refers to all classes, interfaces, and traits.

### 4.1. Constants

- [x] Class constants MUST be declared in all upper case with underscore separators.
For example:

``` {.php}
<?php namespace Vendor\Model;

class Foo {
    const VERSION = '1.0';
    const DATE_APPROVED = '2012-06-01';
}
```

### 4.2. Properties

This guide intentionally avoids any recommendation regarding the use of
`$StudlyCaps`, `$camelCase`, or `$under_score` property names.

Whatever naming convention is used SHOULD be applied consistently within a
reasonable scope. That scope may be vendor-level, package-level, class-level,
or method-level.

### 4.3. Methods

- [x] Method names MUST be declared either in `snake_case()` or in `camelCase()`.

