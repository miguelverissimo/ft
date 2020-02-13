# FT

## Load multiple ssh keys from lastpass

### Requirements
- [Lastpass cli](https://github.com/lastpass/lastpass-cli)
- Your private ssh keys stored in lastpass folder `ssh keys` as a secure note, named like:
  - your main key should be stored on a note named `id_rsa`, this key will always be loaded.
  - each of your other keys should be named following the format `id_rsa-<suffix>`, mind the mandatory `-` and make sure suffix is terse and rememberable as you'll need to type it as often as you need to load the key.
  - `.git-authors` in `$HOME`. File should be in [git-duet](https://github.com/git-duet/git-duet#setup) format. This will be used to infer your lastpass email, but you can override this requirement by always specifying your lastpass account email.

### Instalation
- clone this repo and cd into it
- `chmod +x ft`
- `install ft /usr/local/bin/ft` or wherever else where and if you want it available. Somewhere in your path sounds reasonable.

### Usage
`ft <user_initials|lastpass_email> [key suffix (comma separated, no spaces)] [duration in hours]`
eg: ft user@example.org aws,linode,digitalocean 6

- If you only provide the initials/email the default (or main) key will be loaded with the default duration
- if you don't provide the duration, it will default load the keys until 6pm of that day, or 3 hours, whichever is greatest.

### FAQ

#### Q: Why `ft`?
**A:** **1)** it was available as a cli and **2)** it matches the initials of the two most common words I utter when I notice my keys aren't loaded.

#### Credits
This is basically just a multi-key version of [Waciuma's](https://github.com/waciuma4pivotal) [vkl](https://github.com/waciuma4pivotal/vkl). Thanks for having that tool available for anyone to use.

#### Licence

FT - load multiple ssh keys from lastpass
Copyright © 2020 Miguel Verissimo

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the "Software"),
to deal in the Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish, distribute, sublicense,
and/or sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE
OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

