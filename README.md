# markdown-edit-indirect - Edit markdown code block in a separate buffer

*Author:* Mario Rodas <marsam@users.noreply.github.com><br>
*Version:* 0.1<br>

Edit markdown code block in a separate buffer like `org-edit-src-code`.

### Usage

You need to place the cursor inside a code block i.e. surrounded by triple
backticks (```), and call \\[markdown-edit-indirect]. Alternatively you can
add the following key binding:

        (eval-after-load 'markdown-mode
          '(define-key markdown-mode-map (kbd "C-c '") 'markdown-edit-indirect))

Or in case you use \\[use-package] you can install and configure everything
in one step:

        (use-package markdown-mode
          :ensure t
          :demand markdown-edit-indirect
          :mode (("\\.md" . markdown-mode)
                 ("\\.markdown" . markdown-mode))
          :bind (:markdown-mode-map
                 ("C-c '" . markdown-edit-indirect)))


---
Converted from `markdown-edit-indirect.el` by [*el2markdown*](https://github.com/Lindydancer/el2markdown).
