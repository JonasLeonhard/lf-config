<img src="https://shields.io/badge/pipelines-offline-red?style=flat-square&logo=github" />

<br/><br/>

# Description

Custom https://github.com/gokcehan/lf configuration

## Status

- [ ] _in progress_
- [x] _finished_
- [ ] _no longer continued_

## Table of contents

- [Description](#description)
- [Status](#status)
- [Table of contents](#table-of-contents)
- [General Info](#general-info)
- [Screenshots](#screenshots)
- [Credits](#credits)

## General Info

## Screenshots

<![Lf Prompt](./assets/lf.png)>

## Technologies

lf (https://github.com/gokcehan/lf)

## Setup

copy lfrc in ~/.config/lf or

```
git clone git@github.com:JonasLeonhard/lf-config.git ~/.config/lf
```

and add

```
# Use lf to switch directories and bind it to ctrl-f
lfcd () {
    tmp="$(mktemp)"
    lf -last-dir-path="$tmp" "$@"
    if [ -f "$tmp" ]; then
        dir="$(cat "$tmp")"
        rm -f "$tmp"
        [ -d "$dir" ] && [ "$dir" != "$(pwd)" ] && cd "$dir"
    fi
}
bindkey -s '^f' 'lfcd\n'
```

to your .zshrc to open lf via <c-f>.

to see the keybindings. Press "?" when lf is opened.

## Known Issues / Missing Features

---

## Credits:

Based on Pastel Powerline Preset: https://starship.rs/presets/pastel-powerline.html

```

```