I use this repository to manage my patches for [truecrypt.deb](https://github.com/stefansundin/truecrypt.deb).

There is a different branch for each patch. It is easy to use git to create the patches which can then be used in the debianization.

```
for branch in 7.1a build-fixes gcc5 gcc6 gui-fixes indicator helpfix xdg-open open-doc update-urls
do
  git branch --track $branch origin/$branch
done

git diff --ignore-space-at-eol 7.1a..build-fixes > ../truecrypt-7.1a-build-fixes.patch
git diff --ignore-space-at-eol 7.1a..gcc5 > ../truecrypt-7.1a-gcc5.patch
git diff --ignore-space-at-eol build-fixes..gcc6 > ../truecrypt-7.1a-gcc6.patch
git diff --ignore-space-at-eol 7.1a..gui-fixes > ../truecrypt-7.1a-gui-fixes.patch
git diff --ignore-space-at-eol build-fixes..indicator > ../truecrypt-7.1a-indicator.patch
git diff --ignore-space-at-eol 7.1a..helpfix > ../truecrypt-7.1a-helpfix.patch
git diff --ignore-space-at-eol 7.1a..xdg-open > ../truecrypt-7.1a-xdg-open.patch
git diff --ignore-space-at-eol 7.1a..open-doc > ../truecrypt-7.1a-open-doc.patch
git diff --ignore-space-at-eol 7.1a..update-urls > ../truecrypt-7.1a-update-urls.patch
```
