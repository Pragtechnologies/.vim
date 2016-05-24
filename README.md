# Preq
The vim configurations is manage by bower. For this to work, you need to install node, bower, and vim first. Below are the steps:

## Install Node through NVM
Follow the steps in [nvm by creationix](https://github.com/creationix/nvm) which is to run the command below for Linux setup:
`curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash`

After the installation, check the latest node verions by running `nvm ls-remote`. Then just run `nvm install <latest-version>`.

## Install Bower
Just run the command:
`npm install -g bower`

## Install Vim with Ruby, Clipboard, and Phython
In linux, you could easily do this through:
```sudo apt install vim-gtk-py2```


# Setup

 - Go to `~`
 - Clone this repo. If `/.vim` already exists, delete it.
 - Run `bower install`
 - For first setup, you need to move the autoload folder of vim-pathogen in the `~/.vim` directory. Run the following:
 ```mv bundle/vim-pathogen/autoload .```

## Extra step for Command-T
Command-T needs to be compiled using ruby that was used when you've installed vim. To know the ruby version of your vim:
```:ruby puts "#{RUBY_VERSION}-p#{RUBY_PATCHLEVEL}"```

Make sure to install ruby with the same version. Once done, do the following:
```
cd ~/.vim/bundle/Command-T/ruby/command-t
ruby extconf.rb make
rake make
```

That's it. All your vim pluggins is well maintained through bower.

If ever you want to reformat your vim pluggins, you can simply run the command below:
curl -o- https://raw.githubusercontent.com/Pragtechnologies/.scripts/master/vim-setup.sh | bash
**Warning: This will remove you ~/.vim folder.**
