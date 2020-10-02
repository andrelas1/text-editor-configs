call plug#begin()

" File tree view
Plug 'preservim/nerdtree'

" Fuzzy search files
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }

" Use Prettier to format files
Plug 'prettier/vim-prettier', {
  \ 'do': 'yarn install',
  \ 'for': ['javascript', 'typescript', 'css', 'less', 'scss', 'json', 'graphql', 'markdown', 'vue', 'yaml', 'html'] }
" Theme
Plug 'morhetz/gruvbox'

" Search for words in files
Plug 'gabesoft/vim-ags' 

" Theme
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'

" Change the surround of words using hotkeys
Plug 'tpope/vim-surround'

" Comment lines easily
Plug 'tpope/vim-commentary'

" Lint your files while you type
Plug 'dense-analysis/ale'

" Typescript support
Plug 'quramy/tsuquyomi'
Plug 'leafgarland/typescript-vim'

call plug#end()

" make y p use the OS buffer for copy/paste from VIM to some other app
set clipboard+=unnamed

" enable colors
set termguicolors

" set numbered lines
set number

" set relative number
set relativenumber

" set color theme
autocmd vimenter * colorscheme gruvbox

" variables

" use silver searcher instead of the default find command for FZF
let $FZF_DEFAULT_COMMAND = 'ag -g ""'

" change the leader key to ,
let mapleader=","


" Mappings
map ; :FZF<CR>
map B :NERDTreeToggle<CR>
map <leader>t :e#<CR>
map <leader>f :Ags

" open NERDTREE automatically if no files were specified
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * if argc() == 0 && !exists("s:std_in") | NERDTree | endif

" Fix files with prettier, and then ESLint.
let b:ale_fixers = ['prettier', 'eslint']

" set default tab space
:set tabstop=2
:set shiftwidth=2
:set expandtab

" disable auto indent from ts plugin
let g:typescript_indent_disable = 1
