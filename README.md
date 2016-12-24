# complete-alias

Programmable completion function for shell aliases.

# Intro

Users often don't have a way to complete custom shell aliases.

This program provides a **generic**, **universal** and **programmatic** solution
to this problem:

-   It is **generic**. The program works with all commonly defined aliases, even
    those with leading redirections and those aliasing to themselves.

-   It is **universal**. A single function completes all aliases blindly, which
    means users don't have to define different completion functions for
    different aliases.

-   It is **programmatic**. Aliases are completed automatically by the program
    as you type without any human intervention.

# Installation & Usage

## Bash

1.  If `~/.bash_completion` doesn't exist, create it.

2.  Paste the content of `completions/bash_completion.sh` into
    `~/.bash_completion`.

3.  Complete an alias with:

        complete -F _complete_alias <myalias>

    Multiple aliases can be specified one per line, or as arguments on a single
    line.

# Example

## Bash

In `~/.bash_profile`:

    alias sctl='systemctl'

In `~/.bash_completion`:

    complete -F _complete_alias sctl

Now typing `<Tab>` after `sctl<space>` will show `systemctl` commands:

    add-requires
    add-wants
    cancel
    cat
    condreload
    ...

# LICENSE

The source code is licensed under the [GNU General Public License v3.0][GPLv3].

Copyright (C) 2016 Cyker Way

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program.  If not, see <http://www.gnu.org/licenses/>.


[GPLv3]: https://www.gnu.org/licenses/gpl-3.0.txt
