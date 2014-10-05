turbo-happiness
===============

Yet another attempt at a Tag based filesystem. The files and folder paradigm has served us well, but it is time to move on. Humans do not naturaly organize their data in a hiarchical manner. Many people have imagined tag based filesystems with little success. Here is our stab at it.

The main realization is that today we use already use tag based filesystems. For example, we tag the bash binary with the label "usr", "local" and "bin". Is there really any difference between /usr/local/bin/bash and /bin/local/usr/bash? A hiearchy of tags is not necessary to find the data we need. Today, a human may organize Photos by date, event, people, location, or a mix of all of this. The end result is a mess that is patched over with the help of search engines.


Implementation
--------

- Garbage collection
- Use of existing FS
- 

Objects in tagfs
--------
- Files (I prefer blob but to ease understanding let's use file)
 - Each file has a random unique id (UniqueBlobId) 512 bit long
 - The files are mutable
 - 

- Attributes

- Tags
 - Each tag has a unique ID (512 bit)
 - Are tags attributes with an empty value?
 
- Tagset


File (blob) operations
--------

- Copy
- Move
- Delete

Security
--------
- ACL as attributes
- What operations can be perfomed on the file


Uses of tags
--------

- Each software vendor has it's own tag
- Each software version has it's own tag
- Makes it easy to figure who is using what file (How does that tie into package management?)
- 

Legacy compatibility
--------

Supporting traditional filesystem is key for widespread adoption of a tag based FS. In traditional filesystems, each path element is a tag. The ordering does not matter. 

- fopen compatibility is possible by converting a string path into a set of tags.
- Mountable filesystem start at the root by showing all the tags available. When you change "directory" to one of the tags, the ls command will reval only the tags for which there exists a file with the current tag and the aditional tags. Changing directory to a second tag, will show only files that have both tags and the tags
- File browser

