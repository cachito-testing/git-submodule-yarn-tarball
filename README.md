# git-submodule-yarn

Repo for testing how Cachito handles [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). <br/>
Such repos can be identified with `[submodule "<submodule path>"]` sections* in `.gitmodules`. <br/>

Also, it turns out that Cachito handles Git submodules better than Git itself does.
Git actually does not provide the contents inside of submodules in its [tarball](https://github.com/cachito-testing/git-submodule-yarn/tarball/387dd2f3297ec0253fecc8f13c7ea741127e78e0).
This particular case is handled with [another repository](https://github.com/cachito-testing/git-submodule-yarn-tarball) which contains the same exact contents, but treats the submodule as a normal directory. <br/>

There are **3** of these repos - for package managers pip, npm, and Yarn: <br/>
1. [pip repo with a pip Git submodule](https://github.com/cachito-testing/git-submodule-pip) <br/>
2. [npm repo with a npm Git submodule](https://github.com/cachito-testing/git-submodule-npm) <br/>
3. **Yarn repo with a Yarn Git submodule** <br/>

This particular repo is essentially [cachito-yarn-without-deps](https://github.com/cachito-testing/cachito-yarn-without-deps) containing [cachito-yarn-with-deps](https://github.com/cachito-testing/cachito-yarn-with-deps) as a submodule. <br/>
<br/>*`git-submodule-yarn/.gitmodules`:
```
[submodule "cachito-yarn-with-deps"]
	path = cachito-yarn-with-deps
	url = https://github.com/cachito-testing/cachito-yarn-with-deps.git
```
