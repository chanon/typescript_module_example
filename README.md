# typescript_module_example
An example / test case of importing typescript modules located in a node_modules folder.

# Explanation
This project shows a simple example of importing 3 types of TypeScript (external) modules. 

* First is a normal module declared in a file called ```file_module.ts```
* Next is a module located in ```node_modules``` called ```index_module``` which has index.ts as its main entry point.
* Finally there is ```package_module``` which uses a ```package.json``` file to declare its TypeScript entry point using the ```typings``` property. 
 
Note that for published modules you should use a ```d.ts``` file for the ```typings``` property as you don't want your module consumers to recompile your module, just consume its typings.

# Expected Result
The project should compile without errors. Running the example would display

```
$ node app.js
hello from file_module
hello from index_module
hello from package_module
```

# Current output with TypeScript 1.8.0-dev.20151104

```
$ tsc --version
message TS6029: Version 1.8.0-dev.20151104

$ tsc app.ts --module commonjs --moduleResolution node

$
```
