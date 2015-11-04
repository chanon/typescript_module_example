# typescript_module_example
An example / test case of importing typescript modules located in a node_modules folder.

# Explanation
This project shows a simple example of importing 3 types of TypeScript (external) modules. 

* First is a normal module declared in a file called ```file_module.ts```
* Next is a module located in ```node_modules``` called ```index_module``` which has index.ts as its main entry point.
* Finally there is ```package_module``` which uses a ```package.json``` file to declare its TypeScript entry point using the ```typescript.main``` property.

# Expected Result
The project should compile without errors. Running the example would display

```
$ node app.js
hello from file_module
hello from index_module
hello from package_module
```

# Current output with TypeScript 1.6.2
Currently tsc version 1.6.2 complains that it cannot find the two packages located in ```node_modules```

```
$ tsc --version
message TS6029: Version 1.6.2

$ tsc app.ts --module commonjs --moduleResolution node
app.ts(2,31): error TS2307: Cannot find module 'index_module'.
app.ts(3,33): error TS2307: Cannot find module 'package_module'.
```

