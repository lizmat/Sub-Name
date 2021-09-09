[![Actions Status](https://github.com/lizmat/Sub-Name/workflows/test/badge.svg)](https://github.com/lizmat/Sub-Name/actions)

NAME
====

Raku port of Perl's Sub::Name module

SYNOPSIS
========

    use Sub::Name;

    subname $name, $callable;

    $callable = subname foo => { ... };

DESCRIPTION
===========

This module tries to mimic the behaviour of Perl's `Sub::Name` module as closely as possible in the Raku Programming Language.

This module has only one function, which is also exported by default:

subname NAME, CALLABLE

Assigns a new name to referenced Callable. If package specification is omitted in the name, then the current package is used. The return value is the Callable.

The name is only used for informative routines. You won't be able to actually invoke the Callable by the given name. To allow that, you need to do assign it to a &-sigilled variable yourself.

Note that for anonymous closures (Callables that reference lexicals declared outside the Callable itself) you can name each instance of the closure differently, which can be very useful for debugging.

AUTHOR
======

Elizabeth Mattijsen <liz@raku.rocks>

Re-imagined from the Perl version as part of the CPAN Butterfly Plan. Perl version originally developed by Matthijs van Duin.

COPYRIGHT AND LICENSE
=====================

Copyright 2018, 2019, 2020, 2021 Elizabeth Mattijsen

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

