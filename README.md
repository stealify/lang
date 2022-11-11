# lang designed to replace C and Rust in a incremental way.
The Stealify Lang Reference Implementation

Stealify comes mainly in 3 Flavors .md flavor and a .stealify flavor and .js

## Markdown 
you can use markdown files and indicate that code should be run with stealify via using code block annotations with the lang stealify, ts, js and inside that block use language annotated templateTags 

```js
c`... some c code here`
js`some js code here`
stealify`some stealify code here can contain any flavor`
cpp`some c++`
```

## stealify / ts js ....
Stealify handels everything as Markdown at the start if it discovers shebangs or other code indicators it enters that parsing type
if it discovers for example tripple slash directives or JS import require statments it will jump into the Script Parsing mode.

if it discovers json it will turn that into stealify objects so that it is reference able json parsing is fast. 


## Todo
- Improve Cross Language Boundary Graphs.
- Implement Syntax Highlighting for github.com when the Browser Supports that.
- Improve IDE Integration via typescript-language server wrapper and our external stealify browser interface.
- [ ] - Create a more integrated Encapsulated VSCODE Build with a Hardcoded methods.
  - done @stealify/VSStealify
