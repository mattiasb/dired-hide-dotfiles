# Dired Hide Dotfiles #

Hide dotfiles in dired.

## Installation ##

Via [Melpa](https://melpa.org/#/getting-started):

`M-x package-install dired-hide-dotfiles`

Manually:

1. Clone this repo somewhere
2. Run `package-install-file` and choose the `dired-hide-dotfiles` file.

## Activation ##

To activate this mode add something like this to your init.el:

```elisp
(defun my-dired-mode-hook ()
"My `dired' mode hook."
;; To hide dot-files by default
(dired-hide-dotfiles-mode)

;; To toggle hiding
(define-key dired-mode-map "." #'dired-hide-dotfiles-mode))

(add-hook 'dired-mode-hook #'my-dired-mode-hook)
```
