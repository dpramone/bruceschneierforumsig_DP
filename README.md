# bruceschneierforumsig_DP
PGP signed entries by myself on https://www.schneier.com

### What is this ?
I am a regular commenter on the security and technology blog of Bruce Schneier (see above).
This is an open forum that allows for pseudo-anonymous comments using a free to chose handle.
Unfortunately, handles are being hijacked regularly by trolls and sockpuppets, creating FUD and
bad blood. This repo is meant to PGP sign comments by myself, thus unequivocally establishing who
authored them if someone questions the author and taking away the ability from hijackers to do
the same.
  
### How does it work ?

The forum-posts directory in this repo has a file in `DDMMYYYY` format for each day I make a blog
entry, and can hold multiple records for each post I make that particular day. These records 
contain my name (Dirk Praet), folowed by a date/time stamp (in GMT time) corresponding to the
date/time stamp of the actual post on the forum, and optionally, the thread it was posted in (
for additional clarification).

Whenever I make a comment I need to establish as originating from myself, an entry is added to the
current day file in forum-posts, the git-commit I then (pgp) sign with
git commit -a -S -m '(some identifier)'

To verify if indeed a post belongs to me through its pgp signatures, you would essentially
need to clone this Git repository and compute a signature verification over the Git Commit
using the command 'git log --show-signature -1'.

More details on Git Signing and Verification can be found on the official Git website linked below:
https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work

To view the signed commits on the Github page, click on `X commits` tab and a status will appear next to the commit message.
  
### Keys

PGP public key: https://pgp.mit.edu/pks/lookup?op=vindex&search=0x6AB25603BA8E1E8C

Signify public key: RWQbPYZQpKvFRCNc1yD+rYi73FNMauuIrVeHz5FxyNWUEUtOtf9QWXO6

