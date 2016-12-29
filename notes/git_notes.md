Stash
=====

Save your current work into a changeset.

Tagging
=======

`git tag -a "<tag name>" -m "<message>"`
 
For example:

`git tag v1.0.0 -m "Release 1"`

Then push the tags to the remote server

`git push origin --tags`

Reset
=====

Reset will actually modify the history and brings HEAD to the specified commit.

Ex: HEAD becomes d0cb69

`git reset d0cb69`

Three reset modes:

1. soft - all changes between now and the specified commit are staged to be commited and the HEAD is brought to the specified commit.
2. mixed - all changes between now and the specified commit are marked as modified and are not staged to be commited.  HEAD is brought to the specified commit
3. hard - any committed and uncommited changes after the specified commit are removed and your HEAD now points to the specified commit. 

Revert
======

Revert will modify your files to make it identical to a different version

Example: Can revert multiple unrelated commits in a single command.

`git revert 0b810a eca5cd`