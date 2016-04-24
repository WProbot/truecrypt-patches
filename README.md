I use this repository to manage my patches for [truecrypt.deb](https://github.com/stefansundin/truecrypt.deb).

There is a different branch for each patch. Most patches branch of from `7.1a`, but the indicator patch is based on `build-fixes`.

It is easy to use git to create the patches which can then be used in the debianization:
```
git diff 7.1a..build-fixes > ../truecrypt-7.1a-build-fixes.patch
git diff build-fixes..indicator > ../truecrypt-7.1a-indicator.patch
git diff 7.1a..gcc5 > ../truecrypt-7.1a-gcc5.patch
git diff 7.1a..helpfix > ../truecrypt-7.1a-helpfix.patch
git diff 7.1a..open-doc > ../truecrypt-7.1a-open-doc.patch
git diff 7.1a..update-urls > ../truecrypt-7.1a-update-urls.patch
git diff 7.1a..xdg-open > ../truecrypt-7.1a-xdg-open.patch
```
