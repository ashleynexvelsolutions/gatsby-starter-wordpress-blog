This doesn't seem to be working with React 18 when an image is present in the content of a post. It works fine with React 17.0.2.

Steps to reproduce:
`npm install`
`gatsby develop`
Go to http://localhost:8000/test-post-1/. You should see:
```
Unhandled Runtime Error
One unhandled runtime error found in your files. See the list below to fix it:


Error in function createFiberFromTypeAndProps in ./node_modules/react-dom/cjs/react-dom.development.js:28221
Element type is invalid: expected a string (for built-in components) or a class/function (for composite components) but got: undefined. You likely forgot to export your component from the file it's defined in, or you might have mixed up default and named imports.

./node_modules/react-dom/cjs/react-dom.development.js:28221

  28219 |           }
  28220 |
> 28221 |           throw new Error('Element type is invalid: expected a string (for built-in ' + 'components) or a class/function (for composite components) ' + ("but got: " + (type == null ? type : typeof type) + "." + info));
  28222 |         }
  28223 |     }
  28224 |   }
```