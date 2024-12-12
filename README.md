# Video and docs

Slides for a session on video and documentation.

Originally presented at Canonical sprint in The Hague, Oct 2024.
Later presented at Write the Docs, Ireland.

The slides are made with reveal.js using a rudimentary, custom Ubuntu theme.

The presentation makes heavy use of embedded video that I have not had the opportunity to compress yet!!!

## Outline

Most software documentation is text-based.
Video often seems like a poor alternative.
Videos are difficult to create, maintain and version.
Some videos should probably just be plain text, such as
a video that consists solely of terminal commands.

Video can, however, be a natural solution for specific kinds of documentation problem.
An obvious example is a graphical application with a rich and responsive interface.

In this talk, I will discuss how:

* Certain kinds of interface are best demonstrated through video
* New tools make video documentation easier to create and maintain
* Video is well suited to documentation for acquiring skill or understanding

Even if we choose not to use video, thinking about what video does well may
help us write better documentation.

## Key points

### Slide 1: introduction

I'm a technical author at Canonical, working on software documentation.

### Slide 2: "can we just make this plain text?"

There are videos where the question "can we just make this plain text?"
would be ridiculous.

Many such videos succeed, even if they are not versioned or automated.
The challenge of rendering these videos as plain text would also be
substantial.

In documentation, however, we often finding ourselves questioning the
merit of video, and asking whether videos should just be text.

### Slide 3: this could probably be plain text

This is an example of a simple case.

It is a video, but it largely consists of text.

The video is text rendered in a less ergonomic form.
It cannot be parsed at a glance. It cannot be copied and pasted.

### Slide 4: this might be more difficult

When I started to think about video in documentation, I was initially
quite dogmatic.

I thought that any video that depicts terminal commands should not be a video.

But CLI interfaces are increasingly rich; they are not merely a sequence of
commands and output logs.

Here I'm bootstrapping an npm project using the Motion Canvas library.
You can see that there is:

* Suggested text
* Radio menus
* Dynamic, coloured notifications

If we want to faithfully represent the interface that a user encounters
then video might be a more attractive option in a case like this.

### Slide 5: video as tutorial

This is an example from the Canonical documentation.

This is a tutorial for using a feature of the Ubuntu desktop
and it largely consists of a video.

If we look at the video, it largely consists of terminal commands
and output logs.

We later decided to convert this video into a text-based version
and it wasn't difficult to do so.

### Slide 6: abstracts

I trained originally as a scientist, and for many years I 
wrote scientific papers.

Every paper needed an abstract, which is a concise description
of the contents of the paper.

They are miniature versions of the paper.
They can be read quickly and outline key experiments and results.

As a scientist, reading papers is important, but it is also difficult
and time-consuming.

An abstract acts as a kind of invitation: this is the gist of what
you will find inside, if you are interested read on.

They are short. You don't need to scroll. You can read most of them
in under a minute.

Increasingly, scientists are encouraged to prepared graphical and
even video abstracts to accompany their articles.

### Slide 6: video as abstract (landing pages)

When I was looking at some of our video documentation, it reminded
me of the abstract.

This slide contains the landing page in the how-to section of the docs for LXD,
a tool for creating containers.

It contains a video, which largely consists of text and has no narration.
Essentially, it gives a full walkthrough of LXD's key features.
I can view it in three minutes without doing any work on my computer.
If I'm interested, I can read the rest of the docs.

### Slide 7: video as abstract (storefront)

Another example here is the store page for installing the Go snap.
What I like about this is that it demonstrates how quickly you can
get a Go development environment up and running.

At the same time, it keeps key features of the store page in focus.
You can watch the video but the buttons and dropdowns for installing
and changing release versions are still in view.

Videos condense a lot of content into a small amount of visual space.

### Slide 8: GUIs: a more obvious case?

Arguably, a more immediate candidate for video documentation is the graphical
user interface.

Here's a simple tool that I made a few years ago, which I will quickly demonstrate.

_... Shane clicks around and does stuff... _

The general functionality of this software can be shown very quickly.
Anyone who is familiar with the language of buttons, cursors and checkboxes
should be able to use this after a quick video demo.

Describing it in text, however, is likely to yield unwieldy documentation
with a lot of images that don't capture the feel of the software.

And... as 3D software goes, what I built here is one of the simplest cases!

### Slide 9: Complex interfaces and skill acquisition

Blender is one of the most loved open-source projects.
It can be used for creating 3D models, digital sculpting, motion graphics and video editing.
It is a beautiful piece of software that happens to have a very complex interface.
Its interface has to be more complex than my toy program because it has vastly more functionality.

An interesting thing about Blender is that there is that for many community
members, video tutorials are a key source of knowledge about using the
software.

There is something about following a master user of Blender as they navigate
the interface that is difficult to recreate in a written tutorial.

When I have spoken to other technical authors about this, some have suggested
that this is a failing of Blender's UX. Indeed, Andrew Price, who is probably
the most successful maker of Blender tutorials, recently gave a talk about how
to improve the UI.

This seems to me to be another version of the "a well-designed product doesn't
need documentation" argument. In this case: "a well-designed product doesn't
need video documentation".

Given the relative success of Blender, I think we should carefully reflect on
that line of reasoning.

I also think we should be realistic. Blender may never have a simple UI because
it's a complex product. Many people only need to use a subset of the UI's features.
Until an overhaul of the UI happens, it will likely still need good video documentation.

We always need to document what we have now, not what we might have in the future.

### Slide 10: CLIs can be complex too

I've spoken a lot about GUIs, but CLIs can also have a lot of complexity.

This is a contrived example but it closely resembles some workflows that I
encounter.

We can imagine one terminal session on a Windows computer.
The user wants to use Linux, so they open a WSL instance.
They then ssh into a server, and in that server they launch a VM.

There has been multiple changes of context and environment.
The user is moving between different conceptual spaces.
The distance from the physical computer grows.

The only indication of these changes for someone reading this
documentation is the prompts.
Depending on the expertise of the user, this could be routine
or discombobulating.

### Slide 11: video of multi-pane interface (tmux)

### Slide 12: showing performance

### Slide 13: our current guidelines

So, we had been using video in our documentation but we didn't have
anything about video in our style guide.

I added a section on video that generally advises people to not use
video.
At the same time, I wanted to recognise that there were examples
that seemed to overcome the problems that video poses.

### Slide 14: tooling

To finish, I want to talk about tooling options.

On this grid, I've put some tools that can be used for making videos.

On the bottom left I have a classic video editor, like Kdenlive.
If you're not familiar, these editors are very manual, can be difficult
to learn and produce static videos.

To the right there is the more programmatic tools.
These build video from some kind of source code.
This means they can be versioned.

There are degrees of automation involved.
Asciinema, which we have seen a few examples of,
requires you to first record a terminal session,
which then generates source code.
VHS, on the other hand, allows you to essentially
write videos.

Some tools, like Motion Canvas, give you the full power of
a programming language.
They can produce animations and visualisations, in addition
to text.

### Slide 15: asciinema

The key selling point of this tool is that the
text can be copied from the video.

This is a very unique feature but you need to make
sure that the reader knows this is possible.

With complex terminal examples, it may be unclear
what needs to be copied.

### Slide 16: asciinema: contd.

The source that it generates allows versioning.
However, it is not very readable and not easy to
edit by hand.

### Slide 17: VHS

Far more readable is the source code for videos made
using VHS.

### Slide 18: Automated testing with VHS

TODO

### Slide 19: Motion Canvas

TODO

### Slide 20: Motion Canvas example

TODO

### Slide 21: Text-based version

TODO

### Slide 22: Manim

TODO

### Slide 23: Manim example

TODO

### Slide 24: Diataxis

TODO

### Slide 25: Diataxis: would you watch a reference video?

TODO

## Tools referenced

- [Asciinema](https://asciinema.org/)
- [Bubble Tea](https://github.com/charmbracelet/bubbletea)
- [VHS](https://github.com/charmbracelet/vhs)
- [Motion Canvas](https://motioncanvas.io/)
- [Manim](https://www.manim.community/)
- [kdenlive](https://kdenlive.org/en/)
