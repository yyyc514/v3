# Overview

Generates the needed scaffolding for a concept exercise

## Usage 

When possible, this script should be run from this directory. Otherwise you will
need to manually specify the output and template paths.

```bash
# generate-scaffolding <slug> [OPTIONAL: <output-path> <template-path>]
$ ./generate-scaffolding function-definition
Creating exercises/concept/function-definition/.meta/config.json...
Creating exercises/concept/function-definition/.meta/design.md...
Creating exercises/concept/function-definition/.meta/example.lisp...
Creating exercises/concept/function-definition/.docs/after.md...
Creating exercises/concept/function-definition/.docs/hints.md...
Creating exercises/concept/function-definition/.docs/instructions.md...
Creating exercises/concept/function-definition/.docs/introduction.md...
Creating exercises/concept/function-definition/function-definition-test.lisp...
Creating exercises/concept/function-definition/function-definition.lisp...
```

## Binary Creation

```lisp
(sb-ext:save-lisp-and-die "generate-scaffolding" :toplevel #'main :executable t :compression 9)
```