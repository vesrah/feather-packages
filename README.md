The Feather Project
=======

This repository contains front-end packages for [Project Feather](http://projectfeather.sitefinity.com).

# Issues Fixed in this Fork
Upgrade grunt-sass to one that builds on newer versions of NPM.
Solves issue below during ```npm install```
```
module.js:598
  return process.dlopen(module, path._makeLong(filename));
                 ^

Error: Module did not self-register.
    at Object.Module._extensions..node (module.js:598:18)
    at Module.load (module.js:488:32)
    at tryModuleLoad (module.js:447:12)
    at Function.Module._load (module.js:439:3)
    at Module.require (module.js:498:17)
    at require (internal/module.js:20:19)
    at Object.<anonymous> (/Users/jbrasch/Code/UTI/UTI.SitefinityWebApp/ResourcePackages/Foundation6/node_modules/node-sass/lib/index.js:181:15)
    at Module._compile (module.js:571:32)
    at Object.Module._extensions..js (module.js:580:10)
    at Module.load (module.js:488:32)
npm WARN Foundation@ No repository field.
npm WARN Foundation@ No license field.
npm ERR! Darwin 15.6.0
npm ERR! argv "/usr/local/Cellar/node/7.10.0/bin/node" "/usr/local/bin/npm" "install" "--save-dev" "node-sass@1.2.3"
npm ERR! node v7.10.0
npm ERR! npm  v4.2.0
npm ERR! code ELIFECYCLE
npm ERR! errno 1

npm ERR! node-sass@1.2.3 postinstall: `node scripts/build.js`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the node-sass@1.2.3 postinstall script 'node scripts/build.js'.
npm ERR! Make sure you have the latest version of node.js and npm installed.
npm ERR! If you do, this is most likely a problem with the node-sass package,
npm ERR! not with npm itself.
npm ERR! Tell the author that this fails on your system:
npm ERR!     node scripts/build.js
npm ERR! You can get information on how to open an issue for this project with:
npm ERR!     npm bugs node-sass
npm ERR! Or if that isn't available, you can get their info via:
npm ERR!     npm owner ls node-sass
npm ERR! There is likely additional logging output above.
```
Fix grunt uglify option to allow building without error.  Error shown below:
```
Running "uglify:dist" (uglify) task
TypeError: Cannot create property 'warnings' on boolean 'true'
    at Object.exports.minify (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt-contrib-uglify/tasks/lib/uglify.js:82:35)
    at /Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt-contrib-uglify/tasks/uglify.js:136:25
    at Array.forEach (native)
    at Object.<anonymous> (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt-contrib-uglify/tasks/uglify.js:61:16)
    at Object.<anonymous> (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt/lib/grunt/task.js:264:15)
    at Object.thisTask.fn (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt/lib/grunt/task.js:82:16)
    at Object.<anonymous> (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt/lib/util/task.js:301:30)
    at Task.runTaskFn (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt/lib/util/task.js:251:24)
    at Task.<anonymous> (/Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt/lib/util/task.js:300:12)
    at /Users/jbrasch/Code/feather-packages/community-packages/Foundation/node_modules/grunt/lib/util/task.js:227:11
>> Uglifying source node_modules/zurb-foundation-5/js/foundation/foundation.js failed.
Warning: Uglification failed.
Cannot create property 'warnings' on boolean 'true'.
 Use --force to continue.
```

# Related Repositories

[feather](https://github.com/Sitefinity/feather) - This repository contains the core infrastructure related to the Feather project.

[feather-widgets](https://github.com/Sitefinity/feather-widgets) - This repository contains custom MVC widgets which are part of the Feather project.

[feather-samples](https://github.com/Sitefinity/feather-samples) - This repository contains code samples related to the Feather project.

# Sitefinity  compatibility

| Feather version | Sitefinity version |
|----|----|
| v.1.9.800.0 - latest | 10.0.6400.0 to 10.0.9999 |
| v.1.7.600.0 - 1.7.690.0 | 9.2.6200.0 to 9.2.9999 |
| v.1.6.500.0 - 1.6.560.0 | 9.1.6100.0 to 9.1.9999 |
| v.1.5.470.0 - 1.5.490.0 | 9.0.6000.0 to 9.0.9999 |
| v.1.4.360.0 - 1.4.460.0 | 8.2.5900.0 to 8.2.9999 |
| v.1.3.300.1 - 1.3.350.0 | 8.1.5800.0 to 8.1.9999 |
| v.1.2.120.0 - 1.2.290.1 | 8.0.5700.0 to 8.0.9999 |
| v.1.1.20.3 - 1.1.110.0 | 7.3.5600.0 to 7.3.9999 |
| v.1.0.0.0 - 1.0.10.2 | 7.2.5300.0 to 7.2.9999 |
| v.0.5.1000.4  | 7.1.5208.0 to 7.1.9999 |
| v.0.4.1000.2  | 7.1.5200.0 to 7.1.9999 |
| v0.1.1000.1 - v.0.3.1000.4  | 7.0.5100.0 to 7.0.9999 |

# License Information

This project has been released under the Apache License, version 2.0, the text of which is included below. This license applies ONLY to the project-specific source of each repository and does not extend to Telerik Sitefinity CMS itself, or any other 3rd party libraries used in a repository. For licensing information about Telerik Sitefinity CMS, see the [License Agreements page](http://www.sitefinity.com/purchase/license-agreement) at [Sitefinity.com](http://www.sitefinity.com/).

Copyright © 2005-2017 Telerik AD

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
