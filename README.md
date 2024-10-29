git-diff-image
==============

!!NOTE!!:
This fork is customized for [gin-diff-image.nvim](https://github.com/sankantsu/gin-diff-image.nvim).
Preview window is **not** displayed.
Image is rendered by Neovim buffer if you use `gin-diff-image.nvim` plugin.

If you wnat to view image diffs in preview window, see original repository [ewanmellor/git-diff-image](https://github.com/ewanmellor/git-diff-image).

## Setup example

- `~/.gitattribute`

```gitattributes
# Use custome diff driver `image` for image files.
*.jpeg diff=image
*.jpg diff=image
*.png diff=image
```

- `~/.gitconfig`

```gitconfig
[core]
    # use ~/.gitattributes as global git attributes
	attributesfile = ~/.gitattributes
[diff "image"]
    # use `git_diff_image` script as diff driver `image`
	command = ~/ghq/github.com/sankantsu/git-diff-image/git_diff_image
```
