PSR-1 Coding Standard
=====================

A CodeSniffer sniff to check against the [PSR-1 Coding Standard](https://github.com/pmjones/fig-standards/blob/psr-1-style-guide/proposed/PSR-1.md)


Overview
--------

- Use only `<?php` and `<?=` opening tags for PHP code; leave out the closing
  `?>` tag when the file contains only PHP code.

- Use 4 spaces for indenting, not tabs.

- There is no hard limit on line length; the soft limit is 120 characters;
  lines of 80 characters or less are encouraged. Do not add trailing
  whitespace at the end of lines. Use Unix line endings (LF).

- Namespace all classes; place one blank line after the `namespace`
  declaration, and one blank line after the block of `use` declarations.

- Declare class names in `StudlyCaps`; opening braces for classes go on the
  next line, and closing braces go on their own line.

- Declare method names in `camelCase`; opening braces for methods go on the
  next line, and closing braces go on their own line.

- Declare visibility on all properties and methods; declare `abstract` and
  `final` before the visibility, and declare `static` after the visibility.
  
- Control structure keywords have one space after them; function and method
  calls do not.

- Opening braces for control structures go on the same line, and closing
  braces go on their own line.

- Opening parentheses for control structures have no space after them, and
  closing parentheses for control structures have no space before.
  
- Check the [official guide](https://github.com/pmjones/fig-standards/blob/psr-1-style-guide/proposed/PSR-1.md) for more information.

How to use
----------

1. Install CodeSniffer:

        pear install PHP_CodeSniffer

2. Clone this repository to a folder called PSR inside your CodeSniffer
   Standards directory (eg.: /usr/share/php/PHP/CodeSniffer/Standards)

        cd /usr/share/php/PHP/CodeSniffer/Standards
        git clone https://github.com/klaussilveira/phpcs-psr1 PSR

3. Set PSR-1 as the default sniff for CodeSniffer:

        phpcs --config-set default_standard PSR
