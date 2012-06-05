CodeSniffer for PSR's
=========================

This is a PHP_CodeSniffer sniff to check against the PHP Standard Resolutions: [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md), [PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md) and [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md). Those standards were approved by the [PHP Framework Interoperability Group](https://github.com/php-fig/fig-standards).

You can read more about the PHP FIG and the PSR's on this [excellent article](http://paul-m-jones.com/archives/2420) by Paul Jones.

PSR-1 Overview
-----------

- Files MUST use only `<?php` and `<?=` tags.

- Files MUST use only UTF-8 without BOM for PHP code.

- Files SHOULD *either* declare symbols (classes, functions, constants, etc.)
  *or* cause side-effects (e.g. generate output, change .ini settings, etc.)
  but SHOULD NOT do both.

- Namespaces and classes MUST follow [PSR-0](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md).

- Class names MUST be declared in `StudlyCaps`.

- Class constants MUST be declared in all upper case with underscore separators.

- Method names MUST be declared in `camelCase`.


PSR-2 Overview
--------------

- Code MUST follow [PSR-1](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md).

- Code MUST use 4 spaces for indenting, not tabs.

- There MUST NOT be a hard limit on line length; the soft limit MUST be 120
  characters; lines SHOULD be 80 characters or less.

- There MUST be one blank line after the `namespace` declaration, and there
  MUST be one blank line after the block of `use` declarations.

- Opening braces for classes MUST go on the next line, and closing braces MUST
  go on the next line after the body.

- Opening braces for methods MUST go on the next line, and closing braces MUST
  go on the next line after the body.

- Visibility MUST be declared on all properties and methods; `abstract` and
  `final` MUST be declared before the visibility; `static` MUST be declared
  after the visibility.
  
- Control structure keywords MUST have one space after them; method and
  function calls MUST NOT.

- Opening braces for control structures MUST go on the same line, and closing
  braces MUST go on the next line after the body.

- Opening parentheses for control structures MUST NOT have a space after them,
  and closing parentheses for control structures MUST NOT have a space before.


How to use
----------

1. Install CodeSniffer:

        pear install PHP_CodeSniffer

2. Clone this repository to a folder called PSR inside your CodeSniffer
   Standards directory (eg.: /usr/share/php/PHP/CodeSniffer/Standards)

        cd /usr/share/php/PHP/CodeSniffer/Standards
        git clone https://github.com/klaussilveira/phpcs-psr PSR

3. Set PSR as the default sniff for CodeSniffer:

        phpcs --config-set default_standard PSR
