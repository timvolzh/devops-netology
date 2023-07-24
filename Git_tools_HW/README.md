## Инструменты Git


### Задание № 1. 

>git show  aefea

commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>
Date:   Thu Jun 18 10:29:58 2020 -0400
Update CHANGELOG.md

### Задание № 2.
___

>git log 85024d3

commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)

___

>git show b8d720^1

56cd7859e05c36c06b56d013b55a252d0bb7e158

>git show b8d720^2

9ea88f22fc6269854151c571162c5bcf958bee2b

___

>git log --pretty=oneline v0.12.23...v0.12.24

 33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24) v0.12.24  
b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links  
3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md  
6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable  
5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location  
06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md  
d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows  
4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md  
dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md  
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release  


___

git grep -n -p  -H providerSource
берём оттуда название файла для следующей команды:

git log -L :providerSource:internal/command/init_test.go

Коммит в котором создана функция:
83e84e547712f565d2ea74619eb6562a442a52b1


---

>git log --oneline -G'globalPluginDirs'

22a2580e93 main: Use the new cliconfig package credentials source

35a058fb3d main: configure credentials from the CLI config file

c0b1761096 prevent log output during init

8364383c35 Push plugin discovery down into command package


 ---
>git log -S 'synchronizedWriters' --oneline

bdfea50cc8 remove unused

fd4f7eb0b9 remove prefixed io

5ac311e2a9 main: synchronize writes to VT100-faker on Windows

>git log 5ac311e2a

commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5
Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Wed May 3 16:25:41 2017 -0700