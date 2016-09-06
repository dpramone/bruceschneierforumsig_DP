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
contain my name (Dirk Praet), followed by a date/time stamp (in GMT time) corresponding to the
date/time stamp of the actual post on the forum, and optionally, the thread it was posted in (
for additional clarification).

Whenever I make a comment I need to establish as originating from myself, an entry is added to the
current day file in forum-posts, the git-commit I then (pgp) sign with
git commit -a -S -m '(some identifier)'

To view the signed commits on the Github page, click on `X commits` tab and a status will appear next to the commit message.
Alternatively, to verify if indeed a post belongs to me through its pgp signatures, you can
clone this Git repository and compute a signature verification over the Git Commit using the command
'git log --show-signature -1'.

More details on Git Signing and Verification can be found on the official Git website linked below:
https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work

###  Step by Step Guide

#### Signing your posts

1) Generate a PGP keypair if you don't already have one.

2) Create a Git account and a "schneierforumsig" repo in the Github webinterface.

3) Go to "SSH and PGP keys"-section of your profile's Settings. Add public keys for both if you haven't already done so.

4) Clone the repo to your local hard disk with a git clone https://github.com/your_id/your_repo

5) Edit the README.md to reflect your own thoughts or just copy this one. 
   Add your PGP public key or a key server link to it at the bottom. Optionally, do the same for BSD signify or other key systems.

6) Create a "forum-posts" directory within the repo

7) Create an empty file in DDMMYYY name format in that directory when you're going to make a post, e.g. 06092016

8) After you've made a post, add your comments date/time stamp on the forum as a record to current day file. Prefix with your handle,
   optionally append thread name.

9) git add and sign-commit the changes you've just made: git commit -a -S -m '(some identifier)'

10) git push to remote Github repository

11) Done. Repeat 9-10 for each new post you wish to sign or do a bulk update whenever you feel like it.

#### Verifying others posts

1) Obtain and sign poster's public key

2) Go to poster's Git hub commit page of their (Schneier) blog signed posts repository. Check if commits have the "verified" status.

Alternatively:
2) Clone/Update their "schneierforumsig" repo to hard disk.
3) Verify pgp signatures for specific posts with 'git log --show-signature -1'.
  
### Keys

PGP public key: https://pgp.mit.edu/pks/lookup?op=vindex&search=0x6AB25603BA8E1E8C

Signify public key: RWQbPYZQpKvFRCNc1yD+rYi73FNMauuIrVeHz5FxyNWUEUtOtf9QWXO6

