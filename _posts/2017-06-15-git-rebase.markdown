---
layout: post
title:  "关于rebase"
date:   2017-06-15 16:04:05 +0800
categories: jekyll update
---
简单来说rebase就是把某个分支上的一部分commit嫁接到另一个commit后面，而在这个过程中这些commit的base（基）变了，所以这个操作叫做『变基』。

{% highlight sh %}
git rebase [<上游> [<分支>]]
$ git checkout experiment
$ git rebase master   #<---将分支experiment的提交修改应用到master上
{% endhighlight %}

总的原则是，只对尚未推送或分享给别人的本地修改执行变基操作清理历史，从不对已推送至别处的提交执行变基操作，这样，你才能享受到两种方式带来的便利。
