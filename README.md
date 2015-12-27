## spacemacs.d
config file for spacemacs

#### Trouble Shooting

Q: Weird character zsh in emacs terminal

A: <http://stackoverflow.com/questions/8918910/weird-character-zsh-in-emacs-terminal/8920373#8920373>

> You don't have eterm-color terminfo. First, you try to add following S-exp in your configuration file and evaluate.
> ```lisp
> ;; Use Emacs terminfo, not system terminfo
> (setq system-uses-terminfo nil)
> ```
> If problem is not resolved previous setting, you should create eterm-color terminfo by using following command. (terminfo path may different from your system)
> ```sh
> # If you use Cocoa Emacs or Carbon Emacs
> tic -o ~/.terminfo /Applications/Emacs.app/Contents/Resources/etc/e/eterm-color.ti
> ```

If `eterm-color.ti` is not exist, and you installed emacs from brew, you can find
this file from `/usr/local/Cellar/emacs/{VERSION}/share/emacs/{VERSION}/etc/e/eterm-color.ti`
