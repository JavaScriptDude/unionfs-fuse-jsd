[unionfs-fuse-jsd](https://github.com/JavaScriptDude/unionfs-fuse-jsd)
============

This is a customized fork of the unionfs-fuse project that implements feature that notifies the caller of copy on write (COW) events for custom usecases where this information can be leveraged downstream.

This version is intended to be run in 'follow mode' (-f) so the invoking tool (eg Python) can read the stdout and trigger events off the COW notices.

For any standard unionfs applications, please use the excellent [unionfs-fuse] project by rpodgorny
