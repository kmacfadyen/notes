# notes
React Native snippets:

import React from 'react';
import {Text, View} from 'react-native';

const YourApp = () => {
  return (
    <View
      style={{
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
      }}>
      <Text>Try editing me! 🎉</Text>
    </View>
  );
};

export default YourApp;

--------------------------

import React from 'react';
import {View, Text, Image, ScrollView, TextInput} from 'react-native';

const App = () => {
  return (
    <ScrollView>
      <Text>Some text</Text>
      <View>
        <Text>Some more text</Text>
        <Image
          source={{
            uri: 'https://reactnative.dev/docs/assets/p_cat2.png',
          }}
          style={{width: 200, height: 200}}
        />
      </View>
      <TextInput
        style={{
          height: 40,
          borderColor: 'gray',
          borderWidth: 1,
        }}
        defaultValue="You can type in me"
      />
    </ScrollView>
  );
};

export default App;

------------------

Hello world! 

import React from 'react';
import {Text, View} from 'react-native';

const HelloWorldApp = () => {
  return (
    <View
      style={{
        flex: 1,
        justifyContent: 'center',
        alignItems: 'center',
      }}>
      <Text>Hello, world!</Text>
    </View>
  );
};
export default HelloWorldApp;

--------------

1. Install the React Native Elements package from the NPM
npm install @rneui/base @rneui/themed

--------------
Python has a set of built-in functions.

Function	Description
abs()	Returns the absolute value of a number
all()	Returns True if all items in an iterable object are true
any()	Returns True if any item in an iterable object is true
ascii()	Returns a readable version of an object. Replaces none-ascii characters with escape character
bin()	Returns the binary version of a number
bool()	Returns the boolean value of the specified object
bytearray()	Returns an array of bytes
bytes()	Returns a bytes object
callable()	Returns True if the specified object is callable, otherwise False
chr()	Returns a character from the specified Unicode code.
classmethod()	Converts a method into a class method
compile()	Returns the specified source as an object, ready to be executed
complex()	Returns a complex number
delattr()	Deletes the specified attribute (property or method) from the specified object
dict()	Returns a dictionary (Array)
dir()	Returns a list of the specified object's properties and methods
divmod()	Returns the quotient and the remainder when argument1 is divided by argument2
enumerate()	Takes a collection (e.g. a tuple) and returns it as an enumerate object
eval()	Evaluates and executes an expression
exec()	Executes the specified code (or object)
filter()	Use a filter function to exclude items in an iterable object
float()	Returns a floating point number
format()	Formats a specified value
frozenset()	Returns a frozenset object
getattr()	Returns the value of the specified attribute (property or method)
globals()	Returns the current global symbol table as a dictionary
hasattr()	Returns True if the specified object has the specified attribute (property/method)
hash()	Returns the hash value of a specified object
help()	Executes the built-in help system
hex()	Converts a number into a hexadecimal value
id()	Returns the id of an object
input()	Allowing user input
int()	Returns an integer number
isinstance()	Returns True if a specified object is an instance of a specified object
issubclass()	Returns True if a specified class is a subclass of a specified object
iter()	Returns an iterator object
len()	Returns the length of an object
list()	Returns a list
locals()	Returns an updated dictionary of the current local symbol table
map()	Returns the specified iterator with the specified function applied to each item
max()	Returns the largest item in an iterable
memoryview()	Returns a memory view object
min()	Returns the smallest item in an iterable
next()	Returns the next item in an iterable
object()	Returns a new object
oct()	Converts a number into an octal
open()	Opens a file and returns a file object
ord()	Convert an integer representing the Unicode of the specified character
pow()	Returns the value of x to the power of y
print()	Prints to the standard output device
property()	Gets, sets, deletes a property
range()	Returns a sequence of numbers, starting from 0 and increments by 1 (by default)
repr()	Returns a readable version of an object
reversed()	Returns a reversed iterator
round()	Rounds a numbers
set()	Returns a new set object
setattr()	Sets an attribute (property/method) of an object
slice()	Returns a slice object
sorted()	Returns a sorted list
staticmethod()	Converts a method into a static method
str()	Returns a string object
sum()	Sums the items of an iterator
super()	Returns an object that represents the parent class
tuple()	Returns a tuple
type()	Returns the type of an object
vars()	Returns the __dict__ property of an object
zip()	Returns an iterator, from two or more iterators

2. Import the component and use it in your project
import React from 'react';
import { Button } from '@rneui/base';

const AwesomeButton = () => (<Button title='Welcome'/>)

--------------

TYPESCRIPT:

Within your npm project, run the following command to install the compiler:

npm install typescript --save-dev
Which should give you an output similar to:

added 1 package, and audited 2 packages in 2s
found 0 vulnerabilities
The compiler is installed in the node_modules directory and can be run with: npx tsc.

npx tsc
Which should give you an output similar to:

Version 4.5.5
tsc: The TypeScript Compiler - Version 4.5.5
Followed by a list of all the Common Commands.

---------------

(https://github.com/kmacfadyen/notes/assets/113712611/fdcb9912-73f1-4803-a5da-bb17dec4215b)

---------------

More TypeScript:

let ids: number[] = [1, 2, 3, 4, 5]; // can only contain numbers
let names: string[] = ['Danny', 'Anna', 'Bazza']; // can only contain strings
let options: boolean[] = [true, false, false]; can only contain true or false
let books: object[] = [
  { name: 'Fooled by randomness', author: 'Nassim Taleb' },
  { name: 'Sapiens', author: 'Yuval Noah Harari' },
]; // can only contain objects
let arr: any[] = ['hello', 1, true]; // any basically reverts TypeScript back into JavaScript

ids.push(6);
ids.push('7'); // ERROR: Argument of type 'string' is not assignable to parameter of type 'number'.

---------------

Debugging

VS Code has built-in support for TypeScript debugging. To support debugging TypeScript in combination with the executing JavaScript code, VS Code relies on source maps for the debugger to map between the original TypeScript source code and the running JavaScript. You can create source maps during the build by setting "sourceMap": true in your tsconfig.json.

{
  "compilerOptions": {
    "target": "ES5",
    "module": "CommonJS",
    "outDir": "out",
    "sourceMap": true
  }
}

---------------

Step 3: Make the TypeScript Build the default
You can also define the TypeScript build task as the default build task so that it is executed directly when triggering Run Build Task (⇧⌘B). To do so, select Configure Default Build Task from the global Terminal menu. This shows you a picker with the available build tasks. Select TypeScript tsc: build, which generates the following tasks.json file in a .vscode folder:

{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "type": "typescript",
            "tsconfig": "tsconfig.json",
            "problemMatcher": [
                "$tsc"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}

---------------

Class declarations must not be terminated with semicolons:

class Foo {
}
class Foo {
}; // Unnecessary semicolon
In contrast, statements that contain class expressions must be terminated with a semicolon:

export const Baz = class extends Bar {
  method(): number {
    return this.x;
  }
}; // Semicolon here as this is a statement, not a declaration
exports const Baz = class extends Bar {
  method(): number {
    return this.x;
  }
}
It is neither encouraged nor discouraged to have blank lines separating class declaration braces from other class content:

// No spaces around braces - fine.
class Baz {
  method(): number {
    return this.x;
  }
}

// A single space around both braces - also fine.
class Foo {

  method(): number {
    return this.x;
  }

}

--------------------------

Tailwind CSS Examples:

<div>
  <form class="m-4 flex">
    <input class="rounded-l-lg p-4 border-t mr-0 border-b border-l text-gray-800 border-gray-200 bg-white" placeholder="your@mail.com" />
    <button class="px-8 rounded-r-lg bg-yellow-400 text-gray-800 font-bold p-4 uppercase border-yellow-500 border-t border-b border-r">Subscribe</button>
  </form>
</div>



<div class="max-w-2xl mx-auto">
  <form class="flex items-center">
    <label for="simple-search" class="sr-only">Search</label>
    <div class="relative w-full">
      <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
        <svg class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path>
        </svg>
      </div>
      <input type="text" id="simple-search" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full pl-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Search" required>
    </div>
    <button type="submit" class="p-2.5 ml-2 text-sm font-medium text-white bg-blue-700 rounded-lg border border-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"><svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
      </svg></button>
  </form>
</div>

--------------------------

TypeScript Angular Snippets
Snippet	Purpose
a-component	component
a-component-standalone	standalone component
a-component-inline	component with inline template
a-component-root	root app component
a-ctor-skip-self	angular NgModule's skipself constructor
a-directive	directive
a-guard-can-activate	CanActivate guard
a-guard-can-activate-child	CanActivateChild guard
a-guard-can-deactivate	CanDeactivate guard
a-guard-can-match	CanMatch guard
a-httpclient-get	httpClient.get with Rx Observable
a-http-interceptor	Empty Angular HttpInterceptor for HttpClient
a-http-interceptor-headers	Angular HttpInterceptor that sets headers for HttpClient
a-http-interceptor-logging	Angular HttpInterceptor that logs traffic for HttpClient
a-module	module
a-module-root	root app module
a-output-event	@Output event and emitter
a-pipe	pipe
a-preload-opt-in-strategy	custom preload strategy that allows choosing which routes to preload
a-preload-network-strategy	custom preload strategy that preloads based on network connectivity
a-resolver	resolver
a-routes	Route definition file
a-rxjs-import	import RxJs features
a-rxjs-operators	import RxJs operators
a-route-path-404	404 route path
a-route-path-default	default route path
a-route-path-with-children	route path with children
a-route-path-eager	eager route path
a-route-path-lazy	lazy route path
a-router-events	listen to one or more router events
a-route-params-subscribe	subscribe to route parameters
a-service	service with injectable provided in root
a-service-httpclient	service with HttpClient
a-subscribe	Rx Observable subscription
a-trackby	to create a trackby function in TypeScript for the ngFor
NgRx Snippets
Snippet	Purpose
a-ngrx-store-module	create an NgRx store module
a-ngrx-create-action	create an NgRx action with createAction
a-ngrx-create-action-props	create an NgRx action with createAction with props
a-ngrx-create-reducer	create an NgRx reducer with createReducer
a-ngrx-create-effect	create an NgRx effect with createEffect
a-ngrx-create-effect-api	create an NgRx effect with createEffect for an API call
a-ngrx-create-selector	create an NgRx selector with createSelector
a-ngrx-create-selector-props	create an NgRx selector with createSelector with props
a-ngrx-data-entity-data-module-import	add EntityDataModule
a-ngrx-data-entity-metadata	create the entity metadata for NgRx
a-ngrx-data-entity-collection-data-service	create a data service using NgRx

--------------------------
