# TRANSPILATION

## 1. Definition

### **HISTORY**
_Transpilation comes from two words "translate" and "compilation". It first emerged between the 1960s and 1970s with tools for translating languages like COBOL , assembly , etc._

Transpilation is the type of compilation that takes high-level source code and converts it into another high-level source code while keeping the abstraction level same (not changing the logic of code, mostly changing just the syntax). It is also called source to source compilation. Examples of transpilers include Babel, CoffeeScript, TypeScript, etc.

Unlike compilation, it does not convert human read-able source code into machine read-able code , rather it transpiles HLL source code into another HLL source code.

## 2. Necessity 

1. It was needed so that the code written in latest syntax could be run on older version of browser which won't recogize the latest version of HLL source code.It also helps developers in converting some program or code written in one HLL into another HLL or HLL version. Example JS(ES6) to JS(ES5).

2. It is also needed for langauges like TypeScript, CoffeeScript, etc.,that browsers cannot execute or read directly. So, a transpiler convers TypeScript source code into JavaScript source code. In this way way the browser can run the code after transpilation.

## 3. Working

A transpiler reads the source code and builds an AST, Abstract Syntax Tree. Then it makes tokens of sections of code for parsing. These tokens are then parsed in the form of group to be syntaxized accordingly. The changes are saved in the AST tree and then the code is executed. It can then translate the updated AST with new syntax source code. It is finally then used to give output source code.


## 4. Proof 

-Proof 1:

**TypeScript:**
```typescript
function square(x: number, z: string) {
    let y = x * x;
    console.log(z + y)
}
square(4, "Square:");

```
**JavaScript:**
```javascript
"use strict";
function square(x, z) {
    let y = x * x;
    console.log(z + y);
}
square(4, "Square:");
```
**Changes**

The transpiler converted TypeScript source code into simple JS source code. It basically just changed the syntax. Its purpose was to make it executable or read-able for older versions of browser or softwares that don't recognize TypeScript.

-Proof 2:

**Newer JS:**
```javascript
const add = (a, b) => {
  return a + b;
};

```

**Older JS:**

```javascript
var add = function add(a, b) {
  return a + b;
};

```

__Changes__

The transpiler converted the code function written in latest JS into older version of JS. Basically changing the arrow (=>) function method into simple funtion. Before transpilation, source code was using JS(ES6) version of javascript but afterwards, it is converted into JS(ES5) version.


## 5. Source maps


Source map is a file created by the transpiler, i.e Babel. It is used to access the developer source code (non-transpiled code) even after transpilation. The browser may use the transpiled code but when user opens DevTools, user doesn't want to see the transpiled source code, he wants to see the original code. Source map keeps that track, it uses `.map` file to give user the exact changes in code by transpilation. It basically tells which part of newer code replaces which part of older code version after transpilation. 


## 6. Transpilation vs Minification

Minification is essentially only shriking the text or code, making code smaller in terms of size. Making functions for repeating code parts and statements. It does not change the language level or change the syntax. On the other hand, transpilation is not shrinking code, it changes the language level. Transpilation is the conversion of code, __not__ minification or shrinking. It may shrink or minimize some part of code but that is not the concept of transpilation. It is based on source to source compilation from one High level source code into another. It may also enlarge the code size as the newer versions of code usually comes smaller and concise in size.



### Sources





