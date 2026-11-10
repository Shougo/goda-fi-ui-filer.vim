# goda-fi-ui-filer.vim

The UI `filer` of [goda-fi.vim](https://github.com/Shougo/goda-fi.vim), as
ddu-ui-filer: the items of trees in a buffer, the path of each source on the
line before its items.

It is made of the UI ff (`ff.NewUI()`): its params and actions are those of
ff, with other defaults, and its own.

## Requirements

- [goda-fi.vim](https://github.com/Shougo/goda-fi.vim)
- [goda-fi-ui-ff.vim](https://github.com/Shougo/goda-fi-ui-ff.vim): its Vim
  script is that of ff too. With goda-pm.vim:

  ```toml
  [[plugins]]
  repo = 'Shougo/goda-fi-ui-filer.vim'
  depends = 'goda-fi-ui-ff.vim'
  ```

## Usage

Add it in the configuration of goda-fi.vim:

```go
import "github.com/Shougo/goda-fi-ui-filer.vim/ui/filer"

b.AddUI(filer.New())
```

Then:

```vim
call goda_fi#start(#{ui: 'filer', sources: ['file']})
```

See `:help goda-fi-ui-filer`.
