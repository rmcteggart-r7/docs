# Components.json

All component libraries must contain a `components.json` file. The purpose of this file is to describe which components are available to the Budibase builder, and to describe their properties.

This file is not used at runtime by your built app. It is only used to describe components to the builder.

The file will take the overall structure of:

```javascript
{
  // Path to your built javascript package 
  "_lib": "./dist/index.js", 

  // Generators for the library 
  "_generators": {
    // Keyed by generator name 
    "form": {
        // See later for generator json API 
     }
  },

  // Every other key refers to a component, exported by the file in '_lib'  
  "textInput" : {
      // See later for json API 
  },

  "datePicker" : {

  }
}
```

* `_lib` : the path to your packaged components file \(javascript\). This file must export all components and generators declared in the `components.json` file
* `_generators` a JSON object. Keys of this object must correspond to exports from your \_lib file
* All other root keys in `components.json` should correspond to exports from your \_lib file. Root keys are assumed to be components

