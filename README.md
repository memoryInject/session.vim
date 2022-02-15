# Vim Session Plugin

Create and restore vim session with NerdTree.  
When running vim on project directory root ( nvim . ) this plugin will create   
.session.vim file to store the current vim session on the project root, also save current session for NerdTree.

**Note: To use this plugin make sure to install   
- NerdTree: https://github.com/preservim/nerdtree
- nerdtree-project-plugin: https://github.com/scrooloose/nerdtree-project-plugin


## Installation

Install with your favourite plugin manager but make sure it installed after nerdtree and nerdtree-project-plugin


```vim
  Plug 'scrooloose/nerdtree'
  Plug 'scrooloose/nerdtree-project-plugin'
  Plug 'memoryInject/session.vim'
```
    
## Usage/Examples

This plugin does not need any additional setup.  
When running ' nvim . ' on bash, it will create .session.vim file on the root directory. You can add .session.vim on .gitignore and delete after the project finish. 

```bash
nvim .
```

When opening a single file with nvim it output a message on nvim command line like "Session Disabled: Not running on project root directory".   

If there is already a .session.vim file on the root, it will output "Session loaded".   
If there is no .session.vim file on the root, it will output "No session loaded".  
Session file only create after exiting nvim like qa! or q!.  
  
If you pass 'ns' argument when opening nvim ( nvim . ns ) this will disable the session and won't create .session.vim file.

```bash
nvim . ns
```

## Contributing

Contributions are always welcome!  
For major changes, please open an issue first to discuss what you would like to change.


## License

[MIT](https://choosealicense.com/licenses/mit/)
