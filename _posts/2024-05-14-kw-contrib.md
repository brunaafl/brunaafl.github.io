---
layout: post
title: "Contribution to kworkflow"
date: 2024-05-14
description: Description of our PR to kw =]
tags:
 - kw
 - kernel
---

[Gustavo](gustavohenriquesr.github.io) and I decided to tackle the issue [#951](https://github.com/kworkflow/kworkflow/issues/951#issue-1977355255), opened by Rodrigo 
Siqueira in 2023, which proposes to add more information on the output of the `kw device` command, such as kernel version and some display info, such as the number of 
connected and active displays, ports, and resolution. 

Since this task has two requests, we divided it so Gustavo would take care of kernel-related information, and I would deal with the display. We opened a 
[Pull Request](https://github.com/kworkflow/kworkflow/pull/1107#issue-2281861843) with our changes, wich recently got reviewed by Rodrigo Siqueira.

For my part, I used `xrandr` to return the displays list ant to search for active ones. 

```bash
  n_display=$(xrandr -q | wc -l)

  n_active=$(xrandr -q | grep -c " connected ")

  act_name=$(xrandr | grep " connected " | awk '{ print $1 }')
  act_resol=$(xrandr | grep "\*" | awk '{ print $1 }')
  name_resol=$(xrandr | grep " connected " | awk '{ print $1, "- resolution", $4 }')
```

However, Rodrigo pointed out that `xrandr` cannot be used across different UIs, and also needs some extra setup to work via SSH. He suggested me to use the 
src/plugins/subsystem/drm.sh file to get this information.
