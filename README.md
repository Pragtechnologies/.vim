# Preq
The vim configurations is manage by bower. For this to work, you need to install node and bower first. Below are the steps:

## Install Node through NVM
Follow the steps in [nvm by creationix](https://github.com/creationix/nvm) which is to run the command below for Linux setup:
`curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash`

After the installation, check the latest node verions by running `nvm ls-remote`. Then just run `nvm install <latest-version>`.

## Install Bower
Just run the command:
`npm install -g bower`

# Setup

 - Go to `~`
 - Clone this repo. If `/.vim` already exists, delete it.
 - Run `bower install`
 - For first setup, you need to move the autoload folder of vim-pathogen in the `~/.vim` directory. Run the following:
 ```mv bundle/vim-pathogen/autoload .```

That's it. All your vim pluggins is well maintained through bower.
