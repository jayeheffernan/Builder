<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Syntax](#syntax)
  - [Directives](#directives)
    - [@set](#@set)
    - [@macro](#@macro)
    - [@if – @elseif – @else](#@if-%E2%80%93-@elseif-%E2%80%93-@else)
    - [@{...} (inline expressions)](#@-inline-expressions)
    - [@error](#@error)
    - [@include](#@include)
      - [Local Files](#local-files)
      - [Remote Locations](#remote-locations)
      - [Git Repositories](#git-repositories)
  - [Comments](#comments)
  - [Expressions](#expressions)
    - [Types](#types)
    - [Operators](#operators)
      - [Binary Operators](#binary-operators)
      - [Unary Operators](#unary-operators)
    - [Member Expressions](#member-expressions)
    - [Conditional Expressions](#conditional-expressions)
    - [Variables](#variables)
    - [Functions](#functions)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


<br /><img src=docs/logo.png width=200 alt=Builder><br /><br />

_Builder_ language combines a preprocessor with an expression language and advanced importing.

_Please note that this is in-progress version and published here for preview only._

# Syntax

## Directives

Directives start with __@__ symbol.

### @set

```sass
@set variable_name expression
// or
@set variable_name = expression
```

Assigns a result of an expression to a variable.

Example:

```sass
@set MY_VAR min(1, 2, 3) // sets MY_VAR to 1
```

### @macro

### @if – @elseif – @else

### @{...} (inline expressions)

### @error

### @include

#### Local Files
#### Remote Locations
#### Git Repositories

## Comments

Directives can contain both `//`- and `/* */`-style comments.

## Expressions

### Types

The following types are supported in expressions:

- _numbers_ (eg: `1`,`1E6`, `1e-6`, `1.567`)
- _strings_ (eg: `"abc"`, `'abc'`)
- `null`
- `true`
- `false`

### Operators

#### Binary Operators

`|| && == != < > <= >= + - * / %`

#### Unary Operators

`+ - !`

### Member Expressions

- `somevar.member`
- `somevar["member"]`
- `([1, 2, 3])[1]`

### Conditional Expressions

`test ? consequent : alternate`

### Variables

Variables defined by `@set` statements are available in expressions. Undefined variables are evaluated as `null`.

### Functions

- `min(<numbers>)`
- `max(<numbers>)`
- `abs(<number>)`
- `defined(<variable_name>)` – returns `true` if _<variable_name>_ is defined or `false` otherwise.

# License

MIT
