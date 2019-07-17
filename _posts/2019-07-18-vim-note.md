# NERDTree
File Browsing System
## Invoke
Command :NERDTree  (my vimrc map <\leader>ND)
## Command 
* t: open the selected file in a new tab
* i: open the selected file in a horizontal split window
* s: open the selected file in a vertical split window
* i: toggle hidden files
* m: Show the NERD Tree menu
* R: Refresh the tree, useful if files change outside of Vim
* ?: Toggle NERD Tree's quick help
## Red
https://medium.com/usevim/nerd-tree-guide-bb22c803dcd2

# Surround
surround word with quote, bracket, tag etc
## Command
* ds delete surround
* cs change surround
* ys add surround
* viwS add surround a word in visual mode
* VS<strong> surround line

before:
hello "world"

after:
<strong>
hello world
</strong>

* viwS" surround a word by quote

before
hello world

after 
hello "world"

Press cs"' inside

"Hello world!"
to change it to

'Hello world!'
Now press cs'<q> to change it to

<q>Hello world!</q>
To go full circle, press cst" to get

"Hello world!"
To remove the delimiters entirely, press ds".

Hello world!
Now with the cursor on "Hello", press ysiw] (iw is a text object).

[Hello] world!
Let's make that braces and add some space (use } instead of { for no space): cs]{

{ Hello } world!
Now wrap the entire line in parentheses with yssb or yss).

({ Hello } world!)
Revert to the original text: ds{ds)

Hello world!
Emphasize hello: ysiw<em>

<em>Hello</em> world!
Finally, let's try out visual mode. Press a capital V (for linewise visual mode) followed by S<p class="important">.

<p class="important">
  <em>Hello</em> world!
</p>

Ref:
* https://github.com/tpope/vim-surround
* http://www.futurile.net/2016/03/19/vim-surround-plugin-tutorial/
