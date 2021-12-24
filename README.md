# Brett's Fish Files

A collection of configuration files and functions for the Fish shell. These would be installed in `~/.config/fish/`, though I don't recommend overwriting your current setup wholesale. Pick and choose, use this repo as examples for your own exploration.

## The folders

- __bash_scripts__: some utilities that were too much trouble to port from Bash and work just as well run with hashbangs. They just need to be in the $PATH (some commands reference my local path, `~/scripts/fish`, which will need updating).

- __completions__: various completion configurations for custom commands. 

- __custom__: some files I source at login (from `config.fish`), mostly shared functions I think I need to have in memory (as opposed to autoloaded), and some aliases that don't make great functions.

- __functions__: the mother lode. All of my favorite commands (and some experimental ones). Most have a description on the function declaration, so you can see it in source or by running the `describe` command that you'll find in this folder (which essentially runs `functions -Dv`, but prettier).

__COMPLETIONS NOTE:__ for the file extension completion function to work, it needs to be able to find the `filecomplete.rb` script located in the `bash_scripts` directory. Edit `functions/__complete_extension.fish` to point to that file on your system.

## All the functions


- `64enc`: encode a given image file as base64 and output css background property to clipboard
- `64font`: encode a given font file as base64 and output css background property to clipboard
- `64svg`: encode a given svg file as base64 and output css background-image property to clipboard
- `__auto_dir`: if command fails see if it\'s a directory or local executable
- `__best_pager`: Choose the best available pager (opinionated)
- `__complete_extension`: n/a
- `__exec_available`: test if command is available
- `__expand_path`: commandline function to expand str/str using fasd and fzf
- `__f_dir_regex`: n/a
- `__fuzzy_cd`: fuzzy cd with jump bookmarks
- `__human_time`: Humanize a time interval for display
- `__is_text`: Test if a file is plain text
- `__ls_text_files`: List all text files in current directory
- `__prev_token`: Get the previous token on the command line
- `__re_extension`: remove extension from word under/before cursor
- `__regex_from_args`: Helper to create greedy regular expression from multiple arguments
- `__unfuck_previous_command`: n/a
- `_tide_item_message`: n/a
- `_tide_item_ssh_badge`: n/a
- `abbrs`: Search abbreviations
- `ack`: ack defaults, ~/.ackrc for more
- `acorn`: Open Acorn.app with optional file(completion available)
- `add_user_path`: Shortcut to add a user path
- `affd`: Open Affinity Designer with optional file (completion available)
- `afff`: Open Affinity Photo with optional file (completion available)
- `ag`: Silver Surfer defaults, smart case, ignore VCS
- `alpha`: Open ImageAlpha with optional file (completion available)
- `ax`: Make file executable
- `badge`: Set iTerm session badge
- `bak`: move file to .bak version
- `be`: n/a
- `bid`: Get bundle id for app name
- `bld`: Run howzit build system
- `box`: Draw a box around text.
- `browser`: Write output to a temp HTML file and open in default browser
- `bunches`: Edit Bunches in Sublime
- `c`: n/a
- `calc`: CLI calculator
- `cat`: Use bat instead of cat unless it\'s a Markdown file, then use mdless
- `cbp`: n/a
- `cd_fuzz`: n/a
- `cdb`: Open broot with folders only
- `cdd`: Choose cd dir from menu (fzf)
- `cdr`: cd to a recently visited directory
- `cdt`: Change dir based on TagFiler tags
- `chrome`: Open Google Chrome with optional file (completion available)
- `cl`: copy output of last command to clipboard
- `clip`: Copy file to clipboard
- `code`: n/a
- `copy`: n/a
- `corner_print`: n/a
- `cpwd`: Copy the current directory path to the clipboard
- `cr`: Open CodeRunner
- `crush`: pngcrush
- `dadjoke`: Get a dad joke from icanhazdadjoke.com
- `dash`: Open argument in Dash
- `days_in`: get the number of days in a given month/year
- `ddg`: search duckduckgo
- `degit`: Remove all traces of git from a folder
- `desc`: Print the description of a Fish function.
- `describe`: Show description for function
- `dirfor`: get origin directory for running process
- `dman`: Open man page in Dash
- `docx2mmd`: Convert docx to markdown: docx2md [source] [target]
- `eds`: Shortcut for editscript
- `er`: edit recent file using fasd and fzf
- `esc`: Ruby cgi escape
- `eschtml`: Ruby cgi HTML escape
- `extract`: unarchive any file type
- `f`: Open directory in Finder with jump shortcuts
- `fallback`: allow a fallback value for variable
- `farch`: Test Architecture of Framework
- `fasdfzf`: Helper function to return a file via fasd and fzf
- `ffdir`: fuzzy find a directory, pass root dir and sequential search strings
- `fffile`: fuzzy find a file, pass root dir and sequential search strings
- `ffmark`: fuzzy find a jump mark
- `filetype`: Returns the kMDItemContentTypeTree for a file
- `findgist`: select gist from list and display contents
- `findgistid`: select gist from list and display contents
- `fire`: Open Firefox with optional file (completion available)
- `fish_prompt`: n/a
- `fix`: Fix up last command with search/replace
- `flush`: Flush DNS cache
- `fo`: Open file using jump shortcuts and fuzzy matching
- `fp`: Find and list processes matching a case-insensitive fuzzy-match string
- `ft`: A shortcut for mdfinding tagged items system-wide
- `fuck`: Correct your previous console command
- `g2`: Fish "jump" replacement with fuzzy subdirectory matching
- `gc`: n/a
- `geminfo`: Get info for a gem with partial name matching
- `geminstall`: install a gem with fuzzy search
- `gemuninstall`: Uninstall a gem with partial name matching
- `get_ext`: Get the file extension from the argument
- `getignore`: Get ignore file from gitignore.io and save to .gitignore
- `getignores`: Pull gitignore.io list of available .gitignore files
- `gg`: Commit pending changes and quote all args as message
- `gitar`: Automatically add new and remove deleted files from the git index
- `gitrelease`: Create a git release
- `gmine`: Resolve git conflicts with mine
- `gsearch`: Grep git commit history
- `gt`: jump to top level of git repo
- `gtheirs`: Resolve git conflicts with theirs
- `hook`: n/a
- `hooks`: Return a list of files hooked to target (Hook.app)
- `howlong`: alias howlong=echo $CMD_DURATION
- `hs`: Search, select, and exec from history
- `idea`: Record an idea with doing
- `imdown`: Test for internet connection and notify when it comes up
- `imgsize`: Quickly get image dimensions from the command line
- `index_of`: return the 1-based index of the first argument in remaining arguments
- `ip`: Get external IP address
- `ips`: Display all ip addresses for this host
- `is`: test if given file is of a file type. is TYPE FILE
- `istext`: test if given file is plain text
- `js`: lint with jslint
- `jump_fasd`: n/a
- `jump`: Fish "jump" replacement with subdirectory matching
- `lb`: Select file in LaunchBar, fall back to the current directory
- `lbash`: launch bash login shell
- `lld`: n/a
- `lno`: Print file with line numbers
- `lsgrep`: Wildcard folder/file search
- `lsregister`: n/a
- `lsz`: ls for inside of compressed archives
- `lt`: List directory from oldest to newest
- `ltr`: List directory from newest to oldest
- `m.`: Check if the current directory is bookmarked
- `mack`: ack for markdown
- `md`: n/a
- `mdgrep`: alias mdgrep=rg -S --type markdown
- `mkdir`: mkdir with subdirs, option to cd after creating
- `mmdc`: Open MultiMarkdown Composer with optional file (completion available)
- `nope`: echo "nope"
- `o`: Shortcut to open an app from the command line
- `optim`: Open ImageOptim with optional file (completion available)
- `pbgist`: private gist from clipboard
- `pbgistp`: private gist from clipboard
- `pbp`: Pasteboard Preview
- `pbpmd`: Pasteboard Markdown Preview
- `percentof`: Quick calculation for sale discounts
- `percentoff`: Quick calculation for sale discounts
- `pg`: alias pg=ps -ax | grep -i
- `pless`: cat a file with pygments highlighting
- `pman`: Display a man page as a PostScript PDF in Preview.app
- `prev`: Open Preview with optional file (completion available)
- `preview`: Preview text files using fzf and bat
- `prioritize`: set a numeric prefix on a file for sorting
- `prompt_message`: n/a
- `r`: Run Reiki via bash
- `raise`: Like ruby raise, but for fish
- `rule`: Print a horizontal rule
- `rulem`: Print a horizontal rule with message
- `rvm`: n/a
- `serve`: Start a local server for the current directory, open in browser
- `shellesc`: Ruby shellwords escape
- `shellunesc`: Ruby shellwords unescape
- `shorten`: Truncate every line of input to specified width
- `shortest`: Return the shortest string in array
- `showalias`: Show an alias
- `skylight`: alias skylight=skylighting -n -t ~/styles/kde/breeze-dark.theme
- `spell`: Get spelling options from aspell
- `spellcheck`: Check all Markdown files in git repo (recursive)
- `spellf`: Get spelling options from aspell
- `src`: reload config file
- `sublp`: Open a Sublime Text project (completion available)
- `sum`: Take a list of numbers and return the sum
- `td`: [Create and] open project todo
- `tmj`: For use with my tmux utility (bash_scripts/tm)
- `tower`: Open Tower for directory (default CWD)
- `tp`: Open TaskPaper with optional file (completion available)
- `unbak`: remove bak extension
- `uncolor`: Remove color codes from string
- `unesc`: Ruby cgi unescape
- `up`: cd to a parent folder with fuzzy matching
- `updown`: cd to a directory and then fuzzy search its tree
- `urlenc`: url encode the passed string
- `v`: vim via fasd and fzf
- `warn`: Echo to STDERR
- `watchthis`: Watch for changes in the current directory and execute command
- `xc`: Open Xcode with optional file (completion available)
- `yep`: echo "yep"
- `yn`: Simple pass/fail test for given command
- `z`: Custom fasd cd with fzf
- `zipup`: exports a clean copy of the current git repo (master) to a zip file

### Utility functions

- `__by_length`: n/a
- `__ff_dir_regex`: n/a
- `__ff_dir_to_regex`: n/a
- `__should_na`: n/a
- `__sort_by_length`: n/a
- `append_slash`: append a slash to each line/argument if needed
- `map`: n/a
- `remove_empty`: removes empty elements from an array
- `return_array`: Echo out an array one line at a time
- `shorten_home`: substitutes $HOME with ~
- `shortest_common`: n/a
- `slash_if_dir`: Add trailing slash if directory
- `trim_pwd`: removes the current working directory from an array of paths


I'll update these every once in a while. If you're digging through and spot a problem, a stupid mistake, or something that could just plain be done better, please add an issue and let me know!
