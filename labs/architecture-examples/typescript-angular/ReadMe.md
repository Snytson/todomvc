# TypeScript + AngularJS #

## Motivation ##
[Typescript](http://www.typescriptlang.org/) 
is a superset of JavaScript, with optional type annotations. 
As any JS is valid TS, there is no interoperability issue. 
You could slowly convert existing JS code-base and use JS libraries natively. 
You already know most of the language. 
It compiles back to JS.

It's attractive to people with strongly typed languages background, 
who are willing to type in more code (classes and type annotations). 
Receiving benefit of type checking on compile time. 
Also IntelliSense works better. 

Generally recommended for large projects.

## Editors ##
The best editor for TypeScript is at the moment Visual Studio 2012 with 
[TypeScript](http://go.microsoft.com/fwlink/?LinkID=266563) and 
[Web Essentials 2012](http://visualstudiogallery.msdn.microsoft.com/07d54d12-7133-4e15-becb-6f451ea3bea6) plugins. 

Webstorm is [coming soon](http://joeriks.com/2012/11/20/a-first-look-at-the-typescript-support-in-webstorm-6-eap/).

## Node.js ##
standalone compiler is is available on NPM.
```
npm install -g typescript
```

To compile the TS code in this project run this in the current directory.
```
tsc -sourcemap js/_all.ts 
```

## Ambient declarations ##
It is useful to have type information for the API of libraries you use. 
[DefinitelyTyped](https://github.com/borisyankov/DefinitelyTyped) is a nice collection of annotations by Boris Yankov.


## Files ##
* `*.ts` are source code.
* `*.d.ts` are ambient declarations for libraries.
* `*.js` are generated by the compiler, except in `js/libs` folder.
* `*.js.map` are [source maps](http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/) generated by the compiler, for better debugging experience.
* `_all.ts` is convention used to enumerate file references in the project for benefit of TypeScript compiler. 

If the number of files grows, you could put an `_all.ts` file into each folder, move all nested references to it and reference the nested `_all.ts` from the parent `_all.ts`.

Start reading `TodoCtrl.ts` first and continue with `Application.ts` and `Index.html`, the rest of it is easy. 

AngularJS has a steeper learning curve than TypeScript.

## AngularJS ##
There is very little difference between this app and the vanilla AngularJS todo app in how AngularJS is used.
The only significant difference is that dependency injection is done via annotated constructors, which allows minification of JavaScript.

It's definitely possible to convert the vanillajs todo app into TypeScript, but TypeScript's benefits are more obvious with a *full blown framework and project structure*.

[AngularJS](http://docs.angularjs.org/)
[documentation](http://docs.angularjs.org/guide/),
[reference](http://docs.angularjs.org/api/) and 
[tutorials](http://docs.angularjs.org/tutorial) 
are worth reading in detail.