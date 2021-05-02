## LATEX TEMPLATE using VSC

This repository shows how to use `latex` on `Visual Studio Code`. I used a custom simple `latex template`


## Requirements & installation

> Tested on Ubuntu 20.04 but it should be very similar on other OS. Just download the right `texlive` file on `[https://ctan.javinator9889.com/systems/texlive/tlnet/](https://ctan.javinator9889.com/systems/texlive/tlnet/)` depending on your OS and then set the path properly.

1. Download `tex live` -->  `wget [http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz](http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz)`

2. Unzip --> `tar zxvf install-tl-unx.tar.gz`

3. Installation `sudo ./install-tl` (While installing select option `I`)

> This may take some time (around 45min in my case)

4. Add the following to  `~/.bashrc`:

```bash
#==============
# Latex
#==============
export MANPATH="/usr/local/texlive/2021/texmf-dist/doc/man:$MANPATH"
export INFOPATH="/usr/local/texlive/2021/texmf-dist/doc/info:$INFOPATH"
export PATH="/usr/local/texlive/2021/bin/x86_64-linux:$PATH"
```

5. [VSC] Install extension `LaTeX Workshop` in VSC



## Usage

### From terminal

Go to  `~/path_to_project` on terminal:

1. Compile

```bash 
make
```
This will generate all files inside `out/` folder

2. In case you want to remove all files in `out` folder

```bash 
make clean
```



### Using Visual Studio Code

This is the simplest case scenario.

Go to  `Latex Workshop` settings and modify `Out Dir` option:

1. This is the default state

![latex_outdir](figures/latex_outdir.png)



2. This is how it should be

![latex_outdir2](figures/latex_outdir2.png)
