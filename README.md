emacs-evernote-mode-mod
=======================
* WHAT'S THIS?
This is a modified version of Evernote-Mode for Emacs, originally authored by Yusuke KAWAKAMI and Akihiro ARISAWA,
hosted on http://code.google.com/p/emacs-evernote-mode/.

* WHAT'S NEW?
** Support of local Evernote service in China, a.k.a YXBJ
** Use developer token instead of the old api-key, since OAuth is mandatory for API-Key authentication with Evernote.
** Open linked notebooks, including publich notebooks, notebooks shared by others, and joined business notebooks
** Open and update notes in linked notebooks with write permission

* INSTALL
1. Emacs 23.1 or later is required
2. Copy evernote-mode.el into a directory in Emacs' load-path
3. Add the following in your ~/.emacs

      (add-to-list 'load-path "~/lisp")
      (setq eemm-install-path "<where this repo was checked out>")
      (require 'evernote-mode)
      (setq evernote-devtoken "Developer Token")
      ;; supported evernote-svchost are: www.evernote.com, app.yinxiang.com, sandbox.evernote.com etc.
      (setq evernote-svchost "app.yinxiang.com")
      (setq evernote-enml-formatter-command '("w3m" "-dump" "-I" "UTF8" "-O" "UTF8"))
      (global-set-key "\C-cec" 'evernote-create-note)
      (global-set-key "\C-ceo" 'evernote-open-note)
      (global-set-key "\C-ces" 'evernote-search-notes)
      (global-set-key "\C-ceS" 'evernote-do-saved-search)
      (global-set-key "\C-cew" 'evernote-write-note)
      (global-set-key "\C-cep" 'evernote-post-region)
      (global-set-key "\C-ceb" 'evernote-browser)

