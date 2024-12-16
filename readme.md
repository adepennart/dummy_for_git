# intro to git
## why git?

Git was built for version control.
Also allows branches to be built (ie. developer branch, main functional branch)

## git as a user (not a developer)

1. download git repository from github
2. update to local version with latest version on github
3. check out other versions

## 1. download/cloning git repository from github

Find github repository of interest. In the top right should be a green button. Clicking on it, you will see writting 'clone' copy the https link below it. 

Find a directory you intend to work in.

```bash=
#i.e.,
mkdir dung_track
cd dung_track
```

Then we will clone repository in this directory
```bash=
#i.e.,
git clone https://github.com/refmitchell/autotracker-deluxe.git

#outputed should be something like

#Cloning into 'autotracker-deluxe'...
#remote: Enumerating objects: 101, done.
#remote: Counting objects: 100% (101/101), done.
#remote: Compressing objects: 100% (71/71), done.
#remote: Total 101 (delta 59), reused 58 (delta 26), pack-reused 0
#Receiving objects: 100% (101/101), 53.85 KiB | 2.07 MiB/s, done.
#Resolving deltas: 100% (59/59), done.
```

If all works correctly you should have the repository downloaded in your intended directory!

## 2. update to local version with latest version on github
If you want to update your local version with a update version on github. the following code will allow this.(ensure you are in the correct directory (i.e., ))
```bash=
git pull
```

## 3. check out other versions/branches
If for some reason the newest version is not working for you but a older version is you can revert to a older version.

First you need to find which version. The following command will get the full history of previous versions.
```bash=
git log

#i recommend if you want a simplified version
git log --oneline

#i.e., output
#0751ace (HEAD -> master, origin/master, origin/HEAD) Fix issue #12
#298da0d Fix issue #9
#49a195e Fixes issue #10
#dda71a1 Fix issue #7

#if you are stuck in log view
#pressing q will get you out
```

Then change to the version of interest. Each version has a id, so copy the from one of the versions and sue the following command
```bash=
git checkout [version_id_of_interest]

#i.e.,
git checkout 298da0d

#i.e., output
#Note: switching to '298da0d'.
#[...]
#HEAD is now at 298da0d Fix issue #9
```
You can now the older code instead of the new one.

It is easy to switch back to the newest version on your local machine.
```bash=
git checkout master
```
This will bring you back to the newest version.

