
lbhua@lbhua-PC MINGW64 ~
$ mkdir test

lbhua@lbhua-PC MINGW64 ~
$ cd test

lbhua@lbhua-PC MINGW64 ~/test
$ touch a.md

lbhua@lbhua-PC MINGW64 ~/test
$ git status
fatal: Not a git repository (or any of the parent directories): .git

lbhua@lbhua-PC MINGW64 ~/test
$ git init
Initialized empty Git repository in C:/Users/lbhua/test/.git/

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        a.md

nothing added to commit but untracked files present (use "git add" to track)

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git add a.md

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   a.md


lbhua@lbhua-PC MINGW64 ~/test (master)
$ git commit -m 'my first commit'

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <(null)>) not allowed

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git config --global user.email "MikiLol"

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git config --global user.email "hualibai1993@163.com"

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git commit -m 'my first commit'

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <(null)>) not allowed

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git config --global user.name "MikiLol"

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git commit -m 'my first commit'
[master (root-commit) 0d86752] my first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.md

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   a.md

no changes added to commit (use "git add" and/or "git commit -a")

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git diff
diff --git a/a.md b/a.md
index e69de29..6b76118 100644
--- a/a.md
+++ b/a.md
@@ -0,0 +1 @@
+git is free software
\ No newline at end of file

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git add a.md

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   a.md


lbhua@lbhua-PC MINGW64 ~/test (master)
$ git commit -m "update"
[master 4887aef] update
 1 file changed, 1 insertion(+)

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git status
On branch master
nothing to commit, working directory clean

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git log
commit 4887aef6a9e8a30637737540f1062da39eb21820
Author: MikiLol <hualibai1993@163.com>
Date:   Fri Jun 17 10:43:18 2016 +0800

    update

commit 0d86752ae6364078a77df39ad7281cdff53bfac5
Author: MikiLol <hualibai1993@163.com>
Date:   Fri Jun 17 10:32:37 2016 +0800

    my first commit

lbhua@lbhua-PC MINGW64 ~/test (master)
$ ssh
usage: ssh [-1246AaCfGgKkMNnqsTtVvXxYy] [-b bind_address] [-c cipher_spec]
           [-D [bind_address:]port] [-E log_file] [-e escape_char]
           [-F configfile] [-I pkcs11] [-i identity_file]
           [-L address] [-l login_name] [-m mac_spec]
           [-O ctl_cmd] [-o option] [-p port]
           [-Q cipher | cipher-auth | mac | kex | key]
           [-R address] [-S ctl_path] [-W host:port]
           [-w local_tun[:remote_tun]] [user@]hostname [command]

lbhua@lbhua-PC MINGW64 ~/test (master)
$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/lbhua/.ssh/id_rsa):
Created directory '/c/Users/lbhua/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/lbhua/.ssh/id_rsa.
Your public key has been saved in /c/Users/lbhua/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:ItYAKegsnlKvz4fZWqmaCUu4Ti5KewCh5ASe7flU8jI lbhua@lbhua-PC
The key's randomart image is:
+---[RSA 2048]----+
|+ ..             |
|=o+.             |
|B= ... .         |
|++o .o+          |
|+..+oEo.S        |
|o+ .+.oo         |
|++.. =o          |
|*+o=ooo          |
|B+=o=o           |
+----[SHA256]-----+

lbhua@lbhua-PC MINGW64 ~/test (master)
$ ssh -T git@github.com
The authenticity of host 'github.com (192.30.252.120)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'github.com,192.30.252.120' (RSA) to the list of know                                                                                                                n hosts.
Hi MiKiLol! You've successfully authenticated, but GitHub does not provide shell                                                                                                                 access.

lbhua@lbhua-PC MINGW64 ~/test (master)
$ ssh -T git@github.com
Hi MiKiLol! You've successfully authenticated, but GitHub does not provide shell                                                                                                                 access.

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git remote add origin https://github.com/MikiLol/test.git

lbhua@lbhua-PC MINGW64 ~/test (master)
$ git push  -u origin master
Username for 'https://github.com': MikiLol
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 429 bytes | 0 bytes/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/MikiLol/test.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.

lbhua@lbhua-PC MINGW64 ~/test (master)
$
