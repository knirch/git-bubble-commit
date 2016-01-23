git-bubble-commit
=================
When working on a large branch with lots of small commits and general fixups
I often found myself in the situation where I'd try to move a commit further
up the history when doing rebase only to find that the commit "meh" changed
the same file I was trying to move closer to the top. After the umpteenth
time of single stepping a commit in a 60+ commit rebase I decided to write
git-bubble-commit.

git-bubble-commit is designed to be used in another terminal during a rebase.
It will do a clone into a temporary directory and do its work there to not
get in your way during a rebase.

```
knirch@traktor:~/source/project (rewrite)$ git bubble-commit origin/master 8938648
Commit(s) can be moved up 11 commits:
   4fdc301: ... pffrht, typo
 > 8938648: Rework logic.. again
   fa205db: <random git-auto-commit quote here>
```

License
-------
git-bubble-commit is public domain, see UNLICENSE or http://unlicense.org
for more information.
