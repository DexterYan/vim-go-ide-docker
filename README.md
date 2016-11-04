
cker
If you want a perfect Go development with autocomplete in minutes, here is the solution

### 1. Why docker
Docker runs your code in a container, which runs on the host operating system and hardware in an isolated userspace. Without overwritting your host vim settings, you will be very easy to start to develop your golang app.


### 2.  What is this
After you build the image, it will add some cool vim plugins to the [official go image](https://hub.docker.com/_/golang/). You will be able to use golang youcompleteme, ultisnips, vim-colorscheme and more other cool vim plugin.

### 3. How to build and use it
```
docker-compose build
docker-compose run vim bash
```
You will attach to the docker image to do the development. You can change the code in app/main.go. It is sync with the host machine

### 4. Folder Struture
- app/
  - main.go (you app code here)
  - docker-compose.yml
  - Dockerfile-vim
  - vimrc (your vim settings)

  ### 5. Vim Plugins List
  You will install these plugins in default.
  - [Vundle](https://github.com/VundleVim/Vundle.vim)
  - [vim-go](https://github.com/fatih/vim-go)
  - [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)
  - [ultisnips](https://github.com/SirVer/ultisnips)
  - [vim-snippets](https://github.com/honza/vim-snippets)
  - [delimitMate](https://github.com/Raimondi/delimitMate)
  - [vim-colorschemes](https://github.com/flazz/vim-colorschemes)

  ### 6. Default Go Mappings
  ```
  au FileType go nmap <Leader>s <Plug>(go-implements)
  au FileType go nmap <Leader>i <Plug>(go-info)
  au FileType go nmap <Leader>gd <Plug>(go-doc)
  au FileType go nmap <Leader>gv <Plug>(go-doc-vertical)
  au FileType go nmap <leader>r <Plug>(go-run)
  au FileType go nmap <leader>b <Plug>(go-build)
  au FileType go nmap <leader>t <Plug>(go-test)
  au FileType go nmap <leader>c <Plug>(go-coverage)
  au FileType go nmap <Leader>ds <Plug>(go-def-split)
  au FileType go nmap <Leader>dv <Plug>(go-def-vertical)
  au FileType go nmap <Leader>dt <Plug>(go-def-tab)
  au FileType go nmap <Leader>e <Plug>(go-rename)
  ```
  ### 7. Vim Colorscheme
  It is use [monoacc](http://vimcolors.com/?utf8=%E2%9C%93&order=relevance&query=monoacc)
  You can change it by modify vimrc
  ```
  colorscheme molokai
  ```
  For more color, check here the [list](https://github.com/flazz/vim-colorschemes/tree/master/colors)

  ### 8. Something missing? Fork!
  fork this repo; send a pull request!; My email yanshaocong@gmail.com

  ### MIT

  Copyright (c) 2016 Dexter Yan

  Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE
