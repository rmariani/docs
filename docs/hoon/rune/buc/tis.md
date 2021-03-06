---
navhome: /docs/
next: true
sort: 8
title: $= "buctis"
---

# `$= "buctis"`

`[%bcts p=@tas q=model]`: mold which wraps a face around another mold.

## Expands to

```
|=  *
^=(p %-(q +6))
```

## Syntax

Regular: *2-fixed*.

Irregular (mold mode): `foo=bar` is `$=(foo bar)`.

## Discussion

Note that the Hoon compiler is at least slightly clever about
compiling molds, and almost never has to actually put in a gate
layer (as seen in the expansion above) to apply a `$=`.

## Examples

```
~zod:dojo> =a $=(p %foo)

~zod:dojo> (a %foo)
p=%foo

~zod:dojo> (a %bar)
p=%foo
```
