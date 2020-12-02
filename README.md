# backup-policy
Documentation and tools for backing up and archiving data.

## Documentation

Documentation and notes will be written to a wiki.

## Tools

A number of programs and scripts will be referenced/created.

## Background

My data is in need of organisation and my backup "system" needs redesigning.

I have a computer dubbed PC2 that currently acts as a storage server and (among other things) a gitbucket server.

It has several large hard disks of varying sizes with each disk having a sister disk of the same capacity that is stored in a hard disk storage case. Both disks in a matching pair should have bit-identical content.

### Current Methods

The current method of backing up data depends on the data. In general, I currently have four integrity checking methods depending on data type classifcation:

1. Documents
    * These are files that are typically stored in **My Documents** and includes things like text documents, spreadsheets, and images. These tend to be commited to a git repository.
    * Other files of this type include source code, which tend to have a per-project git repository.
2. Audio Files
    * Most of my (music) audio files are in FLAC+CUE format, with individual tracks format-shifted to ALAC or FLAC. The FLAC format has builtin checksums.
3. Large Media Files
    * Large media files, such as SD and HD video, are individual static/source files. These files have a ```.md5``` and ```.torrent``` file created for integrity checking using ```md5sum``` and ```torrentcheck```.
4. Large Media Folders
    * Large media folders, such as those containing a static/source collection of many related files, are treated as a folder. Such folders have a ```.torrent``` file created for integrity checking using ```torrentcheck```.
    * Unlike *Large Media Files*, *Large Media Folders* typically also contain tiny files, with such files slowing down copying.
