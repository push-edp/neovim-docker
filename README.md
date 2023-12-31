# neovim-docker
[![Docker Image CI](https://github.com/push-edp/neovim-docker/actions/workflows/docker-image.yml/badge.svg)](https://github.com/push-edp/neovim-docker/actions/workflows/docker-image.yml)
## Built from the Neovim source code, it natively supports both arm64 and amd64 platforms and includes a basic build environment for Neovim plugins.

![](./img/example.png)
![](./img/example1.png)

## You need to install the nerd font on the host first, otherwise the icons will not be displayed.

To run for the first time:
```
docker run --name neovim -d aspushedp/neovim
```
Alternatively, if you want to mount your own config and projects:
```
docker run --name neovim -v my-nvim-config:/root/.config/nvim -v my-projects:/root/projects -d aspushedp/neovim
```

Then, whenever you need to use Neovim:
```
docker exec -it neovim nvim
```
Or to run a bash shell:
```
docker exec -it neovim bash
```

You can also create an alias in your .bashrc or .zshrc:
```
alias nvim="docker exec -it neovim nvim"
```
