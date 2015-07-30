# Native Module Path
Give love to path of native Node.js modules to support different runtime versions.

## API

### NMP.join
Acts like path.join but injects a version string of current running v8 engine running.
```javascript
var NMP = require("nmp");
var nmp = new NMP();

var dir = nmp.join(__dirname, "bin", "my-native-module-name.node");
console.log(dir)

// --> c:\git\nmp\test\bin\win32-ia32-v8-3.28\my-native-module-name.node