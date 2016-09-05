
## get error while running hexo
(http://kikoroc.com/2016/05/04/resolve-hexo-DTraceProviderBindings-MODULE-NOT-FOUND.html)
```shell
{ [Error: Cannot find module './build/Release/DTraceProviderBindings'] code: 'MODULE_NOT_FOUND' }
{ [Error: Cannot find module './build/default/DTraceProviderBindings'] code: 'MODULE_NOT_FOUND' }
{ [Error: Cannot find module './build/Debug/DTraceProviderBindings'] code: 'MODULE_NOT_FOUND' }
```

```shell
npm i -S hexo --no-optional
``` 

```shell
npm uninstall hexo-cli -g
npm i hexo-cli -g --no-optional
```

## switch theme
```shell
g co master; g pull

# KEEP .git, .gitignore, and files listed in .gitignore
# REMOVE others

# ( optional ) add a temporary index.html
g ci -am 'switch theme xxx'
g push origin master:master

g co gh-pages; hexo generate; hexo deploy
```
