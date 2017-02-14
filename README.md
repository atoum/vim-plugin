# VIM plugin

<p align="center">
    <img src="http://atoum.org/images/logo/atoum.png" alt="atoum"/>
    <img src="https://raw.githubusercontent.com/atoum/vim-plugin/master/vim.png" alt="VIM" height="144px"/>
</p>

## Install

Clone this repository or download the `atoum.vmb` file then open in:

```sh
vim path/to/atoum.vmb
```

Now install the plug-in by using the following command in VIM:

```vim
:source %
```

## Usage

To use the plug-in, atoum must be installed and you must be editing a file containing a atoum unit test.

Once configured, the following command will launch the execution of tests:

```vim
:Atoum
```

The tests will be executed, and once finished, a report based on the configuration of atoum file located in the 
directory `ftplugin/php/atoum.php` in your .vim directory is generated in a new window.

Of course, you are free to bind this command to any keystrokes combination of your choice, for example you can add the 
following line in your `.vimrc` file:

```vim
nnoremap *.php <F12> :Atoum<CR>
```

Doing so will make <kbd>F12</kbd> to call the command `:Atoum` in normal mode will.

## Configuration

You can specify another configuration file for atoum by adding the following line to your `.vimrc file:

```vim
call atoum#defineConfiguration('/path/to/project/directory', '/path/to/atoum/configuration/file', '.php')
```

Indeed the function `atoum#defineConfiguration` lets you configure the file to use, based on the directory where the 
unit test files are located. It take three arguments:

* a path to the directory containing the unit tests;
* a path to the configuration file of atoum to be used;
* the extension’s file of relevant unit tests.

You can access help about the plug-in in VIM with the following command:

```vim
:help atoum
```
