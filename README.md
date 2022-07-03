# easyFHE

For each submodule run

```
npm run install
```

```
npm run build
```

## Update site demo

1. Delete `dist` folder from the root directory

```
rm -rf dist/
```

2. Delete branch locally

```
git branch -d gh-pages
```

3. Delete branch remotely

```
git push origin --delete gh-pages
```

4. To build quasar demo go in `fhe-module-quasar-demo`

```
quasar build
```

5. Copy folder `dist` folder to root folder

```
cp -r dist/ ../
```

6. Commit changes

```
cd ..
git add dist && git commit -m 'updated demo'
```

7. Recreate gh-pages branch

```
git subtree push --prefix dist/spa origin gh-pages
```

## All commands

### (must be in easyFHE root directory)

```
rm -rf dist/
git branch -d gh-pages
git push origin --delete gh-pages
cd fhe-module-quasar-demo/
rm -rf dist/
quasar build
cp -r dist/ ../
cd ..
git add dist && git commit -m 'updated demo'
git subtree push --prefix dist/spa origin gh-pages

```
