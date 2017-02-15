# Initial Setup
* Plug everything in and start up. Select Jessie Pixel from NOOBS. Takes awhile to initialize. 
* You will want to run `sudo apt-get update` if you have not run it yet that day before installing any packages using `sudo apt-get install`.

  ```
  $ sudo apt-get update
  $ sudo apt-get upgrade
  $ sudo rpi-upgrade
  ```

* If your screen is too large / too small for the display
  * [Troubleshoot screen size](http://stackoverflow.com/questions/22891235/how-to-change-screen-resolution-of-raspberry-pi)
  * [RPi configuration](http://elinux.org/RPiconfig)
  * sudo vi /boot/config.txt
  
    ```
    overscan_left=230
    overscan_right=230
    overscan_top=10
    overscan_bottom=10 
    ```
# Install git
```
$ sudo apt-get install git
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```

# Install vim and vim packages
* Install vim 

  ```
  $ sudo apt-get install vim
  ```

* Copy .vimrc file from this folder into home directory

  ```
  $ cp .vimrc ~/
  ```

* Install [Pathogen](https://github.com/tpope/vim-pathogen)

  ```
  $ mkdir -p ~/.vim/autoload ~/.vim/bundle && \
    curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
  ```

* Install [Vundle](https://github.com/VundleVim/Vundle.vim)

  ```
  $ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
  ```

* Copy colors directory from this directory to ~/.vim

  ```
  $ cp -r colors ~/.vim/
  ```

* Launch `vim` and run `:PluginInstall`

* Install [NERDTree](https://github.com/scrooloose/nerdtree) using Pathogen

  ```
  git clone https://github.com/scrooloose/nerdtree.git ~/.vim/bundle/nerdtree
  ```


# Install gpio command line interface
* Install wiringpi gpio interface

  ```
  $ git clone git://git.drogon.net/wiringPi
  $ cd wiringPi
  $ ./build
  ```
* WiringPi [gpio pinout](http://wiringpi.com/pins/) and [commands](http://wiringpi.com/the-gpio-utility/)


# Install Emacs
  ```
  $ sudo apt-get install emacs
  ```
