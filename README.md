# bang
Shebangs on steroids

# Proposal
Ever gone down the rabbit hole of trying to find out which shebang you should use for your script?
For Python, the shebang standard has changed from (in no particular order):
> `#!python` (Unix) and `#!py` (Windows)

> `#!/bin/python` and `#!/usr/bin/python`

> `#!/usr/local/bin python` And `/usr/bin/env python`

What does this all mean? It means there's no cross-platform and truly standardized way to do shebangs.
With [bang](https://github.com/Aareon/bang), it's one line, and whatever options you want. Easy, documented, safe.

Put `#!bang` at the top of all of your scripts, execute bang, and fret no longer if you're using the right shebang. Bang will figure it out for you!

## Usage
Add `#!bang` to any supported file (see: [supported file types](/SUPPORTED_FILE_TYPES.md).)

If you know what interpreter you want to use, do
`#!bang python` for example.

## Interpreter version
`#!bang python 3.8.10`

`#!bang python ^3.6`

## Running tools with bang
`#!bang python - isort`

`#!bang python ^3.6 - isort, black`
Bang will find the specified interpreter, run the scripts, and update the shebang appropriately.
