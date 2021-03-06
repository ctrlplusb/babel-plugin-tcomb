# Changelog

> **Tags:**
> - [New Feature]
> - [Bug Fix]
> - [Breaking Change]
> - [Documentation]
> - [Internal]
> - [Polish]
> - [Experimental]

**Note**: Gaps between patch versions are faulty/broken releases.
**Note**: A feature tagged as Experimental is in a high state of flux, you're at risk of it changing without notice.

## v0.2.2

- **New Feature**
  - support alternative format for default param type annotations, fix #18
  - "require" based imports of tcomb libraries now resolve to a `tcombLocalName` (@ctrlplusb)
  - Guarding of tcomb imports, ensuring that tcomb is imported within the scope of any functions that have type checking, fix #21 (@ctrlplusb)
  - add support for object structure type annotations, e.g. `function foo(x : { bob: t.String, baz: t.Number })`, fix #24 (@ctrlplusb)
  - better error messages, fix #25
- **Bug fix**
  - Errors were thrown for functions with default'ed params and a type checked return value, fix #19 (@ctrlplusb)
  - Imports of extended tcomb libraries (e.g. "tcomb-react") now correctly resolve to a `tcombLocalName` (@ctrlplusb)

## v0.2.1

- **Bug fix**
  - Functions that had a destructured argument as well as a type checked return would fail transpilation, fix #16 (@ctrlplusb)

## v0.2.0

- **Breaking Change**
    - upgrade to babel ^6.0.0 https://github.com/gcanti/babel-plugin-tcomb/pull/12 (thanks @ctrlplusb)
    - support for default values https://github.com/gcanti/babel-plugin-tcomb/pull/15

## v0.1.4 (babel ^5.0.0)

- **New Feature**
    - support for default values

