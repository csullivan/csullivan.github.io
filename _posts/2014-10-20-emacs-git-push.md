---
layout: post
title:  "Creating a keybind in Emacs for automagically pushing to GitHub."
date:   2014-10-21 00:40:45
description: A website from the terminal (part 1).
categories:
- blog
---

It's actually pretty simple to get emacs to make a new commit with the current buffer and then push to github. I do it with this emacs lisp global keybind

{% highlight lisp %}
(define-key global-map (kbd "C-x p") 
  '(lambda() (interactive) 
     (async-shell-command 
      (format 
       "cd %s; git add %s; git commit -m 'Incremental Update'; git push;" 
       default-directory (current-buffer)))))
{% endhighlight %}

I set up ssh-keys with github to make it even easier, but you don't have to. Emacs properly handles sending credentials via the action buffer.

Hi Chris