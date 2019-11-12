# es6-modules
TL;DR version of Lin Clark's deep dive on [ES6 modules](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)

## What problem do modules solve?

Every JS code has to deal with variables and their modifications.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/01_variables.png)

With scopes, functions can't access varialbes in other functions.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/02_module_scope_01.png)

Downside of this approach is handling shared variables. Back in jquery days, we used to have all the shared variables in global scope.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/02_module_scope_02.png)

Downside of this approach is to handle order of scripts.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/02_module_scope_03.png)

## How do modules help?

 Module scopes have a way of making their variables available to other modules through imports and exports.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/02_module_scope_04.png)

## How ES modules work

With modules you build graph of dependencies. You need to provide entry point and it follows any import statements to find rest of code.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/04_import_graph.png)

Module record file is created for every module.
![](https://2r4s9p1yi1fa2jd7j43zph8r-wpengine.netdna-ssl.com/files/2018/03/05_module_record.png)

Module record is later turned into module instance.
Instance has code (instructions) and state (values of varialbes or function)
![]()
