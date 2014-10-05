turbo-happiness
===============

Yet another attempt at a Tag based filesystem. The files and folder paradigm has served us well, but it is time to move on. Humans do not naturaly organize their data in a hiarchical manner. Many people have imagined tag based filesystems with little success. Here is our stab at it.

The main realization is that today we use already use tag based filesystems. For example, we tag the bash binary with the label "usr", "local" and "bin". Is there really any difference between /usr/local/bin/bash and /bin/local/usr/bash? A hiearchy of tags is not necessary to find the data we need. Today, a human may organize Photos by date, event, people, location, or a mix of all of this. The end result is a mess that is patched over with the help of search engines.


h1. Implementation

- Garbage collection
- Use of existing FS
- 

h1. Files, Attributes, Tags and Tagset

What are those?



h1. File (blob) operations

- Copy
- Move
- Delete

h1. Uses of tags

- Each software vendor has it's own tag
- Each software version has it's own tag
- Makes it easy to figure who is using what file (How does that tie into package management?)
- 

h1. Legacy compatibility

In traditional filesystems, each path element is a tag. 
- fopen compatibility
- Mountable filesystem
- File browser

