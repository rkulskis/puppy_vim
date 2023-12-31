# Background

This repo isn't so much a set of code as it is a tutorial on how to get a nice looking vim setup on the puppylinux 2.6.33 VM
which cannot connect to github.com. There was a decent amount of workarounds that went into this, for example the color themes simply didn't work in the `.vimrc` so instead, I found
the roxterm metadata version of the theme and imported it through roxterm preferences. Also,
there was a weird scancode that kept popping up upon using vim, but this is a result of [vim keyprotocol mappings](https://vimhelp.org/options.txt.html#%27keyprotocol%27) with xterm. The first two lines of the `.vimrc` fix this.

I just decided I wanted to work directly on the VM instead of using a git push script and pulling onto my puppy VM each time, so that's the reason for going the hoops
and whatnot to get vim on puppy.

# Setup Steps

---VIM CONFIG---
1. clone this repo (`puppy_vim`) and inside of it clone `git clone git@github.com:vim/vim.git`
2. ssh onto your username@csa2.bu.edu machine use `git init --bare` to make a repo there inside a folder (e.g. cs552)
3. push this repo to your csa repo **note: you need to first cd into the vim repo and do rm -rf .git**
4. pull from your csa machine to puppy VM (puppy 2.6.33 cannot pull from github.com)
5. cd into `vim_stuff/vim`
6. run `make`
7. run `make install` **note: steps 4 and 5 take rather long**
8. `cd ..` back up into the top of the git repo
9. run `cp .vimrc ~/`

---ROXTERM CONFIG---

10. run `cp gruvbox ~/.config/roxterm.sourceforge.net/Colours/`
11. in Roxterm, navigate in the top left `Preferences > Configuration Manager`. This will open a new window, and in the
top right under color scheme choose `gruvbox`

Enjoy!

# Demo
<img width="1512" alt="Screenshot 2023-12-09 at 6 35 12 PM" src="https://github.com/rkulskis/puppy_vim/assets/91744036/457349b9-28cd-4eca-a960-d36d735d487e">
