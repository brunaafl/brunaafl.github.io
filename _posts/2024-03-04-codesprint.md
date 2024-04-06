---
layout: post
title: "Braindecode CodeSprint"
date: 03-04-2024
---

## Braindecode CodeSprint

I imagine that the best thing I can do to honor the first post on this blog is to document this very nice experience I had in 2023 between 4-8 September, at INRIA Paris-Saclay.

[Braindecode](https://braindecode.org/stable/index.html) is an open-source library for Brain-Computer Interfaces focused on implementing main steps for inference using brain data, such as preprocessing, data loaders, and published models, facilitating the use.

Researching in the field of BCIs, I have used Braindecode before in my implementations for my scientific initiation project, and therefore, participating in the code sprint and contributing to the library was an amazing experience, that helped me deepen my understanding regarding EEG signals, Deep Learning, and programming in general.

During this week, we focused mainly on fixing open issues and improving documentation. Some major contributions I can list were:

1) The addition of three new BCI models and one for Sleep-Stage classification;

2) Organizing the structure of the tutorials and examples;

3) Increasing the speed of data windowing and model training.

On my side, I helped improve documentation and solve some of the open issues. For instance, I worked with Bruno Aristimunha on creating new preprocessor objects for data based on MNE’s raw/Epochs methods, and with Pierre Guetschel on standardizing layers' names. All the changes for the new release can be found at [here](https://braindecode.org/stable/whats_new.html).

If someone is reading this and wants to know more about Braindecode, check [https://braindecode.org/stable/index.html](https://braindecode.org/stable/index.html) !

---
