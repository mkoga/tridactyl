# Vimperator-like Firefox addon in the age of WebExtensions

Vimperator is going to die once Firefox deprecates XUL and switches webextensions. Needs fixing, or nobody will be able to use the internet any more.

Valiant efforts have been begun to sort out some parts of Firefox's WebExtension implementation:
https://bugzilla.mozilla.org/show_bug.cgi?id=1215061

This only deals with the keyboard binding aspect. We need to think about the GUI / hinting etc: we need to make sure everything we want to have in Vimperator is possible using WebExtensions.


Chrome et al. already use WebExtensions, and there are a few vim-like extensions for it, such as cVim/Vimium. It would make sense to look at how these extensions work and see what is not currently possible in Firefox. An obvious part of what they cannot do is change the GUI of the browser. Vimperator allows you to hide parts of the browser when they are not needed.


It would also be sensible to have a list of ideal things that can't currently be done in Vimperator, e.g. embedding Vim client, that we would like. (look at Petrosaur)


There is currently a magic console in Firefox that we could perhaps hijack, which is built on GCLI:
https://developer.mozilla.org/en/docs/Tools/GCLI
https://github.com/joewalker/gcli/blob/master/docs/index.md -- even says that it could be used as part of a browser extension

# Avoiding JavaScript:
CoffeeScript; EMScripten, ELM, Node.js (interpretereter?)
(broccoli)
What is NPM? Browserify is dependency management

# Useful libraries
PEG - parses stuff (e.g. command input)

# cVim
Code not well documented, could glean useful stuff from just stripping out what Chrome API is used

## Useful links:
https://www.codementor.io/gmuresan/building-a-chrome-extension-reactjs-broccoli-sass-du1081zv0



# Useful links
https://developer.chrome.com/extensions/commands
https://github.com/lydell/webextension-keyboard
https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts
https://github.com/shinglyu/QuantumVim - Vimium style stuff in WebExtensions


# Names
Tridactyl (like Pentadactyl, but worse, last cuturally relevant in 2005 like Salad Fingers)

# Features we really really want
- Hiding misc UI (tabs, menu, urlbar, etc.)
- Interacting with other addons (simulating presses on buttons?)
- ]][[ to inc/dec url
- command line for opening tabs/completion/interacting with addons/changing settings
- "buffer" tab searching / tab groups?
- searching for tabs between windows?

# Features we need less?
autocmds?
macros?