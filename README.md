About helm-shell-history
=================

Overview
------------
Find shell history by helm

## Installation
You can install this using git:

    mkdir -p ~/.emacs.d/packages/
    cd ~/.emacs.d/packages/
    git clone https://github.com/emacsmirror/helm-shell-history.git

You can also install this using use-package:

    (use-package 'helm-shell-history
		:ensure t)
    
## Example configuration
Ensure that (getenv "HISTFILE") points to your shell's the history file. Eg: ~/.bash_history or ~/.zsh_history
Else, explicitly set the history file location by setting the variable helm-shell-history-file

You may set a keybinding to invoke helm-shell-history when inside an emacs shell

    (use-package 'helm-shell-history
		:ensure t
		:config
		(setq helm-shell-history-file "~/.zsh_history")
		(add-hook 'shell-mode-hook
          (lambda ()
            (define-key shell-mode-map [M-r] 'helm-shell-history))))

## License
This is GNU General Public License. see <http://www.gnu.org/licenses/>
