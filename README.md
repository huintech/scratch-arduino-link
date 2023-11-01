# Scratch Arduino Link
[![](https://github.com/OttawaSTEM/scratch-arduino-link/actions/workflows/release.yml/badge.svg?branch=main)](https://github.com/OttawaSTEM/scratch-arduino-link/actions/workflows/release.yml)
![Github Releases](https://img.shields.io/github/downloads/ottawastem/scratch-arduino-link/total?color=orange)
![](https://img.shields.io/github/license/OttawaSTEM/scratch-arduino-link)


Scratch Arduino Link is a helper application that lets you connect Scratch to Arduino Robots and Arduino Boards.

Using Scratch Arduino Link requires both [Scratch Arduino](https://scratch.ottawastem.com) and a compatible Arduino Robot or Arduino device.

Scratch Arduino Link appears as an icon at the bottom of your screen.

[Scratch Arduino](https://scratch.ottawastem.com) is fork of [official Scratch 3.0](https://github.com/LLK/scratch-gui),

# Using Scratch Arduino Link with Scratch 3.0
to use Scratch Arduino with Scratch 3.0:
1. Download [Scratch Arudino Link](https://github.com/OttawaSTEM/scratch-arduino-link/releases/latest/)
2. Install and run Scratch Arudino Link
3. Open [Scratch Arduino](https://scratch.ottawastem.com)
4. Select Arduino Robot or Arduino Device
5. Build a porject with the new extension blocks. Scratch Arduino Link will help Scratch cummunicate with your Arduino Robot and Arduino Device
# Development
```bash
npm install
npm run fetch
npm start
```

# Error
```shell
$ npm start

> scratch-arduino-link@1.0.0 start D:\workspaces\workspace-scratch\arduino\scratch-arduino-link
> electron .


App threw an error during load
Error: The module '\\?\D:\workspaces\workspace-scratch\arduino\scratch-arduino-link\node_modules\@serialport\bindings\build\Release\bindings.node'
was compiled against a different Node.js version using
NODE_MODULE_VERSION 83. This version of Node.js requires
NODE_MODULE_VERSION 89. Please try re-compiling or re-installing
the module (for instance, using `npm rebuild` or `npm install`).
    at process.func [as dlopen] (electron/js2c/asar_bundle.js:5:1846)
    at Object.Module._extensions..node (internal/modules/cjs/loader.js:1138:18)
    at Object.func [as .node] (electron/js2c/asar_bundle.js:5:1846)
    at Module.load (internal/modules/cjs/loader.js:935:32)
    at Module._load (internal/modules/cjs/loader.js:776:14)
    at Function.f._load (electron/js2c/asar_bundle.js:5:12913)
    at Module.require (internal/modules/cjs/loader.js:959:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at bindings (D:\workspaces\workspace-scratch\arduino\scratch-arduino-link\node_modules\bindings\bindings.js:112:48)
    at Object.<anonymous> (D:\workspaces\workspace-scratch\arduino\scratch-arduino-link\node_modules\@serialport\bindings\lib\win32.js:1:36)
```

package.json 파일에 electron-rebuild 추가
```json
{
  // ...(생략)...
  "scripts": {
    // ...(생략)...
    "install": "electron-rebuild"
  },
    // ...(생략)...
}
```

# Attribution
Thanks to all these great people it has been possible to make this project:
* [OpenBlock](https://github.com/openblockcc)
