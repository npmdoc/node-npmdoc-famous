# api documentation for  [famous (v0.7.1)](https://github.com/Famous/engine#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-famous.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-famous) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-famous.svg)](https://travis-ci.org/npmdoc/node-npmdoc-famous)
#### Famous Engine =================

[![NPM](https://nodei.co/npm/famous.png?downloads=true)](https://www.npmjs.com/package/famous)

[![apidoc](https://npmdoc.github.io/node-npmdoc-famous/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-famous_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-famous/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-famous/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-famous/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Famous"
    },
    "browserify": {
        "transform": [
            "glslify"
        ]
    },
    "bugs": {
        "url": "https://github.com/Famous/engine/issues"
    },
    "dependencies": {
        "glslify": "^2.0.0"
    },
    "description": "Famous Engine =================",
    "devDependencies": {
        "browserify": "^10.2.1",
        "colors": "^1.1.0",
        "eslint": "^0.21.2",
        "glob": "^5.0.10",
        "istanbul": "^0.3.15",
        "rewire": "^2.3.3",
        "sinon": "^1.14.1",
        "smokestack": "^3.2.2",
        "tap-closer": "^1.0.0",
        "tap-spec": "^4.0.0",
        "tape": "^4.0.0",
        "uglify-js": "^2.4.17"
    },
    "directories": {},
    "dist": {
        "shasum": "1e3751912b2f44ac4a22930c153e647dce52a5c8",
        "tarball": "https://registry.npmjs.org/famous/-/famous-0.7.1.tgz"
    },
    "gitHead": "68dd0345078ef44daa74de6a22b89e19eaeaaa9f",
    "homepage": "https://github.com/Famous/engine#readme",
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "thealphanerd",
            "email": "myles.borins@gmail.com"
        },
        {
            "name": "famous",
            "email": "npm@famo.us"
        },
        {
            "name": "michaelobriena",
            "email": "michaelobriena@gmail.com"
        }
    ],
    "name": "famous",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Famous/engine.git"
    },
    "scripts": {
        "build": "npm run build-debug && npm run build-min",
        "build-debug": "browserify index.js -d --standalone famous > dist/famous.js",
        "build-min": "browserify index.js --standalone famous | uglifyjs --screw-ie8 -m -c dead_code,sequences,conditionals,booleans,unused,if_return,join_vars,drop_debugger > dist/famous.min.js",
        "check-jsdoc": "eslint --reset --no-eslintrc --rule 'valid-jsdoc: 2' --ignore-path .gitignore .",
        "lint": "eslint --ignore-path .gitignore .",
        "tape": "tap-closer | smokestack -b firefox | tap-spec",
        "test": "EXIT_STATUS=0; npm run test-components || EXIT_STATUS=$?; npm run test-core || EXIT_STATUS=$?; npm run test-dom-renderables || EXIT_STATUS=$?; npm run test-dom-renderers || EXIT_STATUS=$?; npm run test-render-loops || EXIT_STATUS=$?; npm run test-math || EXIT_STATUS=$?; npm run test-physics || EXIT_STATUS=$?; npm run test-polyfills || EXIT_STATUS=$?; npm run test-renderers || EXIT_STATUS=$?; npm run test-transitions || EXIT_STATUS=$?; npm run test-utilities || EXIT_STATUS=$?; npm run test-webgl-geometries || EXIT_STATUS=$?; npm run test-webgl-materials || EXIT_STATUS=$?; npm run test-webgl-renderables || EXIT_STATUS=$?; npm run test-webgl-renderers; exit $EXIT_STATUS",
        "test-components": "browserify components/test/*.js | npm run tape",
        "test-core": "npm run test-new",
        "test-dom-renderables": "browserify dom-renderables/test/*.js | npm run tape",
        "test-dom-renderers": "browserify dom-renderers/test/*.js | npm run tape",
        "test-math": "browserify math/test/*.js | npm run tape",
        "test-new": "node ./scripts/test.js ./core/**/*.spec.js",
        "test-physics": "browserify physics/test/*.js physics/test/*/*.js | npm run tape",
        "test-polyfills": "browserify polyfills/test/*.js | npm run tape",
        "test-render-loops": "browserify render-loops/test/*.js | npm run tape",
        "test-renderers": "browserify renderers/test/*.js | npm run tape",
        "test-transitions": "browserify transitions/test/*.js | npm run tape",
        "test-utilities": "browserify utilities/test/*.js | npm run tape",
        "test-webgl-geometries": "browserify webgl-geometries/test/*.js | npm run tape",
        "test-webgl-materials": "browserify webgl-materials/test/*.js | npm run tape",
        "test-webgl-renderables": "browserify webgl-renderables/test/*.js | npm run tape",
        "test-webgl-renderers": "browserify webgl-renderers/test/*.js | npm run tape"
    },
    "version": "0.7.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module famous](#apidoc.module.famous)
1.  [function <span class="apidocSignatureSpan">famous.</span>Align (node)](#apidoc.element.famous.Align)
1.  [function <span class="apidocSignatureSpan">famous.</span>Buffer (target, type, gl)](#apidoc.element.famous.Buffer)
1.  [function <span class="apidocSignatureSpan">famous.</span>BufferRegistry (context)](#apidoc.element.famous.BufferRegistry)
1.  [function <span class="apidocSignatureSpan">famous.</span>CallbackStore ()](#apidoc.element.famous.CallbackStore)
1.  [function <span class="apidocSignatureSpan">famous.</span>Camera (node)](#apidoc.element.famous.Camera)
1.  [function <span class="apidocSignatureSpan">famous.</span>Channel ()](#apidoc.element.famous.Channel)
1.  [function <span class="apidocSignatureSpan">famous.</span>Clock ()](#apidoc.element.famous.Clock)
1.  [function <span class="apidocSignatureSpan">famous.</span>Color (color, transition, cb)](#apidoc.element.famous.Color)
1.  [function <span class="apidocSignatureSpan">famous.</span>Compositor ()](#apidoc.element.famous.Compositor)
1.  [function <span class="apidocSignatureSpan">famous.</span>Context (selector, compositor)](#apidoc.element.famous.Context)
1.  [function <span class="apidocSignatureSpan">famous.</span>DOMElement (node, options)](#apidoc.element.famous.DOMElement)
1.  [function <span class="apidocSignatureSpan">famous.</span>DOMRenderer (element, selector, compositor)](#apidoc.element.famous.DOMRenderer)
1.  [function <span class="apidocSignatureSpan">famous.</span>DynamicGeometry (options)](#apidoc.element.famous.DynamicGeometry)
1.  [function <span class="apidocSignatureSpan">famous.</span>GestureHandler (node, events)](#apidoc.element.famous.GestureHandler)
1.  [function <span class="apidocSignatureSpan">famous.</span>Mat33 (values)](#apidoc.element.famous.Mat33)
1.  [function <span class="apidocSignatureSpan">famous.</span>Mesh (node, options)](#apidoc.element.famous.Mesh)
1.  [function <span class="apidocSignatureSpan">famous.</span>MountPoint (node)](#apidoc.element.famous.MountPoint)
1.  [function <span class="apidocSignatureSpan">famous.</span>Node ()](#apidoc.element.famous.Node)
1.  [function <span class="apidocSignatureSpan">famous.</span>Opacity (node)](#apidoc.element.famous.Opacity)
1.  [function <span class="apidocSignatureSpan">famous.</span>Origin (node)](#apidoc.element.famous.Origin)
1.  [function <span class="apidocSignatureSpan">famous.</span>PathStore ()](#apidoc.element.famous.PathStore)
1.  [function <span class="apidocSignatureSpan">famous.</span>PhysicsEngine (options)](#apidoc.element.famous.PhysicsEngine)
1.  [function <span class="apidocSignatureSpan">famous.</span>Position (node)](#apidoc.element.famous.Position)
1.  [function <span class="apidocSignatureSpan">famous.</span>Program (gl, options)](#apidoc.element.famous.Program)
1.  [function <span class="apidocSignatureSpan">famous.</span>Quaternion (w, x, y, z)](#apidoc.element.famous.Quaternion)
1.  [function <span class="apidocSignatureSpan">famous.</span>Registry ()](#apidoc.element.famous.Registry)
1.  [function <span class="apidocSignatureSpan">famous.</span>RequestAnimationFrameLoop ()](#apidoc.element.famous.RequestAnimationFrameLoop)
1.  [function <span class="apidocSignatureSpan">famous.</span>Rotation (node)](#apidoc.element.famous.Rotation)
1.  [function <span class="apidocSignatureSpan">famous.</span>Scale (node)](#apidoc.element.famous.Scale)
1.  [function <span class="apidocSignatureSpan">famous.</span>Scene (selector, updater)](#apidoc.element.famous.Scene)
1.  [function <span class="apidocSignatureSpan">famous.</span>Size (node)](#apidoc.element.famous.Size)
1.  [function <span class="apidocSignatureSpan">famous.</span>Texture (gl, options)](#apidoc.element.famous.Texture)
1.  [function <span class="apidocSignatureSpan">famous.</span>TextureManager (gl)](#apidoc.element.famous.TextureManager)
1.  [function <span class="apidocSignatureSpan">famous.</span>Transform (node)](#apidoc.element.famous.Transform)
1.  [function <span class="apidocSignatureSpan">famous.</span>Transitionable (initialState)](#apidoc.element.famous.Transitionable)
1.  [function <span class="apidocSignatureSpan">famous.</span>UIManager (thread, compositor, renderLoop)](#apidoc.element.famous.UIManager)
1.  [function <span class="apidocSignatureSpan">famous.</span>Vec2 (x, y)](#apidoc.element.famous.Vec2)
1.  [function <span class="apidocSignatureSpan">famous.</span>Vec3 (x , y, z)](#apidoc.element.famous.Vec3)
1.  [function <span class="apidocSignatureSpan">famous.</span>WebGLRenderer (canvas, compositor)](#apidoc.element.famous.WebGLRenderer)
1.  object <span class="apidocSignatureSpan">famous.</span>Align.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Buffer.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>BufferRegistry.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>CallbackStore.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Camera.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Channel.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Clock.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Color.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Commands
1.  object <span class="apidocSignatureSpan">famous.</span>Compositor.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Context.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Curves
1.  object <span class="apidocSignatureSpan">famous.</span>DOMElement.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>DOMRenderer.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>DynamicGeometry.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Geometry
1.  object <span class="apidocSignatureSpan">famous.</span>GeometryHelper
1.  object <span class="apidocSignatureSpan">famous.</span>GestureHandler.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Mat33.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Material
1.  object <span class="apidocSignatureSpan">famous.</span>Math
1.  object <span class="apidocSignatureSpan">famous.</span>Mesh.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>MountPoint.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Node.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>OBJLoader
1.  object <span class="apidocSignatureSpan">famous.</span>ObjectManager
1.  object <span class="apidocSignatureSpan">famous.</span>Opacity.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Origin.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Path
1.  object <span class="apidocSignatureSpan">famous.</span>PathStore.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>PhysicsEngine.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Position.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Program.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Quaternion.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Registry.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>RequestAnimationFrameLoop.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Rotation.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Scale.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Scene.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Size.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Texture.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>TextureManager.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>TextureRegistry
1.  object <span class="apidocSignatureSpan">famous.</span>Transform.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Transitionable.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>UIManager.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Vec2.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>Vec3.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>WebGLRenderer.prototype
1.  object <span class="apidocSignatureSpan">famous.</span>animationFrame

#### [module famous.Align](#apidoc.module.famous.Align)
1.  [function <span class="apidocSignatureSpan">famous.</span>Align (node)](#apidoc.element.famous.Align.Align)

#### [module famous.Align.prototype](#apidoc.module.famous.Align.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Align.prototype.</span>constructor (node)](#apidoc.element.famous.Align.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">famous.Align.prototype.</span>onUpdate ()](#apidoc.element.famous.Align.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Align.prototype.</span>update ()](#apidoc.element.famous.Align.prototype.update)

#### [module famous.Buffer](#apidoc.module.famous.Buffer)
1.  [function <span class="apidocSignatureSpan">famous.</span>Buffer (target, type, gl)](#apidoc.element.famous.Buffer.Buffer)

#### [module famous.Buffer.prototype](#apidoc.module.famous.Buffer.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Buffer.prototype.</span>subData ()](#apidoc.element.famous.Buffer.prototype.subData)

#### [module famous.BufferRegistry](#apidoc.module.famous.BufferRegistry)
1.  [function <span class="apidocSignatureSpan">famous.</span>BufferRegistry (context)](#apidoc.element.famous.BufferRegistry.BufferRegistry)

#### [module famous.BufferRegistry.prototype](#apidoc.module.famous.BufferRegistry.prototype)
1.  [function <span class="apidocSignatureSpan">famous.BufferRegistry.prototype.</span>allocate (geometryId, name, value, spacing, dynamic)](#apidoc.element.famous.BufferRegistry.prototype.allocate)

#### [module famous.CallbackStore](#apidoc.module.famous.CallbackStore)
1.  [function <span class="apidocSignatureSpan">famous.</span>CallbackStore ()](#apidoc.element.famous.CallbackStore.CallbackStore)

#### [module famous.CallbackStore.prototype](#apidoc.module.famous.CallbackStore.prototype)
1.  [function <span class="apidocSignatureSpan">famous.CallbackStore.prototype.</span>off (key, callback)](#apidoc.element.famous.CallbackStore.prototype.off)
1.  [function <span class="apidocSignatureSpan">famous.CallbackStore.prototype.</span>on (key, callback)](#apidoc.element.famous.CallbackStore.prototype.on)
1.  [function <span class="apidocSignatureSpan">famous.CallbackStore.prototype.</span>trigger (key, payload)](#apidoc.element.famous.CallbackStore.prototype.trigger)

#### [module famous.Camera](#apidoc.module.famous.Camera)
1.  [function <span class="apidocSignatureSpan">famous.</span>Camera (node)](#apidoc.element.famous.Camera.Camera)
1.  number <span class="apidocSignatureSpan">famous.Camera.</span>FRUSTUM_PROJECTION
1.  number <span class="apidocSignatureSpan">famous.Camera.</span>ORTHOGRAPHIC_PROJECTION
1.  number <span class="apidocSignatureSpan">famous.Camera.</span>PINHOLE_PROJECTION

#### [module famous.Camera.prototype](#apidoc.module.famous.Camera.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>getValue ()](#apidoc.element.famous.Camera.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>onTransformChange (transform)](#apidoc.element.famous.Camera.prototype.onTransformChange)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>onUpdate ()](#apidoc.element.famous.Camera.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>set (type, depth, near, far)](#apidoc.element.famous.Camera.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setDepth (depth)](#apidoc.element.famous.Camera.prototype.setDepth)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setFlat ()](#apidoc.element.famous.Camera.prototype.setFlat)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setFrustum (near, far)](#apidoc.element.famous.Camera.prototype.setFrustum)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setValue (state)](#apidoc.element.famous.Camera.prototype.setValue)
1.  [function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>toString ()](#apidoc.element.famous.Camera.prototype.toString)

#### [module famous.Channel](#apidoc.module.famous.Channel)
1.  [function <span class="apidocSignatureSpan">famous.</span>Channel ()](#apidoc.element.famous.Channel.Channel)

#### [module famous.Channel.prototype](#apidoc.module.famous.Channel.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Channel.prototype.</span>_enterWorkerMode ()](#apidoc.element.famous.Channel.prototype._enterWorkerMode)
1.  [function <span class="apidocSignatureSpan">famous.Channel.prototype.</span>postMessage (message)](#apidoc.element.famous.Channel.prototype.postMessage)
1.  [function <span class="apidocSignatureSpan">famous.Channel.prototype.</span>sendMessage (message)](#apidoc.element.famous.Channel.prototype.sendMessage)
1.  object <span class="apidocSignatureSpan">famous.Channel.prototype.</span>onMessage
1.  object <span class="apidocSignatureSpan">famous.Channel.prototype.</span>onmessage

#### [module famous.Clock](#apidoc.module.famous.Clock)
1.  [function <span class="apidocSignatureSpan">famous.</span>Clock ()](#apidoc.element.famous.Clock.Clock)

#### [module famous.Clock.prototype](#apidoc.module.famous.Clock.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>clearTimer (timer)](#apidoc.element.famous.Clock.prototype.clearTimer)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>getFrame ()](#apidoc.element.famous.Clock.prototype.getFrame)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>getScale ()](#apidoc.element.famous.Clock.prototype.getScale)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>getTime ()](#apidoc.element.famous.Clock.prototype.getTime)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>now ()](#apidoc.element.famous.Clock.prototype.now)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>setInterval (callback, delay)](#apidoc.element.famous.Clock.prototype.setInterval)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>setScale (scale)](#apidoc.element.famous.Clock.prototype.setScale)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>setTimeout (callback, delay)](#apidoc.element.famous.Clock.prototype.setTimeout)
1.  [function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>step (time)](#apidoc.element.famous.Clock.prototype.step)

#### [module famous.Color](#apidoc.module.famous.Color)
1.  [function <span class="apidocSignatureSpan">famous.</span>Color (color, transition, cb)](#apidoc.element.famous.Color.Color)
1.  [function <span class="apidocSignatureSpan">famous.Color.</span>determineType (type)](#apidoc.element.famous.Color.determineType)
1.  [function <span class="apidocSignatureSpan">famous.Color.</span>isColorInstance (val)](#apidoc.element.famous.Color.isColorInstance)
1.  [function <span class="apidocSignatureSpan">famous.Color.</span>isHex (val)](#apidoc.element.famous.Color.isHex)
1.  [function <span class="apidocSignatureSpan">famous.Color.</span>isString (val)](#apidoc.element.famous.Color.isString)
1.  [function <span class="apidocSignatureSpan">famous.Color.</span>toHex (num)](#apidoc.element.famous.Color.toHex)

#### [module famous.Color.prototype](#apidoc.module.famous.Color.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>changeTo (color, transition, cb)](#apidoc.element.famous.Color.prototype.changeTo)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getB ()](#apidoc.element.famous.Color.prototype.getB)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getColor (option)](#apidoc.element.famous.Color.prototype.getColor)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getG ()](#apidoc.element.famous.Color.prototype.getG)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getHex ()](#apidoc.element.famous.Color.prototype.getHex)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getNormalizedRGB ()](#apidoc.element.famous.Color.prototype.getNormalizedRGB)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getNormalizedRGBA ()](#apidoc.element.famous.Color.prototype.getNormalizedRGBA)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getOpacity ()](#apidoc.element.famous.Color.prototype.getOpacity)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getR ()](#apidoc.element.famous.Color.prototype.getR)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getRGB ()](#apidoc.element.famous.Color.prototype.getRGB)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>halt ()](#apidoc.element.famous.Color.prototype.halt)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>isActive ()](#apidoc.element.famous.Color.prototype.isActive)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>set (color, transition, cb)](#apidoc.element.famous.Color.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setB (b, transition, cb)](#apidoc.element.famous.Color.prototype.setB)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setColor (name, transition, cb)](#apidoc.element.famous.Color.prototype.setColor)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setG (g, transition, cb)](#apidoc.element.famous.Color.prototype.setG)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setHex (hex, transition, cb)](#apidoc.element.famous.Color.prototype.setHex)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setOpacity (opacity, transition, cb)](#apidoc.element.famous.Color.prototype.setOpacity)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setR (r, transition, cb)](#apidoc.element.famous.Color.prototype.setR)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setRGB (r, g, b, transition, cb)](#apidoc.element.famous.Color.prototype.setRGB)
1.  [function <span class="apidocSignatureSpan">famous.Color.prototype.</span>toString ()](#apidoc.element.famous.Color.prototype.toString)

#### [module famous.Commands](#apidoc.module.famous.Commands)
1.  [function <span class="apidocSignatureSpan">famous.Commands.</span>prettyPrint (buffer, start, count)](#apidoc.element.famous.Commands.prettyPrint)
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>ADD_CLASS
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>ALLOW_DEFAULT
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>CHANGE_ATTRIBUTE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>CHANGE_CONTENT
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>CHANGE_PROPERTY
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>CHANGE_SIZE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>CHANGE_TRANSFORM
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>CHANGE_VIEW_TRANSFORM
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>DOM
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>DOM_RENDER_SIZE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>ENGINE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>FRAME
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_AMBIENT_LIGHT
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_BUFFER_DATA
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_CUTOUT_STATE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_LIGHT_COLOR
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_LIGHT_POSITION
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_MESH_VISIBILITY
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_REMOVE_MESH
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_SET_DRAW_OPTIONS
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_SET_GEOMETRY
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>GL_UNIFORMS
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>INIT_DOM
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>MATERIAL_INPUT
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>NEED_SIZE_FOR
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>ORTHOGRAPHIC_PROJECTION
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>PINHOLE_PROJECTION
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>PREVENT_DEFAULT
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>READY
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>REMOVE_CLASS
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>START
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>STOP
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>SUBSCRIBE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>TIME
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>TRIGGER
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>UNSUBSCRIBE
1.  number <span class="apidocSignatureSpan">famous.Commands.</span>WITH

#### [module famous.Compositor](#apidoc.module.famous.Compositor)
1.  [function <span class="apidocSignatureSpan">famous.</span>Compositor ()](#apidoc.element.famous.Compositor.Compositor)

#### [module famous.Compositor.prototype](#apidoc.module.famous.Compositor.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>clearCommands ()](#apidoc.element.famous.Compositor.prototype.clearCommands)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>drawCommands ()](#apidoc.element.famous.Compositor.prototype.drawCommands)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>getContext (selector)](#apidoc.element.famous.Compositor.prototype.getContext)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>getOrSetContext (selector)](#apidoc.element.famous.Compositor.prototype.getOrSetContext)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>getTime ()](#apidoc.element.famous.Compositor.prototype.getTime)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>giveSizeFor (iterator, commands)](#apidoc.element.famous.Compositor.prototype.giveSizeFor)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>handleWith (iterator, commands)](#apidoc.element.famous.Compositor.prototype.handleWith)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>onResize ()](#apidoc.element.famous.Compositor.prototype.onResize)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>receiveCommands (commands)](#apidoc.element.famous.Compositor.prototype.receiveCommands)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>sendEvent (path, ev, payload)](#apidoc.element.famous.Compositor.prototype.sendEvent)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>sendResize (selector, size)](#apidoc.element.famous.Compositor.prototype.sendResize)
1.  [function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>updateSize ()](#apidoc.element.famous.Compositor.prototype.updateSize)

#### [module famous.Context](#apidoc.module.famous.Context)
1.  [function <span class="apidocSignatureSpan">famous.</span>Context (selector, compositor)](#apidoc.element.famous.Context.Context)

#### [module famous.Context.prototype](#apidoc.module.famous.Context.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>_initDOMRenderer ()](#apidoc.element.famous.Context.prototype._initDOMRenderer)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>_initWebGLRenderer ()](#apidoc.element.famous.Context.prototype._initWebGLRenderer)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>checkInit ()](#apidoc.element.famous.Context.prototype.checkInit)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>draw ()](#apidoc.element.famous.Context.prototype.draw)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>getDOMRenderer ()](#apidoc.element.famous.Context.prototype.getDOMRenderer)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>getRootSize ()](#apidoc.element.famous.Context.prototype.getRootSize)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>getWebGLRenderer ()](#apidoc.element.famous.Context.prototype.getWebGLRenderer)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>initCommandCallbacks ()](#apidoc.element.famous.Context.prototype.initCommandCallbacks)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>receive (path, commands, iterator)](#apidoc.element.famous.Context.prototype.receive)
1.  [function <span class="apidocSignatureSpan">famous.Context.prototype.</span>updateSize ()](#apidoc.element.famous.Context.prototype.updateSize)

#### [module famous.Curves](#apidoc.module.famous.Curves)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>easeIn (t)](#apidoc.element.famous.Curves.easeIn)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>easeInOut (t)](#apidoc.element.famous.Curves.easeInOut)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>easeOut (t)](#apidoc.element.famous.Curves.easeOut)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>easeOutBounce (t)](#apidoc.element.famous.Curves.easeOutBounce)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>flat ()](#apidoc.element.famous.Curves.flat)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inBack (t, s)](#apidoc.element.famous.Curves.inBack)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inBounce (t)](#apidoc.element.famous.Curves.inBounce)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inCirc (t)](#apidoc.element.famous.Curves.inCirc)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inCubic (t)](#apidoc.element.famous.Curves.inCubic)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inElastic (t)](#apidoc.element.famous.Curves.inElastic)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inExpo (t)](#apidoc.element.famous.Curves.inExpo)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutBack (t, s)](#apidoc.element.famous.Curves.inOutBack)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutBounce (t)](#apidoc.element.famous.Curves.inOutBounce)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutCirc (t)](#apidoc.element.famous.Curves.inOutCirc)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutCubic (t)](#apidoc.element.famous.Curves.inOutCubic)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutElastic (t)](#apidoc.element.famous.Curves.inOutElastic)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutExpo (t)](#apidoc.element.famous.Curves.inOutExpo)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutQuad (t)](#apidoc.element.famous.Curves.inOutQuad)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutQuart (t)](#apidoc.element.famous.Curves.inOutQuart)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutQuint (t)](#apidoc.element.famous.Curves.inOutQuint)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inOutSine (t)](#apidoc.element.famous.Curves.inOutSine)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inQuad (t)](#apidoc.element.famous.Curves.inQuad)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inQuart (t)](#apidoc.element.famous.Curves.inQuart)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inQuint (t)](#apidoc.element.famous.Curves.inQuint)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>inSine (t)](#apidoc.element.famous.Curves.inSine)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>linear (t)](#apidoc.element.famous.Curves.linear)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outBack (t, s)](#apidoc.element.famous.Curves.outBack)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outBounce (t)](#apidoc.element.famous.Curves.outBounce)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outCirc (t)](#apidoc.element.famous.Curves.outCirc)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outCubic (t)](#apidoc.element.famous.Curves.outCubic)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outElastic (t)](#apidoc.element.famous.Curves.outElastic)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outExpo (t)](#apidoc.element.famous.Curves.outExpo)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outQuad (t)](#apidoc.element.famous.Curves.outQuad)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outQuart (t)](#apidoc.element.famous.Curves.outQuart)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outQuint (t)](#apidoc.element.famous.Curves.outQuint)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>outSine (t)](#apidoc.element.famous.Curves.outSine)
1.  [function <span class="apidocSignatureSpan">famous.Curves.</span>spring (t)](#apidoc.element.famous.Curves.spring)

#### [module famous.DOMElement](#apidoc.module.famous.DOMElement)
1.  [function <span class="apidocSignatureSpan">famous.</span>DOMElement (node, options)](#apidoc.element.famous.DOMElement.DOMElement)

#### [module famous.DOMElement.prototype](#apidoc.module.famous.DOMElement.prototype)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>_requestUpdate ()](#apidoc.element.famous.DOMElement.prototype._requestUpdate)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>_subscribe (uiEvent)](#apidoc.element.famous.DOMElement.prototype._subscribe)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>_unsubscribe (UIEvent)](#apidoc.element.famous.DOMElement.prototype._unsubscribe)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>addClass (value)](#apidoc.element.famous.DOMElement.prototype.addClass)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>allowDefault (uiEvent)](#apidoc.element.famous.DOMElement.prototype.allowDefault)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>draw ()](#apidoc.element.famous.DOMElement.prototype.draw)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>getRenderSize ()](#apidoc.element.famous.DOMElement.prototype.getRenderSize)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>getValue ()](#apidoc.element.famous.DOMElement.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>hasClass (value)](#apidoc.element.famous.DOMElement.prototype.hasClass)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>init ()](#apidoc.element.famous.DOMElement.prototype.init)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>on (event, listener)](#apidoc.element.famous.DOMElement.prototype.on)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onAddUIEvent (uiEvent)](#apidoc.element.famous.DOMElement.prototype.onAddUIEvent)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onDismount ()](#apidoc.element.famous.DOMElement.prototype.onDismount)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onHide ()](#apidoc.element.famous.DOMElement.prototype.onHide)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onMount (node, id)](#apidoc.element.famous.DOMElement.prototype.onMount)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onOpacityChange (opacity)](#apidoc.element.famous.DOMElement.prototype.onOpacityChange)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onReceive (event, payload)](#apidoc.element.famous.DOMElement.prototype.onReceive)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onRemoveUIEvent (UIEvent)](#apidoc.element.famous.DOMElement.prototype.onRemoveUIEvent)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onShow ()](#apidoc.element.famous.DOMElement.prototype.onShow)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onSizeChange (x, y)](#apidoc.element.famous.DOMElement.prototype.onSizeChange)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onSizeModeChange (x, y, z)](#apidoc.element.famous.DOMElement.prototype.onSizeModeChange)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onTransformChange (transform)](#apidoc.element.famous.DOMElement.prototype.onTransformChange)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onUpdate ()](#apidoc.element.famous.DOMElement.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>preventDefault (uiEvent)](#apidoc.element.famous.DOMElement.prototype.preventDefault)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>removeClass (value)](#apidoc.element.famous.DOMElement.prototype.removeClass)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setAttribute (name, value)](#apidoc.element.famous.DOMElement.prototype.setAttribute)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setContent (content)](#apidoc.element.famous.DOMElement.prototype.setContent)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setCutoutState (usesCutout)](#apidoc.element.famous.DOMElement.prototype.setCutoutState)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setId (id)](#apidoc.element.famous.DOMElement.prototype.setId)
1.  [function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setProperty (name, value)](#apidoc.element.famous.DOMElement.prototype.setProperty)

#### [module famous.DOMRenderer](#apidoc.module.famous.DOMRenderer)
1.  [function <span class="apidocSignatureSpan">famous.</span>DOMRenderer (element, selector, compositor)](#apidoc.element.famous.DOMRenderer.DOMRenderer)

#### [module famous.DOMRenderer.prototype](#apidoc.module.famous.DOMRenderer.prototype)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertChildrenLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertChildrenLoaded)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertParentLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertParentLoaded)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertPathLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertPathLoaded)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertTargetLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertTargetLoaded)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_listen (type)](#apidoc.element.famous.DOMRenderer.prototype._listen)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_stringifyMatrix (m)](#apidoc.element.famous.DOMRenderer.prototype._stringifyMatrix)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_triggerEvent (ev)](#apidoc.element.famous.DOMRenderer.prototype._triggerEvent)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>addClass (domClass)](#apidoc.element.famous.DOMRenderer.prototype.addClass)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>allowDefault (type)](#apidoc.element.famous.DOMRenderer.prototype.allowDefault)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>draw (renderState)](#apidoc.element.famous.DOMRenderer.prototype.draw)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>findParent ()](#apidoc.element.famous.DOMRenderer.prototype.findParent)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>findTarget ()](#apidoc.element.famous.DOMRenderer.prototype.findTarget)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>getSizeOf (path)](#apidoc.element.famous.DOMRenderer.prototype.getSizeOf)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>insertEl (tagName)](#apidoc.element.famous.DOMRenderer.prototype.insertEl)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>loadPath (path)](#apidoc.element.famous.DOMRenderer.prototype.loadPath)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>offInsertEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.offInsertEl)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>offRemoveEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.offRemoveEl)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>onInsertEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.onInsertEl)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>onRemoveEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.onRemoveEl)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>preventDefault (type)](#apidoc.element.famous.DOMRenderer.prototype.preventDefault)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>removeClass (domClass)](#apidoc.element.famous.DOMRenderer.prototype.removeClass)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>resolveChildren (element, parent)](#apidoc.element.famous.DOMRenderer.prototype.resolveChildren)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setAttribute (name, value)](#apidoc.element.famous.DOMRenderer.prototype.setAttribute)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setContent (content)](#apidoc.element.famous.DOMRenderer.prototype.setContent)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setHeight (height)](#apidoc.element.famous.DOMRenderer.prototype.setHeight)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setMatrix (transform)](#apidoc.element.famous.DOMRenderer.prototype.setMatrix)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setProperty (name, value)](#apidoc.element.famous.DOMRenderer.prototype.setProperty)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setSize (width, height)](#apidoc.element.famous.DOMRenderer.prototype.setSize)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setWidth (width)](#apidoc.element.famous.DOMRenderer.prototype.setWidth)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>subscribe (type)](#apidoc.element.famous.DOMRenderer.prototype.subscribe)
1.  [function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>unsubscribe (type)](#apidoc.element.famous.DOMRenderer.prototype.unsubscribe)

#### [module famous.DynamicGeometry](#apidoc.module.famous.DynamicGeometry)
1.  [function <span class="apidocSignatureSpan">famous.</span>DynamicGeometry (options)](#apidoc.element.famous.DynamicGeometry.DynamicGeometry)

#### [module famous.DynamicGeometry.prototype](#apidoc.module.famous.DynamicGeometry.prototype)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>fromGeometry (geometry)](#apidoc.element.famous.DynamicGeometry.prototype.fromGeometry)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getLength ()](#apidoc.element.famous.DynamicGeometry.prototype.getLength)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getNormals ()](#apidoc.element.famous.DynamicGeometry.prototype.getNormals)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getTextureCoords ()](#apidoc.element.famous.DynamicGeometry.prototype.getTextureCoords)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getVertexBuffer (bufferName)](#apidoc.element.famous.DynamicGeometry.prototype.getVertexBuffer)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getVertexPositions ()](#apidoc.element.famous.DynamicGeometry.prototype.getVertexPositions)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setDrawType (value)](#apidoc.element.famous.DynamicGeometry.prototype.setDrawType)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setIndices (value)](#apidoc.element.famous.DynamicGeometry.prototype.setIndices)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setNormals (value)](#apidoc.element.famous.DynamicGeometry.prototype.setNormals)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setTextureCoords (value)](#apidoc.element.famous.DynamicGeometry.prototype.setTextureCoords)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setVertexBuffer (bufferName, value, size)](#apidoc.element.famous.DynamicGeometry.prototype.setVertexBuffer)
1.  [function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setVertexPositions (value)](#apidoc.element.famous.DynamicGeometry.prototype.setVertexPositions)

#### [module famous.Geometry](#apidoc.module.famous.Geometry)
1.  [function <span class="apidocSignatureSpan">famous.Geometry.</span>ConvexHull (vertices, iterations)](#apidoc.element.famous.Geometry.ConvexHull)
1.  [function <span class="apidocSignatureSpan">famous.Geometry.</span>DynamicGeometry ()](#apidoc.element.famous.Geometry.DynamicGeometry)

#### [module famous.GeometryHelper](#apidoc.module.famous.GeometryHelper)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>addBackfaceTriangles (vertices, indices)](#apidoc.element.famous.GeometryHelper.addBackfaceTriangles)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>computeNormals (vertices, indices, out)](#apidoc.element.famous.GeometryHelper.computeNormals)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>generateParametric (detailX, detailY, func, wrap)](#apidoc.element.famous.GeometryHelper.generateParametric)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getAltitude (v)](#apidoc.element.famous.GeometryHelper.getAltitude)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getAzimuth (v)](#apidoc.element.famous.GeometryHelper.getAzimuth)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getSpheroidNormals (vertices, out)](#apidoc.element.famous.GeometryHelper.getSpheroidNormals)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getSpheroidUV (vertices, out)](#apidoc.element.famous.GeometryHelper.getSpheroidUV)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getUniqueFaces (vertices, indices)](#apidoc.element.famous.GeometryHelper.getUniqueFaces)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>normalizeAll (vertices, out)](#apidoc.element.famous.GeometryHelper.normalizeAll)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>normalizeVertices (vertices, out)](#apidoc.element.famous.GeometryHelper.normalizeVertices)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>subdivide (indices, vertices, textureCoords)](#apidoc.element.famous.GeometryHelper.subdivide)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>subdivideSpheroid (vertices, indices)](#apidoc.element.famous.GeometryHelper.subdivideSpheroid)
1.  [function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>trianglesToLines (indices, out)](#apidoc.element.famous.GeometryHelper.trianglesToLines)

#### [module famous.GestureHandler](#apidoc.module.famous.GestureHandler)
1.  [function <span class="apidocSignatureSpan">famous.</span>GestureHandler (node, events)](#apidoc.element.famous.GestureHandler.GestureHandler)

#### [module famous.GestureHandler.prototype](#apidoc.module.famous.GestureHandler.prototype)
1.  [function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>on (ev, cb)](#apidoc.element.famous.GestureHandler.prototype.on)
1.  [function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>onReceive (ev, payload)](#apidoc.element.famous.GestureHandler.prototype.onReceive)
1.  [function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>toString ()](#apidoc.element.famous.GestureHandler.prototype.toString)
1.  [function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>trigger (ev, payload)](#apidoc.element.famous.GestureHandler.prototype.trigger)
1.  [function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>triggerGestures ()](#apidoc.element.famous.GestureHandler.prototype.triggerGestures)

#### [module famous.Mat33](#apidoc.module.famous.Mat33)
1.  [function <span class="apidocSignatureSpan">famous.</span>Mat33 (values)](#apidoc.element.famous.Mat33.Mat33)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.</span>add (matrix1, matrix2, output)](#apidoc.element.famous.Mat33.add)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.</span>clone (m)](#apidoc.element.famous.Mat33.clone)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.</span>inverse (matrix, output)](#apidoc.element.famous.Mat33.inverse)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.</span>multiply (matrix1, matrix2, output)](#apidoc.element.famous.Mat33.multiply)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.</span>subtract (matrix1, matrix2, output)](#apidoc.element.famous.Mat33.subtract)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.</span>transpose (matrix, output)](#apidoc.element.famous.Mat33.transpose)

#### [module famous.Mat33.prototype](#apidoc.module.famous.Mat33.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>copy (matrix)](#apidoc.element.famous.Mat33.prototype.copy)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>get ()](#apidoc.element.famous.Mat33.prototype.get)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>getDeterminant ()](#apidoc.element.famous.Mat33.prototype.getDeterminant)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>inverse ()](#apidoc.element.famous.Mat33.prototype.inverse)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>multiply (matrix)](#apidoc.element.famous.Mat33.prototype.multiply)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>set (values)](#apidoc.element.famous.Mat33.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>transpose ()](#apidoc.element.famous.Mat33.prototype.transpose)
1.  [function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>vectorMultiply (v, output)](#apidoc.element.famous.Mat33.prototype.vectorMultiply)

#### [module famous.Material](#apidoc.module.famous.Material)
1.  [function <span class="apidocSignatureSpan">famous.</span>Material (name, chunk, inputs, options)](#apidoc.element.famous.Material.Material)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>Custom (schema, inputs, uniforms)](#apidoc.element.famous.Material.Custom)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>Texture (source)](#apidoc.element.famous.Material.Texture)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>abs (inputs, options)](#apidoc.element.famous.Material.abs)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>add (inputs, options)](#apidoc.element.famous.Material.add)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>ceiling (inputs, options)](#apidoc.element.famous.Material.ceiling)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>clamp (inputs, options)](#apidoc.element.famous.Material.clamp)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>constant (inputs, options)](#apidoc.element.famous.Material.constant)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>cos (inputs, options)](#apidoc.element.famous.Material.cos)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>dot (inputs, options)](#apidoc.element.famous.Material.dot)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>floor (inputs, options)](#apidoc.element.famous.Material.floor)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>fragCoord (inputs, options)](#apidoc.element.famous.Material.fragCoord)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>image (inputs, options)](#apidoc.element.famous.Material.image)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>max (inputs, options)](#apidoc.element.famous.Material.max)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>meshPosition (inputs, options)](#apidoc.element.famous.Material.meshPosition)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>min (inputs, options)](#apidoc.element.famous.Material.min)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>mix (inputs, options)](#apidoc.element.famous.Material.mix)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>mod (inputs, options)](#apidoc.element.famous.Material.mod)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>multiply (inputs, options)](#apidoc.element.famous.Material.multiply)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>normal (inputs, options)](#apidoc.element.famous.Material.normal)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>normalize (inputs, options)](#apidoc.element.famous.Material.normalize)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>parameter (inputs, options)](#apidoc.element.famous.Material.parameter)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>pow (inputs, options)](#apidoc.element.famous.Material.pow)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>registerExpression (name, schema)](#apidoc.element.famous.Material.registerExpression)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>sign (inputs, options)](#apidoc.element.famous.Material.sign)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>sin (inputs, options)](#apidoc.element.famous.Material.sin)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>smoothstep (inputs, options)](#apidoc.element.famous.Material.smoothstep)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>sqrt (inputs, options)](#apidoc.element.famous.Material.sqrt)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>step (inputs, options)](#apidoc.element.famous.Material.step)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>subtract (inputs, options)](#apidoc.element.famous.Material.subtract)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>time (inputs, options)](#apidoc.element.famous.Material.time)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>uv (inputs, options)](#apidoc.element.famous.Material.uv)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>vec2 (inputs, options)](#apidoc.element.famous.Material.vec2)
1.  [function <span class="apidocSignatureSpan">famous.Material.</span>vec3 (inputs, options)](#apidoc.element.famous.Material.vec3)

#### [module famous.Math](#apidoc.module.famous.Math)
1.  [function <span class="apidocSignatureSpan">famous.Math.</span>invert (out, a)](#apidoc.element.famous.Math.invert)
1.  [function <span class="apidocSignatureSpan">famous.Math.</span>multiply (out, a, b)](#apidoc.element.famous.Math.multiply)

#### [module famous.Mesh](#apidoc.module.famous.Mesh)
1.  [function <span class="apidocSignatureSpan">famous.</span>Mesh (node, options)](#apidoc.element.famous.Mesh.Mesh)

#### [module famous.Mesh.prototype](#apidoc.module.famous.Mesh.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>_pushInvalidations (expressionName)](#apidoc.element.famous.Mesh.prototype._pushInvalidations)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>_requestUpdate ()](#apidoc.element.famous.Mesh.prototype._requestUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>draw ()](#apidoc.element.famous.Mesh.prototype.draw)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getBaseColor ()](#apidoc.element.famous.Mesh.prototype.getBaseColor)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getDrawOptions ()](#apidoc.element.famous.Mesh.prototype.getDrawOptions)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getFlatShading ()](#apidoc.element.famous.Mesh.prototype.getFlatShading)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getGeometry ()](#apidoc.element.famous.Mesh.prototype.getGeometry)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getGlossiness ()](#apidoc.element.famous.Mesh.prototype.getGlossiness)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getMaterialExpressions ()](#apidoc.element.famous.Mesh.prototype.getMaterialExpressions)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getNormals (materialExpression)](#apidoc.element.famous.Mesh.prototype.getNormals)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getPositionOffset ()](#apidoc.element.famous.Mesh.prototype.getPositionOffset)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getValue ()](#apidoc.element.famous.Mesh.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>init ()](#apidoc.element.famous.Mesh.prototype.init)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onAddUIEvent (UIEvent)](#apidoc.element.famous.Mesh.prototype.onAddUIEvent)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onDismount ()](#apidoc.element.famous.Mesh.prototype.onDismount)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onHide ()](#apidoc.element.famous.Mesh.prototype.onHide)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onMount (node, id)](#apidoc.element.famous.Mesh.prototype.onMount)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onOpacityChange (opacity)](#apidoc.element.famous.Mesh.prototype.onOpacityChange)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onShow ()](#apidoc.element.famous.Mesh.prototype.onShow)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onSizeChange (x, y, z)](#apidoc.element.famous.Mesh.prototype.onSizeChange)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onTransformChange (transform)](#apidoc.element.famous.Mesh.prototype.onTransformChange)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onUpdate ()](#apidoc.element.famous.Mesh.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setBaseColor (color)](#apidoc.element.famous.Mesh.prototype.setBaseColor)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setDrawOptions (options)](#apidoc.element.famous.Mesh.prototype.setDrawOptions)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setFlatShading (bool)](#apidoc.element.famous.Mesh.prototype.setFlatShading)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setGeometry (geometry, options)](#apidoc.element.famous.Mesh.prototype.setGeometry)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setGlossiness (glossiness, strength)](#apidoc.element.famous.Mesh.prototype.setGlossiness)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setNormals (materialExpression)](#apidoc.element.famous.Mesh.prototype.setNormals)
1.  [function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setPositionOffset (materialExpression)](#apidoc.element.famous.Mesh.prototype.setPositionOffset)

#### [module famous.MountPoint](#apidoc.module.famous.MountPoint)
1.  [function <span class="apidocSignatureSpan">famous.</span>MountPoint (node)](#apidoc.element.famous.MountPoint.MountPoint)

#### [module famous.MountPoint.prototype](#apidoc.module.famous.MountPoint.prototype)
1.  [function <span class="apidocSignatureSpan">famous.MountPoint.prototype.</span>constructor (node)](#apidoc.element.famous.MountPoint.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">famous.MountPoint.prototype.</span>onUpdate ()](#apidoc.element.famous.MountPoint.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.MountPoint.prototype.</span>update ()](#apidoc.element.famous.MountPoint.prototype.update)

#### [module famous.Node](#apidoc.module.famous.Node)
1.  boolean <span class="apidocSignatureSpan">famous.Node.</span>NO_DEFAULT_COMPONENTS
1.  [function <span class="apidocSignatureSpan">famous.</span>Node ()](#apidoc.element.famous.Node.Node)
1.  number <span class="apidocSignatureSpan">famous.Node.</span>ABSOLUTE_SIZE
1.  number <span class="apidocSignatureSpan">famous.Node.</span>DEFAULT_SIZE
1.  number <span class="apidocSignatureSpan">famous.Node.</span>RELATIVE_SIZE
1.  number <span class="apidocSignatureSpan">famous.Node.</span>RENDER_SIZE

#### [module famous.Node.prototype](#apidoc.module.famous.Node.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_init ()](#apidoc.element.famous.Node.prototype._init)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_requestUpdate (force)](#apidoc.element.famous.Node.prototype._requestUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setMounted (mounted, path)](#apidoc.element.famous.Node.prototype._setMounted)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setParent (parent)](#apidoc.element.famous.Node.prototype._setParent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setShown (shown)](#apidoc.element.famous.Node.prototype._setShown)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setUpdater (updater)](#apidoc.element.famous.Node.prototype._setUpdater)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_vecOptionalSet (vec, index, val)](#apidoc.element.famous.Node.prototype._vecOptionalSet)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>addChild (child)](#apidoc.element.famous.Node.prototype.addChild)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>addComponent (component)](#apidoc.element.famous.Node.prototype.addComponent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>addUIEvent (eventName)](#apidoc.element.famous.Node.prototype.addUIEvent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>dismount ()](#apidoc.element.famous.Node.prototype.dismount)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>emit (event, payload)](#apidoc.element.famous.Node.prototype.emit)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getAbsoluteSize ()](#apidoc.element.famous.Node.prototype.getAbsoluteSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getAlign ()](#apidoc.element.famous.Node.prototype.getAlign)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getChildren ()](#apidoc.element.famous.Node.prototype.getChildren)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getComponent (index)](#apidoc.element.famous.Node.prototype.getComponent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getComponents ()](#apidoc.element.famous.Node.prototype.getComponents)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getComputedValue ()](#apidoc.element.famous.Node.prototype.getComputedValue)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getDifferentialSize ()](#apidoc.element.famous.Node.prototype.getDifferentialSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getFrame ()](#apidoc.element.famous.Node.prototype.getFrame)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getId ()](#apidoc.element.famous.Node.prototype.getId)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getLocation ()](#apidoc.element.famous.Node.prototype.getLocation)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getMountPoint ()](#apidoc.element.famous.Node.prototype.getMountPoint)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getOpacity ()](#apidoc.element.famous.Node.prototype.getOpacity)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getOrigin ()](#apidoc.element.famous.Node.prototype.getOrigin)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getParent ()](#apidoc.element.famous.Node.prototype.getParent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getPosition ()](#apidoc.element.famous.Node.prototype.getPosition)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getProportionalSize ()](#apidoc.element.famous.Node.prototype.getProportionalSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getRawChildren ()](#apidoc.element.famous.Node.prototype.getRawChildren)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getRenderSize ()](#apidoc.element.famous.Node.prototype.getRenderSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getRotation ()](#apidoc.element.famous.Node.prototype.getRotation)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getScale ()](#apidoc.element.famous.Node.prototype.getScale)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getSize ()](#apidoc.element.famous.Node.prototype.getSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getSizeMode ()](#apidoc.element.famous.Node.prototype.getSizeMode)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getTransform ()](#apidoc.element.famous.Node.prototype.getTransform)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getUIEvents ()](#apidoc.element.famous.Node.prototype.getUIEvents)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getValue ()](#apidoc.element.famous.Node.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>hide ()](#apidoc.element.famous.Node.prototype.hide)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>isMounted ()](#apidoc.element.famous.Node.prototype.isMounted)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>isRendered ()](#apidoc.element.famous.Node.prototype.isRendered)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>isShown ()](#apidoc.element.famous.Node.prototype.isShown)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>mount (path)](#apidoc.element.famous.Node.prototype.mount)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>removeChild (child)](#apidoc.element.famous.Node.prototype.removeChild)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>removeComponent (component)](#apidoc.element.famous.Node.prototype.removeComponent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>removeUIEvent (eventName)](#apidoc.element.famous.Node.prototype.removeUIEvent)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>requestUpdate (requester)](#apidoc.element.famous.Node.prototype.requestUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>requestUpdateOnNextTick (requester)](#apidoc.element.famous.Node.prototype.requestUpdateOnNextTick)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>sendDrawCommand (message)](#apidoc.element.famous.Node.prototype.sendDrawCommand)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setAbsoluteSize (x, y, z)](#apidoc.element.famous.Node.prototype.setAbsoluteSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setAlign (x, y, z)](#apidoc.element.famous.Node.prototype.setAlign)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setDifferentialSize (x, y, z)](#apidoc.element.famous.Node.prototype.setDifferentialSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setMountPoint (x, y, z)](#apidoc.element.famous.Node.prototype.setMountPoint)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setOpacity (val)](#apidoc.element.famous.Node.prototype.setOpacity)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setOrigin (x, y, z)](#apidoc.element.famous.Node.prototype.setOrigin)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setPosition (x, y, z)](#apidoc.element.famous.Node.prototype.setPosition)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setProportionalSize (x, y, z)](#apidoc.element.famous.Node.prototype.setProportionalSize)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setRotation (x, y, z, w)](#apidoc.element.famous.Node.prototype.setRotation)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setScale (x, y, z)](#apidoc.element.famous.Node.prototype.setScale)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setSizeMode (x, y, z)](#apidoc.element.famous.Node.prototype.setSizeMode)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>show ()](#apidoc.element.famous.Node.prototype.show)
1.  [function <span class="apidocSignatureSpan">famous.Node.prototype.</span>update (time)](#apidoc.element.famous.Node.prototype.update)

#### [module famous.OBJLoader](#apidoc.module.famous.OBJLoader)
1.  [function <span class="apidocSignatureSpan">famous.OBJLoader.</span>_onsuccess (url, options, text)](#apidoc.element.famous.OBJLoader._onsuccess)
1.  [function <span class="apidocSignatureSpan">famous.OBJLoader.</span>formatText (text, options)](#apidoc.element.famous.OBJLoader.formatText)
1.  [function <span class="apidocSignatureSpan">famous.OBJLoader.</span>load (url, cb, options)](#apidoc.element.famous.OBJLoader.load)
1.  object <span class="apidocSignatureSpan">famous.OBJLoader.</span>cached
1.  object <span class="apidocSignatureSpan">famous.OBJLoader.</span>requests

#### [module famous.ObjectManager](#apidoc.module.famous.ObjectManager)
1.  [function <span class="apidocSignatureSpan">famous.ObjectManager.</span>disposeOf (type)](#apidoc.element.famous.ObjectManager.disposeOf)
1.  [function <span class="apidocSignatureSpan">famous.ObjectManager.</span>freeDynamicGeometry (obj)](#apidoc.element.famous.ObjectManager.freeDynamicGeometry)
1.  [function <span class="apidocSignatureSpan">famous.ObjectManager.</span>freeDynamicGeometryFeature (obj)](#apidoc.element.famous.ObjectManager.freeDynamicGeometryFeature)
1.  [function <span class="apidocSignatureSpan">famous.ObjectManager.</span>register (type, Constructor)](#apidoc.element.famous.ObjectManager.register)
1.  [function <span class="apidocSignatureSpan">famous.ObjectManager.</span>requestDynamicGeometry ()](#apidoc.element.famous.ObjectManager.requestDynamicGeometry)
1.  [function <span class="apidocSignatureSpan">famous.ObjectManager.</span>requestDynamicGeometryFeature ()](#apidoc.element.famous.ObjectManager.requestDynamicGeometryFeature)
1.  object <span class="apidocSignatureSpan">famous.ObjectManager.</span>pools

#### [module famous.Opacity](#apidoc.module.famous.Opacity)
1.  [function <span class="apidocSignatureSpan">famous.</span>Opacity (node)](#apidoc.element.famous.Opacity.Opacity)

#### [module famous.Opacity.prototype](#apidoc.module.famous.Opacity.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>get ()](#apidoc.element.famous.Opacity.prototype.get)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>getValue ()](#apidoc.element.famous.Opacity.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>halt ()](#apidoc.element.famous.Opacity.prototype.halt)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>isActive ()](#apidoc.element.famous.Opacity.prototype.isActive)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>onUpdate ()](#apidoc.element.famous.Opacity.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>set (value, transition, callback)](#apidoc.element.famous.Opacity.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>setValue (value)](#apidoc.element.famous.Opacity.prototype.setValue)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>toString ()](#apidoc.element.famous.Opacity.prototype.toString)
1.  [function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>update ()](#apidoc.element.famous.Opacity.prototype.update)

#### [module famous.Origin](#apidoc.module.famous.Origin)
1.  [function <span class="apidocSignatureSpan">famous.</span>Origin (node)](#apidoc.element.famous.Origin.Origin)

#### [module famous.Origin.prototype](#apidoc.module.famous.Origin.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Origin.prototype.</span>constructor (node)](#apidoc.element.famous.Origin.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">famous.Origin.prototype.</span>onUpdate ()](#apidoc.element.famous.Origin.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Origin.prototype.</span>update ()](#apidoc.element.famous.Origin.prototype.update)

#### [module famous.Path](#apidoc.module.famous.Path)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>depth (path)](#apidoc.element.famous.Path.depth)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>getSelector (path)](#apidoc.element.famous.Path.getSelector)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>hasTrailingSlash (path)](#apidoc.element.famous.Path.hasTrailingSlash)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>index (path)](#apidoc.element.famous.Path.index)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>indexAtDepth (path, depth)](#apidoc.element.famous.Path.indexAtDepth)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>isChildOf (child, parent)](#apidoc.element.famous.Path.isChildOf)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>isDescendentOf (child, parent)](#apidoc.element.famous.Path.isDescendentOf)
1.  [function <span class="apidocSignatureSpan">famous.Path.</span>parent (path)](#apidoc.element.famous.Path.parent)

#### [module famous.PathStore](#apidoc.module.famous.PathStore)
1.  [function <span class="apidocSignatureSpan">famous.</span>PathStore ()](#apidoc.element.famous.PathStore.PathStore)

#### [module famous.PathStore.prototype](#apidoc.module.famous.PathStore.prototype)
1.  [function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>get (path)](#apidoc.element.famous.PathStore.prototype.get)
1.  [function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>getItems ()](#apidoc.element.famous.PathStore.prototype.getItems)
1.  [function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>getPaths ()](#apidoc.element.famous.PathStore.prototype.getPaths)
1.  [function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>insert (path, item)](#apidoc.element.famous.PathStore.prototype.insert)
1.  [function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>remove (path)](#apidoc.element.famous.PathStore.prototype.remove)

#### [module famous.PhysicsEngine](#apidoc.module.famous.PhysicsEngine)
1.  [function <span class="apidocSignatureSpan">famous.</span>PhysicsEngine (options)](#apidoc.element.famous.PhysicsEngine.PhysicsEngine)

#### [module famous.PhysicsEngine.prototype](#apidoc.module.famous.PhysicsEngine.prototype)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>add ()](#apidoc.element.famous.PhysicsEngine.prototype.add)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>addBody (body)](#apidoc.element.famous.PhysicsEngine.prototype.addBody)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>addConstraint (constraint)](#apidoc.element.famous.PhysicsEngine.prototype.addConstraint)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>addForce (force)](#apidoc.element.famous.PhysicsEngine.prototype.addForce)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>getTransform (body)](#apidoc.element.famous.PhysicsEngine.prototype.getTransform)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>off (key, callback)](#apidoc.element.famous.PhysicsEngine.prototype.off)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>on (key, callback)](#apidoc.element.famous.PhysicsEngine.prototype.on)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>remove ()](#apidoc.element.famous.PhysicsEngine.prototype.remove)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>removeBody (body)](#apidoc.element.famous.PhysicsEngine.prototype.removeBody)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>removeConstraint (constraint)](#apidoc.element.famous.PhysicsEngine.prototype.removeConstraint)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>removeForce (force)](#apidoc.element.famous.PhysicsEngine.prototype.removeForce)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>setOrientation (w, x, y, z)](#apidoc.element.famous.PhysicsEngine.prototype.setOrientation)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>setOrigin (x, y, z)](#apidoc.element.famous.PhysicsEngine.prototype.setOrigin)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>trigger (key, payload)](#apidoc.element.famous.PhysicsEngine.prototype.trigger)
1.  [function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>update (time)](#apidoc.element.famous.PhysicsEngine.prototype.update)

#### [module famous.Position](#apidoc.module.famous.Position)
1.  [function <span class="apidocSignatureSpan">famous.</span>Position (node)](#apidoc.element.famous.Position.Position)

#### [module famous.Position.prototype](#apidoc.module.famous.Position.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>_checkUpdate ()](#apidoc.element.famous.Position.prototype._checkUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getValue ()](#apidoc.element.famous.Position.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getX ()](#apidoc.element.famous.Position.prototype.getX)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getY ()](#apidoc.element.famous.Position.prototype.getY)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getZ ()](#apidoc.element.famous.Position.prototype.getZ)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>halt ()](#apidoc.element.famous.Position.prototype.halt)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>isActive ()](#apidoc.element.famous.Position.prototype.isActive)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>onUpdate ()](#apidoc.element.famous.Position.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>set (x, y, z, transition, callback)](#apidoc.element.famous.Position.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setValue (state)](#apidoc.element.famous.Position.prototype.setValue)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setX (val, transition, callback)](#apidoc.element.famous.Position.prototype.setX)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setY (val, transition, callback)](#apidoc.element.famous.Position.prototype.setY)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setZ (val, transition, callback)](#apidoc.element.famous.Position.prototype.setZ)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>toString ()](#apidoc.element.famous.Position.prototype.toString)
1.  [function <span class="apidocSignatureSpan">famous.Position.prototype.</span>update ()](#apidoc.element.famous.Position.prototype.update)

#### [module famous.Program](#apidoc.module.famous.Program)
1.  [function <span class="apidocSignatureSpan">famous.</span>Program (gl, options)](#apidoc.element.famous.Program.Program)

#### [module famous.Program.prototype](#apidoc.module.famous.Program.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Program.prototype.</span>compileShader (shader, source)](#apidoc.element.famous.Program.prototype.compileShader)
1.  [function <span class="apidocSignatureSpan">famous.Program.prototype.</span>getUniformTypeFromValue (value)](#apidoc.element.famous.Program.prototype.getUniformTypeFromValue)
1.  [function <span class="apidocSignatureSpan">famous.Program.prototype.</span>registerMaterial (name, material)](#apidoc.element.famous.Program.prototype.registerMaterial)
1.  [function <span class="apidocSignatureSpan">famous.Program.prototype.</span>resetProgram ()](#apidoc.element.famous.Program.prototype.resetProgram)
1.  [function <span class="apidocSignatureSpan">famous.Program.prototype.</span>setUniforms (uniformNames, uniformValue)](#apidoc.element.famous.Program.prototype.setUniforms)
1.  [function <span class="apidocSignatureSpan">famous.Program.prototype.</span>uniformIsCached (targetName, value)](#apidoc.element.famous.Program.prototype.uniformIsCached)

#### [module famous.Quaternion](#apidoc.module.famous.Quaternion)
1.  [function <span class="apidocSignatureSpan">famous.</span>Quaternion (w, x, y, z)](#apidoc.element.famous.Quaternion.Quaternion)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.</span>clone (q)](#apidoc.element.famous.Quaternion.clone)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.</span>conjugate (q, output)](#apidoc.element.famous.Quaternion.conjugate)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.</span>dot (q1, q2)](#apidoc.element.famous.Quaternion.dot)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.</span>multiply (q1, q2, output)](#apidoc.element.famous.Quaternion.multiply)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.</span>normalize (q, output)](#apidoc.element.famous.Quaternion.normalize)

#### [module famous.Quaternion.prototype](#apidoc.module.famous.Quaternion.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>clear ()](#apidoc.element.famous.Quaternion.prototype.clear)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>conjugate ()](#apidoc.element.famous.Quaternion.prototype.conjugate)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>copy (q)](#apidoc.element.famous.Quaternion.prototype.copy)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>dot (q)](#apidoc.element.famous.Quaternion.prototype.dot)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>fromAngleAxis (angle, x, y, z)](#apidoc.element.famous.Quaternion.prototype.fromAngleAxis)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>fromEuler (x, y, z)](#apidoc.element.famous.Quaternion.prototype.fromEuler)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>invert ()](#apidoc.element.famous.Quaternion.prototype.invert)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>leftMultiply (q)](#apidoc.element.famous.Quaternion.prototype.leftMultiply)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>length ()](#apidoc.element.famous.Quaternion.prototype.length)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>multiply (q)](#apidoc.element.famous.Quaternion.prototype.multiply)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>normalize ()](#apidoc.element.famous.Quaternion.prototype.normalize)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>rotateVector (v, output)](#apidoc.element.famous.Quaternion.prototype.rotateVector)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>set (w, x , y, z)](#apidoc.element.famous.Quaternion.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>slerp (q, t, output)](#apidoc.element.famous.Quaternion.prototype.slerp)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>toEuler (output)](#apidoc.element.famous.Quaternion.prototype.toEuler)
1.  [function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>toMatrix (output)](#apidoc.element.famous.Quaternion.prototype.toMatrix)

#### [module famous.Registry](#apidoc.module.famous.Registry)
1.  [function <span class="apidocSignatureSpan">famous.</span>Registry ()](#apidoc.element.famous.Registry.Registry)

#### [module famous.Registry.prototype](#apidoc.module.famous.Registry.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>get (key)](#apidoc.element.famous.Registry.prototype.get)
1.  [function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>getKeyToValue ()](#apidoc.element.famous.Registry.prototype.getKeyToValue)
1.  [function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>getKeys ()](#apidoc.element.famous.Registry.prototype.getKeys)
1.  [function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>getValues ()](#apidoc.element.famous.Registry.prototype.getValues)
1.  [function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>register (key, value)](#apidoc.element.famous.Registry.prototype.register)
1.  [function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>unregister (key)](#apidoc.element.famous.Registry.prototype.unregister)

#### [module famous.RequestAnimationFrameLoop](#apidoc.module.famous.RequestAnimationFrameLoop)
1.  [function <span class="apidocSignatureSpan">famous.</span>RequestAnimationFrameLoop ()](#apidoc.element.famous.RequestAnimationFrameLoop.RequestAnimationFrameLoop)

#### [module famous.RequestAnimationFrameLoop.prototype](#apidoc.module.famous.RequestAnimationFrameLoop.prototype)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_onFocus ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._onFocus)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_onUnfocus ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._onUnfocus)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_onVisibilityChange ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._onVisibilityChange)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_start ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._start)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_stop ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._stop)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>isRunning ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.isRunning)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>loop (time)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.loop)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>noLongerUpdate (updateable)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.noLongerUpdate)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>start ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.start)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>step (time)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.step)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>stop ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.stop)
1.  [function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>update (updateable)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.update)

#### [module famous.Rotation](#apidoc.module.famous.Rotation)
1.  [function <span class="apidocSignatureSpan">famous.</span>Rotation (node)](#apidoc.element.famous.Rotation.Rotation)

#### [module famous.Rotation.prototype](#apidoc.module.famous.Rotation.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Rotation.prototype.</span>constructor (node)](#apidoc.element.famous.Rotation.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">famous.Rotation.prototype.</span>onUpdate ()](#apidoc.element.famous.Rotation.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Rotation.prototype.</span>update ()](#apidoc.element.famous.Rotation.prototype.update)

#### [module famous.Scale](#apidoc.module.famous.Scale)
1.  [function <span class="apidocSignatureSpan">famous.</span>Scale (node)](#apidoc.element.famous.Scale.Scale)

#### [module famous.Scale.prototype](#apidoc.module.famous.Scale.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Scale.prototype.</span>constructor (node)](#apidoc.element.famous.Scale.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">famous.Scale.prototype.</span>onUpdate ()](#apidoc.element.famous.Scale.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Scale.prototype.</span>update ()](#apidoc.element.famous.Scale.prototype.update)

#### [module famous.Scene](#apidoc.module.famous.Scene)
1.  boolean <span class="apidocSignatureSpan">famous.Scene.</span>NO_DEFAULT_COMPONENTS
1.  [function <span class="apidocSignatureSpan">famous.</span>Scene (selector, updater)](#apidoc.element.famous.Scene.Scene)

#### [module famous.Scene.prototype](#apidoc.module.famous.Scene.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>constructor (selector, updater)](#apidoc.element.famous.Scene.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>getDispatch ()](#apidoc.element.famous.Scene.prototype.getDispatch)
1.  [function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>getSelector ()](#apidoc.element.famous.Scene.prototype.getSelector)
1.  [function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>getUpdater ()](#apidoc.element.famous.Scene.prototype.getUpdater)
1.  [function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>mount (path)](#apidoc.element.famous.Scene.prototype.mount)
1.  [function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>onReceive (event, payload)](#apidoc.element.famous.Scene.prototype.onReceive)

#### [module famous.Size](#apidoc.module.famous.Size)
1.  [function <span class="apidocSignatureSpan">famous.</span>Size (node)](#apidoc.element.famous.Size.Size)
1.  number <span class="apidocSignatureSpan">famous.Size.</span>ABSOLUTE
1.  number <span class="apidocSignatureSpan">famous.Size.</span>DEFAULT
1.  number <span class="apidocSignatureSpan">famous.Size.</span>RELATIVE
1.  number <span class="apidocSignatureSpan">famous.Size.</span>RENDER

#### [module famous.Size.prototype](#apidoc.module.famous.Size.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>_isActive (type)](#apidoc.element.famous.Size.prototype._isActive)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>get ()](#apidoc.element.famous.Size.prototype.get)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>getValue ()](#apidoc.element.famous.Size.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>halt ()](#apidoc.element.famous.Size.prototype.halt)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>isActive ()](#apidoc.element.famous.Size.prototype.isActive)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>onUpdate ()](#apidoc.element.famous.Size.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setAbsolute (x, y, z, options, callback)](#apidoc.element.famous.Size.prototype.setAbsolute)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setDifferential (x, y, z, options, callback)](#apidoc.element.famous.Size.prototype.setDifferential)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setMode (x, y, z)](#apidoc.element.famous.Size.prototype.setMode)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setProportional (x, y, z, options, callback)](#apidoc.element.famous.Size.prototype.setProportional)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setValue (state)](#apidoc.element.famous.Size.prototype.setValue)
1.  [function <span class="apidocSignatureSpan">famous.Size.prototype.</span>toString ()](#apidoc.element.famous.Size.prototype.toString)

#### [module famous.Texture](#apidoc.module.famous.Texture)
1.  [function <span class="apidocSignatureSpan">famous.</span>Texture (gl, options)](#apidoc.element.famous.Texture.Texture)

#### [module famous.Texture.prototype](#apidoc.module.famous.Texture.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>bind ()](#apidoc.element.famous.Texture.prototype.bind)
1.  [function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>readBack (x, y, width, height)](#apidoc.element.famous.Texture.prototype.readBack)
1.  [function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>setArray (input)](#apidoc.element.famous.Texture.prototype.setArray)
1.  [function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>setImage (img)](#apidoc.element.famous.Texture.prototype.setImage)
1.  [function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>unbind ()](#apidoc.element.famous.Texture.prototype.unbind)

#### [module famous.TextureManager](#apidoc.module.famous.TextureManager)
1.  [function <span class="apidocSignatureSpan">famous.</span>TextureManager (gl)](#apidoc.element.famous.TextureManager.TextureManager)

#### [module famous.TextureManager.prototype](#apidoc.module.famous.TextureManager.prototype)
1.  [function <span class="apidocSignatureSpan">famous.TextureManager.prototype.</span>bindTexture (id)](#apidoc.element.famous.TextureManager.prototype.bindTexture)
1.  [function <span class="apidocSignatureSpan">famous.TextureManager.prototype.</span>register (input, slot)](#apidoc.element.famous.TextureManager.prototype.register)
1.  [function <span class="apidocSignatureSpan">famous.TextureManager.prototype.</span>update (time)](#apidoc.element.famous.TextureManager.prototype.update)

#### [module famous.TextureRegistry](#apidoc.module.famous.TextureRegistry)
1.  [function <span class="apidocSignatureSpan">famous.TextureRegistry.</span>get (accessor)](#apidoc.element.famous.TextureRegistry.get)
1.  [function <span class="apidocSignatureSpan">famous.TextureRegistry.</span>register (accessor, data, options)](#apidoc.element.famous.TextureRegistry.register)
1.  number <span class="apidocSignatureSpan">famous.TextureRegistry.</span>textureIds
1.  object <span class="apidocSignatureSpan">famous.TextureRegistry.</span>registry

#### [module famous.Transform](#apidoc.module.famous.Transform)
1.  [function <span class="apidocSignatureSpan">famous.</span>Transform (node)](#apidoc.element.famous.Transform.Transform)

#### [module famous.Transform.prototype](#apidoc.module.famous.Transform.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>clean ()](#apidoc.element.famous.Transform.prototype.clean)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>getValue ()](#apidoc.element.famous.Transform.prototype.getValue)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>onUpdate ()](#apidoc.element.famous.Transform.prototype.onUpdate)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>rotate (x, y, z, w, options, callback)](#apidoc.element.famous.Transform.prototype.rotate)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setAlign (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setAlign)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setMountPoint (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setMountPoint)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setOrigin (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setOrigin)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setPosition (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setPosition)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setRotation (x, y, z, w, options, callback)](#apidoc.element.famous.Transform.prototype.setRotation)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setScale (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setScale)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setState (state)](#apidoc.element.famous.Transform.prototype.setState)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>toString ()](#apidoc.element.famous.Transform.prototype.toString)
1.  [function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>translate (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.translate)

#### [module famous.Transitionable](#apidoc.module.famous.Transitionable)
1.  [function <span class="apidocSignatureSpan">famous.</span>Transitionable (initialState)](#apidoc.element.famous.Transitionable.Transitionable)
1.  object <span class="apidocSignatureSpan">famous.Transitionable.</span>Clock

#### [module famous.Transitionable.prototype](#apidoc.module.famous.Transitionable.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>_interpolate (output, from, to, progress, method)](#apidoc.element.famous.Transitionable.prototype._interpolate)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>_sync (output, input)](#apidoc.element.famous.Transitionable.prototype._sync)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>delay (duration, callback)](#apidoc.element.famous.Transitionable.prototype.delay)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>from (initialState)](#apidoc.element.famous.Transitionable.prototype.from)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>get (t)](#apidoc.element.famous.Transitionable.prototype.get)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>halt ()](#apidoc.element.famous.Transitionable.prototype.halt)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>isActive ()](#apidoc.element.famous.Transitionable.prototype.isActive)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>isPaused ()](#apidoc.element.famous.Transitionable.prototype.isPaused)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>override (finalState, curve, duration, callback, method)](#apidoc.element.famous.Transitionable.prototype.override)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>pause ()](#apidoc.element.famous.Transitionable.prototype.pause)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>reset (start)](#apidoc.element.famous.Transitionable.prototype.reset)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>resume ()](#apidoc.element.famous.Transitionable.prototype.resume)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>set (state, transition, callback)](#apidoc.element.famous.Transitionable.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>to (finalState, curve, duration, callback, method)](#apidoc.element.famous.Transitionable.prototype.to)

#### [module famous.UIManager](#apidoc.module.famous.UIManager)
1.  [function <span class="apidocSignatureSpan">famous.</span>UIManager (thread, compositor, renderLoop)](#apidoc.element.famous.UIManager.UIManager)

#### [module famous.UIManager.prototype](#apidoc.module.famous.UIManager.prototype)
1.  [function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getCompositor ()](#apidoc.element.famous.UIManager.prototype.getCompositor)
1.  [function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getEngine ()](#apidoc.element.famous.UIManager.prototype.getEngine)
1.  [function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getRenderLoop ()](#apidoc.element.famous.UIManager.prototype.getRenderLoop)
1.  [function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getThread ()](#apidoc.element.famous.UIManager.prototype.getThread)
1.  [function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>update (time)](#apidoc.element.famous.UIManager.prototype.update)

#### [module famous.Vec2](#apidoc.module.famous.Vec2)
1.  [function <span class="apidocSignatureSpan">famous.</span>Vec2 (x, y)](#apidoc.element.famous.Vec2.Vec2)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>add (v1, v2, output)](#apidoc.element.famous.Vec2.add)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>clone (v)](#apidoc.element.famous.Vec2.clone)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>cross (v1, v2)](#apidoc.element.famous.Vec2.cross)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>dot (v1, v2)](#apidoc.element.famous.Vec2.dot)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>normalize (v, output)](#apidoc.element.famous.Vec2.normalize)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>scale (v, s, output)](#apidoc.element.famous.Vec2.scale)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.</span>subtract (v1, v2, output)](#apidoc.element.famous.Vec2.subtract)

#### [module famous.Vec2.prototype](#apidoc.module.famous.Vec2.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>add (v)](#apidoc.element.famous.Vec2.prototype.add)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>clear ()](#apidoc.element.famous.Vec2.prototype.clear)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>copy (v)](#apidoc.element.famous.Vec2.prototype.copy)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>cross (v)](#apidoc.element.famous.Vec2.prototype.cross)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>dot (v)](#apidoc.element.famous.Vec2.prototype.dot)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>invert ()](#apidoc.element.famous.Vec2.prototype.invert)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>isZero ()](#apidoc.element.famous.Vec2.prototype.isZero)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>length ()](#apidoc.element.famous.Vec2.prototype.length)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>map (fn)](#apidoc.element.famous.Vec2.prototype.map)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>rotate (theta)](#apidoc.element.famous.Vec2.prototype.rotate)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>scale (s)](#apidoc.element.famous.Vec2.prototype.scale)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>set (x, y)](#apidoc.element.famous.Vec2.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>subtract (v)](#apidoc.element.famous.Vec2.prototype.subtract)
1.  [function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>toArray ()](#apidoc.element.famous.Vec2.prototype.toArray)

#### [module famous.Vec3](#apidoc.module.famous.Vec3)
1.  [function <span class="apidocSignatureSpan">famous.</span>Vec3 (x , y, z)](#apidoc.element.famous.Vec3.Vec3)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>add (v1, v2, output)](#apidoc.element.famous.Vec3.add)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>applyRotation (v, q, output)](#apidoc.element.famous.Vec3.applyRotation)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>clone (v)](#apidoc.element.famous.Vec3.clone)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>cross (v1, v2, output)](#apidoc.element.famous.Vec3.cross)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>dot (v1, v2)](#apidoc.element.famous.Vec3.dot)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>normalize (v, output)](#apidoc.element.famous.Vec3.normalize)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>project (v1, v2, output)](#apidoc.element.famous.Vec3.project)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>scale (v, s, output)](#apidoc.element.famous.Vec3.scale)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.</span>subtract (v1, v2, output)](#apidoc.element.famous.Vec3.subtract)

#### [module famous.Vec3.prototype](#apidoc.module.famous.Vec3.prototype)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>add (v)](#apidoc.element.famous.Vec3.prototype.add)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>applyMatrix (matrix)](#apidoc.element.famous.Vec3.prototype.applyMatrix)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>applyRotation (q)](#apidoc.element.famous.Vec3.prototype.applyRotation)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>clear ()](#apidoc.element.famous.Vec3.prototype.clear)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>copy (v)](#apidoc.element.famous.Vec3.prototype.copy)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>cross (v)](#apidoc.element.famous.Vec3.prototype.cross)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>dot (v)](#apidoc.element.famous.Vec3.prototype.dot)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>invert ()](#apidoc.element.famous.Vec3.prototype.invert)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>isZero ()](#apidoc.element.famous.Vec3.prototype.isZero)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>length ()](#apidoc.element.famous.Vec3.prototype.length)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>lengthSq ()](#apidoc.element.famous.Vec3.prototype.lengthSq)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>map (fn)](#apidoc.element.famous.Vec3.prototype.map)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>normalize ()](#apidoc.element.famous.Vec3.prototype.normalize)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>rotateX (theta)](#apidoc.element.famous.Vec3.prototype.rotateX)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>rotateY (theta)](#apidoc.element.famous.Vec3.prototype.rotateY)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>rotateZ (theta)](#apidoc.element.famous.Vec3.prototype.rotateZ)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>scale (s)](#apidoc.element.famous.Vec3.prototype.scale)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>set (x, y, z)](#apidoc.element.famous.Vec3.prototype.set)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>subtract (v)](#apidoc.element.famous.Vec3.prototype.subtract)
1.  [function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>toArray ()](#apidoc.element.famous.Vec3.prototype.toArray)

#### [module famous.WebGLRenderer](#apidoc.module.famous.WebGLRenderer)
1.  [function <span class="apidocSignatureSpan">famous.</span>WebGLRenderer (canvas, compositor)](#apidoc.element.famous.WebGLRenderer.WebGLRenderer)

#### [module famous.WebGLRenderer.prototype](#apidoc.module.famous.WebGLRenderer.prototype)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>bufferData (geometryId, bufferName, bufferValue, bufferSpacing, isDynamic)](#apidoc.element.famous.WebGLRenderer.prototype.bufferData)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>createLight (path)](#apidoc.element.famous.WebGLRenderer.prototype.createLight)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>createMesh (path)](#apidoc.element.famous.WebGLRenderer.prototype.createMesh)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>draw (renderState)](#apidoc.element.famous.WebGLRenderer.prototype.draw)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>drawBuffers (vertexBuffers, mode, id)](#apidoc.element.famous.WebGLRenderer.prototype.drawBuffers)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>drawCutouts ()](#apidoc.element.famous.WebGLRenderer.prototype.drawCutouts)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>drawMeshes ()](#apidoc.element.famous.WebGLRenderer.prototype.drawMeshes)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>getOrSetCutout (path)](#apidoc.element.famous.WebGLRenderer.prototype.getOrSetCutout)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>getWebGLContext (canvas)](#apidoc.element.famous.WebGLRenderer.prototype.getWebGLContext)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>handleMaterialInput (path, name, material)](#apidoc.element.famous.WebGLRenderer.prototype.handleMaterialInput)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>handleOptions (options, mesh)](#apidoc.element.famous.WebGLRenderer.prototype.handleOptions)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>removeMesh (path)](#apidoc.element.famous.WebGLRenderer.prototype.removeMesh)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>resetOptions (options)](#apidoc.element.famous.WebGLRenderer.prototype.resetOptions)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setAmbientLightColor (path, r, g, b)](#apidoc.element.famous.WebGLRenderer.prototype.setAmbientLightColor)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setCutoutState (path, usesCutout)](#apidoc.element.famous.WebGLRenderer.prototype.setCutoutState)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setCutoutUniform (path, uniformName, uniformValue)](#apidoc.element.famous.WebGLRenderer.prototype.setCutoutUniform)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setGeometry (path, geometry, drawType, dynamic)](#apidoc.element.famous.WebGLRenderer.prototype.setGeometry)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setGlobalUniforms (renderState)](#apidoc.element.famous.WebGLRenderer.prototype.setGlobalUniforms)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setLightColor (path, r, g, b)](#apidoc.element.famous.WebGLRenderer.prototype.setLightColor)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setLightPosition (path, x, y, z)](#apidoc.element.famous.WebGLRenderer.prototype.setLightPosition)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setMeshOptions (path, options)](#apidoc.element.famous.WebGLRenderer.prototype.setMeshOptions)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setMeshUniform (path, uniformName, uniformValue)](#apidoc.element.famous.WebGLRenderer.prototype.setMeshUniform)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setMeshVisibility (path, visibility)](#apidoc.element.famous.WebGLRenderer.prototype.setMeshVisibility)
1.  [function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>updateSize (size)](#apidoc.element.famous.WebGLRenderer.prototype.updateSize)

#### [module famous.animationFrame](#apidoc.module.famous.animationFrame)
1.  [function <span class="apidocSignatureSpan">famous.animationFrame.</span>cancelAnimationFrame (id)](#apidoc.element.famous.animationFrame.cancelAnimationFrame)
1.  [function <span class="apidocSignatureSpan">famous.animationFrame.</span>requestAnimationFrame (callback)](#apidoc.element.famous.animationFrame.requestAnimationFrame)



# <a name="apidoc.module.famous"></a>[module famous](#apidoc.module.famous)

#### <a name="apidoc.element.famous.Align"></a>[function <span class="apidocSignatureSpan">famous.</span>Align (node)](#apidoc.element.famous.Align)
- description and source-code
```javascript
function Align(node) {
    Position.call(this, node);

    var initial = node.getAlign();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Buffer"></a>[function <span class="apidocSignatureSpan">famous.</span>Buffer (target, type, gl)](#apidoc.element.famous.Buffer)
- description and source-code
```javascript
function Buffer(target, type, gl) {
    this.buffer = null;
    this.target = target;
    this.type = type;
    this.data = [];
    this.gl = gl;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.BufferRegistry"></a>[function <span class="apidocSignatureSpan">famous.</span>BufferRegistry (context)](#apidoc.element.famous.BufferRegistry)
- description and source-code
```javascript
function BufferRegistry(context) {
    this.gl = context;

    this.registry = {};
    this._dynamicBuffers = [];
    this._staticBuffers = [];

    this._arrayBufferMax = 30000;
    this._elementBufferMax = 30000;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.CallbackStore"></a>[function <span class="apidocSignatureSpan">famous.</span>CallbackStore ()](#apidoc.element.famous.CallbackStore)
- description and source-code
```javascript
function CallbackStore() {
    this._events = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Camera"></a>[function <span class="apidocSignatureSpan">famous.</span>Camera (node)](#apidoc.element.famous.Camera)
- description and source-code
```javascript
function Camera(node) {
    this._node = node;
    this._projectionType = Camera.ORTHOGRAPHIC_PROJECTION;
    this._focalDepth = 0;
    this._near = 0;
    this._far = 0;
    this._requestingUpdate = false;
    this._id = node.addComponent(this);
    this._viewTransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);
    this._viewDirty = false;
    this._perspectiveDirty = false;
    this.setFlat();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Channel"></a>[function <span class="apidocSignatureSpan">famous.</span>Channel ()](#apidoc.element.famous.Channel)
- description and source-code
```javascript
function Channel() {
    if (typeof self !== 'undefined' && self.window !== self) {
        this._enterWorkerMode();
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Clock"></a>[function <span class="apidocSignatureSpan">famous.</span>Clock ()](#apidoc.element.famous.Clock)
- description and source-code
```javascript
function Clock() {
    this._time = 0;
    this._frame = 0;
    this._timerQueue = [];
    this._updatingIndex = 0;

    this._scale = 1;
    this._scaledTime = this._time;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Color"></a>[function <span class="apidocSignatureSpan">famous.</span>Color (color, transition, cb)](#apidoc.element.famous.Color)
- description and source-code
```javascript
function Color(color, transition, cb) {
    this._r = new Transitionable(0);
    this._g = new Transitionable(0);
    this._b = new Transitionable(0);
    this._opacity = new Transitionable(1);
    if (color) this.set(color, transition, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Compositor"></a>[function <span class="apidocSignatureSpan">famous.</span>Compositor ()](#apidoc.element.famous.Compositor)
- description and source-code
```javascript
function Compositor() {
    injectCSS();

    this._contexts = {};
    this._outCommands = [];
    this._inCommands = [];
    this._time = null;

    this._resized = false;

    var _this = this;
    window.addEventListener('resize', function() {
        _this.onResize();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Context"></a>[function <span class="apidocSignatureSpan">famous.</span>Context (selector, compositor)](#apidoc.element.famous.Context)
- description and source-code
```javascript
function Context(selector, compositor) {
    this._compositor = compositor;
    this._rootEl = document.querySelector(selector);
    this._selector = selector;

    if (this._rootEl === null) {
        throw new Error(
            'Failed to create Context: ' +
            'No matches for "' + selector + '" found.'
        );
    }

    this._selector = selector;

    // Initializes the DOMRenderer.
    // Every Context has at least a DOMRenderer for now.
    this._initDOMRenderer();

    // WebGLRenderer will be instantiated when needed.
    this._webGLRenderer = null;
    this._domRenderer = new DOMRenderer(this._domRendererRootEl, selector, compositor);
    this._canvasEl = null;

    // State holders

    this._renderState = {
        projectionType: Camera.ORTHOGRAPHIC_PROJECTION,
        perspectiveTransform: new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]),
        viewTransform: new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]),
        viewDirty: false,
        perspectiveDirty: false
    };

    this._size = [];

    this._meshTransform = new Float32Array(16);
    this._meshSize = [0, 0, 0];

    this._initDOM = false;

    this._commandCallbacks = [];
    this.initCommandCallbacks();

    this.updateSize();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMElement"></a>[function <span class="apidocSignatureSpan">famous.</span>DOMElement (node, options)](#apidoc.element.famous.DOMElement)
- description and source-code
```javascript
function DOMElement(node, options) {
    if (!node) throw new Error('DOMElement must be instantiated on a node');

    this._changeQueue = [];

    this._requestingUpdate = false;
    this._renderSized = false;
    this._requestRenderSize = false;

    this._UIEvents = node.getUIEvents().slice(0);
    this._classes = ['famous-dom-element'];
    this._requestingEventListeners = [];
    this._styles = {};

    this._attributes = {};
    this._content = '';

    this._tagName = options && options.tagName ? options.tagName : 'div';
    this._renderSize = [0, 0, 0];

    this._node = node;

    if (node) node.addComponent(this);

    this._callbacks = new CallbackStore();

    this.setProperty('display', node.isShown() ? 'block' : 'none');
    this.onOpacityChange(node.getOpacity());

    if (!options) return;

    var i;
    var key;

    if (options.classes)
        for (i = 0; i < options.classes.length; i++)
            this.addClass(options.classes[i]);

    if (options.attributes)
        for (key in options.attributes)
            this.setAttribute(key, options.attributes[key]);

    if (options.properties)
        for (key in options.properties)
            this.setProperty(key, options.properties[key]);

    if (options.id) this.setId(options.id);
    if (options.content) this.setContent(options.content);
    if (options.cutout === false) this.setCutoutState(options.cutout);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer"></a>[function <span class="apidocSignatureSpan">famous.</span>DOMRenderer (element, selector, compositor)](#apidoc.element.famous.DOMRenderer)
- description and source-code
```javascript
function DOMRenderer(element, selector, compositor) {
    var _this = this;

    element.classList.add('famous-dom-renderer');

    TRANSFORM = TRANSFORM || vendorPrefix('transform');
    this._compositor = compositor; // a reference to the compositor

    this._target = null; // a register for holding the current
                         // element that the Renderer is operating
                         // upon

    this._parent = null; // a register for holding the parent
                         // of the target

    this._path = null; // a register for holding the path of the target
                       // this register must be set first, and then
                       // children, target, and parent are all looked
                       // up from that.

    this._children = []; // a register for holding the children of the
                         // current target.

     this._insertElCallbackStore = new CallbackStore();
     this._removeElCallbackStore = new CallbackStore();

    this._root = new ElementCache(element, selector); // the root
                                                      // of the dom tree that this
                                                      // renderer is responsible
                                                      // for

    this._boundTriggerEvent = function (ev) {
        return _this._triggerEvent(ev);
    };

    this._selector = selector;

    this._elements = {};

    this._elements[selector] = this._root;

    this.perspectiveTransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);
    this._VPtransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);

    this._lastEv = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry"></a>[function <span class="apidocSignatureSpan">famous.</span>DynamicGeometry (options)](#apidoc.element.famous.DynamicGeometry)
- description and source-code
```javascript
function DynamicGeometry(options) {
    Geometry.call(this, options);

    this.spec.dynamic = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GestureHandler"></a>[function <span class="apidocSignatureSpan">famous.</span>GestureHandler (node, events)](#apidoc.element.famous.GestureHandler)
- description and source-code
```javascript
function GestureHandler(node, events) {
    this.node = node;
    this.id = node.addComponent(this);

    this._events = new CallbackStore();

    this.last1 = new Vec2();
    this.last2 = new Vec2();

    this.delta1 = new Vec2();
    this.delta2 = new Vec2();

    this.velocity1 = new Vec2();
    this.velocity2 = new Vec2();

    this.dist = 0;
    this.diff12 = new Vec2();

    this.center = new Vec2();
    this.centerDelta = new Vec2();
    this.centerVelocity = new Vec2();

    this.pointer1 = {
        position: this.last1,
        delta: this.delta1,
        velocity: this.velocity1
    };

    this.pointer2 = {
        position: this.last2,
        delta: this.delta2,
        velocity: this.velocity2
    };

    this.event = {
        status: null,
        time: 0,
        pointers: [],
        center: this.center,
        centerDelta: this.centerDelta,
        centerVelocity: this.centerVelocity,
        points: 0,
        current: 0
    };

    this.trackedPointerIDs = [-1, -1];
    this.timeOfPointer = 0;
    this.multiTap = 0;

    this.mice = [];

    this.gestures = [];
    this.options = {};
    this.trackedGestures = {};

    var i;
    var len;

    if (events) {
        for (i = 0, len = events.length; i < len; i++) {
            this.on(events[i], events[i].callback);
        }
    }

    node.addUIEvent('touchstart');
    node.addUIEvent('mousedown');
    node.addUIEvent('touchmove');
    node.addUIEvent('mousemove');
    node.addUIEvent('touchend');
    node.addUIEvent('mouseup');
    node.addUIEvent('mouseleave');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33"></a>[function <span class="apidocSignatureSpan">famous.</span>Mat33 (values)](#apidoc.element.famous.Mat33)
- description and source-code
```javascript
function Mat33(values) {
    this.values = values || [1,0,0,0,1,0,0,0,1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh"></a>[function <span class="apidocSignatureSpan">famous.</span>Mesh (node, options)](#apidoc.element.famous.Mesh)
- description and source-code
```javascript
function Mesh(node, options) {
    this._node = null;
    this._id = null;
    this._changeQueue = [];
    this._initialized = false;
    this._requestingUpdate = false;
    this._inDraw = false;
    this.value = {
        geometry: defaultGeometry,
        drawOptions: null,
        color: null,
        expressions: {},
        flatShading: null,
        glossiness: null,
        positionOffset: null,
        normals: null
    };
    if (node) node.addComponent(this);
    if (options) this.setDrawOptions(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.MountPoint"></a>[function <span class="apidocSignatureSpan">famous.</span>MountPoint (node)](#apidoc.element.famous.MountPoint)
- description and source-code
```javascript
function MountPoint(node) {
    Position.call(this, node);

    var initial = node.getMountPoint();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node"></a>[function <span class="apidocSignatureSpan">famous.</span>Node ()](#apidoc.element.famous.Node)
- description and source-code
```javascript
function Node() {
    this._requestingUpdate = false;
    this._inUpdate = false;
    this._mounted = false;
    this._shown = true;
    this._updater = null;
    this._opacity = 1;
    this._UIEvents = [];

    this._updateQueue = [];
    this._nextUpdateQueue = [];

    this._freedComponentIndicies = [];
    this._components = [];

    this._freedChildIndicies = [];
    this._children = [];

    this._fullChildren = [];

    this._parent = null;

    this._id = null;

    this._transformID = null;
    this._sizeID = null;

    if (!this.constructor.NO_DEFAULT_COMPONENTS) this._init();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Opacity"></a>[function <span class="apidocSignatureSpan">famous.</span>Opacity (node)](#apidoc.element.famous.Opacity)
- description and source-code
```javascript
function Opacity(node) {
    this._node = node;
    this._id = node.addComponent(this);
    this._value = new Transitionable(1);

    this._requestingUpdate = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Origin"></a>[function <span class="apidocSignatureSpan">famous.</span>Origin (node)](#apidoc.element.famous.Origin)
- description and source-code
```javascript
function Origin(node) {
    Position.call(this, node);

    var initial = node.getOrigin();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.PathStore"></a>[function <span class="apidocSignatureSpan">famous.</span>PathStore ()](#apidoc.element.famous.PathStore)
- description and source-code
```javascript
function PathStore() {
    this.items = [];
    this.paths = [];
    this.memo = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.PhysicsEngine"></a>[function <span class="apidocSignatureSpan">famous.</span>PhysicsEngine (options)](#apidoc.element.famous.PhysicsEngine)
- description and source-code
```javascript
function PhysicsEngine(options) {
    this.events = new CallbackStore();

    options = options || {};
<span class="apidocCodeCommentSpan">    /** @prop bodies The bodies currently active in the engine. */
</span>    this.bodies = [];
    /** @prop forces The forces currently active in the engine. */
    this.forces = [];
    /** @prop constraints The constraints currently active in the engine. */
    this.constraints = [];

    /** @prop step The time between frames in the engine. */
    this.step = options.step || 1000/60;
    /** @prop iterations The number of times each constraint is solved per frame. */
    this.iterations = options.iterations || 10;
    /** @prop _indexPool Pools of indicies to track holes in the arrays. */
    this._indexPools = {
        bodies: [],
        forces: [],
        constraints: []
    };

    this._entityMaps = {
        bodies: {},
        forces: {},
        constraints: {}
    };

    this.speed = options.speed || 1.0;
    this.time = 0;
    this.delta = 0;

    this.origin = options.origin || new Vec3();
    this.orientation = options.orientation ? options.orientation.normalize() :  new Quaternion();

    this.frameDependent = options.frameDependent || false;

    this.transformBuffers = {
        position: [0, 0, 0],
        rotation: [0, 0, 0, 1]
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position"></a>[function <span class="apidocSignatureSpan">famous.</span>Position (node)](#apidoc.element.famous.Position)
- description and source-code
```javascript
function Position(node) {
    this._node = node;
    this._id = node.addComponent(this);

    this._requestingUpdate = false;

    var initialPosition = node.getPosition();

    this._x = new Transitionable(initialPosition[0]);
    this._y = new Transitionable(initialPosition[1]);
    this._z = new Transitionable(initialPosition[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Program"></a>[function <span class="apidocSignatureSpan">famous.</span>Program (gl, options)](#apidoc.element.famous.Program)
- description and source-code
```javascript
function Program(gl, options) {
    this.gl = gl;
    this.options = options || {};

    this.registeredMaterials = {};
    this.cachedUniforms = {};
    this.uniformTypes = [];

    this.definitionVec4 = [];
    this.definitionVec3 = [];
    this.definitionFloat = [];
    this.applicationVec3 = [];
    this.applicationVec4 = [];
    this.applicationFloat = [];
    this.applicationVert = [];
    this.definitionVert = [];

    if (this.options.debug) {
        this.gl.compileShader = Debug.call(this);
    }

    this.resetProgram();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion"></a>[function <span class="apidocSignatureSpan">famous.</span>Quaternion (w, x, y, z)](#apidoc.element.famous.Quaternion)
- description and source-code
```javascript
function Quaternion(w, x, y, z) {
    this.w = w || 1;
    this.x = x || 0;
    this.y = y || 0;
    this.z = z || 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Registry"></a>[function <span class="apidocSignatureSpan">famous.</span>Registry ()](#apidoc.element.famous.Registry)
- description and source-code
```javascript
function Registry() {
    this._keyToValue = {};
    this._values = [];
    this._keys = [];
    this._keyToIndex = {};
    this._freedIndices = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop"></a>[function <span class="apidocSignatureSpan">famous.</span>RequestAnimationFrameLoop ()](#apidoc.element.famous.RequestAnimationFrameLoop)
- description and source-code
```javascript
function RequestAnimationFrameLoop() {
    var _this = this;

    // References to objects to be updated on next frame.
    this._updates = [];

    this._looper = function(time) {
        _this.loop(time);
    };
    this._time = 0;
    this._stoppedAt = 0;
    this._sleep = 0;

    // Indicates whether the engine should be restarted when the tab/ window is
    // being focused again (visibility change).
    this._startOnVisibilityChange = true;

    // requestId as returned by requestAnimationFrame function;
    this._rAF = null;

    this._sleepDiff = true;

    // The engine is being started on instantiation.
    // TODO(alexanderGugel)
    this.start();

    // The RequestAnimationFrameLoop supports running in a non-browser
    // environment (e.g. Worker).
    if (DOCUMENT_ACCESS) {
        document.addEventListener(VENDOR_VISIBILITY_CHANGE, function() {
            _this._onVisibilityChange();
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Rotation"></a>[function <span class="apidocSignatureSpan">famous.</span>Rotation (node)](#apidoc.element.famous.Rotation)
- description and source-code
```javascript
function Rotation(node) {
    Position.call(this, node);

    var initial = node.getRotation();

    var x = initial[0];
    var y = initial[1];
    var z = initial[2];
    var w = initial[3];

    var xx = x * x;
    var yy = y * y;
    var zz = z * z;

    var ty = 2 * (x * z + y * w);
    ty = ty < -1 ? -1 : ty > 1 ? 1 : ty;

    var rx = Math.atan2(2 * (x * w - y * z), 1 - 2 * (xx + yy));
    var ry = Math.asin(ty);
    var rz = Math.atan2(2 * (z * w - x * y), 1 - 2 * (yy + zz));

    this._x.set(rx);
    this._y.set(ry);
    this._z.set(rz);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Scale"></a>[function <span class="apidocSignatureSpan">famous.</span>Scale (node)](#apidoc.element.famous.Scale)
- description and source-code
```javascript
function Scale(node) {
    Position.call(this, node);

    this._x.set(1);
    this._y.set(1);
    this._z.set(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Scene"></a>[function <span class="apidocSignatureSpan">famous.</span>Scene (selector, updater)](#apidoc.element.famous.Scene)
- description and source-code
```javascript
function Scene(selector, updater) {
    if (!selector) throw new Error('Scene needs to be created with a DOM selector');
    if (!updater) throw new Error('Scene needs to be created with a class like Famous');

    Node.call(this);         // Scene inherits from node

    this._globalUpdater = updater; // The updater that will both
                                   // send messages to the renderers
                                   // and update dirty nodes

    this._selector = selector; // reference to the DOM selector
                               // that represents the element
                               // in the dom that this context
                               // inhabits

    this.mount(selector); // Mount the context to itself
                          // (it is its own parent)

    this._globalUpdater                  // message a request for the dom
        .message(Commands.NEED_SIZE_FOR)  // size of the context so that
        .message(selector);               // the scene graph has a total size

    this.show(); // the context begins shown (it's already present in the dom)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Size"></a>[function <span class="apidocSignatureSpan">famous.</span>Size (node)](#apidoc.element.famous.Size)
- description and source-code
```javascript
function Size(node) {
    this._node = node;
    this._id = node.addComponent(this);
    this._requestingUpdate = false;

    var initialProportionalSize = node.getProportionalSize();
    var initialDifferentialSize = node.getDifferentialSize();
    var initialAbsoluteSize = node.getAbsoluteSize();

    this._proportional = {
        x: new Transitionable(initialProportionalSize[0]),
        y: new Transitionable(initialProportionalSize[1]),
        z: new Transitionable(initialProportionalSize[2])
    };
    this._differential = {
        x: new Transitionable(initialDifferentialSize[0]),
        y: new Transitionable(initialDifferentialSize[1]),
        z: new Transitionable(initialDifferentialSize[2])
    };
    this._absolute = {
        x: new Transitionable(initialAbsoluteSize[0]),
        y: new Transitionable(initialAbsoluteSize[1]),
        z: new Transitionable(initialAbsoluteSize[2])
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Texture"></a>[function <span class="apidocSignatureSpan">famous.</span>Texture (gl, options)](#apidoc.element.famous.Texture)
- description and source-code
```javascript
function Texture(gl, options) {
    options = options || {};
    this.id = gl.createTexture();
    this.width = options.width || 0;
    this.height = options.height || 0;
    this.mipmap = options.mipmap;
    this.format = options.format || 'RGBA';
    this.type = options.type || 'UNSIGNED_BYTE';
    this.gl = gl;

    this.bind();

    gl.pixelStorei(gl.UNPACK_FLIP_Y_WEBGL, options.flipYWebgl || false);
    gl.pixelStorei(gl.UNPACK_PREMULTIPLY_ALPHA_WEBGL, options.premultiplyAlphaWebgl || false);

    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_MAG_FILTER, gl[options.magFilter] || gl.NEAREST);
    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_MIN_FILTER, gl[options.minFilter] || gl.NEAREST);

    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_S, gl[options.wrapS] || gl.CLAMP_TO_EDGE);
    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_T, gl[options.wrapT] || gl.CLAMP_TO_EDGE);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.TextureManager"></a>[function <span class="apidocSignatureSpan">famous.</span>TextureManager (gl)](#apidoc.element.famous.TextureManager)
- description and source-code
```javascript
function TextureManager(gl) {
    this.registry = [];
    this._needsResample = [];

    this._activeTexture = 0;
    this._boundTexture = null;

    this._checkerboard = createCheckerboard();

    this.gl = gl;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Transform"></a>[function <span class="apidocSignatureSpan">famous.</span>Transform (node)](#apidoc.element.famous.Transform)
- description and source-code
```javascript
function Transform(node) {
    this._node = node;
    this._id = node.addComponent(this);
    this.origin = null;
    this.mountPoint = null;
    this.align = null;
    this.scale = null;
    this.position = null;
    this.rotation = null;

    this._dirty = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Transitionable"></a>[function <span class="apidocSignatureSpan">famous.</span>Transitionable (initialState)](#apidoc.element.famous.Transitionable)
- description and source-code
```javascript
function Transitionable(initialState) {
    this._queue = [];
    this._from = null;
    this._state = null;
    this._startedAt = null;
    this._pausedAt = null;
    if (initialState != null) this.from(initialState);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.UIManager"></a>[function <span class="apidocSignatureSpan">famous.</span>UIManager (thread, compositor, renderLoop)](#apidoc.element.famous.UIManager)
- description and source-code
```javascript
function UIManager(thread, compositor, renderLoop) {
    this._thread = thread;
    this._compositor = compositor;
    this._renderLoop = renderLoop;

    this._renderLoop.update(this);

    var _this = this;
    this._thread.onmessage = function (ev) {
        var message = ev.data ? ev.data : ev;
        if (message[0] === Commands.ENGINE) {
            switch (message[1]) {
                case Commands.START:
                    _this._engine.start();
                    break;
                case Commands.STOP:
                    _this._engine.stop();
                    break;
                default:
                    console.error(
                        'Unknown ENGINE command "' + message[1] + '"'
                    );
                    break;
            }
        }
        else {
            _this._compositor.receiveCommands(message);
        }
    };
    this._thread.onerror = function (error) {
        console.error(error);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec2"></a>[function <span class="apidocSignatureSpan">famous.</span>Vec2 (x, y)](#apidoc.element.famous.Vec2)
- description and source-code
```javascript
Vec2 = function (x, y) {
    if (x instanceof Array || x instanceof Float32Array) {
        this.x = x[0] || 0;
        this.y = x[1] || 0;
    }
    else {
        this.x = x || 0;
        this.y = y || 0;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3"></a>[function <span class="apidocSignatureSpan">famous.</span>Vec3 (x , y, z)](#apidoc.element.famous.Vec3)
- description and source-code
```javascript
Vec3 = function (x , y, z){
    this.x = x || 0;
    this.y = y || 0;
    this.z = z || 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.WebGLRenderer"></a>[function <span class="apidocSignatureSpan">famous.</span>WebGLRenderer (canvas, compositor)](#apidoc.element.famous.WebGLRenderer)
- description and source-code
```javascript
function WebGLRenderer(canvas, compositor) {
    canvas.classList.add('famous-webgl-renderer');

    this.canvas = canvas;
    this.compositor = compositor;

    var gl = this.gl = this.getWebGLContext(this.canvas);

    gl.clearColor(0.0, 0.0, 0.0, 0.0);
    gl.polygonOffset(0.1, 0.1);
    gl.enable(gl.POLYGON_OFFSET_FILL);
    gl.enable(gl.DEPTH_TEST);
    gl.enable(gl.BLEND);
    gl.depthFunc(gl.LEQUAL);
    gl.blendFunc(gl.SRC_ALPHA, gl.ONE_MINUS_SRC_ALPHA);
    gl.enable(gl.CULL_FACE);
    gl.cullFace(gl.BACK);

    this.meshRegistry = new Registry();
    this.cutoutRegistry = new Registry();
    this.lightRegistry = new Registry();

    this.numLights = 0;
    this.ambientLightColor = [0, 0, 0];
    this.lightPositions = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
    this.lightColors = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];

    this.textureManager = new TextureManager(gl);
    this.bufferRegistry = new BufferRegistry(gl);
    this.program = new Program(gl, { debug: true });

    this.state = {
        boundArrayBuffer: null,
        boundElementBuffer: null,
        lastDrawn: null,
        enabledAttributes: {},
        enabledAttributesKeys: []
    };

    this.resolutionName = ['u_resolution'];
    this.resolutionValues = [[0, 0, 0]];

    this.cachedSize = [];

<span class="apidocCodeCommentSpan">    /*
    The projectionTransform has some constant components, i.e. the z scale, and the x and y translation.

    The z scale keeps the final z position of any vertex within the clip's domain by scaling it by an
    arbitrarily small coefficient. This has the advantage of being a useful default in the event of the
    user forgoing a near and far plane, an alien convention in dom space as in DOM overlapping is
    conducted via painter's algorithm.

    The x and y translation transforms the world space origin to the top left corner of the screen.

    The final component (this.projectionTransform[15]) is initialized as 1 because certain projection models,
    e.g. the WC3 specified model, keep the XY plane as the projection hyperplane.
    */
</span>    this.projectionTransform = [1, 0, 0, 0, 0, 1, 0, 0, 0, 0, -0.000001, 0, -1, 1, 0, 1];

    // TODO: remove this hack

    var cutout = this.cutoutGeometry = {
        spec: {
            id: -1,
            bufferValues: [[-1, -1, 0, 1, -1, 0, -1, 1, 0, 1, 1, 0]],
            bufferNames: ['a_pos'],
            type: 'TRIANGLE_STRIP'
        }
    };

    this.bufferRegistry.allocate(
        this.cutoutGeometry.spec.id,
        cutout.spec.bufferNames[0],
        cutout.spec.bufferValues[0],
        3
    );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Align"></a>[module famous.Align](#apidoc.module.famous.Align)

#### <a name="apidoc.element.famous.Align.Align"></a>[function <span class="apidocSignatureSpan">famous.</span>Align (node)](#apidoc.element.famous.Align.Align)
- description and source-code
```javascript
function Align(node) {
    Position.call(this, node);

    var initial = node.getAlign();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Align.prototype"></a>[module famous.Align.prototype](#apidoc.module.famous.Align.prototype)

#### <a name="apidoc.element.famous.Align.prototype.constructor"></a>[function <span class="apidocSignatureSpan">famous.Align.prototype.</span>constructor (node)](#apidoc.element.famous.Align.prototype.constructor)
- description and source-code
```javascript
function Align(node) {
    Position.call(this, node);

    var initial = node.getAlign();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Align.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Align.prototype.</span>onUpdate ()](#apidoc.element.famous.Align.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Align.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Align.prototype.</span>update ()](#apidoc.element.famous.Align.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Buffer"></a>[module famous.Buffer](#apidoc.module.famous.Buffer)

#### <a name="apidoc.element.famous.Buffer.Buffer"></a>[function <span class="apidocSignatureSpan">famous.</span>Buffer (target, type, gl)](#apidoc.element.famous.Buffer.Buffer)
- description and source-code
```javascript
function Buffer(target, type, gl) {
    this.buffer = null;
    this.target = target;
    this.type = type;
    this.data = [];
    this.gl = gl;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Buffer.prototype"></a>[module famous.Buffer.prototype](#apidoc.module.famous.Buffer.prototype)

#### <a name="apidoc.element.famous.Buffer.prototype.subData"></a>[function <span class="apidocSignatureSpan">famous.Buffer.prototype.</span>subData ()](#apidoc.element.famous.Buffer.prototype.subData)
- description and source-code
```javascript
function subData() {
    var gl = this.gl;
    var data = [];

    // to prevent against maximum call-stack issue.
    for (var i = 0, chunk = 10000; i < this.data.length; i += chunk)
        data = Array.prototype.concat.apply(data, this.data.slice(i, i + chunk));

    this.buffer = this.buffer || gl.createBuffer();
    gl.bindBuffer(this.target, this.buffer);
    gl.bufferData(this.target, new this.type(data), gl.STATIC_DRAW);
}
```
- example usage
```shell
...
        vertexBuffers.length.push(length);
    }

    var len = value.length;
    for (k = 0; k < len; k++) {
        vertexBuffers.values[j].data[offset + k] = value[k];
    }
    vertexBuffers.values[j].subData();
};

module.exports = BufferRegistry;
...
```



# <a name="apidoc.module.famous.BufferRegistry"></a>[module famous.BufferRegistry](#apidoc.module.famous.BufferRegistry)

#### <a name="apidoc.element.famous.BufferRegistry.BufferRegistry"></a>[function <span class="apidocSignatureSpan">famous.</span>BufferRegistry (context)](#apidoc.element.famous.BufferRegistry.BufferRegistry)
- description and source-code
```javascript
function BufferRegistry(context) {
    this.gl = context;

    this.registry = {};
    this._dynamicBuffers = [];
    this._staticBuffers = [];

    this._arrayBufferMax = 30000;
    this._elementBufferMax = 30000;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.BufferRegistry.prototype"></a>[module famous.BufferRegistry.prototype](#apidoc.module.famous.BufferRegistry.prototype)

#### <a name="apidoc.element.famous.BufferRegistry.prototype.allocate"></a>[function <span class="apidocSignatureSpan">famous.BufferRegistry.prototype.</span>allocate (geometryId, name, value, spacing, dynamic)](#apidoc.element.famous.BufferRegistry.prototype.allocate)
- description and source-code
```javascript
function allocate(geometryId, name, value, spacing, dynamic) {
    var vertexBuffers = this.registry[geometryId] || (this.registry[geometryId] = { keys: [], values: [], spacing: [], offset: [],
length: [] });

    var j = vertexBuffers.keys.indexOf(name);
    var isIndex = name === INDICES;
    var bufferFound = false;
    var newOffset;
    var offset = 0;
    var length;
    var buffer;
    var k;

    if (j === -1) {
        j = vertexBuffers.keys.length;
        length = isIndex ? value.length : Math.floor(value.length / spacing);

        if (!dynamic) {

            // Use a previously created buffer if available.

            for (k = 0; k < this._staticBuffers.length; k++) {

                if (isIndex === this._staticBuffers[k].isIndex) {
                    newOffset = this._staticBuffers[k].offset + value.length;
                    if ((!isIndex && newOffset < this._arrayBufferMax) || (isIndex && newOffset < this._elementBufferMax)) {
                        buffer = this._staticBuffers[k].buffer;
                        offset = this._staticBuffers[k].offset;
                        this._staticBuffers[k].offset += value.length;
                        bufferFound = true;
                        break;
                    }
                }
            }

            // Create a new static buffer in none were found.

            if (!bufferFound) {
                buffer = new Buffer(
                    isIndex ? this.gl.ELEMENT_ARRAY_BUFFER : this.gl.ARRAY_BUFFER,
                    isIndex ? Uint16Array : Float32Array,
                    this.gl
                );

                this._staticBuffers.push({ buffer: buffer, offset: value.length, isIndex: isIndex });
            }
        }
        else {

            // For dynamic geometries, always create new buffer.

            buffer = new Buffer(
                isIndex ? this.gl.ELEMENT_ARRAY_BUFFER : this.gl.ARRAY_BUFFER,
                isIndex ? Uint16Array : Float32Array,
                this.gl
            );

            this._dynamicBuffers.push({ buffer: buffer, offset: value.length, isIndex: isIndex });
        }

        // Update the registry for the spec with buffer information.

        vertexBuffers.keys.push(name);
        vertexBuffers.values.push(buffer);
        vertexBuffers.spacing.push(spacing);
        vertexBuffers.offset.push(offset);
        vertexBuffers.length.push(length);
    }

    var len = value.length;
    for (k = 0; k < len; k++) {
        vertexBuffers.values[j].data[offset + k] = value[k];
    }
    vertexBuffers.values[j].subData();
}
```
- example usage
```shell
...
            id: -1,
            bufferValues: [[-1, -1, 0, 1, -1, 0, -1, 1, 0, 1, 1, 0]],
            bufferNames: ['a_pos'],
            type: 'TRIANGLE_STRIP'
        }
    };

    this.bufferRegistry.allocate(
        this.cutoutGeometry.spec.id,
        cutout.spec.bufferNames[0],
        cutout.spec.bufferValues[0],
        3
    );
}
...
```



# <a name="apidoc.module.famous.CallbackStore"></a>[module famous.CallbackStore](#apidoc.module.famous.CallbackStore)

#### <a name="apidoc.element.famous.CallbackStore.CallbackStore"></a>[function <span class="apidocSignatureSpan">famous.</span>CallbackStore ()](#apidoc.element.famous.CallbackStore.CallbackStore)
- description and source-code
```javascript
function CallbackStore() {
    this._events = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.CallbackStore.prototype"></a>[module famous.CallbackStore.prototype](#apidoc.module.famous.CallbackStore.prototype)

#### <a name="apidoc.element.famous.CallbackStore.prototype.off"></a>[function <span class="apidocSignatureSpan">famous.CallbackStore.prototype.</span>off (key, callback)](#apidoc.element.famous.CallbackStore.prototype.off)
- description and source-code
```javascript
function off(key, callback) {
    var events = this._events[key];
    if (events) events.splice(events.indexOf(callback), 1);
    return this;
}
```
- example usage
```shell
...
*
* @param  {String}   path      Path at which the listener function has been
*                              registered.
* @param  {Function} callback  Callback function to be deregistered.
* @return {DOMRenderer}        this
*/
DOMRenderer.prototype.offInsertEl = function offInsertEl(path, callback) {
   this._insertElCallbackStore.off(path, callback);
   return this;
};

/**
* Registers an event handler to be triggered as soon as an element at the
* specified path is being removed.
*
...
```

#### <a name="apidoc.element.famous.CallbackStore.prototype.on"></a>[function <span class="apidocSignatureSpan">famous.CallbackStore.prototype.</span>on (key, callback)](#apidoc.element.famous.CallbackStore.prototype.on)
- description and source-code
```javascript
function on(key, callback) {
    if (!this._events[key]) this._events[key] = [];
    var callbackList = this._events[key];
    callbackList.push(callback);
    return function () {
        callbackList.splice(callbackList.indexOf(callback), 1);
    };
}
```
- example usage
```shell
...
this.trackedGestures = {};

var i;
var len;

if (events) {
    for (i = 0, len = events.length; i < len; i++) {
        this.on(events[i], events[i].callback);
    }
}

node.addUIEvent('touchstart');
node.addUIEvent('mousedown');
node.addUIEvent('touchmove');
node.addUIEvent('mousemove');
...
```

#### <a name="apidoc.element.famous.CallbackStore.prototype.trigger"></a>[function <span class="apidocSignatureSpan">famous.CallbackStore.prototype.</span>trigger (key, payload)](#apidoc.element.famous.CallbackStore.prototype.trigger)
- description and source-code
```javascript
function trigger(key, payload) {
    var events = this._events[key];
    if (events) {
        var i = 0;
        var len = events.length;
        for (; i < len ; i++) events[i](payload);
    }
    return this;
}
```
- example usage
```shell
...
GestureHandler.prototype.triggerGestures = function() {
var payload = this.event;
for (var i = 0, len = this.gestures.length; i < len; i++) {
    var gesture = this.gestures[i];
    switch (gesture) {
        case 'rotate':
        case 'pinch':
            if (payload.points === 2) this.trigger(gesture, payload);
            break;
        case 'tap':
            if (payload.status === 'start') {
                if (this.options.tap) {
                    var pts = this.options.tap.points || 1;
                    if(this.multiTap >= pts && payload.points >= pts) this.trigger(gesture, payload);
                }
...
```



# <a name="apidoc.module.famous.Camera"></a>[module famous.Camera](#apidoc.module.famous.Camera)

#### <a name="apidoc.element.famous.Camera.Camera"></a>[function <span class="apidocSignatureSpan">famous.</span>Camera (node)](#apidoc.element.famous.Camera.Camera)
- description and source-code
```javascript
function Camera(node) {
    this._node = node;
    this._projectionType = Camera.ORTHOGRAPHIC_PROJECTION;
    this._focalDepth = 0;
    this._near = 0;
    this._far = 0;
    this._requestingUpdate = false;
    this._id = node.addComponent(this);
    this._viewTransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);
    this._viewDirty = false;
    this._perspectiveDirty = false;
    this.setFlat();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Camera.prototype"></a>[module famous.Camera.prototype](#apidoc.module.famous.Camera.prototype)

#### <a name="apidoc.element.famous.Camera.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>getValue ()](#apidoc.element.famous.Camera.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Camera.prototype.onTransformChange"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>onTransformChange (transform)](#apidoc.element.famous.Camera.prototype.onTransformChange)
- description and source-code
```javascript
function onTransformChange(transform) {
    var a = transform;
    this._viewDirty = true;

    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    var a00 = a[0], a01 = a[1], a02 = a[2], a03 = a[3],
    a10 = a[4], a11 = a[5], a12 = a[6], a13 = a[7],
    a20 = a[8], a21 = a[9], a22 = a[10], a23 = a[11],
    a30 = a[12], a31 = a[13], a32 = a[14], a33 = a[15],

    b00 = a00 * a11 - a01 * a10,
    b01 = a00 * a12 - a02 * a10,
    b02 = a00 * a13 - a03 * a10,
    b03 = a01 * a12 - a02 * a11,
    b04 = a01 * a13 - a03 * a11,
    b05 = a02 * a13 - a03 * a12,
    b06 = a20 * a31 - a21 * a30,
    b07 = a20 * a32 - a22 * a30,
    b08 = a20 * a33 - a23 * a30,
    b09 = a21 * a32 - a22 * a31,
    b10 = a21 * a33 - a23 * a31,
    b11 = a22 * a33 - a23 * a32,

    det = 1/(b00 * b11 - b01 * b10 + b02 * b09 + b03 * b08 - b04 * b07 + b05 * b06);

    this._viewTransform[0] = (a11 * b11 - a12 * b10 + a13 * b09) * det;
    this._viewTransform[1] = (a02 * b10 - a01 * b11 - a03 * b09) * det;
    this._viewTransform[2] = (a31 * b05 - a32 * b04 + a33 * b03) * det;
    this._viewTransform[3] = (a22 * b04 - a21 * b05 - a23 * b03) * det;
    this._viewTransform[4] = (a12 * b08 - a10 * b11 - a13 * b07) * det;
    this._viewTransform[5] = (a00 * b11 - a02 * b08 + a03 * b07) * det;
    this._viewTransform[6] = (a32 * b02 - a30 * b05 - a33 * b01) * det;
    this._viewTransform[7] = (a20 * b05 - a22 * b02 + a23 * b01) * det;
    this._viewTransform[8] = (a10 * b10 - a11 * b08 + a13 * b06) * det;
    this._viewTransform[9] = (a01 * b08 - a00 * b10 - a03 * b06) * det;
    this._viewTransform[10] = (a30 * b04 - a31 * b02 + a33 * b00) * det;
    this._viewTransform[11] = (a21 * b02 - a20 * b04 - a23 * b00) * det;
    this._viewTransform[12] = (a11 * b07 - a10 * b09 - a12 * b06) * det;
    this._viewTransform[13] = (a00 * b09 - a01 * b07 + a02 * b06) * det;
    this._viewTransform[14] = (a31 * b01 - a30 * b03 - a32 * b00) * det;
    this._viewTransform[15] = (a20 * b03 - a21 * b01 + a22 * b00) * det;
}
```
- example usage
```shell
...
* @param {Node} node the node on which to trigger a change event if necessary
* @param {Array} components the components on which to trigger a change event if necessary
* @param {Transform} transform the transform class that changed
*
* @return {undefined} undefined
*/
function transformChanged (node, components, transform) {
   if (node.onTransformChange) node.onTransformChange(transform);
   for (var i = 0, len = components.length ; i < len ; i++)
       if (components[i] && components[i].onTransformChange)
           components[i].onTransformChange(transform);
}

/**
* Private method to call when the local transform changes. Triggers 'onLocalTransformChange' methods
...
```

#### <a name="apidoc.element.famous.Camera.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>onUpdate ()](#apidoc.element.famous.Camera.prototype.onUpdate)
- description and source-code
```javascript
function onUpdate() {
    this._requestingUpdate = false;

    var path = this._node.getLocation();

    this._node
        .sendDrawCommand(Commands.WITH)
        .sendDrawCommand(path);

    if (this._perspectiveDirty) {
        this._perspectiveDirty = false;

        switch (this._projectionType) {
            case Camera.FRUSTUM_PROJECTION:
                this._node.sendDrawCommand(Commands.FRUSTRUM_PROJECTION);
                this._node.sendDrawCommand(this._near);
                this._node.sendDrawCommand(this._far);
                break;
            case Camera.PINHOLE_PROJECTION:
                this._node.sendDrawCommand(Commands.PINHOLE_PROJECTION);
                this._node.sendDrawCommand(this._focalDepth);
                break;
            case Camera.ORTHOGRAPHIC_PROJECTION:
                this._node.sendDrawCommand(Commands.ORTHOGRAPHIC_PROJECTION);
                break;
        }
    }

    if (this._viewDirty) {
        this._viewDirty = false;

        this._node.sendDrawCommand(Commands.CHANGE_VIEW_TRANSFORM);
        this._node.sendDrawCommand(this._viewTransform[0]);
        this._node.sendDrawCommand(this._viewTransform[1]);
        this._node.sendDrawCommand(this._viewTransform[2]);
        this._node.sendDrawCommand(this._viewTransform[3]);

        this._node.sendDrawCommand(this._viewTransform[4]);
        this._node.sendDrawCommand(this._viewTransform[5]);
        this._node.sendDrawCommand(this._viewTransform[6]);
        this._node.sendDrawCommand(this._viewTransform[7]);

        this._node.sendDrawCommand(this._viewTransform[8]);
        this._node.sendDrawCommand(this._viewTransform[9]);
        this._node.sendDrawCommand(this._viewTransform[10]);
        this._node.sendDrawCommand(this._viewTransform[11]);

        this._node.sendDrawCommand(this._viewTransform[12]);
        this._node.sendDrawCommand(this._viewTransform[13]);
        this._node.sendDrawCommand(this._viewTransform[14]);
        this._node.sendDrawCommand(this._viewTransform[15]);
    }
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Camera.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>set (type, depth, near, far)](#apidoc.element.famous.Camera.prototype.set)
- description and source-code
```javascript
function set(type, depth, near, far) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }
    this._projectionType = type;
    this._focalDepth = depth;
    this._near = near;
    this._far = far;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Camera.prototype.setDepth"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setDepth (depth)](#apidoc.element.famous.Camera.prototype.setDepth)
- description and source-code
```javascript
function setDepth(depth) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }
    this._perspectiveDirty = true;
    this._projectionType = Camera.PINHOLE_PROJECTION;
    this._focalDepth = depth;
    this._near = 0;
    this._far = 0;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Camera.prototype.setFlat"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setFlat ()](#apidoc.element.famous.Camera.prototype.setFlat)
- description and source-code
```javascript
function setFlat() {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    this._perspectiveDirty = true;
    this._projectionType = Camera.ORTHOGRAPHIC_PROJECTION;
    this._focalDepth = 0;
    this._near = 0;
    this._far = 0;

    return this;
}
```
- example usage
```shell
...
    this._near = 0;
    this._far = 0;
    this._requestingUpdate = false;
    this._id = node.addComponent(this);
    this._viewTransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);
    this._viewDirty = false;
    this._perspectiveDirty = false;
    this.setFlat();
}

Camera.FRUSTUM_PROJECTION = 0;
Camera.PINHOLE_PROJECTION = 1;
Camera.ORTHOGRAPHIC_PROJECTION = 2;

/**
...
```

#### <a name="apidoc.element.famous.Camera.prototype.setFrustum"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setFrustum (near, far)](#apidoc.element.famous.Camera.prototype.setFrustum)
- description and source-code
```javascript
function setFrustum(near, far) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    this._perspectiveDirty = true;
    this._projectionType = Camera.FRUSTUM_PROJECTION;
    this._focalDepth = 0;
    this._near = near;
    this._far = far;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Camera.prototype.setValue"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>setValue (state)](#apidoc.element.famous.Camera.prototype.setValue)
- description and source-code
```javascript
function setValue(state) {
    if (this.toString() === state.component) {
        this.set(state.projectionType, state.focalDepth, state.near, state.far);
        return true;
    }
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Camera.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.Camera.prototype.</span>toString ()](#apidoc.element.famous.Camera.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'Camera';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```



# <a name="apidoc.module.famous.Channel"></a>[module famous.Channel](#apidoc.module.famous.Channel)

#### <a name="apidoc.element.famous.Channel.Channel"></a>[function <span class="apidocSignatureSpan">famous.</span>Channel ()](#apidoc.element.famous.Channel.Channel)
- description and source-code
```javascript
function Channel() {
    if (typeof self !== 'undefined' && self.window !== self) {
        this._enterWorkerMode();
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Channel.prototype"></a>[module famous.Channel.prototype](#apidoc.module.famous.Channel.prototype)

#### <a name="apidoc.element.famous.Channel.prototype._enterWorkerMode"></a>[function <span class="apidocSignatureSpan">famous.Channel.prototype.</span>_enterWorkerMode ()](#apidoc.element.famous.Channel.prototype._enterWorkerMode)
- description and source-code
```javascript
function _enterWorkerMode() {
    this._workerMode = true;
    var _this = this;
    self.addEventListener('message', function onmessage(ev) {
        _this.onMessage(ev.data);
    });
}
```
- example usage
```shell
...
* threaded mode (no Web Worker).
*
* @class Channel
* @constructor
*/
function Channel() {
   if (typeof self !== 'undefined' && self.window !== self) {
       this._enterWorkerMode();
   }
}


/**
* Called during construction. Subscribes for 'message' event and routes all
* future 'sendMessage' messages to the Main Thread ("UI Thread").
...
```

#### <a name="apidoc.element.famous.Channel.prototype.postMessage"></a>[function <span class="apidocSignatureSpan">famous.Channel.prototype.</span>postMessage (message)](#apidoc.element.famous.Channel.prototype.postMessage)
- description and source-code
```javascript
function postMessage(message) {
    return this.onMessage(message);
}
```
- example usage
```shell
...
 *
 * @param  {Any}    message Arbitrary message object.
 *
 * @return {undefined} undefined
 */
Channel.prototype.sendMessage = function sendMessage (message) {
    if (this._workerMode) {
        self.postMessage(message);
    }
    else {
        this.onmessage(message);
    }
};

/**
...
```

#### <a name="apidoc.element.famous.Channel.prototype.sendMessage"></a>[function <span class="apidocSignatureSpan">famous.Channel.prototype.</span>sendMessage (message)](#apidoc.element.famous.Channel.prototype.sendMessage)
- description and source-code
```javascript
function sendMessage(message) {
    if (this._workerMode) {
        self.postMessage(message);
    }
    else {
        this.onmessage(message);
    }
}
```
- example usage
```shell
...
FamousEngine.prototype.step = function step (time) {
    if (time == null) throw new Error('step must be called with a time');

    this._clock.step(time);
    this._update();

    if (this._messages.length) {
        this._channel.sendMessage(this._messages);
        while (this._messages.length > 2) this._messages.pop();
    }

    return this;
};

/**
...
```



# <a name="apidoc.module.famous.Clock"></a>[module famous.Clock](#apidoc.module.famous.Clock)

#### <a name="apidoc.element.famous.Clock.Clock"></a>[function <span class="apidocSignatureSpan">famous.</span>Clock ()](#apidoc.element.famous.Clock.Clock)
- description and source-code
```javascript
function Clock() {
    this._time = 0;
    this._frame = 0;
    this._timerQueue = [];
    this._updatingIndex = 0;

    this._scale = 1;
    this._scaledTime = this._time;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Clock.prototype"></a>[module famous.Clock.prototype](#apidoc.module.famous.Clock.prototype)

#### <a name="apidoc.element.famous.Clock.prototype.clearTimer"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>clearTimer (timer)](#apidoc.element.famous.Clock.prototype.clearTimer)
- description and source-code
```javascript
clearTimer = function (timer) {
    var index = this._timerQueue.indexOf(timer);
    if (index !== -1) {
        this._timerQueue.splice(index, 1);
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Clock.prototype.getFrame"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>getFrame ()](#apidoc.element.famous.Clock.prototype.getFrame)
- description and source-code
```javascript
function getFrame() {
    return this._frame;
}
```
- example usage
```shell
...
* Method for getting the current frame. Will be deprecated.
*
* @method
*
* @return {Number} current frame
*/
Node.prototype.getFrame = function getFrame () {
   return this._updater.getFrame();
};

/**
* returns an array of the components currently attached to this
* node.
*
* @method getComponents
...
```

#### <a name="apidoc.element.famous.Clock.prototype.getScale"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>getScale ()](#apidoc.element.famous.Clock.prototype.getScale)
- description and source-code
```javascript
function getScale() {
    return this._scale;
}
```
- example usage
```shell
...
    }
    this.align.set(x, y, z, options, callback);
    return this;
};

Transform.prototype.setScale = function setScale(x, y, z, options, callback) {
    if (!this.scale) {
        var v = this._node.getScale();
        this.scale = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.scale.set(x, y, z, options, callback);
    return this;
};

Transform.prototype.setPosition = function setPosition(x, y, z, options, callback) {
...
```

#### <a name="apidoc.element.famous.Clock.prototype.getTime"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>getTime ()](#apidoc.element.famous.Clock.prototype.getTime)
- description and source-code
```javascript
function now() {
    return this._scaledTime;
}
```
- example usage
```shell
...
    // Fall back to setInterval for now (very rare).
    rAF = null;
}
}

if (!rAF) {
var now = Date.now ? Date.now : function () {
    return new Date().getTime();
};

rAF = function(callback) {
    var currTime = now();
    var timeToCall = Math.max(0, 16 - (currTime - lastTime));
    var id = setTimeout(function () {
        callback(currTime + timeToCall);
...
```

#### <a name="apidoc.element.famous.Clock.prototype.now"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>now ()](#apidoc.element.famous.Clock.prototype.now)
- description and source-code
```javascript
function now() {
    return this._scaledTime;
}
```
- example usage
```shell
...
}
else t = e.targetTouches;

if (t[0] && t[1] && this.trackedPointerIDs[0] === t[0].identifier && this.trackedPointerIDs[1] === t[1].identifier) {
    return;
}

this.event.time = Date.now();

var threshold;
var id;

if (this.trackedPointerIDs[0] !== t[0].identifier) {
    if (this.trackedGestures.tap) {
        threshold = (this.options.tap && this.options.tap.threshold) || 250;
...
```

#### <a name="apidoc.element.famous.Clock.prototype.setInterval"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>setInterval (callback, delay)](#apidoc.element.famous.Clock.prototype.setInterval)
- description and source-code
```javascript
function setInterval(callback, delay) {
    var params = Array.prototype.slice.call(arguments, 2);
    var startedAt = this._time;
    var timer = function(time) {
        if (time - startedAt >= delay) {
            callback.apply(null, params);
            startedAt = time;
        }
        return false;
    };
    this._timerQueue.push(timer);
    return timer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Clock.prototype.setScale"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>setScale (scale)](#apidoc.element.famous.Clock.prototype.setScale)
- description and source-code
```javascript
function setScale(scale) {
    this._scale = scale;
    return this;
}
```
- example usage
```shell
...
 * of the Node's scale.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Scale.prototype.update = function update() {
    this._node.setScale(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Scale.prototype.onUpdate = Scale.prototype.update;

module.exports = Scale;
...
```

#### <a name="apidoc.element.famous.Clock.prototype.setTimeout"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>setTimeout (callback, delay)](#apidoc.element.famous.Clock.prototype.setTimeout)
- description and source-code
```javascript
setTimeout = function (callback, delay) {
    var params = Array.prototype.slice.call(arguments, 2);
    var startedAt = this._time;
    var timer = function(time) {
        if (time - startedAt >= delay) {
            callback.apply(null, params);
            return true;
        }
        return false;
    };
    this._timerQueue.push(timer);
    return timer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Clock.prototype.step"></a>[function <span class="apidocSignatureSpan">famous.Clock.prototype.</span>step (time)](#apidoc.element.famous.Clock.prototype.step)
- description and source-code
```javascript
function step(time) {
    this._frame++;

    this._scaledTime = this._scaledTime + (time - this._time)*this._scale;
    this._time = time;

    for (var i = 0; i < this._timerQueue.length; i++) {
        if (this._timerQueue[i](this._scaledTime)) {
            this._timerQueue.splice(i, 1);
        }
    }
    return this;
}
```
- example usage
```shell
...
*
* @return {FamousEngine} this
*/
FamousEngine.prototype.handleFrame = function handleFrame (messages) {
   if (!messages) throw new Error('handleFrame must be called with an array of messages');
   if (!messages.length) throw new Error('FRAME must be sent with a time');

   this.step(messages.shift());
   return this;
};

/**
* step updates the clock and the scene graph and then sends the draw commands
* that accumulated in the update to the renderers.
*
...
```



# <a name="apidoc.module.famous.Color"></a>[module famous.Color](#apidoc.module.famous.Color)

#### <a name="apidoc.element.famous.Color.Color"></a>[function <span class="apidocSignatureSpan">famous.</span>Color (color, transition, cb)](#apidoc.element.famous.Color.Color)
- description and source-code
```javascript
function Color(color, transition, cb) {
    this._r = new Transitionable(0);
    this._g = new Transitionable(0);
    this._b = new Transitionable(0);
    this._opacity = new Transitionable(1);
    if (color) this.set(color, transition, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Color.determineType"></a>[function <span class="apidocSignatureSpan">famous.Color.</span>determineType (type)](#apidoc.element.famous.Color.determineType)
- description and source-code
```javascript
function determineType(type) {
    if (Color.isColorInstance(type)) return 'instance';
    if (colorNames[type]) return 'colorName';
    if (Color.isHex(type)) return 'hex';
    if (Array.isArray(type)) return 'rgb';
}
```
- example usage
```shell
...
 * @param {Color|String|Array} color Sets color using Hex, a Color instance, color name or RGB.
 * @param {Object} transition Optional transition
 * @param {Function} cb Callback function to be called on completion of the transition.
 *
 * @return {Color} Color
 */
Color.prototype.set = function set(color, transition, cb) {
    switch (Color.determineType(color)) {
        case 'hex': return this.setHex(color, transition, cb);
        case 'colorName': return this.setColor(color, transition, cb);
        case 'instance': return this.changeTo(color, transition, cb);
        case 'rgb': return this.setRGB(color[0], color[1], color[2], transition, cb);
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.Color.isColorInstance"></a>[function <span class="apidocSignatureSpan">famous.Color.</span>isColorInstance (val)](#apidoc.element.famous.Color.isColorInstance)
- description and source-code
```javascript
function isColorInstance(val) {
    return !!val.getColor;
}
```
- example usage
```shell
...
 * @param {Color} color Color instance.
 * @param {Object} transition Optional transition.
 * @param {Function} cb Optional callback function.
 *
 * @return {Color} Color
 */
Color.prototype.changeTo = function changeTo(color, transition, cb) {
    if (Color.isColorInstance(color)) {
        var rgb = color.getRGB();
        this.setRGB(rgb[0], rgb[1], rgb[2], transition, cb);
    }
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.Color.isHex"></a>[function <span class="apidocSignatureSpan">famous.Color.</span>isHex (val)](#apidoc.element.famous.Color.isHex)
- description and source-code
```javascript
function isHex(val) {
    if (!Color.isString(val)) return false;
    return val[0] === '#';
}
```
- example usage
```shell
...
* @param {Color|String|Array} type Color type
*
* @returns {String} Appropriate color type
*/
Color.determineType = function determineType(type) {
   if (Color.isColorInstance(type)) return 'instance';
   if (colorNames[type]) return 'colorName';
   if (Color.isHex(type)) return 'hex';
   if (Array.isArray(type)) return 'rgb';
};

/**
* Returns a boolean checking whether input is a 'String'
*
* @method
...
```

#### <a name="apidoc.element.famous.Color.isString"></a>[function <span class="apidocSignatureSpan">famous.Color.</span>isString (val)](#apidoc.element.famous.Color.isString)
- description and source-code
```javascript
function isString(val) {
    return (typeof val === 'string');
}
```
- example usage
```shell
...
* @method
*
* @param {String} option Optional argument for determining which type of color to get (default is RGB)
*
* @returns {Object} Color in either RGB or specific option value
*/
Color.prototype.getColor = function getColor(option) {
   if (Color.isString(option)) option = option.toLowerCase();
   return (option === 'hex') ? this.getHex() : this.getRGB();
};

/**
* Sets the R of the Color's RGB
*
* @method
...
```

#### <a name="apidoc.element.famous.Color.toHex"></a>[function <span class="apidocSignatureSpan">famous.Color.</span>toHex (num)](#apidoc.element.famous.Color.toHex)
- description and source-code
```javascript
function toHex(num) {
    var hex = num.toString(16);
    return hex.length === 1 ? '0' + hex : hex;
}
```
- example usage
```shell
...
* Returns the current color in Hex
*
* @method
*
* @returns {String} Hex value
*/
Color.prototype.getHex = function getHex() {
   var r = Color.toHex(this.getR());
   var g = Color.toHex(this.getG());
   var b = Color.toHex(this.getB());
   return '#' + r + g + b;
};

/**
* Sets color using Hex
...
```



# <a name="apidoc.module.famous.Color.prototype"></a>[module famous.Color.prototype](#apidoc.module.famous.Color.prototype)

#### <a name="apidoc.element.famous.Color.prototype.changeTo"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>changeTo (color, transition, cb)](#apidoc.element.famous.Color.prototype.changeTo)
- description and source-code
```javascript
function changeTo(color, transition, cb) {
    if (Color.isColorInstance(color)) {
        var rgb = color.getRGB();
        this.setRGB(rgb[0], rgb[1], rgb[2], transition, cb);
    }
    return this;
}
```
- example usage
```shell
...
*
* @return {Color} Color
*/
Color.prototype.set = function set(color, transition, cb) {
   switch (Color.determineType(color)) {
       case 'hex': return this.setHex(color, transition, cb);
       case 'colorName': return this.setColor(color, transition, cb);
       case 'instance': return this.changeTo(color, transition, cb);
       case 'rgb': return this.setRGB(color[0], color[1], color[2], transition, cb);
   }
   return this;
};

/**
* Returns whether Color is still in an animating (transitioning) state.
...
```

#### <a name="apidoc.element.famous.Color.prototype.getB"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getB ()](#apidoc.element.famous.Color.prototype.getB)
- description and source-code
```javascript
function getB() {
    return this._b.get();
}
```
- example usage
```shell
...
* Returns RGB
*
* @method
*
* @returns {Array} RGB
*/
Color.prototype.getRGB = function getRGB() {
   return [this.getR(), this.getG(), this.getB()];
};

/**
* Returns Normalized RGB
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.getColor"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getColor (option)](#apidoc.element.famous.Color.prototype.getColor)
- description and source-code
```javascript
function getColor(option) {
    if (Color.isString(option)) option = option.toLowerCase();
    return (option === 'hex') ? this.getHex() : this.getRGB();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Color.prototype.getG"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getG ()](#apidoc.element.famous.Color.prototype.getG)
- description and source-code
```javascript
function getG() {
    return this._g.get();
}
```
- example usage
```shell
...
* Returns RGB
*
* @method
*
* @returns {Array} RGB
*/
Color.prototype.getRGB = function getRGB() {
   return [this.getR(), this.getG(), this.getB()];
};

/**
* Returns Normalized RGB
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.getHex"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getHex ()](#apidoc.element.famous.Color.prototype.getHex)
- description and source-code
```javascript
function getHex() {
    var r = Color.toHex(this.getR());
    var g = Color.toHex(this.getG());
    var b = Color.toHex(this.getB());
    return '#' + r + g + b;
}
```
- example usage
```shell
...
*
* @param {String} option Optional argument for determining which type of color to get (default is RGB)
*
* @returns {Object} Color in either RGB or specific option value
*/
Color.prototype.getColor = function getColor(option) {
   if (Color.isString(option)) option = option.toLowerCase();
   return (option === 'hex') ? this.getHex() : this.getRGB();
};

/**
* Sets the R of the Color's RGB
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.getNormalizedRGB"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getNormalizedRGB ()](#apidoc.element.famous.Color.prototype.getNormalizedRGB)
- description and source-code
```javascript
function getNormalizedRGB() {
    var r = this.getR() / 255.0;
    var g = this.getG() / 255.0;
    var b = this.getB() / 255.0;
    return [r, g, b];
}
```
- example usage
```shell
...
    addMeshToMaterial(this, glossiness, 'glossiness');
    this.value.glossiness = [null, null];
    this.value.expressions.glossiness = glossiness;
}
else if (isColor) {
    this.value.expressions.glossiness = null;
    this.value.glossiness = [glossiness, strength || 20];
    glossiness = glossiness ? glossiness.getNormalizedRGB() : [0, 0, 0];
    glossiness.push(strength || 20);
}

if (this._initialized) {
    this._changeQueue.push(glossiness.__isAMaterial__ ? Commands.MATERIAL_INPUT : Commands.GL_UNIFORMS);
    this._changeQueue.push('u_glossiness');
    this._changeQueue.push(glossiness);
...
```

#### <a name="apidoc.element.famous.Color.prototype.getNormalizedRGBA"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getNormalizedRGBA ()](#apidoc.element.famous.Color.prototype.getNormalizedRGBA)
- description and source-code
```javascript
function getNormalizedRGB() {
    var r = this.getR() / 255.0;
    var g = this.getG() / 255.0;
    var b = this.getB() / 255.0;
    var opacity = this.getOpacity();
    return [r, g, b, opacity];
}
```
- example usage
```shell
...
this.value.color = null;
this.value.expressions.baseColor = color;
uniformValue = color;
    }
    else if (isColor) {
this.value.expressions.baseColor = null;
this.value.color = color;
uniformValue = color.getNormalizedRGBA();
    }

    if (this._initialized) {

// If a material expression

if (color.__isAMaterial__) {
...
```

#### <a name="apidoc.element.famous.Color.prototype.getOpacity"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getOpacity ()](#apidoc.element.famous.Color.prototype.getOpacity)
- description and source-code
```javascript
function getOpacity() {
    return this._opacity.get();
}
```
- example usage
```shell
...
    var value = {
location: this.getId(),
spec: {
    location: this.getId(),
    showState: {
        mounted: this.isMounted(),
        shown: this.isShown(),
        opacity: this.getOpacity() || null
    },
    offsets: {
        mountPoint: [0, 0, 0],
        align: [0, 0, 0],
        origin: [0, 0, 0]
    },
    vectors: {
...
```

#### <a name="apidoc.element.famous.Color.prototype.getR"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getR ()](#apidoc.element.famous.Color.prototype.getR)
- description and source-code
```javascript
function getR() {
    return this._r.get();
}
```
- example usage
```shell
...
* Returns RGB
*
* @method
*
* @returns {Array} RGB
*/
Color.prototype.getRGB = function getRGB() {
   return [this.getR(), this.getG(), this.getB()];
};

/**
* Returns Normalized RGB
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.getRGB"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>getRGB ()](#apidoc.element.famous.Color.prototype.getRGB)
- description and source-code
```javascript
function getRGB() {
    return [this.getR(), this.getG(), this.getB()];
}
```
- example usage
```shell
...
* @param {Object} transition Optional transition.
* @param {Function} cb Optional callback function.
*
* @return {Color} Color
*/
Color.prototype.changeTo = function changeTo(color, transition, cb) {
   if (Color.isColorInstance(color)) {
       var rgb = color.getRGB();
       this.setRGB(rgb[0], rgb[1], rgb[2], transition, cb);
   }
   return this;
};

/**
* Sets the color based on static color names.
...
```

#### <a name="apidoc.element.famous.Color.prototype.halt"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>halt ()](#apidoc.element.famous.Color.prototype.halt)
- description and source-code
```javascript
function halt() {
    this._r.halt();
    this._g.halt();
    this._b.halt();
    this._opacity.halt();
    return this;
}
```
- example usage
```shell
...
* Stops Opacity transition
*
* @method
*
* @return {Opacity} this
*/
Opacity.prototype.halt = function halt() {
   this._value.halt();
   return this;
};

/**
* Tells whether or not the opacity is in a transition
*
* @method
...
```

#### <a name="apidoc.element.famous.Color.prototype.isActive"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>isActive ()](#apidoc.element.famous.Color.prototype.isActive)
- description and source-code
```javascript
function isActive() {
    return this._r.isActive() ||
           this._g.isActive() ||
           this._b.isActive() ||
           this._opacity.isActive();
}
```
- example usage
```shell
...
* Tells whether or not the opacity is in a transition
*
* @method
*
* @return {Boolean} whether or not the opacity is transitioning
*/
Opacity.prototype.isActive = function isActive(){
   return this._value.isActive();
};

/**
* When the node this component is attached to updates, update the value
* of the Node's opacity.
*
* @method
...
```

#### <a name="apidoc.element.famous.Color.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>set (color, transition, cb)](#apidoc.element.famous.Color.prototype.set)
- description and source-code
```javascript
function set(color, transition, cb) {
    switch (Color.determineType(color)) {
        case 'hex': return this.setHex(color, transition, cb);
        case 'colorName': return this.setColor(color, transition, cb);
        case 'instance': return this.changeTo(color, transition, cb);
        case 'rgb': return this.setRGB(color[0], color[1], color[2], transition, cb);
    }
    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.setB"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setB (b, transition, cb)](#apidoc.element.famous.Color.prototype.setB)
- description and source-code
```javascript
function setB(b, transition, cb) {
    this._b.set(b, transition, cb);
    return this;
}
```
- example usage
```shell
...
* @param {Function} cb Optional callback
*
* @return {Color} Color
*/
Color.prototype.setRGB = function setRGB(r, g, b, transition, cb) {
   this.setR(r, transition);
   this.setG(g, transition);
   this.setB(b, transition, cb);
   return this;
};

/**
* Returns R of RGB
*
* @method
...
```

#### <a name="apidoc.element.famous.Color.prototype.setColor"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setColor (name, transition, cb)](#apidoc.element.famous.Color.prototype.setColor)
- description and source-code
```javascript
function setColor(name, transition, cb) {
    if (colorNames[name]) {
        this.setHex(colorNames[name], transition, cb);
    }
    return this;
}
```
- example usage
```shell
...
 * @param {Function} cb Callback function to be called on completion of the transition.
 *
 * @return {Color} Color
 */
Color.prototype.set = function set(color, transition, cb) {
    switch (Color.determineType(color)) {
        case 'hex': return this.setHex(color, transition, cb);
        case 'colorName': return this.setColor(color, transition, cb);
        case 'instance': return this.changeTo(color, transition, cb);
        case 'rgb': return this.setRGB(color[0], color[1], color[2], transition, cb);
    }
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.Color.prototype.setG"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setG (g, transition, cb)](#apidoc.element.famous.Color.prototype.setG)
- description and source-code
```javascript
function setG(g, transition, cb) {
    this._g.set(g, transition, cb);
    return this;
}
```
- example usage
```shell
...
* @param {Object} transition Optional transition parameters
* @param {Function} cb Optional callback
*
* @return {Color} Color
*/
Color.prototype.setRGB = function setRGB(r, g, b, transition, cb) {
   this.setR(r, transition);
   this.setG(g, transition);
   this.setB(b, transition, cb);
   return this;
};

/**
* Returns R of RGB
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.setHex"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setHex (hex, transition, cb)](#apidoc.element.famous.Color.prototype.setHex)
- description and source-code
```javascript
function setHex(hex, transition, cb) {
    hex = (hex.charAt(0) === '#') ? hex.substring(1, hex.length) : hex;

    if (hex.length === 3) {
        var shorthandRegex = /^#?([a-f\d])([a-f\d])([a-f\d])$/i;
        hex = hex.replace(shorthandRegex, function(m, r, g, b) {
            return r + r + g + g + b + b;
        });
    }

    var r = parseInt(hex.substring(0, 2), 16);
    var g = parseInt(hex.substring(2, 4), 16);
    var b = parseInt(hex.substring(4, 6), 16);
    this.setRGB(r, g, b, transition, cb);
    return this;
}
```
- example usage
```shell
...
 * @param {Object} transition Optional transition
 * @param {Function} cb Callback function to be called on completion of the transition.
 *
 * @return {Color} Color
 */
Color.prototype.set = function set(color, transition, cb) {
    switch (Color.determineType(color)) {
        case 'hex': return this.setHex(color, transition, cb);
        case 'colorName': return this.setColor(color, transition, cb);
        case 'instance': return this.changeTo(color, transition, cb);
        case 'rgb': return this.setRGB(color[0], color[1], color[2], transition, cb);
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.Color.prototype.setOpacity"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setOpacity (opacity, transition, cb)](#apidoc.element.famous.Color.prototype.setOpacity)
- description and source-code
```javascript
function setOpacity(opacity, transition, cb) {
    this._opacity.set(opacity, transition, cb);
    return this;
}
```
- example usage
```shell
...
 * of the Node's opacity.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Opacity.prototype.update = function update () {
this._node.setOpacity(this._value.get());

if (this._value.isActive()) {
  this._node.requestUpdateOnNextTick(this._id);
}
else {
  this._requestingUpdate = false;
}
...
```

#### <a name="apidoc.element.famous.Color.prototype.setR"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setR (r, transition, cb)](#apidoc.element.famous.Color.prototype.setR)
- description and source-code
```javascript
function setR(r, transition, cb) {
    this._r.set(r, transition, cb);
    return this;
}
```
- example usage
```shell
...
* @param {Number} b B channel of color
* @param {Object} transition Optional transition parameters
* @param {Function} cb Optional callback
*
* @return {Color} Color
*/
Color.prototype.setRGB = function setRGB(r, g, b, transition, cb) {
   this.setR(r, transition);
   this.setG(g, transition);
   this.setB(b, transition, cb);
   return this;
};

/**
* Returns R of RGB
...
```

#### <a name="apidoc.element.famous.Color.prototype.setRGB"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>setRGB (r, g, b, transition, cb)](#apidoc.element.famous.Color.prototype.setRGB)
- description and source-code
```javascript
function setRGB(r, g, b, transition, cb) {
    this.setR(r, transition);
    this.setG(g, transition);
    this.setB(b, transition, cb);
    return this;
}
```
- example usage
```shell
...
* @return {Color} Color
*/
Color.prototype.set = function set(color, transition, cb) {
   switch (Color.determineType(color)) {
       case 'hex': return this.setHex(color, transition, cb);
       case 'colorName': return this.setColor(color, transition, cb);
       case 'instance': return this.changeTo(color, transition, cb);
       case 'rgb': return this.setRGB(color[0], color[1], color[2], transition, cb);
   }
   return this;
};

/**
* Returns whether Color is still in an animating (transitioning) state.
*
...
```

#### <a name="apidoc.element.famous.Color.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.Color.prototype.</span>toString ()](#apidoc.element.famous.Color.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'Color';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```



# <a name="apidoc.module.famous.Commands"></a>[module famous.Commands](#apidoc.module.famous.Commands)

#### <a name="apidoc.element.famous.Commands.prettyPrint"></a>[function <span class="apidocSignatureSpan">famous.Commands.</span>prettyPrint (buffer, start, count)](#apidoc.element.famous.Commands.prettyPrint)
- description and source-code
```javascript
prettyPrint = function (buffer, start, count) {
    var callback;
    start = start ? start : 0;
    var data = {
        i: start,
        result: ''
    };
    for (var len = count ? count + start : buffer.length ; data.i < len ; data.i++) {
        callback = commandPrinters[buffer[data.i]];
        if (!callback) throw new Error('PARSE ERROR: no command registered for: ' + buffer[data.i]);
        callback(buffer, data);
    }
    return data.result;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Compositor"></a>[module famous.Compositor](#apidoc.module.famous.Compositor)

#### <a name="apidoc.element.famous.Compositor.Compositor"></a>[function <span class="apidocSignatureSpan">famous.</span>Compositor ()](#apidoc.element.famous.Compositor.Compositor)
- description and source-code
```javascript
function Compositor() {
    injectCSS();

    this._contexts = {};
    this._outCommands = [];
    this._inCommands = [];
    this._time = null;

    this._resized = false;

    var _this = this;
    window.addEventListener('resize', function() {
        _this.onResize();
    });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Compositor.prototype"></a>[module famous.Compositor.prototype](#apidoc.module.famous.Compositor.prototype)

#### <a name="apidoc.element.famous.Compositor.prototype.clearCommands"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>clearCommands ()](#apidoc.element.famous.Compositor.prototype.clearCommands)
- description and source-code
```javascript
function clearCommands() {
    this._inCommands.length = 0;
    this._outCommands.length = 0;
    this._resized = false;
}
```
- example usage
```shell
...
 * FRAME command
 * @return {undefined} undefined
 */
UIManager.prototype.update = function update (time) {
    this._thread.postMessage([Commands.FRAME, time]);
    var threadMessages = this._compositor.drawCommands();
    this._thread.postMessage(threadMessages);
    this._compositor.clearCommands();
};

module.exports = UIManager;
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.drawCommands"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>drawCommands ()](#apidoc.element.famous.Compositor.prototype.drawCommands)
- description and source-code
```javascript
function drawCommands() {
    var commands = this._inCommands;
    var localIterator = 0;
    var command = commands[localIterator];
    while (command) {
        switch (command) {
            case Commands.TIME:
                this._time = commands[++localIterator];
                break;
            case Commands.WITH:
                localIterator = this.handleWith(++localIterator, commands);
                break;
            case Commands.NEED_SIZE_FOR:
                this.giveSizeFor(++localIterator, commands);
                break;
        }
        command = commands[++localIterator];
    }

    // TODO: Switch to associative arrays here...

    for (var key in this._contexts) {
        this._contexts[key].draw();
    }

    if (this._resized) {
        this.updateSize();
    }

    return this._outCommands;
}
```
- example usage
```shell
...
 *
 * @param  {Number} time unix timestamp to be passed down to the worker as a
 * FRAME command
 * @return {undefined} undefined
 */
UIManager.prototype.update = function update (time) {
    this._thread.postMessage([Commands.FRAME, time]);
    var threadMessages = this._compositor.drawCommands();
    this._thread.postMessage(threadMessages);
    this._compositor.clearCommands();
};

module.exports = UIManager;
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.getContext"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>getContext (selector)](#apidoc.element.famous.Compositor.prototype.getContext)
- description and source-code
```javascript
function getContext(selector) {
    if (this._contexts[selector])
        return this._contexts[selector];
}
```
- example usage
```shell
...
 * @param  {Array} commands remaining message queue received, used to
 * shift single messages
 *
 * @return {undefined} undefined
 */
Compositor.prototype.giveSizeFor = function giveSizeFor(iterator, commands) {
    var selector = commands[iterator];
    var context = this.getContext(selector);
    if (context) {
        var size = context.getRootSize();
        this.sendResize(selector, size);
    } else {
        this.getOrSetContext(selector);
    }
};
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.getOrSetContext"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>getOrSetContext (selector)](#apidoc.element.famous.Compositor.prototype.getOrSetContext)
- description and source-code
```javascript
function getOrSetContext(selector) {
    if (this._contexts[selector]) {
        return this._contexts[selector];
    }
    else {
        var context = new Context(selector, this);
        this._contexts[selector] = context;
        return context;
    }
}
```
- example usage
```shell
...
* shift single messages from
*
* @return {undefined} undefined
*/
Compositor.prototype.handleWith = function handleWith (iterator, commands) {
   var path = commands[iterator];
   var pathArr = path.split('/');
   var context = this.getOrSetContext(pathArr.shift());
   return context.receive(path, commands, iterator);
};

/**
* Retrieves the top-level Context associated with the passed in document
* query selector. If no such Context exists, a new one will be instantiated.
*
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.getTime"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>getTime ()](#apidoc.element.famous.Compositor.prototype.getTime)
- description and source-code
```javascript
function getTime() {
    return this._time;
}
```
- example usage
```shell
...
    // Fall back to setInterval for now (very rare).
    rAF = null;
}
}

if (!rAF) {
var now = Date.now ? Date.now : function () {
    return new Date().getTime();
};

rAF = function(callback) {
    var currTime = now();
    var timeToCall = Math.max(0, 16 - (currTime - lastTime));
    var id = setTimeout(function () {
        callback(currTime + timeToCall);
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.giveSizeFor"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>giveSizeFor (iterator, commands)](#apidoc.element.famous.Compositor.prototype.giveSizeFor)
- description and source-code
```javascript
function giveSizeFor(iterator, commands) {
    var selector = commands[iterator];
    var context = this.getContext(selector);
    if (context) {
        var size = context.getRootSize();
        this.sendResize(selector, size);
    } else {
        this.getOrSetContext(selector);
    }
}
```
- example usage
```shell
...
        case Commands.TIME:
            this._time = commands[++localIterator];
            break;
        case Commands.WITH:
            localIterator = this.handleWith(++localIterator, commands);
            break;
        case Commands.NEED_SIZE_FOR:
            this.giveSizeFor(++localIterator, commands);
            break;
    }
    command = commands[++localIterator];
}

// TODO: Switch to associative arrays here...
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.handleWith"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>handleWith (iterator, commands)](#apidoc.element.famous.Compositor.prototype.handleWith)
- description and source-code
```javascript
function handleWith(iterator, commands) {
    var path = commands[iterator];
    var pathArr = path.split('/');
    var context = this.getOrSetContext(pathArr.shift());
    return context.receive(path, commands, iterator);
}
```
- example usage
```shell
...

var command;

while (messages.length > 0) {
    command = messages.shift();
    switch (command) {
        case Commands.WITH:
            this.handleWith(messages);
            break;
        case Commands.FRAME:
            this.handleFrame(messages);
            break;
        default:
            throw new Error('received unknown command: ' + command);
    }
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.onResize"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>onResize ()](#apidoc.element.famous.Compositor.prototype.onResize)
- description and source-code
```javascript
function onResize() {
    this._resized = true;
    for (var selector in this._contexts) {
        this._contexts[selector].updateSize();
    }
}
```
- example usage
```shell
...
this._inCommands = [];
this._time = null;

this._resized = false;

var _this = this;
window.addEventListener('resize', function() {
    _this.onResize();
});
}

Compositor.prototype.onResize = function onResize () {
this._resized = true;
for (var selector in this._contexts) {
    this._contexts[selector].updateSize();
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.receiveCommands"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>receiveCommands (commands)](#apidoc.element.famous.Compositor.prototype.receiveCommands)
- description and source-code
```javascript
function receiveCommands(commands) {
    var len = commands.length;
    for (var i = 0; i < len; i++) {
        this._inCommands.push(commands[i]);
    }

    for (var selector in this._contexts) {
        this._contexts[selector].checkInit();
    }
}
```
- example usage
```shell
...
                    console.error(
                        'Unknown ENGINE command "' + message[1] + '"'
                    );
                    break;
            }
        }
        else {
            _this._compositor.receiveCommands(message);
        }
    };
    this._thread.onerror = function (error) {
        console.error(error);
    };
}
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.sendEvent"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>sendEvent (path, ev, payload)](#apidoc.element.famous.Compositor.prototype.sendEvent)
- description and source-code
```javascript
function sendEvent(path, ev, payload) {
    this._outCommands.push(Commands.WITH, path, Commands.TRIGGER, ev, payload);
}
```
- example usage
```shell
...
        if (this._elements[path] && this._elements[path].subscribe[ev.type]) {
            this._lastEv = ev;

            var NormalizedEventConstructor = eventMap[ev.type][0];

            // Finally send the event to the Worker Thread through the
            // compositor.
            this._compositor.sendEvent(path, ev.type, new NormalizedEventConstructor(ev));

            break;
        }
    }
};
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.sendResize"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>sendResize (selector, size)](#apidoc.element.famous.Compositor.prototype.sendResize)
- description and source-code
```javascript
function sendResize(selector, size) {
    this.sendEvent(selector, 'CONTEXT_RESIZE', size);
}
```
- example usage
```shell
...
* @return {undefined} undefined
*/
Compositor.prototype.giveSizeFor = function giveSizeFor(iterator, commands) {
   var selector = commands[iterator];
   var context = this.getContext(selector);
   if (context) {
       var size = context.getRootSize();
       this.sendResize(selector, size);
   } else {
       this.getOrSetContext(selector);
   }
};

/**
* Flushes the queue of outgoing "out" commands.
...
```

#### <a name="apidoc.element.famous.Compositor.prototype.updateSize"></a>[function <span class="apidocSignatureSpan">famous.Compositor.prototype.</span>updateSize ()](#apidoc.element.famous.Compositor.prototype.updateSize)
- description and source-code
```javascript
function updateSize() {
    for (var selector in this._contexts) {
        this._contexts[selector].updateSize();
    }
}
```
- example usage
```shell
...
       _this.onResize();
   });
}

Compositor.prototype.onResize = function onResize () {
   this._resized = true;
   for (var selector in this._contexts) {
       this._contexts[selector].updateSize();
   }
};

/**
* Retrieves the time being used by the internal clock managed by
* 'FamousEngine'.
*
...
```



# <a name="apidoc.module.famous.Context"></a>[module famous.Context](#apidoc.module.famous.Context)

#### <a name="apidoc.element.famous.Context.Context"></a>[function <span class="apidocSignatureSpan">famous.</span>Context (selector, compositor)](#apidoc.element.famous.Context.Context)
- description and source-code
```javascript
function Context(selector, compositor) {
    this._compositor = compositor;
    this._rootEl = document.querySelector(selector);
    this._selector = selector;

    if (this._rootEl === null) {
        throw new Error(
            'Failed to create Context: ' +
            'No matches for "' + selector + '" found.'
        );
    }

    this._selector = selector;

    // Initializes the DOMRenderer.
    // Every Context has at least a DOMRenderer for now.
    this._initDOMRenderer();

    // WebGLRenderer will be instantiated when needed.
    this._webGLRenderer = null;
    this._domRenderer = new DOMRenderer(this._domRendererRootEl, selector, compositor);
    this._canvasEl = null;

    // State holders

    this._renderState = {
        projectionType: Camera.ORTHOGRAPHIC_PROJECTION,
        perspectiveTransform: new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]),
        viewTransform: new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]),
        viewDirty: false,
        perspectiveDirty: false
    };

    this._size = [];

    this._meshTransform = new Float32Array(16);
    this._meshSize = [0, 0, 0];

    this._initDOM = false;

    this._commandCallbacks = [];
    this.initCommandCallbacks();

    this.updateSize();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Context.prototype"></a>[module famous.Context.prototype](#apidoc.module.famous.Context.prototype)

#### <a name="apidoc.element.famous.Context.prototype._initDOMRenderer"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>_initDOMRenderer ()](#apidoc.element.famous.Context.prototype._initDOMRenderer)
- description and source-code
```javascript
function _initDOMRenderer() {
    this._domRendererRootEl = document.createElement('div');
    this._rootEl.appendChild(this._domRendererRootEl);
    this._domRendererRootEl.style.visibility = 'hidden';

    this._domRenderer = new DOMRenderer(
        this._domRendererRootEl,
        this._selector,
        this._compositor
    );
}
```
- example usage
```shell
...
    );
}

this._selector = selector;

// Initializes the DOMRenderer.
// Every Context has at least a DOMRenderer for now.
this._initDOMRenderer();

// WebGLRenderer will be instantiated when needed.
this._webGLRenderer = null;
this._domRenderer = new DOMRenderer(this._domRendererRootEl, selector, compositor);
this._canvasEl = null;

// State holders
...
```

#### <a name="apidoc.element.famous.Context.prototype._initWebGLRenderer"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>_initWebGLRenderer ()](#apidoc.element.famous.Context.prototype._initWebGLRenderer)
- description and source-code
```javascript
function _initWebGLRenderer() {
    this._webGLRendererRootEl = document.createElement('canvas');
    this._rootEl.appendChild(this._webGLRendererRootEl);

    this._webGLRenderer = new WebGLRenderer(
        this._webGLRendererRootEl,
        this._compositor
    );

    // Don't read offset width and height.
    this._webGLRenderer.updateSize(this._size);
}
```
- example usage
```shell
...
function unsubscribe (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.unsubscribe(commands[++iterator]);
return iterator;
}

function glSetDrawOptions (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setMeshOptions(path, commands[++iterator]);
return iterator;
}

function glAmbientLight (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setAmbientLightColor(
...
```

#### <a name="apidoc.element.famous.Context.prototype.checkInit"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>checkInit ()](#apidoc.element.famous.Context.prototype.checkInit)
- description and source-code
```javascript
function checkInit() {
    if (this._initDOM) {
        this._domRendererRootEl.style.visibility = 'visible';
        this._initDOM = false;
    }
}
```
- example usage
```shell
...
Compositor.prototype.receiveCommands = function receiveCommands(commands) {
   var len = commands.length;
   for (var i = 0; i < len; i++) {
       this._inCommands.push(commands[i]);
   }

   for (var selector in this._contexts) {
       this._contexts[selector].checkInit();
   }
};

/**
* Internal helper method used by 'drawCommands'.
*
* @method
...
```

#### <a name="apidoc.element.famous.Context.prototype.draw"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>draw ()](#apidoc.element.famous.Context.prototype.draw)
- description and source-code
```javascript
function draw() {
    this._domRenderer.draw(this._renderState);
    if (this._webGLRenderer) this._webGLRenderer.draw(this._renderState);

    if (this._renderState.perspectiveDirty) this._renderState.perspectiveDirty = false;
    if (this._renderState.viewDirty) this._renderState.viewDirty = false;
}
```
- example usage
```shell
...
*/
DOMElement.prototype.onMount = function onMount(node, id) {
   this._node = node;
   this._id = id;
   this._UIEvents = node.getUIEvents().slice(0);
   TransformSystem.makeBreakPointAt(node.getLocation());
   this.onSizeModeChange.apply(this, node.getSizeMode());
   this.draw();
   this.setAttribute('data-fa-path', node.getLocation());
};

/**
* Method to be invoked by the Node as soon as the node is being dismounted
* either directly or by dismounting one of its ancestors.
*
...
```

#### <a name="apidoc.element.famous.Context.prototype.getDOMRenderer"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>getDOMRenderer ()](#apidoc.element.famous.Context.prototype.getDOMRenderer)
- description and source-code
```javascript
function getDOMRenderer() {
    return this._domRenderer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Context.prototype.getRootSize"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>getRootSize ()](#apidoc.element.famous.Context.prototype.getRootSize)
- description and source-code
```javascript
function getRootSize() {
    return [
        this._rootEl.offsetWidth,
        this._rootEl.offsetHeight
    ];
}
```
- example usage
```shell
...
 *
 * @return {undefined} undefined
 */
Compositor.prototype.giveSizeFor = function giveSizeFor(iterator, commands) {
    var selector = commands[iterator];
    var context = this.getContext(selector);
    if (context) {
        var size = context.getRootSize();
        this.sendResize(selector, size);
    } else {
        this.getOrSetContext(selector);
    }
};

/**
...
```

#### <a name="apidoc.element.famous.Context.prototype.getWebGLRenderer"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>getWebGLRenderer ()](#apidoc.element.famous.Context.prototype.getWebGLRenderer)
- description and source-code
```javascript
function getWebGLRenderer() {
    return this._webGLRenderer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Context.prototype.initCommandCallbacks"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>initCommandCallbacks ()](#apidoc.element.famous.Context.prototype.initCommandCallbacks)
- description and source-code
```javascript
function initCommandCallbacks() {
    this._commandCallbacks[Commands.INIT_DOM] = initDOM;
    this._commandCallbacks[Commands.DOM_RENDER_SIZE] = domRenderSize;
    this._commandCallbacks[Commands.CHANGE_TRANSFORM] = changeTransform;
    this._commandCallbacks[Commands.CHANGE_SIZE] = changeSize;
    this._commandCallbacks[Commands.CHANGE_PROPERTY] = changeProperty;
    this._commandCallbacks[Commands.CHANGE_CONTENT] = changeContent;
    this._commandCallbacks[Commands.CHANGE_ATTRIBUTE] = changeAttribute;
    this._commandCallbacks[Commands.ADD_CLASS] = addClass;
    this._commandCallbacks[Commands.REMOVE_CLASS] = removeClass;
    this._commandCallbacks[Commands.SUBSCRIBE] = subscribe;
    this._commandCallbacks[Commands.UNSUBSCRIBE] = unsubscribe;
    this._commandCallbacks[Commands.GL_SET_DRAW_OPTIONS] = glSetDrawOptions;
    this._commandCallbacks[Commands.GL_AMBIENT_LIGHT] = glAmbientLight;
    this._commandCallbacks[Commands.GL_LIGHT_POSITION] = glLightPosition;
    this._commandCallbacks[Commands.GL_LIGHT_COLOR] = glLightColor;
    this._commandCallbacks[Commands.MATERIAL_INPUT] = materialInput;
    this._commandCallbacks[Commands.GL_SET_GEOMETRY] = glSetGeometry;
    this._commandCallbacks[Commands.GL_UNIFORMS] = glUniforms;
    this._commandCallbacks[Commands.GL_BUFFER_DATA] = glBufferData;
    this._commandCallbacks[Commands.GL_CUTOUT_STATE] = glCutoutState;
    this._commandCallbacks[Commands.GL_MESH_VISIBILITY] = glMeshVisibility;
    this._commandCallbacks[Commands.GL_REMOVE_MESH] = glRemoveMesh;
    this._commandCallbacks[Commands.PINHOLE_PROJECTION] = pinholeProjection;
    this._commandCallbacks[Commands.ORTHOGRAPHIC_PROJECTION] = orthographicProjection;
    this._commandCallbacks[Commands.CHANGE_VIEW_TRANSFORM] = changeViewTransform;
    this._commandCallbacks[Commands.PREVENT_DEFAULT] = preventDefault;
    this._commandCallbacks[Commands.ALLOW_DEFAULT] = allowDefault;
    this._commandCallbacks[Commands.READY] = ready;
}
```
- example usage
```shell
...

   this._meshTransform = new Float32Array(16);
   this._meshSize = [0, 0, 0];

   this._initDOM = false;

   this._commandCallbacks = [];
   this.initCommandCallbacks();

   this.updateSize();
}

/**
* Queries DOMRenderer size and updates canvas size. Relays size information to
* WebGLRenderer.
...
```

#### <a name="apidoc.element.famous.Context.prototype.receive"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>receive (path, commands, iterator)](#apidoc.element.famous.Context.prototype.receive)
- description and source-code
```javascript
function receive(path, commands, iterator) {
    var localIterator = iterator;

    var command = commands[++localIterator];

    this._domRenderer.loadPath(path);

    while (command != null) {
        if (command === Commands.WITH || command === Commands.TIME) return localIterator - 1;
        else localIterator = this._commandCallbacks[command](this, path, commands, localIterator) + 1;
        command = commands[localIterator];
    }

    return localIterator;
}
```
- example usage
```shell
...
*
* @return {undefined} undefined
*/
Compositor.prototype.handleWith = function handleWith (iterator, commands) {
   var path = commands[iterator];
   var pathArr = path.split('/');
   var context = this.getOrSetContext(pathArr.shift());
   return context.receive(path, commands, iterator);
};

/**
* Retrieves the top-level Context associated with the passed in document
* query selector. If no such Context exists, a new one will be instantiated.
*
* @method
...
```

#### <a name="apidoc.element.famous.Context.prototype.updateSize"></a>[function <span class="apidocSignatureSpan">famous.Context.prototype.</span>updateSize ()](#apidoc.element.famous.Context.prototype.updateSize)
- description and source-code
```javascript
updateSize = function () {
    var width = this._rootEl.offsetWidth;
    var height = this._rootEl.offsetHeight;

    this._size[0] = width;
    this._size[1] = height;
    this._size[2] = (width > height) ? width : height;

    this._compositor.sendResize(this._selector, this._size);
    if (this._webGLRenderer) this._webGLRenderer.updateSize(this._size);

    return this;
}
```
- example usage
```shell
...
       _this.onResize();
   });
}

Compositor.prototype.onResize = function onResize () {
   this._resized = true;
   for (var selector in this._contexts) {
       this._contexts[selector].updateSize();
   }
};

/**
* Retrieves the time being used by the internal clock managed by
* 'FamousEngine'.
*
...
```



# <a name="apidoc.module.famous.Curves"></a>[module famous.Curves](#apidoc.module.famous.Curves)

#### <a name="apidoc.element.famous.Curves.easeIn"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>easeIn (t)](#apidoc.element.famous.Curves.easeIn)
- description and source-code
```javascript
easeIn = function (t) {
    return t*t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.easeInOut"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>easeInOut (t)](#apidoc.element.famous.Curves.easeInOut)
- description and source-code
```javascript
easeInOut = function (t) {
    if (t <= 0.5) return 2*t*t;
    else return -2*t*t + 4*t - 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.easeOut"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>easeOut (t)](#apidoc.element.famous.Curves.easeOut)
- description and source-code
```javascript
easeOut = function (t) {
    return t*(2-t);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.easeOutBounce"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>easeOutBounce (t)](#apidoc.element.famous.Curves.easeOutBounce)
- description and source-code
```javascript
easeOutBounce = function (t) {
    return t*(3 - 2*t);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.flat"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>flat ()](#apidoc.element.famous.Curves.flat)
- description and source-code
```javascript
flat = function () {
    return 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inBack"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inBack (t, s)](#apidoc.element.famous.Curves.inBack)
- description and source-code
```javascript
inBack = function (t, s) {
    if (s === undefined) s = 1.70158;
    return t*t*((s+1)*t - s);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inBounce"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inBounce (t)](#apidoc.element.famous.Curves.inBounce)
- description and source-code
```javascript
inBounce = function (t) {
    return 1.0 - Curves.outBounce(1.0-t);
}
```
- example usage
```shell
...
        }
        else {
            return (7.5625*(t-=(2.625/2.75))*t + .984375);
        }
    },

    inOutBounce: function(t) {
        if (t < .5) return Curves.inBounce(t*2) * .5;
        return Curves.outBounce(t*2-1.0) * .5 + .5;
    },

    flat: function() {
        return 0;
    }
};
...
```

#### <a name="apidoc.element.famous.Curves.inCirc"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inCirc (t)](#apidoc.element.famous.Curves.inCirc)
- description and source-code
```javascript
inCirc = function (t) {
    return -(Math.sqrt(1 - t*t) - 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inCubic"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inCubic (t)](#apidoc.element.famous.Curves.inCubic)
- description and source-code
```javascript
inCubic = function (t) {
    return t*t*t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inElastic"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inElastic (t)](#apidoc.element.famous.Curves.inElastic)
- description and source-code
```javascript
inElastic = function (t) {
    var s=1.70158;var p=0;var a=1.0;
    if (t===0) return 0.0;  if (t===1) return 1.0;  if (!p) p=.3;
    s = p/(2*Math.PI) * Math.asin(1.0/a);
    return -(a*Math.pow(2,10*(t-=1)) * Math.sin((t-s)*(2*Math.PI)/ p));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inExpo"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inExpo (t)](#apidoc.element.famous.Curves.inExpo)
- description and source-code
```javascript
inExpo = function (t) {
    return (t===0) ? 0.0 : Math.pow(2, 10 * (t - 1));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutBack"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutBack (t, s)](#apidoc.element.famous.Curves.inOutBack)
- description and source-code
```javascript
inOutBack = function (t, s) {
    if (s === undefined) s = 1.70158;
    if ((t/=.5) < 1) return .5*(t*t*(((s*=(1.525))+1)*t - s));
    return .5*((t-=2)*t*(((s*=(1.525))+1)*t + s) + 2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutBounce"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutBounce (t)](#apidoc.element.famous.Curves.inOutBounce)
- description and source-code
```javascript
inOutBounce = function (t) {
    if (t < .5) return Curves.inBounce(t*2) * .5;
    return Curves.outBounce(t*2-1.0) * .5 + .5;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutCirc"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutCirc (t)](#apidoc.element.famous.Curves.inOutCirc)
- description and source-code
```javascript
inOutCirc = function (t) {
    if ((t/=.5) < 1) return -.5 * (Math.sqrt(1 - t*t) - 1);
    return .5 * (Math.sqrt(1 - (t-=2)*t) + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutCubic"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutCubic (t)](#apidoc.element.famous.Curves.inOutCubic)
- description and source-code
```javascript
inOutCubic = function (t) {
    if ((t/=.5) < 1) return .5*t*t*t;
    return .5*((t-=2)*t*t + 2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutElastic"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutElastic (t)](#apidoc.element.famous.Curves.inOutElastic)
- description and source-code
```javascript
inOutElastic = function (t) {
    var s=1.70158;var p=0;var a=1.0;
    if (t===0) return 0.0;  if ((t/=.5)===2) return 1.0;  if (!p) p=(.3*1.5);
    s = p/(2*Math.PI) * Math.asin(1.0/a);
    if (t < 1) return -.5*(a*Math.pow(2,10*(t-=1)) * Math.sin((t-s)*(2*Math.PI)/p));
    return a*Math.pow(2,-10*(t-=1)) * Math.sin((t-s)*(2*Math.PI)/p)*.5 + 1.0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutExpo"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutExpo (t)](#apidoc.element.famous.Curves.inOutExpo)
- description and source-code
```javascript
inOutExpo = function (t) {
    if (t===0) return 0.0;
    if (t===1.0) return 1.0;
    if ((t/=.5) < 1) return .5 * Math.pow(2, 10 * (t - 1));
    return .5 * (-Math.pow(2, -10 * --t) + 2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutQuad"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutQuad (t)](#apidoc.element.famous.Curves.inOutQuad)
- description and source-code
```javascript
inOutQuad = function (t) {
    if ((t/=.5) < 1) return .5*t*t;
    return -.5*((--t)*(t-2) - 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutQuart"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutQuart (t)](#apidoc.element.famous.Curves.inOutQuart)
- description and source-code
```javascript
inOutQuart = function (t) {
    if ((t/=.5) < 1) return .5*t*t*t*t;
    return -.5 * ((t-=2)*t*t*t - 2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutQuint"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutQuint (t)](#apidoc.element.famous.Curves.inOutQuint)
- description and source-code
```javascript
inOutQuint = function (t) {
    if ((t/=.5) < 1) return .5*t*t*t*t*t;
    return .5*((t-=2)*t*t*t*t + 2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inOutSine"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inOutSine (t)](#apidoc.element.famous.Curves.inOutSine)
- description and source-code
```javascript
inOutSine = function (t) {
    return -.5*(Math.cos(Math.PI*t) - 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inQuad"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inQuad (t)](#apidoc.element.famous.Curves.inQuad)
- description and source-code
```javascript
inQuad = function (t) {
    return t*t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inQuart"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inQuart (t)](#apidoc.element.famous.Curves.inQuart)
- description and source-code
```javascript
inQuart = function (t) {
    return t*t*t*t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inQuint"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inQuint (t)](#apidoc.element.famous.Curves.inQuint)
- description and source-code
```javascript
inQuint = function (t) {
    return t*t*t*t*t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.inSine"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>inSine (t)](#apidoc.element.famous.Curves.inSine)
- description and source-code
```javascript
inSine = function (t) {
    return -1.0*Math.cos(t * (Math.PI/2)) + 1.0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.linear"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>linear (t)](#apidoc.element.famous.Curves.linear)
- description and source-code
```javascript
linear = function (t) {
    return t;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outBack"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outBack (t, s)](#apidoc.element.famous.Curves.outBack)
- description and source-code
```javascript
outBack = function (t, s) {
    if (s === undefined) s = 1.70158;
    return ((--t)*t*((s+1)*t + s) + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outBounce"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outBounce (t)](#apidoc.element.famous.Curves.outBounce)
- description and source-code
```javascript
outBounce = function (t) {
    if (t < (1/2.75)) {
        return (7.5625*t*t);
    }
    else if (t < (2/2.75)) {
        return (7.5625*(t-=(1.5/2.75))*t + .75);
    }
    else if (t < (2.5/2.75)) {
        return (7.5625*(t-=(2.25/2.75))*t + .9375);
    }
    else {
        return (7.5625*(t-=(2.625/2.75))*t + .984375);
    }
}
```
- example usage
```shell
...
inOutBack: function(t, s) {
    if (s === undefined) s = 1.70158;
    if ((t/=.5) < 1) return .5*(t*t*(((s*=(1.525))+1)*t - s));
    return .5*((t-=2)*t*(((s*=(1.525))+1)*t + s) + 2);
},

inBounce: function(t) {
    return 1.0 - Curves.outBounce(1.0-t);
},

outBounce: function(t) {
    if (t < (1/2.75)) {
        return (7.5625*t*t);
    }
    else if (t < (2/2.75)) {
...
```

#### <a name="apidoc.element.famous.Curves.outCirc"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outCirc (t)](#apidoc.element.famous.Curves.outCirc)
- description and source-code
```javascript
outCirc = function (t) {
    return Math.sqrt(1 - (--t)*t);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outCubic"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outCubic (t)](#apidoc.element.famous.Curves.outCubic)
- description and source-code
```javascript
outCubic = function (t) {
    return ((--t)*t*t + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outElastic"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outElastic (t)](#apidoc.element.famous.Curves.outElastic)
- description and source-code
```javascript
outElastic = function (t) {
    var s=1.70158;var p=0;var a=1.0;
    if (t===0) return 0.0;  if (t===1) return 1.0;  if (!p) p=.3;
    s = p/(2*Math.PI) * Math.asin(1.0/a);
    return a*Math.pow(2,-10*t) * Math.sin((t-s)*(2*Math.PI)/p) + 1.0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outExpo"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outExpo (t)](#apidoc.element.famous.Curves.outExpo)
- description and source-code
```javascript
outExpo = function (t) {
    return (t===1.0) ? 1.0 : (-Math.pow(2, -10 * t) + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outQuad"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outQuad (t)](#apidoc.element.famous.Curves.outQuad)
- description and source-code
```javascript
outQuad = function (t) {
    return -(t-=1)*t+1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outQuart"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outQuart (t)](#apidoc.element.famous.Curves.outQuart)
- description and source-code
```javascript
outQuart = function (t) {
    return -((--t)*t*t*t - 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outQuint"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outQuint (t)](#apidoc.element.famous.Curves.outQuint)
- description and source-code
```javascript
outQuint = function (t) {
    return ((--t)*t*t*t*t + 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.outSine"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>outSine (t)](#apidoc.element.famous.Curves.outSine)
- description and source-code
```javascript
outSine = function (t) {
    return Math.sin(t * (Math.PI/2));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Curves.spring"></a>[function <span class="apidocSignatureSpan">famous.Curves.</span>spring (t)](#apidoc.element.famous.Curves.spring)
- description and source-code
```javascript
spring = function (t) {
    return (1 - t) * Math.sin(6 * Math.PI * t) + t;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.DOMElement"></a>[module famous.DOMElement](#apidoc.module.famous.DOMElement)

#### <a name="apidoc.element.famous.DOMElement.DOMElement"></a>[function <span class="apidocSignatureSpan">famous.</span>DOMElement (node, options)](#apidoc.element.famous.DOMElement.DOMElement)
- description and source-code
```javascript
function DOMElement(node, options) {
    if (!node) throw new Error('DOMElement must be instantiated on a node');

    this._changeQueue = [];

    this._requestingUpdate = false;
    this._renderSized = false;
    this._requestRenderSize = false;

    this._UIEvents = node.getUIEvents().slice(0);
    this._classes = ['famous-dom-element'];
    this._requestingEventListeners = [];
    this._styles = {};

    this._attributes = {};
    this._content = '';

    this._tagName = options && options.tagName ? options.tagName : 'div';
    this._renderSize = [0, 0, 0];

    this._node = node;

    if (node) node.addComponent(this);

    this._callbacks = new CallbackStore();

    this.setProperty('display', node.isShown() ? 'block' : 'none');
    this.onOpacityChange(node.getOpacity());

    if (!options) return;

    var i;
    var key;

    if (options.classes)
        for (i = 0; i < options.classes.length; i++)
            this.addClass(options.classes[i]);

    if (options.attributes)
        for (key in options.attributes)
            this.setAttribute(key, options.attributes[key]);

    if (options.properties)
        for (key in options.properties)
            this.setProperty(key, options.properties[key]);

    if (options.id) this.setId(options.id);
    if (options.content) this.setContent(options.content);
    if (options.cutout === false) this.setCutoutState(options.cutout);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.DOMElement.prototype"></a>[module famous.DOMElement.prototype](#apidoc.module.famous.DOMElement.prototype)

#### <a name="apidoc.element.famous.DOMElement.prototype._requestUpdate"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>_requestUpdate ()](#apidoc.element.famous.DOMElement.prototype._requestUpdate)
- description and source-code
```javascript
function _requestUpdate() {
    if (!this._requestingUpdate && this._id) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }
}
```
- example usage
```shell
...
* @return {Node} this
*/
Node.prototype.requestUpdate = function requestUpdate (requester) {
   if (this._inUpdate || !this.isMounted())
       return this.requestUpdateOnNextTick(requester);
   if (this._updateQueue.indexOf(requester) === -1) {
       this._updateQueue.push(requester);
       if (!this._requestingUpdate) this._requestUpdate();
   }
   return this;
};

/**
* Schedules an update on the next tick. Similarily to
* {@link Node#requestUpdate}, 'requestUpdateOnNextTick' schedules the node's
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype._subscribe"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>_subscribe (uiEvent)](#apidoc.element.famous.DOMElement.prototype._subscribe)
- description and source-code
```javascript
function _subscribe(uiEvent) {
    if (this._initialized) {
        this._changeQueue.push(Commands.SUBSCRIBE, uiEvent);
    }

    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...
 *
 * @param {String} uiEvent uiEvent to be subscribed to (e.g. 'click')
 *
 * @return {undefined} undefined
 */
DOMElement.prototype.onAddUIEvent = function onAddUIEvent(uiEvent) {
    if (this._UIEvents.indexOf(uiEvent) === -1) {
        this._subscribe(uiEvent);
        this._UIEvents.push(uiEvent);
    }
    else if (this._inDraw) {
        this._subscribe(uiEvent);
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype._unsubscribe"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>_unsubscribe (UIEvent)](#apidoc.element.famous.DOMElement.prototype._unsubscribe)
- description and source-code
```javascript
function _unsubscribe(UIEvent) {
    if (this._initialized) {
        this._changeQueue.push(Commands.UNSUBSCRIBE, UIEvent);
    }

    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...
 * @param {String} UIEvent UIEvent to be removed (e.g. 'mousedown')
 *
 * @return {undefined} undefined
 */
DOMElement.prototype.onRemoveUIEvent = function onRemoveUIEvent(UIEvent) {
    var index = this._UIEvents.indexOf(UIEvent);
    if (index !== -1) {
        this._unsubscribe(UIEvent);
        this._UIEvents.splice(index, 1);
    }
    else if (this._inDraw) {
        this._unsubscribe(UIEvent);
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.addClass"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>addClass (value)](#apidoc.element.famous.DOMElement.prototype.addClass)
- description and source-code
```javascript
function addClass(value) {
    if (this._classes.indexOf(value) < 0) {
        if (this._initialized) this._changeQueue.push(Commands.ADD_CLASS, value);
        this._classes.push(value);
        if (!this._requestingUpdate) this._requestUpdate();
        if (this._renderSized) this._requestRenderSize = true;
        return this;
    }

    if (this._inDraw) {
        if (this._initialized) this._changeQueue.push(Commands.ADD_CLASS, value);
        if (!this._requestingUpdate) this._requestUpdate();
    }
    return this;
}
```
- example usage
```shell
...
if (!options) return;

var i;
var key;

if (options.classes)
    for (i = 0; i < options.classes.length; i++)
        this.addClass(options.classes[i]);

if (options.attributes)
    for (key in options.attributes)
        this.setAttribute(key, options.attributes[key]);

if (options.properties)
    for (key in options.properties)
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.allowDefault"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>allowDefault (uiEvent)](#apidoc.element.famous.DOMElement.prototype.allowDefault)
- description and source-code
```javascript
function allowDefault(uiEvent) {
    if (this._initialized) {
        this._changeQueue.push(Commands.ALLOW_DEFAULT, uiEvent);
    }

    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...
    if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
    context._domRenderer.preventDefault(commands[++iterator]);
    return iterator;
}

function allowDefault (context, path, commands, iterator) {
    if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
    context._domRenderer.allowDefault(commands[++iterator]);
    return iterator;
}

function ready (context, path, commands, iterator) {
    context._initDOM = true;
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.draw"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>draw ()](#apidoc.element.famous.DOMElement.prototype.draw)
- description and source-code
```javascript
function draw() {
    var key;
    var i;
    var len;

    this._inDraw = true;

    this.init();

    for (i = 0, len = this._classes.length ; i < len ; i++)
        this.addClass(this._classes[i]);

    if (this._content) this.setContent(this._content);

    for (key in this._styles)
        if (this._styles[key] != null)
            this.setProperty(key, this._styles[key]);

    for (key in this._attributes)
        if (this._attributes[key] != null)
            this.setAttribute(key, this._attributes[key]);

    for (i = 0, len = this._UIEvents.length ; i < len ; i++)
        this.onAddUIEvent(this._UIEvents[i]);

    this._inDraw = false;
}
```
- example usage
```shell
...
*/
DOMElement.prototype.onMount = function onMount(node, id) {
   this._node = node;
   this._id = id;
   this._UIEvents = node.getUIEvents().slice(0);
   TransformSystem.makeBreakPointAt(node.getLocation());
   this.onSizeModeChange.apply(this, node.getSizeMode());
   this.draw();
   this.setAttribute('data-fa-path', node.getLocation());
};

/**
* Method to be invoked by the Node as soon as the node is being dismounted
* either directly or by dismounting one of its ancestors.
*
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.getRenderSize"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>getRenderSize ()](#apidoc.element.famous.DOMElement.prototype.getRenderSize)
- description and source-code
```javascript
function getRenderSize() {
    return this._renderSize;
}
```
- example usage
```shell
...
 * @param {Node} node Node to potentially call onRenderSizeChange on
 * @param {Array} components a list of the nodes' components
 * @param {Size} size the size class for the Node
 *
 * @return {undefined} undefined
 */
function renderSizeChanged (node, components, size) {
var renderSize = size.getRenderSize();
var x = renderSize[0];
var y = renderSize[1];
var z = renderSize[2];
if (node.onRenderSizeChange) node.onRenderSizeChange(x, y, z);
for (var i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onRenderSizeChange)
        components[i].onRenderSizeChange(x, y, z);
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>getValue ()](#apidoc.element.famous.DOMElement.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return {
        classes: this._classes,
        styles: this._styles,
        attributes: this._attributes,
        content: this._content,
        id: this._attributes.id,
        tagName: this._tagName
    };
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.hasClass"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>hasClass (value)](#apidoc.element.famous.DOMElement.prototype.hasClass)
- description and source-code
```javascript
function hasClass(value) {
    return this._classes.indexOf(value) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMElement.prototype.init"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>init ()](#apidoc.element.famous.DOMElement.prototype.init)
- description and source-code
```javascript
function init() {
    this._changeQueue.push(Commands.INIT_DOM, this._tagName);
    this._initialized = true;
    this.onTransformChange(TransformSystem.get(this._node.getLocation()));
    var size = this._node.getSize();
    this.onSizeChange(size[0], size[1]);
    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...

If you have the Famous Engine included in your project, it is very easy to start getting content rendered to the screen.  Below
is a short example of how to get HTML content written to the screen.

'''js
var FamousEngine = require('famous/core/FamousEngine');
var DOMElement = require('famous/dom-renderables/DOMElement');

FamousEngine.init();
var scene = FamousEngine.createScene();

var node = scene.addChild();
var domEl = new DOMElement(node, {
content: 'Hello World',
properties: {
    fontFamily: 'Arial'
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.on"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>on (event, listener)](#apidoc.element.famous.DOMElement.prototype.on)
- description and source-code
```javascript
function on(event, listener) {
    return this._callbacks.on(event, listener);
}
```
- example usage
```shell
...
this.trackedGestures = {};

var i;
var len;

if (events) {
    for (i = 0, len = events.length; i < len; i++) {
        this.on(events[i], events[i].callback);
    }
}

node.addUIEvent('touchstart');
node.addUIEvent('mousedown');
node.addUIEvent('touchmove');
node.addUIEvent('mousemove');
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onAddUIEvent"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onAddUIEvent (uiEvent)](#apidoc.element.famous.DOMElement.prototype.onAddUIEvent)
- description and source-code
```javascript
function onAddUIEvent(uiEvent) {
    if (this._UIEvents.indexOf(uiEvent) === -1) {
        this._subscribe(uiEvent);
        this._UIEvents.push(uiEvent);
    }
    else if (this._inDraw) {
        this._subscribe(uiEvent);
    }
    return this;
}
```
- example usage
```shell
...
    var component;

    var added = UIEvents.indexOf(eventName) !== -1;
    if (!added) {
        UIEvents.push(eventName);
        for (var i = 0, len = components.length ; i < len ; i++) {
            component = components[i];
            if (component && component.onAddUIEvent) component.onAddUIEvent(eventName);
        }
    }

    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onDismount"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onDismount ()](#apidoc.element.famous.DOMElement.prototype.onDismount)
- description and source-code
```javascript
function onDismount() {
    this.setProperty('display', 'none');
    this.setAttribute('data-fa-path', '');
    this.setCutoutState(false);

    this.onUpdate();
    this._initialized = false;
}
```
- example usage
```shell
...
if (node.onHide) node.onHide();
for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onHide)
        components[i].onHide();
    }

    if (node.isMounted()) {
if (node.onDismount) node.onDismount(path);

for (i = 0, len = children.length ; i < len ; i++)
    if (children[i] && children[i].dismount) children[i].dismount();
    else if (children[i]) this.dismount(path + '/' + i);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onDismount)
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onHide"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onHide ()](#apidoc.element.famous.DOMElement.prototype.onHide)
- description and source-code
```javascript
function onHide() {
    this.setProperty('display', 'none');
}
```
- example usage
```shell
...
var children = node.getChildren();
var components = node.getComponents();
var i;
var len;

if (node.isShown()) {
    node._setShown(false);
    if (node.onHide) node.onHide();
    for (i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onHide)
            components[i].onHide();
}

if (node.isMounted()) {
    if (node.onDismount) node.onDismount(path);
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onMount"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onMount (node, id)](#apidoc.element.famous.DOMElement.prototype.onMount)
- description and source-code
```javascript
function onMount(node, id) {
    this._node = node;
    this._id = id;
    this._UIEvents = node.getUIEvents().slice(0);
    TransformSystem.makeBreakPointAt(node.getLocation());
    this.onSizeModeChange.apply(this, node.getSizeMode());
    this.draw();
    this.setAttribute('data-fa-path', node.getLocation());
}
```
- example usage
```shell
...
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onMount)
        components[i].onMount(node, i);

for (i = 0, len = children.length ; i < len ; i++)
    if (children[i] && children[i].mount) children[i].mount(path + '/' + i);
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onOpacityChange"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onOpacityChange (opacity)](#apidoc.element.famous.DOMElement.prototype.onOpacityChange)
- description and source-code
```javascript
function onOpacityChange(opacity) {
    return this.setProperty('opacity', opacity);
}
```
- example usage
```shell
...

       var i = 0;
       var list = this._components;
       var len = list.length;
       var item;
       for (; i < len ; i++) {
           item = list[i];
           if (item && item.onOpacityChange) item.onOpacityChange(val);
       }
   }
   return this;
};

/**
* Sets the size mode being used for determining the node's final width, height
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onReceive"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onReceive (event, payload)](#apidoc.element.famous.DOMElement.prototype.onReceive)
- description and source-code
```javascript
function onReceive(event, payload) {
    if (event === 'resize') {
        this._renderSize[0] = payload.val[0];
        this._renderSize[1] = payload.val[1];
        if (!this._requestingUpdate) this._requestUpdate();
    }
    this._callbacks.trigger(event, payload);
}
```
- example usage
```shell
...
   if (!node) return;

   this.addChildrenToQueue(node);
   var child;

   while ((child = this.breadthFirstNext()))
       if (child && child.onReceive)
           child.onReceive(event, payload);

};

/**
* dispatchUIevent takes a path, an event name, and a payload and dispatches them in
* a manner anologous to DOM bubbling. It first traverses down to the node specified at
* the path. That node receives the event first, and then every ancestor receives the event
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onRemoveUIEvent"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onRemoveUIEvent (UIEvent)](#apidoc.element.famous.DOMElement.prototype.onRemoveUIEvent)
- description and source-code
```javascript
function onRemoveUIEvent(UIEvent) {
    var index = this._UIEvents.indexOf(UIEvent);
    if (index !== -1) {
        this._unsubscribe(UIEvent);
        this._UIEvents.splice(index, 1);
    }
    else if (this._inDraw) {
        this._unsubscribe(UIEvent);
    }
    return this;
}
```
- example usage
```shell
...
   var component;

   var index = UIEvents.indexOf(eventName);
   if (index !== -1) {
       UIEvents.splice(index, 1);
       for (var i = 0, len = components.length ; i < len ; i++) {
           component = components[i];
           if (component && component.onRemoveUIEvent) component.onRemoveUIEvent(eventName);
       }
   }
};

/**
* Subscribes a node to a UI Event. All components on the node
* will have the opportunity to begin listening to that event
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onShow"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onShow ()](#apidoc.element.famous.DOMElement.prototype.onShow)
- description and source-code
```javascript
function onShow() {
    this.setProperty('display', 'block');
}
```
- example usage
```shell
...

        for (i = 0, len = children.length ; i < len ; i++)
            if (children[i] && children[i].mount) children[i].mount(path + '/' + i);
            else if (children[i]) this.mount(path + '/' + i, children[i]);
    }

    if (parent.isShown()) {
        if (node.onShow) node.onShow();
        for (i = 0, len = components.length ; i < len ; i++)
            if (components[i] && components[i].onShow)
                components[i].onShow();
    }
};

/**
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onSizeChange"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onSizeChange (x, y)](#apidoc.element.famous.DOMElement.prototype.onSizeChange)
- description and source-code
```javascript
function onSizeChange(x, y) {
    var sizeMode = this._node.getSizeMode();
    var sizedX = sizeMode[0] !== Size.RENDER;
    var sizedY = sizeMode[1] !== Size.RENDER;
    if (this._initialized)
        this._changeQueue.push(Commands.CHANGE_SIZE,
            sizedX ? x : sizedX,
            sizedY ? y : sizedY);

    if (!this._requestingUpdate) this._requestUpdate();
    return this;
}
```
- example usage
```shell
...
 * @return {undefined} undefined
 */
function sizeChanged (node, components, size) {
    var finalSize = size.get();
    var x = finalSize[0];
    var y = finalSize[1];
    var z = finalSize[2];
    if (node.onSizeChange) node.onSizeChange(x, y, z);
    for (var i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onSizeChange)
            components[i].onSizeChange(x, y, z);
    size.sizeChanged = false;
}

module.exports = new SizeSystem();
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onSizeModeChange"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onSizeModeChange (x, y, z)](#apidoc.element.famous.DOMElement.prototype.onSizeModeChange)
- description and source-code
```javascript
function onSizeModeChange(x, y, z) {
    if (x === Size.RENDER || y === Size.RENDER || z === Size.RENDER) {
        this._renderSized = true;
        this._requestRenderSize = true;
    }
    var size = this._node.getSize();
    this.onSizeChange(size[0], size[1]);
}
```
- example usage
```shell
...
 * @return {undefined} undefined
 */
function sizeModeChanged (node, components, size) {
    var sizeMode = size.getSizeMode();
    var x = sizeMode[0];
    var y = sizeMode[1];
    var z = sizeMode[2];
    if (node.onSizeModeChange) node.onSizeModeChange(x, y, z);
    for (var i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onSizeModeChange)
            components[i].onSizeModeChange(x, y, z);
    size.sizeModeChanged = false;
}

/**
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onTransformChange"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onTransformChange (transform)](#apidoc.element.famous.DOMElement.prototype.onTransformChange)
- description and source-code
```javascript
function onTransformChange(transform) {
    this._changeQueue.push(Commands.CHANGE_TRANSFORM);
    transform = transform.getLocalTransform();

    for (var i = 0, len = transform.length ; i < len ; i++)
        this._changeQueue.push(transform[i]);

    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...
* @param {Node} node the node on which to trigger a change event if necessary
* @param {Array} components the components on which to trigger a change event if necessary
* @param {Transform} transform the transform class that changed
*
* @return {undefined} undefined
*/
function transformChanged (node, components, transform) {
   if (node.onTransformChange) node.onTransformChange(transform);
   for (var i = 0, len = components.length ; i < len ; i++)
       if (components[i] && components[i].onTransformChange)
           components[i].onTransformChange(transform);
}

/**
* Private method to call when the local transform changes. Triggers 'onLocalTransformChange' methods
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>onUpdate ()](#apidoc.element.famous.DOMElement.prototype.onUpdate)
- description and source-code
```javascript
function onUpdate() {
    var node = this._node;
    var queue = this._changeQueue;
    var len = queue.length;

    if (len && node) {
        node.sendDrawCommand(Commands.WITH);
        node.sendDrawCommand(node.getLocation());

        while (len--) node.sendDrawCommand(queue.shift());
        if (this._requestRenderSize) {
            node.sendDrawCommand(Commands.DOM_RENDER_SIZE);
            node.sendDrawCommand(node.getLocation());
            this._requestRenderSize = false;
        }

    }

    this._requestingUpdate = false;
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.preventDefault"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>preventDefault (uiEvent)](#apidoc.element.famous.DOMElement.prototype.preventDefault)
- description and source-code
```javascript
function preventDefault(uiEvent) {
    if (this._initialized) {
        this._changeQueue.push(Commands.PREVENT_DEFAULT, uiEvent);
    }
    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...
   }

   if (!this._requestingUpdate) this._requestUpdate();
};

/**
* When running in a worker, the browser's default action for specific events
* can't be prevented on a case by case basis (via 'e.preventDefault()').
* Instead this function should be used to register an event to be prevented by
* default.
*
* @method
*
* @param  {String} uiEvent     UI Event (e.g. wheel) for which to prevent the
*                              browser's default action (e.g. form submission,
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.removeClass"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>removeClass (value)](#apidoc.element.famous.DOMElement.prototype.removeClass)
- description and source-code
```javascript
function removeClass(value) {
    var index = this._classes.indexOf(value);

    if (index < 0) return this;

    this._changeQueue.push(Commands.REMOVE_CLASS, value);

    this._classes.splice(index, 1);

    if (!this._requestingUpdate) this._requestUpdate();
    return this;
}
```
- example usage
```shell
...
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.addClass(commands[++iterator]);
return iterator;
}

function removeClass (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.removeClass(commands[++iterator]);
return iterator;
}

function subscribe (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.subscribe(commands[++iterator]);
return iterator;
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.setAttribute"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setAttribute (name, value)](#apidoc.element.famous.DOMElement.prototype.setAttribute)
- description and source-code
```javascript
function setAttribute(name, value) {
    if (this._attributes[name] !== value || this._inDraw) {
        this._attributes[name] = value;
        if (this._initialized) this._changeQueue.push(Commands.CHANGE_ATTRIBUTE, name, value);
        if (!this._requestUpdate) this._requestUpdate();
    }

    return this;
}
```
- example usage
```shell
...

if (options.classes)
    for (i = 0; i < options.classes.length; i++)
        this.addClass(options.classes[i]);

if (options.attributes)
    for (key in options.attributes)
        this.setAttribute(key, options.attributes[key]);

if (options.properties)
    for (key in options.properties)
        this.setProperty(key, options.properties[key]);

if (options.id) this.setId(options.id);
if (options.content) this.setContent(options.content);
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.setContent"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setContent (content)](#apidoc.element.famous.DOMElement.prototype.setContent)
- description and source-code
```javascript
function setContent(content) {
    if (this._content !== content || this._inDraw) {
        this._content = content;
        if (this._initialized) this._changeQueue.push(Commands.CHANGE_CONTENT, content);
        if (!this._requestingUpdate) this._requestUpdate();
        if (this._renderSized) this._requestRenderSize = true;
    }

    return this;
}
```
- example usage
```shell
...
           this.setAttribute(key, options.attributes[key]);

   if (options.properties)
       for (key in options.properties)
           this.setProperty(key, options.properties[key]);

   if (options.id) this.setId(options.id);
   if (options.content) this.setContent(options.content);
   if (options.cutout === false) this.setCutoutState(options.cutout);
}

/**
* Serializes the state of the DOMElement.
*
* @method
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.setCutoutState"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setCutoutState (usesCutout)](#apidoc.element.famous.DOMElement.prototype.setCutoutState)
- description and source-code
```javascript
function setCutoutState(usesCutout) {
    if (this._initialized)
        this._changeQueue.push(Commands.GL_CUTOUT_STATE, usesCutout);

    if (!this._requestingUpdate) this._requestUpdate();
    return this;
}
```
- example usage
```shell
...

   if (options.properties)
       for (key in options.properties)
           this.setProperty(key, options.properties[key]);

   if (options.id) this.setId(options.id);
   if (options.content) this.setContent(options.content);
   if (options.cutout === false) this.setCutoutState(options.cutout);
}

/**
* Serializes the state of the DOMElement.
*
* @method
*
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.setId"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setId (id)](#apidoc.element.famous.DOMElement.prototype.setId)
- description and source-code
```javascript
function setId(id) {
    this.setAttribute('id', id);
    return this;
}
```
- example usage
```shell
...
       for (key in options.attributes)
           this.setAttribute(key, options.attributes[key]);

   if (options.properties)
       for (key in options.properties)
           this.setProperty(key, options.properties[key]);

   if (options.id) this.setId(options.id);
   if (options.content) this.setContent(options.content);
   if (options.cutout === false) this.setCutoutState(options.cutout);
}

/**
* Serializes the state of the DOMElement.
*
...
```

#### <a name="apidoc.element.famous.DOMElement.prototype.setProperty"></a>[function <span class="apidocSignatureSpan">famous.DOMElement.prototype.</span>setProperty (name, value)](#apidoc.element.famous.DOMElement.prototype.setProperty)
- description and source-code
```javascript
function setProperty(name, value) {
    if (this._styles[name] !== value || this._inDraw) {
        this._styles[name] = value;
        if (this._initialized) this._changeQueue.push(Commands.CHANGE_PROPERTY, name, value);
        if (!this._requestingUpdate) this._requestUpdate();
        if (this._renderSized) this._requestRenderSize = true;
    }

    return this;
}
```
- example usage
```shell
...

this._node = node;

if (node) node.addComponent(this);

this._callbacks = new CallbackStore();

this.setProperty('display', node.isShown() ? 'block' : 'none');
this.onOpacityChange(node.getOpacity());

if (!options) return;

var i;
var key;
...
```



# <a name="apidoc.module.famous.DOMRenderer"></a>[module famous.DOMRenderer](#apidoc.module.famous.DOMRenderer)

#### <a name="apidoc.element.famous.DOMRenderer.DOMRenderer"></a>[function <span class="apidocSignatureSpan">famous.</span>DOMRenderer (element, selector, compositor)](#apidoc.element.famous.DOMRenderer.DOMRenderer)
- description and source-code
```javascript
function DOMRenderer(element, selector, compositor) {
    var _this = this;

    element.classList.add('famous-dom-renderer');

    TRANSFORM = TRANSFORM || vendorPrefix('transform');
    this._compositor = compositor; // a reference to the compositor

    this._target = null; // a register for holding the current
                         // element that the Renderer is operating
                         // upon

    this._parent = null; // a register for holding the parent
                         // of the target

    this._path = null; // a register for holding the path of the target
                       // this register must be set first, and then
                       // children, target, and parent are all looked
                       // up from that.

    this._children = []; // a register for holding the children of the
                         // current target.

     this._insertElCallbackStore = new CallbackStore();
     this._removeElCallbackStore = new CallbackStore();

    this._root = new ElementCache(element, selector); // the root
                                                      // of the dom tree that this
                                                      // renderer is responsible
                                                      // for

    this._boundTriggerEvent = function (ev) {
        return _this._triggerEvent(ev);
    };

    this._selector = selector;

    this._elements = {};

    this._elements[selector] = this._root;

    this.perspectiveTransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);
    this._VPtransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);

    this._lastEv = null;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.DOMRenderer.prototype"></a>[module famous.DOMRenderer.prototype](#apidoc.module.famous.DOMRenderer.prototype)

#### <a name="apidoc.element.famous.DOMRenderer.prototype._assertChildrenLoaded"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertChildrenLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertChildrenLoaded)
- description and source-code
```javascript
function _assertChildrenLoaded() {
    if (!this._children) throw new Error('children not loaded');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype._assertParentLoaded"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertParentLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertParentLoaded)
- description and source-code
```javascript
function _assertParentLoaded() {
    if (!this._parent) throw new Error('parent not loaded');
}
```
- example usage
```shell
...
 *
 * @return {undefined} undefined
 */
DOMRenderer.prototype.insertEl = function insertEl (tagName) {

this.findParent();

this._assertParentLoaded();

if (this._parent.void)
    throw new Error(
        this._parent.path + ' is a void element. ' +
        'Void elements are not allowed to have children.'
    );
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype._assertPathLoaded"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertPathLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertPathLoaded)
- description and source-code
```javascript
function _asserPathLoaded() {
    if (!this._path) throw new Error('path not loaded');
}
```
- example usage
```shell
...
 *
 * @method
 * @private
 *
 * @return {ElementCache} Parent element.
 */
DOMRenderer.prototype.findParent = function findParent () {
this._assertPathLoaded();

var path = this._path;
var parent;

while (!parent && path.length) {
    path = path.substring(0, path.lastIndexOf('/'));
    parent = this._elements[path];
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype._assertTargetLoaded"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_assertTargetLoaded ()](#apidoc.element.famous.DOMRenderer.prototype._assertTargetLoaded)
- description and source-code
```javascript
function _assertTargetLoaded() {
    if (!this._target) throw new Error('No target loaded');
}
```
- example usage
```shell
...
*
* @param {String} type DOM event type (e.g. click, mouseover).
* @param {Boolean} preventDefault Whether or not the default browser action should be prevented.
*
* @return {undefined} undefined
*/
DOMRenderer.prototype.subscribe = function subscribe(type) {
   this._assertTargetLoaded();
   this._listen(type);
   this._target.subscribe[type] = true;
};

/**
* Used to preventDefault if an event of the specified type is being emitted on
* the currently loaded target.
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype._listen"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_listen (type)](#apidoc.element.famous.DOMRenderer.prototype._listen)
- description and source-code
```javascript
function _listen(type) {
    this._assertTargetLoaded();

    if (
        !this._target.listeners[type] && !this._root.listeners[type]
    ) {
        // FIXME Add to content DIV if available
        var target = eventMap[type][1] ? this._root : this._target;
        target.listeners[type] = this._boundTriggerEvent;
        target.element.addEventListener(type, this._boundTriggerEvent);
    }
}
```
- example usage
```shell
...
* @param {String} type DOM event type (e.g. click, mouseover).
* @param {Boolean} preventDefault Whether or not the default browser action should be prevented.
*
* @return {undefined} undefined
*/
DOMRenderer.prototype.subscribe = function subscribe(type) {
   this._assertTargetLoaded();
   this._listen(type);
   this._target.subscribe[type] = true;
};

/**
* Used to preventDefault if an event of the specified type is being emitted on
* the currently loaded target.
*
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype._stringifyMatrix"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_stringifyMatrix (m)](#apidoc.element.famous.DOMRenderer.prototype._stringifyMatrix)
- description and source-code
```javascript
function _stringifyMatrix(m) {
    var r = 'matrix3d(';

    r += (m[0] < 0.000001 && m[0] > -0.000001) ? '0,' : m[0] + ',';
    r += (m[1] < 0.000001 && m[1] > -0.000001) ? '0,' : m[1] + ',';
    r += (m[2] < 0.000001 && m[2] > -0.000001) ? '0,' : m[2] + ',';
    r += (m[3] < 0.000001 && m[3] > -0.000001) ? '0,' : m[3] + ',';
    r += (m[4] < 0.000001 && m[4] > -0.000001) ? '0,' : m[4] + ',';
    r += (m[5] < 0.000001 && m[5] > -0.000001) ? '0,' : m[5] + ',';
    r += (m[6] < 0.000001 && m[6] > -0.000001) ? '0,' : m[6] + ',';
    r += (m[7] < 0.000001 && m[7] > -0.000001) ? '0,' : m[7] + ',';
    r += (m[8] < 0.000001 && m[8] > -0.000001) ? '0,' : m[8] + ',';
    r += (m[9] < 0.000001 && m[9] > -0.000001) ? '0,' : m[9] + ',';
    r += (m[10] < 0.000001 && m[10] > -0.000001) ? '0,' : m[10] + ',';
    r += (m[11] < 0.000001 && m[11] > -0.000001) ? '0,' : m[11] + ',';
    r += (m[12] < 0.000001 && m[12] > -0.000001) ? '0,' : m[12] + ',';
    r += (m[13] < 0.000001 && m[13] > -0.000001) ? '0,' : m[13] + ',';
    r += (m[14] < 0.000001 && m[14] > -0.000001) ? '0,' : m[14] + ',';

    r += m[15] + ')';
    return r;
}
```
- example usage
```shell
...
       this.perspectiveTransform[13] = renderState.perspectiveTransform[13];
       this.perspectiveTransform[14] = renderState.perspectiveTransform[14];
       this.perspectiveTransform[15] = renderState.perspectiveTransform[15];
   }

   if (renderState.viewDirty || renderState.perspectiveDirty) {
       math.multiply(this._VPtransform, this.perspectiveTransform, renderState.viewTransform);
       this._root.element.style[TRANSFORM] = this._stringifyMatrix(this._VPtransform);
   }
};


/**
* Internal helper function used for ensuring that a path is currently loaded.
*
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype._triggerEvent"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>_triggerEvent (ev)](#apidoc.element.famous.DOMRenderer.prototype._triggerEvent)
- description and source-code
```javascript
function _triggerEvent(ev) {
    if (this._lastEv === ev) return;

    // Use ev.path, which is an array of Elements (polyfilled if needed).
    var evPath = ev.path ? ev.path : _getPath(ev);
    // First element in the path is the element on which the event has actually
    // been emitted.
    for (var i = 0; i < evPath.length; i++) {
        // Skip nodes that don't have a dataset property or data-fa-path
        // attribute.
        if (!evPath[i].dataset) continue;
        var path = evPath[i].dataset.faPath;
        if (!path) continue;

        // Optionally preventDefault. This needs forther consideration and
        // should be optional. Eventually this should be a separate command/
        // method.
        if (this._elements[path].preventDefault[ev.type]) {
            ev.preventDefault();
        }

        // Stop further event propogation and path traversal as soon as the
        // first ElementCache subscribing for the emitted event has been found.
        if (this._elements[path] && this._elements[path].subscribe[ev.type]) {
            this._lastEv = ev;

            var NormalizedEventConstructor = eventMap[ev.type][0];

            // Finally send the event to the Worker Thread through the
            // compositor.
            this._compositor.sendEvent(path, ev.type, new NormalizedEventConstructor(ev));

            break;
        }
    }
}
```
- example usage
```shell
...

this._root = new ElementCache(element, selector); // the root
                                                  // of the dom tree that this
                                                  // renderer is responsible
                                                  // for

this._boundTriggerEvent = function (ev) {
    return _this._triggerEvent(ev);
};

this._selector = selector;

this._elements = {};

this._elements[selector] = this._root;
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.addClass"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>addClass (domClass)](#apidoc.element.famous.DOMRenderer.prototype.addClass)
- description and source-code
```javascript
function addClass(domClass) {
    this._assertTargetLoaded();
    this._target.element.classList.add(domClass);
}
```
- example usage
```shell
...
if (!options) return;

var i;
var key;

if (options.classes)
    for (i = 0; i < options.classes.length; i++)
        this.addClass(options.classes[i]);

if (options.attributes)
    for (key in options.attributes)
        this.setAttribute(key, options.attributes[key]);

if (options.properties)
    for (key in options.properties)
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.allowDefault"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>allowDefault (type)](#apidoc.element.famous.DOMRenderer.prototype.allowDefault)
- description and source-code
```javascript
function allowDefault(type) {
    this._assertTargetLoaded();
    this._listen(type);
    this._target.preventDefault[type] = false;
}
```
- example usage
```shell
...
    if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
    context._domRenderer.preventDefault(commands[++iterator]);
    return iterator;
}

function allowDefault (context, path, commands, iterator) {
    if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
    context._domRenderer.allowDefault(commands[++iterator]);
    return iterator;
}

function ready (context, path, commands, iterator) {
    context._initDOM = true;
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.draw"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>draw (renderState)](#apidoc.element.famous.DOMRenderer.prototype.draw)
- description and source-code
```javascript
function draw(renderState) {
    if (renderState.perspectiveDirty) {
        this.perspectiveDirty = true;

        this.perspectiveTransform[0] = renderState.perspectiveTransform[0];
        this.perspectiveTransform[1] = renderState.perspectiveTransform[1];
        this.perspectiveTransform[2] = renderState.perspectiveTransform[2];
        this.perspectiveTransform[3] = renderState.perspectiveTransform[3];

        this.perspectiveTransform[4] = renderState.perspectiveTransform[4];
        this.perspectiveTransform[5] = renderState.perspectiveTransform[5];
        this.perspectiveTransform[6] = renderState.perspectiveTransform[6];
        this.perspectiveTransform[7] = renderState.perspectiveTransform[7];

        this.perspectiveTransform[8] = renderState.perspectiveTransform[8];
        this.perspectiveTransform[9] = renderState.perspectiveTransform[9];
        this.perspectiveTransform[10] = renderState.perspectiveTransform[10];
        this.perspectiveTransform[11] = renderState.perspectiveTransform[11];

        this.perspectiveTransform[12] = renderState.perspectiveTransform[12];
        this.perspectiveTransform[13] = renderState.perspectiveTransform[13];
        this.perspectiveTransform[14] = renderState.perspectiveTransform[14];
        this.perspectiveTransform[15] = renderState.perspectiveTransform[15];
    }

    if (renderState.viewDirty || renderState.perspectiveDirty) {
        math.multiply(this._VPtransform, this.perspectiveTransform, renderState.viewTransform);
        this._root.element.style[TRANSFORM] = this._stringifyMatrix(this._VPtransform);
    }
}
```
- example usage
```shell
...
*/
DOMElement.prototype.onMount = function onMount(node, id) {
   this._node = node;
   this._id = id;
   this._UIEvents = node.getUIEvents().slice(0);
   TransformSystem.makeBreakPointAt(node.getLocation());
   this.onSizeModeChange.apply(this, node.getSizeMode());
   this.draw();
   this.setAttribute('data-fa-path', node.getLocation());
};

/**
* Method to be invoked by the Node as soon as the node is being dismounted
* either directly or by dismounting one of its ancestors.
*
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.findParent"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>findParent ()](#apidoc.element.famous.DOMRenderer.prototype.findParent)
- description and source-code
```javascript
function findParent() {
    this._assertPathLoaded();

    var path = this._path;
    var parent;

    while (!parent && path.length) {
        path = path.substring(0, path.lastIndexOf('/'));
        parent = this._elements[path];
    }

    this._parent = parent;
    return parent;
}
```
- example usage
```shell
...
 *
 * @param {String} tagName Tag name (capitalization will be normalized).
 *
 * @return {undefined} undefined
 */
DOMRenderer.prototype.insertEl = function insertEl (tagName) {

this.findParent();

this._assertParentLoaded();

if (this._parent.void)
    throw new Error(
        this._parent.path + ' is a void element. ' +
        'Void elements are not allowed to have children.'
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.findTarget"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>findTarget ()](#apidoc.element.famous.DOMRenderer.prototype.findTarget)
- description and source-code
```javascript
function findTarget() {
    this._target = this._elements[this._path];
    return this._target;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.getSizeOf"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>getSizeOf (path)](#apidoc.element.famous.DOMRenderer.prototype.getSizeOf)
- description and source-code
```javascript
function getSizeOf(path) {
    var element = this._elements[path];
    if (!element) return null;

    var res = {val: element.size};
    this._compositor.sendEvent(path, 'resize', res);
    return res;
}
```
- example usage
```shell
...

function initDOM (context, path, commands, iterator) {
context._domRenderer.insertEl(commands[++iterator]);
return iterator;
}

function domRenderSize (context, path, commands, iterator) {
context._domRenderer.getSizeOf(commands[++iterator]);
return iterator;
}

function changeTransform (context, path, commands, iterator) {
var temp = context._meshTransform;

temp[0] = commands[++iterator];
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.insertEl"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>insertEl (tagName)](#apidoc.element.famous.DOMRenderer.prototype.insertEl)
- description and source-code
```javascript
function insertEl(tagName) {

    this.findParent();

    this._assertParentLoaded();

    if (this._parent.void)
        throw new Error(
            this._parent.path + ' is a void element. ' +
            'Void elements are not allowed to have children.'
        );

    if (!this._target) this._target = new ElementCache(document.createElement(tagName), this._path);

    var el = this._target.element;
    var parent = this._parent.element;

    this.resolveChildren(el, parent);

    parent.appendChild(el);
    this._elements[this._path] = this._target;

    this._insertElCallbackStore.trigger(this._path, this._target);

}
```
- example usage
```shell
...

function ready (context, path, commands, iterator) {
    context._initDOM = true;
    return iterator;
}

function initDOM (context, path, commands, iterator) {
    context._domRenderer.insertEl(commands[++iterator]);
    return iterator;
}

function domRenderSize (context, path, commands, iterator) {
    context._domRenderer.getSizeOf(commands[++iterator]);
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.loadPath"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>loadPath (path)](#apidoc.element.famous.DOMRenderer.prototype.loadPath)
- description and source-code
```javascript
function loadPath(path) {
    this._path = path;
    this._target = this._elements[this._path];
    return this._path;
}
```
- example usage
```shell
...
 * @return {Number} iterator indicating progress through the command queue.
 */
Context.prototype.receive = function receive(path, commands, iterator) {
var localIterator = iterator;

var command = commands[++localIterator];

this._domRenderer.loadPath(path);

while (command != null) {
    if (command === Commands.WITH || command === Commands.TIME) return localIterator - 1;
    else localIterator = this._commandCallbacks[command](this, path, commands, localIterator) + 1;
    command = commands[localIterator];
}
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.offInsertEl"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>offInsertEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.offInsertEl)
- description and source-code
```javascript
function offInsertEl(path, callback) {
    this._insertElCallbackStore.off(path, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.offRemoveEl"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>offRemoveEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.offRemoveEl)
- description and source-code
```javascript
function offRemoveEl(path, callback) {
    this._removeElCallbackStore.off(path, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.onInsertEl"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>onInsertEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.onInsertEl)
- description and source-code
```javascript
function onInsertEl(path, callback) {
    this._insertElCallbackStore.on(path, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.onRemoveEl"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>onRemoveEl (path, callback)](#apidoc.element.famous.DOMRenderer.prototype.onRemoveEl)
- description and source-code
```javascript
function onRemoveEl(path, callback) {
    this._removeElCallbackStore.on(path, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.preventDefault"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>preventDefault (type)](#apidoc.element.famous.DOMRenderer.prototype.preventDefault)
- description and source-code
```javascript
function preventDefault(type) {
    this._assertTargetLoaded();
    this._listen(type);
    this._target.preventDefault[type] = true;
}
```
- example usage
```shell
...
   }

   if (!this._requestingUpdate) this._requestUpdate();
};

/**
* When running in a worker, the browser's default action for specific events
* can't be prevented on a case by case basis (via 'e.preventDefault()').
* Instead this function should be used to register an event to be prevented by
* default.
*
* @method
*
* @param  {String} uiEvent     UI Event (e.g. wheel) for which to prevent the
*                              browser's default action (e.g. form submission,
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.removeClass"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>removeClass (domClass)](#apidoc.element.famous.DOMRenderer.prototype.removeClass)
- description and source-code
```javascript
function removeClass(domClass) {
    this._assertTargetLoaded();
    this._target.element.classList.remove(domClass);
}
```
- example usage
```shell
...
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.addClass(commands[++iterator]);
return iterator;
}

function removeClass (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.removeClass(commands[++iterator]);
return iterator;
}

function subscribe (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.subscribe(commands[++iterator]);
return iterator;
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.resolveChildren"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>resolveChildren (element, parent)](#apidoc.element.famous.DOMRenderer.prototype.resolveChildren)
- description and source-code
```javascript
function resolveChildren(element, parent) {
    var i = 0;
    var childNode;
    var path = this._path;
    var childPath;

    while ((childNode = parent.childNodes[i])) {
        if (!childNode.dataset) {
            i++;
            continue;
        }
        childPath = childNode.dataset.faPath;
        if (!childPath) {
            i++;
            continue;
        }
        if (PathUtils.isDescendentOf(childPath, path)) element.appendChild(childNode);
        else i++;
    }
}
```
- example usage
```shell
...
        );

    if (!this._target) this._target = new ElementCache(document.createElement(tagName), this._path);

    var el = this._target.element;
    var parent = this._parent.element;

    this.resolveChildren(el, parent);

    parent.appendChild(el);
    this._elements[this._path] = this._target;

    this._insertElCallbackStore.trigger(this._path, this._target);

};
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setAttribute"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setAttribute (name, value)](#apidoc.element.famous.DOMRenderer.prototype.setAttribute)
- description and source-code
```javascript
function setAttribute(name, value) {
    this._assertTargetLoaded();
    this._target.element.setAttribute(name, value);
}
```
- example usage
```shell
...

if (options.classes)
    for (i = 0; i < options.classes.length; i++)
        this.addClass(options.classes[i]);

if (options.attributes)
    for (key in options.attributes)
        this.setAttribute(key, options.attributes[key]);

if (options.properties)
    for (key in options.properties)
        this.setProperty(key, options.properties[key]);

if (options.id) this.setId(options.id);
if (options.content) this.setContent(options.content);
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setContent"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setContent (content)](#apidoc.element.famous.DOMRenderer.prototype.setContent)
- description and source-code
```javascript
function setContent(content) {
    this._assertTargetLoaded();

    if (this._target.formElement) {
        this._target.element.value = content;
    }
    else {
        if (!this._target.content) {
            this._target.content = document.createElement('div');
            this._target.content.classList.add('famous-dom-element-content');
            this._target.element.insertBefore(
                this._target.content,
                this._target.element.firstChild
            );
        }
        this._target.content.innerHTML = content;
    }


    this.setSize(
        this._target.explicitWidth ? false : this._target.size[0],
        this._target.explicitHeight ? false : this._target.size[1]
    );
}
```
- example usage
```shell
...
           this.setAttribute(key, options.attributes[key]);

   if (options.properties)
       for (key in options.properties)
           this.setProperty(key, options.properties[key]);

   if (options.id) this.setId(options.id);
   if (options.content) this.setContent(options.content);
   if (options.cutout === false) this.setCutoutState(options.cutout);
}

/**
* Serializes the state of the DOMElement.
*
* @method
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setHeight"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setHeight (height)](#apidoc.element.famous.DOMRenderer.prototype.setHeight)
- description and source-code
```javascript
function setHeight(height) {
    this._assertTargetLoaded();

    var contentWrapper = this._target.content;

    if (height === false) {
        this._target.explicitHeight = true;
        if (contentWrapper) contentWrapper.style.height = '';
        height = contentWrapper ? contentWrapper.offsetHeight : 0;
        this._target.element.style.height = height + 'px';
    }
    else {
        this._target.explicitHeight = false;
        if (contentWrapper) contentWrapper.style.height = height + 'px';
        this._target.element.style.height = height + 'px';
    }

    this._target.size[1] = height;
}
```
- example usage
```shell
...
*
* @return {undefined} undefined
*/
DOMRenderer.prototype.setSize = function setSize (width, height) {
   this._assertTargetLoaded();

   this.setWidth(width);
   this.setHeight(height);
};

/**
* Sets the width of the currently loaded ElementCache.
*
* @method
*
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setMatrix"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setMatrix (transform)](#apidoc.element.famous.DOMRenderer.prototype.setMatrix)
- description and source-code
```javascript
function setMatrix(transform) {
    this._assertTargetLoaded();
    this._target.element.style[TRANSFORM] = this._stringifyMatrix(transform);
}
```
- example usage
```shell
...
    temp[10] = commands[++iterator];
    temp[11] = commands[++iterator];
    temp[12] = commands[++iterator];
    temp[13] = commands[++iterator];
    temp[14] = commands[++iterator];
    temp[15] = commands[++iterator];

    context._domRenderer.setMatrix(temp);

    if (context._webGLRenderer)
        context._webGLRenderer.setCutoutUniform(path, 'u_transform', temp);

    return iterator;
}
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setProperty"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setProperty (name, value)](#apidoc.element.famous.DOMRenderer.prototype.setProperty)
- description and source-code
```javascript
function setProperty(name, value) {
    this._assertTargetLoaded();
    this._target.element.style[name] = value;
}
```
- example usage
```shell
...

this._node = node;

if (node) node.addComponent(this);

this._callbacks = new CallbackStore();

this.setProperty('display', node.isShown() ? 'block' : 'none');
this.onOpacityChange(node.getOpacity());

if (!options) return;

var i;
var key;
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setSize"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setSize (width, height)](#apidoc.element.famous.DOMRenderer.prototype.setSize)
- description and source-code
```javascript
function setSize(width, height) {
    this._assertTargetLoaded();

    this.setWidth(width);
    this.setHeight(height);
}
```
- example usage
```shell
...
                this._target.element.firstChild
            );
        }
        this._target.content.innerHTML = content;
    }


    this.setSize(
        this._target.explicitWidth ? false : this._target.size[0],
        this._target.explicitHeight ? false : this._target.size[1]
    );
};


/**
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.setWidth"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>setWidth (width)](#apidoc.element.famous.DOMRenderer.prototype.setWidth)
- description and source-code
```javascript
function setWidth(width) {
    this._assertTargetLoaded();

    var contentWrapper = this._target.content;

    if (width === false) {
        this._target.explicitWidth = true;
        if (contentWrapper) contentWrapper.style.width = '';
        width = contentWrapper ? contentWrapper.offsetWidth : 0;
        this._target.element.style.width = width + 'px';
    }
    else {
        this._target.explicitWidth = false;
        if (contentWrapper) contentWrapper.style.width = width + 'px';
        this._target.element.style.width = width + 'px';
    }

    this._target.size[0] = width;
}
```
- example usage
```shell
...
* @param {Number|false} height  Height to be set.
*
* @return {undefined} undefined
*/
DOMRenderer.prototype.setSize = function setSize (width, height) {
   this._assertTargetLoaded();

   this.setWidth(width);
   this.setHeight(height);
};

/**
* Sets the width of the currently loaded ElementCache.
*
* @method
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.subscribe"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>subscribe (type)](#apidoc.element.famous.DOMRenderer.prototype.subscribe)
- description and source-code
```javascript
function subscribe(type) {
    this._assertTargetLoaded();
    this._listen(type);
    this._target.subscribe[type] = true;
}
```
- example usage
```shell
...
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.removeClass(commands[++iterator]);
return iterator;
}

function subscribe (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.subscribe(commands[++iterator]);
return iterator;
}

function unsubscribe (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.unsubscribe(commands[++iterator]);
return iterator;
...
```

#### <a name="apidoc.element.famous.DOMRenderer.prototype.unsubscribe"></a>[function <span class="apidocSignatureSpan">famous.DOMRenderer.prototype.</span>unsubscribe (type)](#apidoc.element.famous.DOMRenderer.prototype.unsubscribe)
- description and source-code
```javascript
function unsubscribe(type) {
    this._assertTargetLoaded();
    this._target.subscribe[type] = false;
}
```
- example usage
```shell
...
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.subscribe(commands[++iterator]);
return iterator;
}

function unsubscribe (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.unsubscribe(commands[++iterator]);
return iterator;
}

function glSetDrawOptions (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setMeshOptions(path, commands[++iterator]);
return iterator;
...
```



# <a name="apidoc.module.famous.DynamicGeometry"></a>[module famous.DynamicGeometry](#apidoc.module.famous.DynamicGeometry)

#### <a name="apidoc.element.famous.DynamicGeometry.DynamicGeometry"></a>[function <span class="apidocSignatureSpan">famous.</span>DynamicGeometry (options)](#apidoc.element.famous.DynamicGeometry.DynamicGeometry)
- description and source-code
```javascript
function DynamicGeometry(options) {
    Geometry.call(this, options);

    this.spec.dynamic = true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.DynamicGeometry.prototype"></a>[module famous.DynamicGeometry.prototype](#apidoc.module.famous.DynamicGeometry.prototype)

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.fromGeometry"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>fromGeometry (geometry)](#apidoc.element.famous.DynamicGeometry.prototype.fromGeometry)
- description and source-code
```javascript
function fromGeometry(geometry) {
    var len = geometry.spec.bufferNames.length;
    for (var i = 0; i < len; i++) {
        this.setVertexBuffer(
            geometry.spec.bufferNames[i],
            geometry.spec.bufferValues[i],
            geometry.spec.bufferSpacings[i]
        );
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.getLength"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getLength ()](#apidoc.element.famous.DynamicGeometry.prototype.getLength)
- description and source-code
```javascript
function getLength() {
    return this.getVertexPositions().length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.getNormals"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getNormals ()](#apidoc.element.famous.DynamicGeometry.prototype.getNormals)
- description and source-code
```javascript
getNormals = function () {
    return this.getVertexBuffer('a_normals');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.getTextureCoords"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getTextureCoords ()](#apidoc.element.famous.DynamicGeometry.prototype.getTextureCoords)
- description and source-code
```javascript
getTextureCoords = function () {
    return this.getVertexBuffer('a_texCoord');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.getVertexBuffer"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getVertexBuffer (bufferName)](#apidoc.element.famous.DynamicGeometry.prototype.getVertexBuffer)
- description and source-code
```javascript
function getVertexBuffer(bufferName) {
    if (! bufferName) throw 'getVertexBuffer requires a name';

    var idx = this.spec.bufferNames.indexOf(bufferName);

    if (~idx) return this.spec.bufferValues[idx];
    else      throw 'buffer does not exist';
}
```
- example usage
```shell
...
/**
* Returns the 'pos' vertex buffer of the geometry.
*
* @method
* @return {Array} Vertex buffer.
*/
DynamicGeometry.prototype.getVertexPositions = function () {
   return this.getVertexBuffer('a_pos');
};

/**
* Returns the 'normal' vertex buffer of the geometry.
* @method
* @return {Array} Vertex Buffer.
*/
...
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.getVertexPositions"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>getVertexPositions ()](#apidoc.element.famous.DynamicGeometry.prototype.getVertexPositions)
- description and source-code
```javascript
getVertexPositions = function () {
    return this.getVertexBuffer('a_pos');
}
```
- example usage
```shell
...
*
* @class DynamicGeometry
* @constructor
*
* @return {Object} flattened length of the vertex positions attribute in the geometry.
*/
DynamicGeometry.prototype.getLength = function getLength() {
   return this.getVertexPositions().length;
};

/**
* Gets the buffer object based on buffer name. Throws error
* if bufferName is not provided.
*
* @method
...
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.setDrawType"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setDrawType (value)](#apidoc.element.famous.DynamicGeometry.prototype.setDrawType)
- description and source-code
```javascript
setDrawType = function (value) {
    this.spec.type = value.toUpperCase();
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.setIndices"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setIndices (value)](#apidoc.element.famous.DynamicGeometry.prototype.setIndices)
- description and source-code
```javascript
setIndices = function (value) {
    return this.setVertexBuffer('indices', value, 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.setNormals"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setNormals (value)](#apidoc.element.famous.DynamicGeometry.prototype.setNormals)
- description and source-code
```javascript
setNormals = function (value) {
    return this.setVertexBuffer('a_normals', value, 3);
}
```
- example usage
```shell
...

    if (value.geometry != null) this.setGeometry(value.geometry);
    if (value.color != null) this.setBaseColor(value.color);
    if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
    if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
    if (value.flatShading != null) this.setFlatShading(value.flatShading);

    if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
    if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
    if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
    if (value.expressions.positionOffset != null) this.setPositionOffset(value.expressions.positionOffset);

    this._inDraw = false;
};
...
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.setTextureCoords"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setTextureCoords (value)](#apidoc.element.famous.DynamicGeometry.prototype.setTextureCoords)
- description and source-code
```javascript
setTextureCoords = function (value) {
    return this.setVertexBuffer('a_texCoord', value, 2);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.setVertexBuffer"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setVertexBuffer (bufferName, value, size)](#apidoc.element.famous.DynamicGeometry.prototype.setVertexBuffer)
- description and source-code
```javascript
function setVertexBuffer(bufferName, value, size) {
    var idx = this.spec.bufferNames.indexOf(bufferName);

    if (idx === -1) {
        idx = this.spec.bufferNames.push(bufferName) - 1;
    }

    this.spec.bufferValues[idx] = value || [];
    this.spec.bufferSpacings[idx] = size || this.DEFAULT_BUFFER_SIZE;

    if (this.spec.invalidations.indexOf(idx) === -1) {
        this.spec.invalidations.push(idx);
    }

    return this;
}
```
- example usage
```shell
...
 *
 * @param  {Object} geometry    Geometry instance to copy buffers from.
 * @return {Object}             current geometry.
 */
DynamicGeometry.prototype.fromGeometry = function fromGeometry(geometry) {
    var len = geometry.spec.bufferNames.length;
    for (var i = 0; i < len; i++) {
        this.setVertexBuffer(
            geometry.spec.bufferNames[i],
            geometry.spec.bufferValues[i],
            geometry.spec.bufferSpacings[i]
        );
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.DynamicGeometry.prototype.setVertexPositions"></a>[function <span class="apidocSignatureSpan">famous.DynamicGeometry.prototype.</span>setVertexPositions (value)](#apidoc.element.famous.DynamicGeometry.prototype.setVertexPositions)
- description and source-code
```javascript
setVertexPositions = function (value) {
    return this.setVertexBuffer('a_pos', value, 3);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Geometry"></a>[module famous.Geometry](#apidoc.module.famous.Geometry)

#### <a name="apidoc.element.famous.Geometry.ConvexHull"></a>[function <span class="apidocSignatureSpan">famous.Geometry.</span>ConvexHull (vertices, iterations)](#apidoc.element.famous.Geometry.ConvexHull)
- description and source-code
```javascript
function ConvexHull(vertices, iterations) {
    iterations = iterations || 1e3;
    var hull = _computeConvexHull(vertices, iterations);

    var i, len;

    var indices = [];
    for (i = 0, len = hull.features.length; i < len; i++) {
        var f = hull.features[i];
        if (f) indices.push(f.vertexIndices);
    }

    var polyhedralProperties = _computePolyhedralProperties(hull.vertices, indices);
    var centroid = polyhedralProperties.centroid;

    var worldVertices = [];
    for (i = 0, len = hull.vertices.length; i < len; i++) {
        worldVertices.push(Vec3.subtract(hull.vertices[i].vertex, centroid, new Vec3()));
    }

    var normals = [];
    for (i = 0, len = worldVertices.length; i < len; i++) {
        normals.push(Vec3.normalize(worldVertices[i], new Vec3()));
    }

    var graph = {};
    var _neighborMatrix = {};
    for (i = 0; i < indices.length; i++) {
        var a = indices[i][0];
        var b = indices[i][1];
        var c = indices[i][2];

        _neighborMatrix[a] = _neighborMatrix[a] || {};
        _neighborMatrix[b] = _neighborMatrix[b] || {};
        _neighborMatrix[c] = _neighborMatrix[c] || {};

        graph[a] = graph[a] || [];
        graph[b] = graph[b] || [];
        graph[c] = graph[c] || [];

        if (!_neighborMatrix[a][b]) {
            _neighborMatrix[a][b] = 1;
            graph[a].push(b);
        }
        if (!_neighborMatrix[a][c]) {
            _neighborMatrix[a][c] = 1;
            graph[a].push(c);
        }
        if (!_neighborMatrix[b][a]) {
            _neighborMatrix[b][a] = 1;
            graph[b].push(a);
        }
        if (!_neighborMatrix[b][c]) {
            _neighborMatrix[b][c] = 1;
            graph[b].push(c);
        }
        if (!_neighborMatrix[c][a]) {
            _neighborMatrix[c][a] = 1;
            graph[c].push(a);
        }
        if (!_neighborMatrix[c][b]) {
            _neighborMatrix[c][b] = 1;
            graph[c].push(b);
        }
    }

    this.indices = indices;
    this.vertices = worldVertices;
    this.normals = normals;
    this.polyhedralProperties = polyhedralProperties;
    this.graph = graph;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Geometry.DynamicGeometry"></a>[function <span class="apidocSignatureSpan">famous.Geometry.</span>DynamicGeometry ()](#apidoc.element.famous.Geometry.DynamicGeometry)
- description and source-code
```javascript
function DynamicGeometry() {
    this.vertices = [];
    this.numVertices = 0;
    this.features = [];
    this.numFeatures = 0;
    this.lastVertexIndex = 0;

    this._IDPool = {
        vertices: [],
        features: []
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.GeometryHelper"></a>[module famous.GeometryHelper](#apidoc.module.famous.GeometryHelper)

#### <a name="apidoc.element.famous.GeometryHelper.addBackfaceTriangles"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>addBackfaceTriangles (vertices, indices)](#apidoc.element.famous.GeometryHelper.addBackfaceTriangles)
- description and source-code
```javascript
function addBackfaceTriangles(vertices, indices) {
    var nFaces = indices.length / 3;

    var maxIndex = 0;
    var i = indices.length;
    while (i--) if (indices[i] > maxIndex) maxIndex = indices[i];

    maxIndex++;

    for (i = 0; i < nFaces; i++) {
        var indexOne = indices[i * 3],
            indexTwo = indices[i * 3 + 1],
            indexThree = indices[i * 3 + 2];

        indices.push(indexOne + maxIndex, indexThree + maxIndex, indexTwo + maxIndex);
    }

    // Iterating instead of .slice() here to avoid max call stack issue.

    var nVerts = vertices.length;
    for (i = 0; i < nVerts; i++) {
        vertices.push(vertices[i]);
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.computeNormals"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>computeNormals (vertices, indices, out)](#apidoc.element.famous.GeometryHelper.computeNormals)
- description and source-code
```javascript
function computeNormals(vertices, indices, out) {
    var normals = out || [];
    var indexOne;
    var indexTwo;
    var indexThree;
    var normal;
    var j;
    var len = indices.length / 3;
    var i;
    var x;
    var y;
    var z;
    var length;

    for (i = 0; i < len; i++) {
        indexTwo = indices[i*3 + 0] * 3;
        indexOne = indices[i*3 + 1] * 3;
        indexThree = indices[i*3 + 2] * 3;

        outputs[0].set(vertices[indexOne], vertices[indexOne + 1], vertices[indexOne + 2]);
        outputs[1].set(vertices[indexTwo], vertices[indexTwo + 1], vertices[indexTwo + 2]);
        outputs[2].set(vertices[indexThree], vertices[indexThree + 1], vertices[indexThree + 2]);

        normal = outputs[2].subtract(outputs[0]).cross(outputs[1].subtract(outputs[0])).normalize();

        normals[indexOne + 0] = (normals[indexOne + 0] || 0) + normal.x;
        normals[indexOne + 1] = (normals[indexOne + 1] || 0) + normal.y;
        normals[indexOne + 2] = (normals[indexOne + 2] || 0) + normal.z;

        normals[indexTwo + 0] = (normals[indexTwo + 0] || 0) + normal.x;
        normals[indexTwo + 1] = (normals[indexTwo + 1] || 0) + normal.y;
        normals[indexTwo + 2] = (normals[indexTwo + 2] || 0) + normal.z;

        normals[indexThree + 0] = (normals[indexThree + 0] || 0) + normal.x;
        normals[indexThree + 1] = (normals[indexThree + 1] || 0) + normal.y;
        normals[indexThree + 2] = (normals[indexThree + 2] || 0) + normal.z;
    }

    for (i = 0; i < normals.length; i += 3) {
        x = normals[i];
        y = normals[i+1];
        z = normals[i+2];
        length = Math.sqrt(x * x + y * y + z * z);
        for(j = 0; j< 3; j++) {
            normals[i+j] /= length;
        }
    }

    return normals;
}
```
- example usage
```shell
...
if (options.normalize) {
    cached.vertices = GeometryHelper.normalizeVertices(
        cached.vertices
    );
}

if (options.computeNormals) {
    cached.normals = GeometryHelper.computeNormals(
        cached.vertices,
        cached.indices
    );
}

return {
    vertices: cached.vertices,
...
```

#### <a name="apidoc.element.famous.GeometryHelper.generateParametric"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>generateParametric (detailX, detailY, func, wrap)](#apidoc.element.famous.GeometryHelper.generateParametric)
- description and source-code
```javascript
function generateParametric(detailX, detailY, func, wrap) {
    var vertices = [];
    var i;
    var theta;
    var phi;
    var j;

    // We can wrap around slightly more than once for uv coordinates to look correct.

    var offset = (Math.PI / (detailX - 1));
    var Xrange = wrap ? Math.PI + offset : Math.PI;

    var out = [];

    for (i = 0; i < detailX + 1; i++) {
        theta = (i === 0 ? 0.0001 : i) * Math.PI / detailX;
        for (j = 0; j < detailY; j++) {
            phi = j * 2.0 * Xrange / detailY;
            func(theta, phi, out);
            vertices.push(out[0], out[1], out[2]);
        }
    }

    var indices = [],
        v = 0,
        next;
    for (i = 0; i < detailX; i++) {
        for (j = 0; j < detailY; j++) {
            next = (j + 1) % detailY;
            indices.push(v + j, v + j + detailY, v + next);
            indices.push(v + next, v + j + detailY, v + next + detailY);
        }
        v += detailY;
    }

    return {
        vertices: vertices,
        indices: indices
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.getAltitude"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getAltitude (v)](#apidoc.element.famous.GeometryHelper.getAltitude)
- description and source-code
```javascript
function altitude(v) {
    return Math.atan2(-v[1], Math.sqrt((v[0] * v[0]) + (v[2] * v[2])));
}
```
- example usage
```shell
...
        vertices[i * 3 + 1],
        vertices[i * 3 + 2]
    )
    .normalize()
    .toArray();

    var azimuth = this.getAzimuth(vertex);
    var altitude = this.getAltitude(vertex);

    uv[0] = azimuth * 0.5 / Math.PI + 0.5;
    uv[1] = altitude / Math.PI + 0.5;

    out.push.apply(out, uv);
}
...
```

#### <a name="apidoc.element.famous.GeometryHelper.getAzimuth"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getAzimuth (v)](#apidoc.element.famous.GeometryHelper.getAzimuth)
- description and source-code
```javascript
function azimuth(v) {
    return Math.atan2(v[2], -v[0]);
}
```
- example usage
```shell
...
        vertices[i * 3],
        vertices[i * 3 + 1],
        vertices[i * 3 + 2]
    )
    .normalize()
    .toArray();

    var azimuth = this.getAzimuth(vertex);
    var altitude = this.getAltitude(vertex);

    uv[0] = azimuth * 0.5 / Math.PI + 0.5;
    uv[1] = altitude / Math.PI + 0.5;

    out.push.apply(out, uv);
}
...
```

#### <a name="apidoc.element.famous.GeometryHelper.getSpheroidNormals"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getSpheroidNormals (vertices, out)](#apidoc.element.famous.GeometryHelper.getSpheroidNormals)
- description and source-code
```javascript
function getSpheroidNormals(vertices, out) {
    out = out || [];
    var length = vertices.length / 3;
    var normalized;

    for (var i = 0; i < length; i++) {
        normalized = new Vec3(
            vertices[i * 3 + 0],
            vertices[i * 3 + 1],
            vertices[i * 3 + 2]
        ).normalize().toArray();

        out[i * 3 + 0] = normalized[0];
        out[i * 3 + 1] = normalized[1];
        out[i * 3 + 2] = normalized[2];
    }

    return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.getSpheroidUV"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getSpheroidUV (vertices, out)](#apidoc.element.famous.GeometryHelper.getSpheroidUV)
- description and source-code
```javascript
function getSpheroidUV(vertices, out) {
    out = out || [];
    var length = vertices.length / 3;
    var vertex;

    var uv = [];

    for(var i = 0; i < length; i++) {
        vertex = outputs[0].set(
            vertices[i * 3],
            vertices[i * 3 + 1],
            vertices[i * 3 + 2]
        )
        .normalize()
        .toArray();

        var azimuth = this.getAzimuth(vertex);
        var altitude = this.getAltitude(vertex);

        uv[0] = azimuth * 0.5 / Math.PI + 0.5;
        uv[1] = altitude / Math.PI + 0.5;

        out.push.apply(out, uv);
    }

    return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.getUniqueFaces"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>getUniqueFaces (vertices, indices)](#apidoc.element.famous.GeometryHelper.getUniqueFaces)
- description and source-code
```javascript
function getUniqueFaces(vertices, indices) {
    var triangleIndex = indices.length / 3,
        registered = [],
        index;

    while (triangleIndex--) {
        for (var i = 0; i < 3; i++) {

            index = indices[triangleIndex * 3 + i];

            if (registered[index]) {
                vertices.push(vertices[index * 3], vertices[index * 3 + 1], vertices[index * 3 + 2]);
                indices[triangleIndex * 3 + i] = vertices.length / 3 - 1;
            }
            else {
                registered[index] = true;
            }
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.normalizeAll"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>normalizeAll (vertices, out)](#apidoc.element.famous.GeometryHelper.normalizeAll)
- description and source-code
```javascript
function normalizeAll(vertices, out) {
    out = out || [];
    var len = vertices.length / 3;

    for (var i = 0; i < len; i++) {
        Array.prototype.push.apply(out, new Vec3(vertices[i * 3], vertices[i * 3 + 1], vertices[i * 3 + 2]).normalize().toArray());
    }

    return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.normalizeVertices"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>normalizeVertices (vertices, out)](#apidoc.element.famous.GeometryHelper.normalizeVertices)
- description and source-code
```javascript
function normalizeVertices(vertices, out) {
    out = out || [];
    var len = vertices.length / 3;
    var vectors = [];
    var minX;
    var maxX;
    var minY;
    var maxY;
    var minZ;
    var maxZ;
    var v;
    var i;

    for (i = 0; i < len; i++) {
        v = vectors[i] = new Vec3(
            vertices[i * 3],
            vertices[i * 3 + 1],
            vertices[i * 3 + 2]
        );

        if (minX == null || v.x < minX) minX = v.x;
        if (maxX == null || v.x > maxX) maxX = v.x;

        if (minY == null || v.y < minY) minY = v.y;
        if (maxY == null || v.y > maxY) maxY = v.y;

        if (minZ == null || v.z < minZ) minZ = v.z;
        if (maxZ == null || v.z > maxZ) maxZ = v.z;
    }

    var translation = new Vec3(
        getTranslationFactor(maxX, minX),
        getTranslationFactor(maxY, minY),
        getTranslationFactor(maxZ, minZ)
    );

    var scale = Math.min(
        getScaleFactor(maxX + translation.x, minX + translation.x),
        getScaleFactor(maxY + translation.y, minY + translation.y),
        getScaleFactor(maxZ + translation.z, minZ + translation.z)
    );

    for (i = 0; i < vectors.length; i++) {
        out.push.apply(out, vectors[i].add(translation).scale(scale).toArray());
    }

    return out;
}
```
- example usage
```shell
...

cached.vertices = flatten(cached.vertices);
cached.normals = flatten(cached.normals);
cached.texCoords = flatten(cached.texCoords);
cached.indices = flatten(cached.indices);

if (options.normalize) {
    cached.vertices = GeometryHelper.normalizeVertices(
        cached.vertices
    );
}

if (options.computeNormals) {
    cached.normals = GeometryHelper.computeNormals(
        cached.vertices,
...
```

#### <a name="apidoc.element.famous.GeometryHelper.subdivide"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>subdivide (indices, vertices, textureCoords)](#apidoc.element.famous.GeometryHelper.subdivide)
- description and source-code
```javascript
function subdivide(indices, vertices, textureCoords) {
    var triangleIndex = indices.length / 3;
    var face;
    var i;
    var j;
    var k;
    var pos;
    var tex;

    while (triangleIndex--) {
        face = indices.slice(triangleIndex * 3, triangleIndex * 3 + 3);

        pos = face.map(function(vertIndex) {
            return new Vec3(vertices[vertIndex * 3], vertices[vertIndex * 3 + 1], vertices[vertIndex * 3 + 2]);
        });
        vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[1], outputs[0]), 0.5, outputs[1]).toArray());
        vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[1], pos[2], outputs[0]), 0.5, outputs[1]).toArray());
        vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[2], outputs[0]), 0.5, outputs[1]).toArray());

        if (textureCoords) {
            tex = face.map(function(vertIndex) {
                return new Vec2(textureCoords[vertIndex * 2], textureCoords[vertIndex * 2 + 1]);
            });
            textureCoords.push.apply(textureCoords, Vec2.scale(Vec2.add(tex[0], tex[1], outputs[3]), 0.5, outputs[4]).toArray());
            textureCoords.push.apply(textureCoords, Vec2.scale(Vec2.add(tex[1], tex[2], outputs[3]), 0.5, outputs[4]).toArray());
            textureCoords.push.apply(textureCoords, Vec2.scale(Vec2.add(tex[0], tex[2], outputs[3]), 0.5, outputs[4]).toArray());
        }

        i = vertices.length - 3;
        j = i + 1;
        k = i + 2;

        indices.push(i, j, k);
        indices.push(face[0], i, k);
        indices.push(i, face[1], j);
        indices[triangleIndex] = k;
        indices[triangleIndex + 1] = j;
        indices[triangleIndex + 2] = face[2];
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.subdivideSpheroid"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>subdivideSpheroid (vertices, indices)](#apidoc.element.famous.GeometryHelper.subdivideSpheroid)
- description and source-code
```javascript
function subdivideSpheroid(vertices, indices) {
    var triangleIndex = indices.length / 3,
        abc,
        face,
        i, j, k;

    while (triangleIndex--) {
        face = indices.slice(triangleIndex * 3, triangleIndex * 3 + 3);
        abc = face.map(function(vertIndex) {
            return new Vec3(vertices[vertIndex * 3], vertices[vertIndex * 3 + 1], vertices[vertIndex * 3 + 2]);
        });

        vertices.push.apply(vertices, Vec3.normalize(Vec3.add(abc[0], abc[1], outputs[0]), outputs[1]).toArray());
        vertices.push.apply(vertices, Vec3.normalize(Vec3.add(abc[1], abc[2], outputs[0]), outputs[1]).toArray());
        vertices.push.apply(vertices, Vec3.normalize(Vec3.add(abc[0], abc[2], outputs[0]), outputs[1]).toArray());

        i = vertices.length / 3 - 3;
        j = i + 1;
        k = i + 2;

        indices.push(i, j, k);
        indices.push(face[0], i, k);
        indices.push(i, face[1], j);
        indices[triangleIndex * 3] = k;
        indices[triangleIndex * 3 + 1] = j;
        indices[triangleIndex * 3 + 2] = face[2];
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.GeometryHelper.trianglesToLines"></a>[function <span class="apidocSignatureSpan">famous.GeometryHelper.</span>trianglesToLines (indices, out)](#apidoc.element.famous.GeometryHelper.trianglesToLines)
- description and source-code
```javascript
function triangleToLines(indices, out) {
    var numVectors = indices.length / 3;
    out = out || [];
    var i;

    for (i = 0; i < numVectors; i++) {
        out.push(indices[i * 3 + 0], indices[i * 3 + 1]);
        out.push(indices[i * 3 + 1], indices[i * 3 + 2]);
        out.push(indices[i * 3 + 2], indices[i * 3 + 0]);
    }

    return out;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.GestureHandler"></a>[module famous.GestureHandler](#apidoc.module.famous.GestureHandler)

#### <a name="apidoc.element.famous.GestureHandler.GestureHandler"></a>[function <span class="apidocSignatureSpan">famous.</span>GestureHandler (node, events)](#apidoc.element.famous.GestureHandler.GestureHandler)
- description and source-code
```javascript
function GestureHandler(node, events) {
    this.node = node;
    this.id = node.addComponent(this);

    this._events = new CallbackStore();

    this.last1 = new Vec2();
    this.last2 = new Vec2();

    this.delta1 = new Vec2();
    this.delta2 = new Vec2();

    this.velocity1 = new Vec2();
    this.velocity2 = new Vec2();

    this.dist = 0;
    this.diff12 = new Vec2();

    this.center = new Vec2();
    this.centerDelta = new Vec2();
    this.centerVelocity = new Vec2();

    this.pointer1 = {
        position: this.last1,
        delta: this.delta1,
        velocity: this.velocity1
    };

    this.pointer2 = {
        position: this.last2,
        delta: this.delta2,
        velocity: this.velocity2
    };

    this.event = {
        status: null,
        time: 0,
        pointers: [],
        center: this.center,
        centerDelta: this.centerDelta,
        centerVelocity: this.centerVelocity,
        points: 0,
        current: 0
    };

    this.trackedPointerIDs = [-1, -1];
    this.timeOfPointer = 0;
    this.multiTap = 0;

    this.mice = [];

    this.gestures = [];
    this.options = {};
    this.trackedGestures = {};

    var i;
    var len;

    if (events) {
        for (i = 0, len = events.length; i < len; i++) {
            this.on(events[i], events[i].callback);
        }
    }

    node.addUIEvent('touchstart');
    node.addUIEvent('mousedown');
    node.addUIEvent('touchmove');
    node.addUIEvent('mousemove');
    node.addUIEvent('touchend');
    node.addUIEvent('mouseup');
    node.addUIEvent('mouseleave');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.GestureHandler.prototype"></a>[module famous.GestureHandler.prototype](#apidoc.module.famous.GestureHandler.prototype)

#### <a name="apidoc.element.famous.GestureHandler.prototype.on"></a>[function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>on (ev, cb)](#apidoc.element.famous.GestureHandler.prototype.on)
- description and source-code
```javascript
function on(ev, cb) {
    var gesture = ev.event || ev;
    if (gestures[gesture]) {
        this.trackedGestures[gesture] = true;
        this.gestures.push(gesture);
        if (ev.event) this.options[gesture] = ev;
        this._events.on(gesture, cb);
    }
}
```
- example usage
```shell
...
this.trackedGestures = {};

var i;
var len;

if (events) {
    for (i = 0, len = events.length; i < len; i++) {
        this.on(events[i], events[i].callback);
    }
}

node.addUIEvent('touchstart');
node.addUIEvent('mousedown');
node.addUIEvent('touchmove');
node.addUIEvent('mousemove');
...
```

#### <a name="apidoc.element.famous.GestureHandler.prototype.onReceive"></a>[function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>onReceive (ev, payload)](#apidoc.element.famous.GestureHandler.prototype.onReceive)
- description and source-code
```javascript
function onReceive(ev, payload) {
    switch(ev) {
        case 'touchstart':
        case 'mousedown':
            _processPointerStart.call(this, payload);
            break;
        case 'touchmove':
        case 'mousemove':
            _processPointerMove.call(this, payload);
            break;
        case 'touchend':
        case 'mouseup':
            _processPointerEnd.call(this, payload);
            break;
        case 'mouseleave':
            _processMouseLeave.call(this, payload);
            break;
        default:
            break;
    }
}
```
- example usage
```shell
...
   if (!node) return;

   this.addChildrenToQueue(node);
   var child;

   while ((child = this.breadthFirstNext()))
       if (child && child.onReceive)
           child.onReceive(event, payload);

};

/**
* dispatchUIevent takes a path, an event name, and a payload and dispatches them in
* a manner anologous to DOM bubbling. It first traverses down to the node specified at
* the path. That node receives the event first, and then every ancestor receives the event
...
```

#### <a name="apidoc.element.famous.GestureHandler.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>toString ()](#apidoc.element.famous.GestureHandler.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'GestureHandler';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```

#### <a name="apidoc.element.famous.GestureHandler.prototype.trigger"></a>[function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>trigger (ev, payload)](#apidoc.element.famous.GestureHandler.prototype.trigger)
- description and source-code
```javascript
function trigger(ev, payload) {
    this._events.trigger(ev, payload);
}
```
- example usage
```shell
...
GestureHandler.prototype.triggerGestures = function() {
var payload = this.event;
for (var i = 0, len = this.gestures.length; i < len; i++) {
    var gesture = this.gestures[i];
    switch (gesture) {
        case 'rotate':
        case 'pinch':
            if (payload.points === 2) this.trigger(gesture, payload);
            break;
        case 'tap':
            if (payload.status === 'start') {
                if (this.options.tap) {
                    var pts = this.options.tap.points || 1;
                    if(this.multiTap >= pts && payload.points >= pts) this.trigger(gesture, payload);
                }
...
```

#### <a name="apidoc.element.famous.GestureHandler.prototype.triggerGestures"></a>[function <span class="apidocSignatureSpan">famous.GestureHandler.prototype.</span>triggerGestures ()](#apidoc.element.famous.GestureHandler.prototype.triggerGestures)
- description and source-code
```javascript
triggerGestures = function () {
    var payload = this.event;
    for (var i = 0, len = this.gestures.length; i < len; i++) {
        var gesture = this.gestures[i];
        switch (gesture) {
            case 'rotate':
            case 'pinch':
                if (payload.points === 2) this.trigger(gesture, payload);
                break;
            case 'tap':
                if (payload.status === 'start') {
                    if (this.options.tap) {
                        var pts = this.options.tap.points || 1;
                        if(this.multiTap >= pts && payload.points >= pts) this.trigger(gesture, payload);
                    }
                    else this.trigger(gesture, payload);
                }
                break;
            default:
                this.trigger(gesture, payload);
                break;
        }
    }
}
```
- example usage
```shell
...
       }
       if (this.trackedGestures.rotate) {
           this.event.rotation = 0;
           this.event.rotationDelta = 0;
           this.event.rotationVelocity = 0;
       }
   }
   this.triggerGestures();
}

/**
* Process up to the first two touch/mouse move events.
*
* @method _processPointerMove
* @private
...
```



# <a name="apidoc.module.famous.Mat33"></a>[module famous.Mat33](#apidoc.module.famous.Mat33)

#### <a name="apidoc.element.famous.Mat33.Mat33"></a>[function <span class="apidocSignatureSpan">famous.</span>Mat33 (values)](#apidoc.element.famous.Mat33.Mat33)
- description and source-code
```javascript
function Mat33(values) {
    this.values = values || [1,0,0,0,1,0,0,0,1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33.add"></a>[function <span class="apidocSignatureSpan">famous.Mat33.</span>add (matrix1, matrix2, output)](#apidoc.element.famous.Mat33.add)
- description and source-code
```javascript
function add(matrix1, matrix2, output) {
    var A = matrix1.values;
    var B = matrix2.values;
    var result = output.values;

    var A0 = A[0];
    var A1 = A[1];
    var A2 = A[2];
    var A3 = A[3];
    var A4 = A[4];
    var A5 = A[5];
    var A6 = A[6];
    var A7 = A[7];
    var A8 = A[8];

    var B0 = B[0];
    var B1 = B[1];
    var B2 = B[2];
    var B3 = B[3];
    var B4 = B[4];
    var B5 = B[5];
    var B6 = B[6];
    var B7 = B[7];
    var B8 = B[8];

    result[0] = A0 + B0;
    result[1] = A1 + B1;
    result[2] = A2 + B2;
    result[3] = A3 + B3;
    result[4] = A4 + B4;
    result[5] = A5 + B5;
    result[6] = A6 + B6;
    result[7] = A7 + B7;
    result[8] = A8 + B8;

    return output;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Mat33.clone"></a>[function <span class="apidocSignatureSpan">famous.Mat33.</span>clone (m)](#apidoc.element.famous.Mat33.clone)
- description and source-code
```javascript
function clone(m) {
    return new Mat33(m.values.slice());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33.inverse"></a>[function <span class="apidocSignatureSpan">famous.Mat33.</span>inverse (matrix, output)](#apidoc.element.famous.Mat33.inverse)
- description and source-code
```javascript
function inverse(matrix, output) {
    var M = matrix.values;
    var result = output.values;

    var M0 = M[0];
    var M1 = M[1];
    var M2 = M[2];
    var M3 = M[3];
    var M4 = M[4];
    var M5 = M[5];
    var M6 = M[6];
    var M7 = M[7];
    var M8 = M[8];

    var det = M0*(M4*M8 - M5*M7) -
              M1*(M3*M8 - M5*M6) +
              M2*(M3*M7 - M4*M6);

    if (Math.abs(det) < 1e-40) return null;

    det = 1 / det;

    result[0] = (M4*M8 - M5*M7) * det;
    result[3] = (-M3*M8 + M5*M6) * det;
    result[6] = (M3*M7 - M4*M6) * det;
    result[1] = (-M1*M8 + M2*M7) * det;
    result[4] = (M0*M8 - M2*M6) * det;
    result[7] = (-M0*M7 + M1*M6) * det;
    result[2] = (M1*M5 - M2*M4) * det;
    result[5] = (-M0*M5 + M2*M3) * det;
    result[8] = (M0*M4 - M1*M3) * det;

    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33.multiply"></a>[function <span class="apidocSignatureSpan">famous.Mat33.</span>multiply (matrix1, matrix2, output)](#apidoc.element.famous.Mat33.multiply)
- description and source-code
```javascript
function multiply(matrix1, matrix2, output) {
    var A = matrix1.values;
    var B = matrix2.values;
    var result = output.values;

    var A0 = A[0];
    var A1 = A[1];
    var A2 = A[2];
    var A3 = A[3];
    var A4 = A[4];
    var A5 = A[5];
    var A6 = A[6];
    var A7 = A[7];
    var A8 = A[8];

    var B0 = B[0];
    var B1 = B[1];
    var B2 = B[2];
    var B3 = B[3];
    var B4 = B[4];
    var B5 = B[5];
    var B6 = B[6];
    var B7 = B[7];
    var B8 = B[8];

    result[0] = A0*B0 + A1*B3 + A2*B6;
    result[1] = A0*B1 + A1*B4 + A2*B7;
    result[2] = A0*B2 + A1*B5 + A2*B8;
    result[3] = A3*B0 + A4*B3 + A5*B6;
    result[4] = A3*B1 + A4*B4 + A5*B7;
    result[5] = A3*B2 + A4*B5 + A5*B8;
    result[6] = A6*B0 + A7*B3 + A8*B6;
    result[7] = A6*B1 + A7*B4 + A8*B7;
    result[8] = A6*B2 + A7*B5 + A8*B8;

    return output;
}
```
- example usage
```shell
...
}
else {
    rotQ.fromEuler(x, y, z);
    callback = options;
    options = w;
}

var q = referenceQ.multiply(rotQ);
this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
return this;
};

Transform.prototype.clean = function clean() {
var node = this._node;
var c;
...
```

#### <a name="apidoc.element.famous.Mat33.subtract"></a>[function <span class="apidocSignatureSpan">famous.Mat33.</span>subtract (matrix1, matrix2, output)](#apidoc.element.famous.Mat33.subtract)
- description and source-code
```javascript
function subtract(matrix1, matrix2, output) {
    var A = matrix1.values;
    var B = matrix2.values;
    var result = output.values;

    var A0 = A[0];
    var A1 = A[1];
    var A2 = A[2];
    var A3 = A[3];
    var A4 = A[4];
    var A5 = A[5];
    var A6 = A[6];
    var A7 = A[7];
    var A8 = A[8];

    var B0 = B[0];
    var B1 = B[1];
    var B2 = B[2];
    var B3 = B[3];
    var B4 = B[4];
    var B5 = B[5];
    var B6 = B[6];
    var B7 = B[7];
    var B8 = B[8];

    result[0] = A0 - B0;
    result[1] = A1 - B1;
    result[2] = A2 - B2;
    result[3] = A3 - B3;
    result[4] = A4 - B4;
    result[5] = A5 - B5;
    result[6] = A6 - B6;
    result[7] = A7 - B7;
    result[8] = A8 - B8;

    return output;
}
```
- example usage
```shell
...
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
...
```

#### <a name="apidoc.element.famous.Mat33.transpose"></a>[function <span class="apidocSignatureSpan">famous.Mat33.</span>transpose (matrix, output)](#apidoc.element.famous.Mat33.transpose)
- description and source-code
```javascript
function transpose(matrix, output) {
    var M = matrix.values;
    var result = output.values;

    var M0 = M[0];
    var M1 = M[1];
    var M2 = M[2];
    var M3 = M[3];
    var M4 = M[4];
    var M5 = M[5];
    var M6 = M[6];
    var M7 = M[7];
    var M8 = M[8];

    result[0] = M0;
    result[1] = M3;
    result[2] = M6;
    result[3] = M1;
    result[4] = M4;
    result[5] = M7;
    result[6] = M2;
    result[7] = M5;
    result[8] = M8;

    return output;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Mat33.prototype"></a>[module famous.Mat33.prototype](#apidoc.module.famous.Mat33.prototype)

#### <a name="apidoc.element.famous.Mat33.prototype.copy"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>copy (matrix)](#apidoc.element.famous.Mat33.prototype.copy)
- description and source-code
```javascript
function copy(matrix) {
    var A = this.values;
    var B = matrix.values;

    A[0] = B[0];
    A[1] = B[1];
    A[2] = B[2];
    A[3] = B[3];
    A[4] = B[4];
    A[5] = B[5];
    A[6] = B[6];
    A[7] = B[7];
    A[8] = B[8];

    return this;
}
```
- example usage
```shell
...
        this.event.rotationVelocity = 0;
    }
    this.event.pointers.push(this.pointer2);
}

this.event.status = 'start';
if (this.event.points === 1) {
    this.center.copy(this.last1);
    this.centerDelta.clear();
    this.centerVelocity.clear();
    if (this.trackedGestures.pinch) {
        this.event.scale = 1;
        this.event.scaleDelta = 0;
        this.event.scaleVelocity = 0;
    }
...
```

#### <a name="apidoc.element.famous.Mat33.prototype.get"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>get ()](#apidoc.element.famous.Mat33.prototype.get)
- description and source-code
```javascript
function get() {
    return this.values;
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Mat33.prototype.getDeterminant"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>getDeterminant ()](#apidoc.element.famous.Mat33.prototype.getDeterminant)
- description and source-code
```javascript
function getDeterminant() {
    var M = this.values;

    var M3 = M[3];
    var M4 = M[4];
    var M5 = M[5];
    var M6 = M[6];
    var M7 = M[7];
    var M8 = M[8];

    var det = M[0]*(M4*M8 - M5*M7) -
              M[1]*(M3*M8 - M5*M6) +
              M[2]*(M3*M7 - M4*M6);

    return det;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33.prototype.inverse"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>inverse ()](#apidoc.element.famous.Mat33.prototype.inverse)
- description and source-code
```javascript
function inverse() {
    var M = this.values;

    var M0 = M[0];
    var M1 = M[1];
    var M2 = M[2];
    var M3 = M[3];
    var M4 = M[4];
    var M5 = M[5];
    var M6 = M[6];
    var M7 = M[7];
    var M8 = M[8];

    var det = M0*(M4*M8 - M5*M7) -
              M1*(M3*M8 - M5*M6) +
              M2*(M3*M7 - M4*M6);

    if (Math.abs(det) < 1e-40) return null;

    det = 1 / det;

    M[0] = (M4*M8 - M5*M7) * det;
    M[3] = (-M3*M8 + M5*M6) * det;
    M[6] = (M3*M7 - M4*M6) * det;
    M[1] = (-M1*M8 + M2*M7) * det;
    M[4] = (M0*M8 - M2*M6) * det;
    M[7] = (-M0*M7 + M1*M6) * det;
    M[2] = (M1*M5 - M2*M4) * det;
    M[5] = (-M0*M5 + M2*M3) * det;
    M[8] = (M0*M4 - M1*M3) * det;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33.prototype.multiply"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>multiply (matrix)](#apidoc.element.famous.Mat33.prototype.multiply)
- description and source-code
```javascript
function multiply(matrix) {
    var A = this.values;
    var B = matrix.values;

    var A0 = A[0];
    var A1 = A[1];
    var A2 = A[2];
    var A3 = A[3];
    var A4 = A[4];
    var A5 = A[5];
    var A6 = A[6];
    var A7 = A[7];
    var A8 = A[8];

    var B0 = B[0];
    var B1 = B[1];
    var B2 = B[2];
    var B3 = B[3];
    var B4 = B[4];
    var B5 = B[5];
    var B6 = B[6];
    var B7 = B[7];
    var B8 = B[8];

    A[0] = A0*B0 + A1*B3 + A2*B6;
    A[1] = A0*B1 + A1*B4 + A2*B7;
    A[2] = A0*B2 + A1*B5 + A2*B8;
    A[3] = A3*B0 + A4*B3 + A5*B6;
    A[4] = A3*B1 + A4*B4 + A5*B7;
    A[5] = A3*B2 + A4*B5 + A5*B8;
    A[6] = A6*B0 + A7*B3 + A8*B6;
    A[7] = A6*B1 + A7*B4 + A8*B7;
    A[8] = A6*B2 + A7*B5 + A8*B8;

    return this;
}
```
- example usage
```shell
...
}
else {
    rotQ.fromEuler(x, y, z);
    callback = options;
    options = w;
}

var q = referenceQ.multiply(rotQ);
this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
return this;
};

Transform.prototype.clean = function clean() {
var node = this._node;
var c;
...
```

#### <a name="apidoc.element.famous.Mat33.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>set (values)](#apidoc.element.famous.Mat33.prototype.set)
- description and source-code
```javascript
function set(values) {
    this.values = values;
    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Mat33.prototype.transpose"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>transpose ()](#apidoc.element.famous.Mat33.prototype.transpose)
- description and source-code
```javascript
function transpose() {
    var M = this.values;

    var M1 = M[1];
    var M2 = M[2];
    var M3 = M[3];
    var M5 = M[5];
    var M6 = M[6];
    var M7 = M[7];

    M[1] = M3;
    M[2] = M6;
    M[3] = M1;
    M[5] = M7;
    M[6] = M2;
    M[7] = M5;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mat33.prototype.vectorMultiply"></a>[function <span class="apidocSignatureSpan">famous.Mat33.prototype.</span>vectorMultiply (v, output)](#apidoc.element.famous.Mat33.prototype.vectorMultiply)
- description and source-code
```javascript
function vectorMultiply(v, output) {
    var M = this.values;
    var v0 = v.x;
    var v1 = v.y;
    var v2 = v.z;

    output.x = M[0]*v0 + M[1]*v1 + M[2]*v2;
    output.y = M[3]*v0 + M[4]*v1 + M[5]*v2;
    output.z = M[6]*v0 + M[7]*v1 + M[8]*v2;

    return output;
}
```
- example usage
```shell
...
* @param {Number} dt Delta time.
* @return {undefined} undefined
*/
function _integrateVelocity(body, dt) {
   body.momentum.add(Vec3.scale(body.force, dt, DELTA_REGISTER));
   body.angularMomentum.add(Vec3.scale(body.torque, dt, DELTA_REGISTER));
   Vec3.scale(body.momentum, body.inverseMass, body.velocity);
   body.inverseInertia.vectorMultiply(body.angularMomentum, body.angularVelocity);
   body.force.clear();
   body.torque.clear();
}

/**
* Update the Particle position and orientation based off current translational and angular velocities.
*
...
```



# <a name="apidoc.module.famous.Material"></a>[module famous.Material](#apidoc.module.famous.Material)

#### <a name="apidoc.element.famous.Material.Material"></a>[function <span class="apidocSignatureSpan">famous.</span>Material (name, chunk, inputs, options)](#apidoc.element.famous.Material.Material)
- description and source-code
```javascript
function Material(name, chunk, inputs, options) {
    options = options || {};

    this.name = name;
    this.chunk = chunk;
    this.inputs = inputs ? (Array.isArray(inputs) ? inputs : [inputs]): [];
    this.uniforms = options.uniforms || {};
    this.varyings = options.varyings;
    this.attributes = options.attributes;

    this.meshes = [];

    if (options.texture) {
        this.texture = options.texture.__isATexture__ ? options.texture : TextureRegistry.register(null, options.texture);
    }

    this._id = Material.id++;

    this.invalidations = [];
    this.__isAMaterial__ = true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.Custom"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>Custom (schema, inputs, uniforms)](#apidoc.element.famous.Material.Custom)
- description and source-code
```javascript
Custom = function (schema, inputs, uniforms) {
    return new Material('custom', {glsl: schema, output: 1, uniforms: uniforms || {}} , inputs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.Texture"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>Texture (source)](#apidoc.element.famous.Material.Texture)
- description and source-code
```javascript
Texture = function (source) {
    if (typeof window === 'undefined') return console.error('Texture constructor cannot be run inside of a worker');
    return expressions.image([], { texture: source });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.abs"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>abs (inputs, options)](#apidoc.element.famous.Material.abs)
- description and source-code
```javascript
abs = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
var M7 = M[7];
var M8 = M[8];

var det = M0*(M4*M8 - M5*M7) -
          M1*(M3*M8 - M5*M6) +
          M2*(M3*M7 - M4*M6);

if (Math.abs(det) < 1e-40) return null;

det = 1 / det;

M[0] = (M4*M8 - M5*M7) * det;
M[3] = (-M3*M8 + M5*M6) * det;
M[6] = (M3*M7 - M4*M6) * det;
M[1] = (-M1*M8 + M2*M7) * det;
...
```

#### <a name="apidoc.element.famous.Material.add"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>add (inputs, options)](#apidoc.element.famous.Material.add)
- description and source-code
```javascript
add = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Material.ceiling"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>ceiling (inputs, options)](#apidoc.element.famous.Material.ceiling)
- description and source-code
```javascript
ceiling = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.clamp"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>clamp (inputs, options)](#apidoc.element.famous.Material.clamp)
- description and source-code
```javascript
clamp = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.constant"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>constant (inputs, options)](#apidoc.element.famous.Material.constant)
- description and source-code
```javascript
constant = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.cos"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>cos (inputs, options)](#apidoc.element.famous.Material.cos)
- description and source-code
```javascript
cos = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
 *
 * @return {Vec2} this
 */
Vec2.prototype.rotate = function(theta) {
    var x = this.x;
    var y = this.y;

    var cosTheta = Math.cos(theta);
    var sinTheta = Math.sin(theta);

    this.x = x * cosTheta - y * sinTheta;
    this.y = x * sinTheta + y * cosTheta;

    return this;
};
...
```

#### <a name="apidoc.element.famous.Material.dot"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>dot (inputs, options)](#apidoc.element.famous.Material.dot)
- description and source-code
```javascript
dot = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Material.floor"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>floor (inputs, options)](#apidoc.element.famous.Material.floor)
- description and source-code
```javascript
floor = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
    var offset = 0;
    var length;
    var buffer;
    var k;

    if (j === -1) {
        j = vertexBuffers.keys.length;
        length = isIndex ? value.length : Math.floor(value.length / spacing);

        if (!dynamic) {

// Use a previously created buffer if available.

for (k = 0; k < this._staticBuffers.length; k++) {
...
```

#### <a name="apidoc.element.famous.Material.fragCoord"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>fragCoord (inputs, options)](#apidoc.element.famous.Material.fragCoord)
- description and source-code
```javascript
fragCoord = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.image"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>image (inputs, options)](#apidoc.element.famous.Material.image)
- description and source-code
```javascript
image = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
};

module.exports = expressions;
expressions.Material = Material;

expressions.Texture = function (source) {
    if (typeof window === 'undefined') return console.error('Texture constructor cannot be run inside of a worker');
    return expressions.image([], { texture: source });
};

expressions.Custom = function (schema, inputs, uniforms) {
    return new Material('custom', {glsl: schema, output: 1, uniforms: uniforms || {}} , inputs);
};

// Recursively iterates over a material's inputs, invoking a given callback
...
```

#### <a name="apidoc.element.famous.Material.max"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>max (inputs, options)](#apidoc.element.famous.Material.max)
- description and source-code
```javascript
max = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
if (!rAF) {
var now = Date.now ? Date.now : function () {
    return new Date().getTime();
};

rAF = function(callback) {
    var currTime = now();
    var timeToCall = Math.max(0, 16 - (currTime - lastTime));
    var id = setTimeout(function () {
        callback(currTime + timeToCall);
    }, timeToCall);
    lastTime = currTime + timeToCall;
    return id;
};
...
```

#### <a name="apidoc.element.famous.Material.meshPosition"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>meshPosition (inputs, options)](#apidoc.element.famous.Material.meshPosition)
- description and source-code
```javascript
meshPosition = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.min"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>min (inputs, options)](#apidoc.element.famous.Material.min)
- description and source-code
```javascript
min = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...

var translation = new Vec3(
    getTranslationFactor(maxX, minX),
    getTranslationFactor(maxY, minY),
    getTranslationFactor(maxZ, minZ)
);

var scale = Math.min(
    getScaleFactor(maxX + translation.x, minX + translation.x),
    getScaleFactor(maxY + translation.y, minY + translation.y),
    getScaleFactor(maxZ + translation.z, minZ + translation.z)
);

for (i = 0; i < vectors.length; i++) {
    out.push.apply(out, vectors[i].add(translation).scale(scale).toArray());
...
```

#### <a name="apidoc.element.famous.Material.mix"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>mix (inputs, options)](#apidoc.element.famous.Material.mix)
- description and source-code
```javascript
mix = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.mod"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>mod (inputs, options)](#apidoc.element.famous.Material.mod)
- description and source-code
```javascript
mod = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.multiply"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>multiply (inputs, options)](#apidoc.element.famous.Material.multiply)
- description and source-code
```javascript
multiply = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
}
else {
    rotQ.fromEuler(x, y, z);
    callback = options;
    options = w;
}

var q = referenceQ.multiply(rotQ);
this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
return this;
};

Transform.prototype.clean = function clean() {
var node = this._node;
var c;
...
```

#### <a name="apidoc.element.famous.Material.normal"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>normal (inputs, options)](#apidoc.element.famous.Material.normal)
- description and source-code
```javascript
normal = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.normalize"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>normalize (inputs, options)](#apidoc.element.famous.Material.normalize)
- description and source-code
```javascript
normalize = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
var c = frontierEdges[j][1];
var B = vertices[b].vertex;
var C = vertices[c].vertex;

var AB = Vec3.subtract(B, A, AB_REGISTER);
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
...
```

#### <a name="apidoc.element.famous.Material.parameter"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>parameter (inputs, options)](#apidoc.element.famous.Material.parameter)
- description and source-code
```javascript
parameter = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.pow"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>pow (inputs, options)](#apidoc.element.famous.Material.pow)
- description and source-code
```javascript
pow = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
},

inOutSine: function(t) {
    return -.5*(Math.cos(Math.PI*t) - 1);
},

inExpo: function(t) {
    return (t===0) ? 0.0 : Math.pow(2, 10 * (t - 1));
},

outExpo: function(t) {
    return (t===1.0) ? 1.0 : (-Math.pow(2, -10 * t) + 1);
},

inOutExpo: function(t) {
...
```

#### <a name="apidoc.element.famous.Material.registerExpression"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>registerExpression (name, schema)](#apidoc.element.famous.Material.registerExpression)
- description and source-code
```javascript
function registerExpression(name, schema) {
    this[name] = function (inputs, options) {
        return new Material(name, schema, inputs, options);
    };
}
```
- example usage
```shell
...
expressions.registerExpression = function registerExpression(name, schema) {
   this[name] = function (inputs, options) {
       return new Material(name, schema, inputs, options);
   };
};

for (var snippetName in snippets) {
   expressions.registerExpression(snippetName, snippets[snippetName]);
}

/**
* Material is a public class that composes a material-graph out of expressions
*
*
* @class Material
...
```

#### <a name="apidoc.element.famous.Material.sign"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>sign (inputs, options)](#apidoc.element.famous.Material.sign)
- description and source-code
```javascript
sign = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.sin"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>sin (inputs, options)](#apidoc.element.famous.Material.sin)
- description and source-code
```javascript
sin = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
 * @return {Vec2} this
 */
Vec2.prototype.rotate = function(theta) {
    var x = this.x;
    var y = this.y;

    var cosTheta = Math.cos(theta);
    var sinTheta = Math.sin(theta);

    this.x = x * cosTheta - y * sinTheta;
    this.y = x * sinTheta + y * cosTheta;

    return this;
};
...
```

#### <a name="apidoc.element.famous.Material.smoothstep"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>smoothstep (inputs, options)](#apidoc.element.famous.Material.smoothstep)
- description and source-code
```javascript
smoothstep = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.sqrt"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>sqrt (inputs, options)](#apidoc.element.famous.Material.sqrt)
- description and source-code
```javascript
sqrt = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
*
* @return {Number} the length of the vector
*/
Vec2.prototype.length = function length() {
   var x = this.x;
   var y = this.y;

   return Math.sqrt(x * x + y * y);
};

/**
* Copy the input onto the current Vec2.
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Material.step"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>step (inputs, options)](#apidoc.element.famous.Material.step)
- description and source-code
```javascript
step = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
*
* @return {FamousEngine} this
*/
FamousEngine.prototype.handleFrame = function handleFrame (messages) {
   if (!messages) throw new Error('handleFrame must be called with an array of messages');
   if (!messages.length) throw new Error('FRAME must be sent with a time');

   this.step(messages.shift());
   return this;
};

/**
* step updates the clock and the scene graph and then sends the draw commands
* that accumulated in the update to the renderers.
*
...
```

#### <a name="apidoc.element.famous.Material.subtract"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>subtract (inputs, options)](#apidoc.element.famous.Material.subtract)
- description and source-code
```javascript
subtract = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
...
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
...
```

#### <a name="apidoc.element.famous.Material.time"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>time (inputs, options)](#apidoc.element.famous.Material.time)
- description and source-code
```javascript
time = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.uv"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>uv (inputs, options)](#apidoc.element.famous.Material.uv)
- description and source-code
```javascript
uv = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.vec2"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>vec2 (inputs, options)](#apidoc.element.famous.Material.vec2)
- description and source-code
```javascript
vec2 = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Material.vec3"></a>[function <span class="apidocSignatureSpan">famous.Material.</span>vec3 (inputs, options)](#apidoc.element.famous.Material.vec3)
- description and source-code
```javascript
vec3 = function (inputs, options) {
    return new Material(name, schema, inputs, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Math"></a>[module famous.Math](#apidoc.module.famous.Math)

#### <a name="apidoc.element.famous.Math.invert"></a>[function <span class="apidocSignatureSpan">famous.Math.</span>invert (out, a)](#apidoc.element.famous.Math.invert)
- description and source-code
```javascript
function invert(out, a) {
    var a00 = a[0], a01 = a[1], a02 = a[2], a03 = a[3],
        a10 = a[4], a11 = a[5], a12 = a[6], a13 = a[7],
        a20 = a[8], a21 = a[9], a22 = a[10], a23 = a[11],
        a30 = a[12], a31 = a[13], a32 = a[14], a33 = a[15],

        b00 = a00 * a11 - a01 * a10,
        b01 = a00 * a12 - a02 * a10,
        b02 = a00 * a13 - a03 * a10,
        b03 = a01 * a12 - a02 * a11,
        b04 = a01 * a13 - a03 * a11,
        b05 = a02 * a13 - a03 * a12,
        b06 = a20 * a31 - a21 * a30,
        b07 = a20 * a32 - a22 * a30,
        b08 = a20 * a33 - a23 * a30,
        b09 = a21 * a32 - a22 * a31,
        b10 = a21 * a33 - a23 * a31,
        b11 = a22 * a33 - a23 * a32,

        // Calculate the determinant
        det = b00 * b11 - b01 * b10 + b02 * b09 + b03 * b08 - b04 * b07 + b05 * b06;

    if (!det) {
        return null;
    }
    det = 1.0 / det;

    out[0] = (a11 * b11 - a12 * b10 + a13 * b09) * det;
    out[1] = (a02 * b10 - a01 * b11 - a03 * b09) * det;
    out[2] = (a31 * b05 - a32 * b04 + a33 * b03) * det;
    out[3] = (a22 * b04 - a21 * b05 - a23 * b03) * det;
    out[4] = (a12 * b08 - a10 * b11 - a13 * b07) * det;
    out[5] = (a00 * b11 - a02 * b08 + a03 * b07) * det;
    out[6] = (a32 * b02 - a30 * b05 - a33 * b01) * det;
    out[7] = (a20 * b05 - a22 * b02 + a23 * b01) * det;
    out[8] = (a10 * b10 - a11 * b08 + a13 * b06) * det;
    out[9] = (a01 * b08 - a00 * b10 - a03 * b06) * det;
    out[10] = (a30 * b04 - a31 * b02 + a33 * b00) * det;
    out[11] = (a21 * b02 - a20 * b04 - a23 * b00) * det;
    out[12] = (a11 * b07 - a10 * b09 - a12 * b06) * det;
    out[13] = (a00 * b09 - a01 * b07 + a02 * b06) * det;
    out[14] = (a31 * b01 - a30 * b03 - a32 * b00) * det;
    out[15] = (a20 * b03 - a21 * b01 + a22 * b00) * det;

    return out;
}
```
- example usage
```shell
...
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
    this.addFeature(distance, ABC, [a, b, c]);
}
else {
    var reference = Vec3.subtract(referencePoint, A, VEC_REGISTER);
    if (Vec3.dot(ABC, reference) > -0.001) ABC.invert();
...
```

#### <a name="apidoc.element.famous.Math.multiply"></a>[function <span class="apidocSignatureSpan">famous.Math.</span>multiply (out, a, b)](#apidoc.element.famous.Math.multiply)
- description and source-code
```javascript
function multiply(out, a, b) {
    var a00 = a[0], a01 = a[1], a02 = a[2], a03 = a[3],
        a10 = a[4], a11 = a[5], a12 = a[6], a13 = a[7],
        a20 = a[8], a21 = a[9], a22 = a[10], a23 = a[11],
        a30 = a[12], a31 = a[13], a32 = a[14], a33 = a[15],

        b0 = b[0], b1 = b[1], b2 = b[2], b3 = b[3],
        b4 = b[4], b5 = b[5], b6 = b[6], b7 = b[7],
        b8 = b[8], b9 = b[9], b10 = b[10], b11 = b[11],
        b12 = b[12], b13 = b[13], b14 = b[14], b15 = b[15];

    var changed = false;
    var out0, out1, out2, out3;

    out0 = b0*a00 + b1*a10 + b2*a20 + b3*a30;
    out1 = b0*a01 + b1*a11 + b2*a21 + b3*a31;
    out2 = b0*a02 + b1*a12 + b2*a22 + b3*a32;
    out3 = b0*a03 + b1*a13 + b2*a23 + b3*a33;

    changed = changed ?
              changed : out0 === out[0] ||
                        out1 === out[1] ||
                        out2 === out[2] ||
                        out3 === out[3];

    out[0] = out0;
    out[1] = out1;
    out[2] = out2;
    out[3] = out3;

    b0 = b4; b1 = b5; b2 = b6; b3 = b7;
    out0 = b0*a00 + b1*a10 + b2*a20 + b3*a30;
    out1 = b0*a01 + b1*a11 + b2*a21 + b3*a31;
    out2 = b0*a02 + b1*a12 + b2*a22 + b3*a32;
    out3 = b0*a03 + b1*a13 + b2*a23 + b3*a33;

    changed = changed ?
              changed : out0 === out[4] ||
                        out1 === out[5] ||
                        out2 === out[6] ||
                        out3 === out[7];

    out[4] = out0;
    out[5] = out1;
    out[6] = out2;
    out[7] = out3;

    b0 = b8; b1 = b9; b2 = b10; b3 = b11;
    out0 = b0*a00 + b1*a10 + b2*a20 + b3*a30;
    out1 = b0*a01 + b1*a11 + b2*a21 + b3*a31;
    out2 = b0*a02 + b1*a12 + b2*a22 + b3*a32;
    out3 = b0*a03 + b1*a13 + b2*a23 + b3*a33;

    changed = changed ?
              changed : out0 === out[8] ||
                        out1 === out[9] ||
                        out2 === out[10] ||
                        out3 === out[11];

    out[8] = out0;
    out[9] = out1;
    out[10] = out2;
    out[11] = out3;

    b0 = b12; b1 = b13; b2 = b14; b3 = b15;
    out0 = b0*a00 + b1*a10 + b2*a20 + b3*a30;
    out1 = b0*a01 + b1*a11 + b2*a21 + b3*a31;
    out2 = b0*a02 + b1*a12 + b2*a22 + b3*a32;
    out3 = b0*a03 + b1*a13 + b2*a23 + b3*a33;

    changed = changed ?
              changed : out0 === out[12] ||
                        out1 === out[13] ||
                        out2 === out[14] ||
                        out3 === out[15];

    out[12] = out0;
    out[13] = out1;
    out[14] = out2;
    out[15] = out3;

    return out;
}
```
- example usage
```shell
...
}
else {
    rotQ.fromEuler(x, y, z);
    callback = options;
    options = w;
}

var q = referenceQ.multiply(rotQ);
this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
return this;
};

Transform.prototype.clean = function clean() {
var node = this._node;
var c;
...
```



# <a name="apidoc.module.famous.Mesh"></a>[module famous.Mesh](#apidoc.module.famous.Mesh)

#### <a name="apidoc.element.famous.Mesh.Mesh"></a>[function <span class="apidocSignatureSpan">famous.</span>Mesh (node, options)](#apidoc.element.famous.Mesh.Mesh)
- description and source-code
```javascript
function Mesh(node, options) {
    this._node = null;
    this._id = null;
    this._changeQueue = [];
    this._initialized = false;
    this._requestingUpdate = false;
    this._inDraw = false;
    this.value = {
        geometry: defaultGeometry,
        drawOptions: null,
        color: null,
        expressions: {},
        flatShading: null,
        glossiness: null,
        positionOffset: null,
        normals: null
    };
    if (node) node.addComponent(this);
    if (options) this.setDrawOptions(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Mesh.prototype"></a>[module famous.Mesh.prototype](#apidoc.module.famous.Mesh.prototype)

#### <a name="apidoc.element.famous.Mesh.prototype._pushInvalidations"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>_pushInvalidations (expressionName)](#apidoc.element.famous.Mesh.prototype._pushInvalidations)
- description and source-code
```javascript
function _pushInvalidations(expressionName) {
    var uniformKey;
    var expression = this.value.expressions[expressionName];
    var sender = this._node;
    if (expression) {
        expression.traverse(function (node) {
            var i = node.invalidations.length;
            while (i--) {
                uniformKey = node.invalidations.pop();
                sender.sendDrawCommand(Commands.GL_UNIFORMS);
                sender.sendDrawCommand(uniformKey);
                sender.sendDrawCommand(node.uniforms[uniformKey]);
            }
        });
    }
    return this;
}
```
- example usage
```shell
...
    this._node.requestUpdateOnNextTick(this._id);
}
else {
    this._requestingUpdate = false;
}

// If any invalidations exist, push them into the queue
this._pushInvalidations('baseColor');
this._pushInvalidations('positionOffset');
this._pushInvalidations('normals');
this._pushInvalidations('glossiness');

for (var i = 0; i < queue.length; i++) {
    node.sendDrawCommand(queue[i]);
}
...
```

#### <a name="apidoc.element.famous.Mesh.prototype._requestUpdate"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>_requestUpdate ()](#apidoc.element.famous.Mesh.prototype._requestUpdate)
- description and source-code
```javascript
function _requestUpdate() {
    if (!this._requestingUpdate && this._node) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }
}
```
- example usage
```shell
...
* @return {Node} this
*/
Node.prototype.requestUpdate = function requestUpdate (requester) {
   if (this._inUpdate || !this.isMounted())
       return this.requestUpdateOnNextTick(requester);
   if (this._updateQueue.indexOf(requester) === -1) {
       this._updateQueue.push(requester);
       if (!this._requestingUpdate) this._requestUpdate();
   }
   return this;
};

/**
* Schedules an update on the next tick. Similarily to
* {@link Node#requestUpdate}, 'requestUpdateOnNextTick' schedules the node's
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.draw"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>draw ()](#apidoc.element.famous.Mesh.prototype.draw)
- description and source-code
```javascript
function draw() {
    this._inDraw = true;

    this.init();

    var value = this.getValue();

    if (value.geometry != null) this.setGeometry(value.geometry);
    if (value.color != null) this.setBaseColor(value.color);
    if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
    if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
    if (value.flatShading != null) this.setFlatShading(value.flatShading);

    if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
    if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
    if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
    if (value.expressions.positionOffset != null) this.setPositionOffset(value.expressions.positionOffset);

    this._inDraw = false;
}
```
- example usage
```shell
...
*/
DOMElement.prototype.onMount = function onMount(node, id) {
   this._node = node;
   this._id = id;
   this._UIEvents = node.getUIEvents().slice(0);
   TransformSystem.makeBreakPointAt(node.getLocation());
   this.onSizeModeChange.apply(this, node.getSizeMode());
   this.draw();
   this.setAttribute('data-fa-path', node.getLocation());
};

/**
* Method to be invoked by the Node as soon as the node is being dismounted
* either directly or by dismounting one of its ancestors.
*
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.getBaseColor"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getBaseColor ()](#apidoc.element.famous.Mesh.prototype.getBaseColor)
- description and source-code
```javascript
function getBaseColor() {
    return this.value.expressions.baseColor || this.value.color;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getDrawOptions"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getDrawOptions ()](#apidoc.element.famous.Mesh.prototype.getDrawOptions)
- description and source-code
```javascript
function getDrawOptions() {
    return this.value.drawOptions;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getFlatShading"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getFlatShading ()](#apidoc.element.famous.Mesh.prototype.getFlatShading)
- description and source-code
```javascript
function getFlatShading() {
    return this.value.flatShading;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getGeometry"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getGeometry ()](#apidoc.element.famous.Mesh.prototype.getGeometry)
- description and source-code
```javascript
function getGeometry() {
    return this.value.geometry;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getGlossiness"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getGlossiness ()](#apidoc.element.famous.Mesh.prototype.getGlossiness)
- description and source-code
```javascript
function getGlossiness() {
    return this.value.expressions.glossiness || this.value.glossiness;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getMaterialExpressions"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getMaterialExpressions ()](#apidoc.element.famous.Mesh.prototype.getMaterialExpressions)
- description and source-code
```javascript
function getMaterialExpressions() {
    return this.value.expressions;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getNormals"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getNormals (materialExpression)](#apidoc.element.famous.Mesh.prototype.getNormals)
- description and source-code
```javascript
function getNormals(materialExpression) {
    return this.value.expressions.normals;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getPositionOffset"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getPositionOffset ()](#apidoc.element.famous.Mesh.prototype.getPositionOffset)
- description and source-code
```javascript
function getPositionOffset() {
    return this.value.expressions.positionOffset || this.value.positionOffset;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Mesh.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>getValue ()](#apidoc.element.famous.Mesh.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return this.value;
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.init"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>init ()](#apidoc.element.famous.Mesh.prototype.init)
- description and source-code
```javascript
function init() {
    this._initialized = true;
    this.onTransformChange(TransformSystem.get(this._node.getLocation()));
    var size = this._node.getSize();
    this.onSizeChange(size[0], size[1], size[2]);
    this.onOpacityChange(this._node.getOpacity());
    this._requestUpdate();
}
```
- example usage
```shell
...

If you have the Famous Engine included in your project, it is very easy to start getting content rendered to the screen.  Below
is a short example of how to get HTML content written to the screen.

'''js
var FamousEngine = require('famous/core/FamousEngine');
var DOMElement = require('famous/dom-renderables/DOMElement');

FamousEngine.init();
var scene = FamousEngine.createScene();

var node = scene.addChild();
var domEl = new DOMElement(node, {
content: 'Hello World',
properties: {
    fontFamily: 'Arial'
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onAddUIEvent"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onAddUIEvent (UIEvent)](#apidoc.element.famous.Mesh.prototype.onAddUIEvent)
- description and source-code
```javascript
function onAddUIEvent(UIEvent) {
    //TODO
}
```
- example usage
```shell
...
    var component;

    var added = UIEvents.indexOf(eventName) !== -1;
    if (!added) {
        UIEvents.push(eventName);
        for (var i = 0, len = components.length ; i < len ; i++) {
            component = components[i];
            if (component && component.onAddUIEvent) component.onAddUIEvent(eventName);
        }
    }

    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onDismount"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onDismount ()](#apidoc.element.famous.Mesh.prototype.onDismount)
- description and source-code
```javascript
function onDismount() {
    this._initialized = false;
    this._inDraw = false;

    this._node.sendDrawCommand(Commands.WITH);
    this._node.sendDrawCommand(this._node.getLocation());
    this._node.sendDrawCommand(Commands.GL_REMOVE_MESH);

    this._node = null;
    this._id = null;
}
```
- example usage
```shell
...
if (node.onHide) node.onHide();
for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onHide)
        components[i].onHide();
    }

    if (node.isMounted()) {
if (node.onDismount) node.onDismount(path);

for (i = 0, len = children.length ; i < len ; i++)
    if (children[i] && children[i].dismount) children[i].dismount();
    else if (children[i]) this.dismount(path + '/' + i);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onDismount)
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onHide"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onHide ()](#apidoc.element.famous.Mesh.prototype.onHide)
- description and source-code
```javascript
function onHide() {
    this._changeQueue.push(Commands.GL_MESH_VISIBILITY, false);

    this._requestUpdate();
}
```
- example usage
```shell
...
var children = node.getChildren();
var components = node.getComponents();
var i;
var len;

if (node.isShown()) {
    node._setShown(false);
    if (node.onHide) node.onHide();
    for (i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onHide)
            components[i].onHide();
}

if (node.isMounted()) {
    if (node.onDismount) node.onDismount(path);
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onMount"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onMount (node, id)](#apidoc.element.famous.Mesh.prototype.onMount)
- description and source-code
```javascript
function onMount(node, id) {
    this._node = node;
    this._id = id;

    TransformSystem.makeCalculateWorldMatrixAt(node.getLocation());

    this.draw();
}
```
- example usage
```shell
...
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onMount)
        components[i].onMount(node, i);

for (i = 0, len = children.length ; i < len ; i++)
    if (children[i] && children[i].mount) children[i].mount(path + '/' + i);
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onOpacityChange"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onOpacityChange (opacity)](#apidoc.element.famous.Mesh.prototype.onOpacityChange)
- description and source-code
```javascript
function onOpacityChange(opacity) {
    if (this._initialized) {
        this._changeQueue.push(Commands.GL_UNIFORMS);
        this._changeQueue.push('u_opacity');
        this._changeQueue.push(opacity);
    }

    this._requestUpdate();
}
```
- example usage
```shell
...

       var i = 0;
       var list = this._components;
       var len = list.length;
       var item;
       for (; i < len ; i++) {
           item = list[i];
           if (item && item.onOpacityChange) item.onOpacityChange(val);
       }
   }
   return this;
};

/**
* Sets the size mode being used for determining the node's final width, height
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onShow"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onShow ()](#apidoc.element.famous.Mesh.prototype.onShow)
- description and source-code
```javascript
function onShow() {
    this._changeQueue.push(Commands.GL_MESH_VISIBILITY, true);

    this._requestUpdate();
}
```
- example usage
```shell
...

        for (i = 0, len = children.length ; i < len ; i++)
            if (children[i] && children[i].mount) children[i].mount(path + '/' + i);
            else if (children[i]) this.mount(path + '/' + i, children[i]);
    }

    if (parent.isShown()) {
        if (node.onShow) node.onShow();
        for (i = 0, len = components.length ; i < len ; i++)
            if (components[i] && components[i].onShow)
                components[i].onShow();
    }
};

/**
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onSizeChange"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onSizeChange (x, y, z)](#apidoc.element.famous.Mesh.prototype.onSizeChange)
- description and source-code
```javascript
function onSizeChange(x, y, z) {
    if (this._initialized) {
        this._changeQueue.push(Commands.GL_UNIFORMS);
        this._changeQueue.push('u_size');
        this._changeQueue.push([x, y, z]);
    }

    this._requestUpdate();
}
```
- example usage
```shell
...
 * @return {undefined} undefined
 */
function sizeChanged (node, components, size) {
    var finalSize = size.get();
    var x = finalSize[0];
    var y = finalSize[1];
    var z = finalSize[2];
    if (node.onSizeChange) node.onSizeChange(x, y, z);
    for (var i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onSizeChange)
            components[i].onSizeChange(x, y, z);
    size.sizeChanged = false;
}

module.exports = new SizeSystem();
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onTransformChange"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onTransformChange (transform)](#apidoc.element.famous.Mesh.prototype.onTransformChange)
- description and source-code
```javascript
function onTransformChange(transform) {
    if (this._initialized) {
        this._changeQueue.push(Commands.GL_UNIFORMS);
        this._changeQueue.push('u_transform');
        this._changeQueue.push(transform.getWorldTransform());
    }

    this._requestUpdate();
}
```
- example usage
```shell
...
* @param {Node} node the node on which to trigger a change event if necessary
* @param {Array} components the components on which to trigger a change event if necessary
* @param {Transform} transform the transform class that changed
*
* @return {undefined} undefined
*/
function transformChanged (node, components, transform) {
   if (node.onTransformChange) node.onTransformChange(transform);
   for (var i = 0, len = components.length ; i < len ; i++)
       if (components[i] && components[i].onTransformChange)
           components[i].onTransformChange(transform);
}

/**
* Private method to call when the local transform changes. Triggers 'onLocalTransformChange' methods
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>onUpdate ()](#apidoc.element.famous.Mesh.prototype.onUpdate)
- description and source-code
```javascript
function onUpdate() {
    var node = this._node;
    var queue = this._changeQueue;

    if (node && node.isMounted()) {
        node.sendDrawCommand(Commands.WITH);
        node.sendDrawCommand(node.getLocation());

        // If any invalidations exist, push them into the queue
        if (this.value.color && this.value.color.isActive()) {
            this._node.sendDrawCommand(Commands.GL_UNIFORMS);
            this._node.sendDrawCommand('u_baseColor');
            this._node.sendDrawCommand(this.value.color.getNormalizedRGBA());
            this._node.requestUpdateOnNextTick(this._id);
        }
        if (this.value.glossiness && this.value.glossiness[0] && this.value.glossiness[0].isActive()) {
            this._node.sendDrawCommand(Commands.GL_UNIFORMS);
            this._node.sendDrawCommand('u_glossiness');
            var glossiness = this.value.glossiness[0].getNormalizedRGB();
            glossiness.push(this.value.glossiness[1]);
            this._node.sendDrawCommand(glossiness);
            this._node.requestUpdateOnNextTick(this._id);
        }
        else {
            this._requestingUpdate = false;
        }

        // If any invalidations exist, push them into the queue
        this._pushInvalidations('baseColor');
        this._pushInvalidations('positionOffset');
        this._pushInvalidations('normals');
        this._pushInvalidations('glossiness');

        for (var i = 0; i < queue.length; i++) {
            node.sendDrawCommand(queue[i]);
        }

        queue.length = 0;
    }
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setBaseColor"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setBaseColor (color)](#apidoc.element.famous.Mesh.prototype.setBaseColor)
- description and source-code
```javascript
function setBaseColor(color) {
    var uniformValue;
    var isMaterial = color.__isAMaterial__;
    var isColor = !!color.getNormalizedRGBA;

    if (isMaterial) {
        addMeshToMaterial(this, color, 'baseColor');
        this.value.color = null;
        this.value.expressions.baseColor = color;
        uniformValue = color;
    }
    else if (isColor) {
        this.value.expressions.baseColor = null;
        this.value.color = color;
        uniformValue = color.getNormalizedRGBA();
    }

    if (this._initialized) {

        // If a material expression

        if (color.__isAMaterial__) {
            this._changeQueue.push(Commands.MATERIAL_INPUT);
        }

        // If a color component

        else if (color.getNormalizedRGB) {
            this._changeQueue.push(Commands.GL_UNIFORMS);
        }

        this._changeQueue.push('u_baseColor');
        this._changeQueue.push(uniformValue);
    }

    this._requestUpdate();

    return this;
}
```
- example usage
```shell
...
this._inDraw = true;

this.init();

var value = this.getValue();

if (value.geometry != null) this.setGeometry(value.geometry);
if (value.color != null) this.setBaseColor(value.color);
if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
if (value.flatShading != null) this.setFlatShading(value.flatShading);

if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setDrawOptions"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setDrawOptions (options)](#apidoc.element.famous.Mesh.prototype.setDrawOptions)
- description and source-code
```javascript
function setOptions(options) {
    this._changeQueue.push(Commands.GL_SET_DRAW_OPTIONS);
    this._changeQueue.push(options);

    this.value.drawOptions = options;
    return this;
}
```
- example usage
```shell
...
       expressions: {},
       flatShading: null,
       glossiness: null,
       positionOffset: null,
       normals: null
   };
   if (node) node.addComponent(this);
   if (options) this.setDrawOptions(options);
}
/**
* Pass custom options to Mesh, such as a 3 element map
* which displaces the position of each vertex in world space.
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setFlatShading"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setFlatShading (bool)](#apidoc.element.famous.Mesh.prototype.setFlatShading)
- description and source-code
```javascript
function setFlatShading(bool) {
    if (this._inDraw || this.value.flatShading !== bool) {
        this.value.flatShading = bool;
        if (this._initialized) {
            this._changeQueue.push(Commands.GL_UNIFORMS);
            this._changeQueue.push('u_flatShading');
            this._changeQueue.push(bool ? 1 : 0);
        }
        this._requestUpdate();
    }

    return this;
}
```
- example usage
```shell
...

var value = this.getValue();

if (value.geometry != null) this.setGeometry(value.geometry);
if (value.color != null) this.setBaseColor(value.color);
if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
if (value.flatShading != null) this.setFlatShading(value.flatShading);

if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
if (value.expressions.positionOffset != null) this.setPositionOffset(value.expressions.positionOffset);

this._inDraw = false;
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setGeometry"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setGeometry (geometry, options)](#apidoc.element.famous.Mesh.prototype.setGeometry)
- description and source-code
```javascript
function setGeometry(geometry, options) {
    if (typeof geometry === 'string') {
        if (!Geometry[geometry]) throw 'Invalid geometry: "' + geometry + '".';
        else geometry = new Geometry[geometry](options);
    }

    if (this.value.geometry !== geometry || this._inDraw) {
        if (this._initialized) {
            this._changeQueue.push(Commands.GL_SET_GEOMETRY);
            this._changeQueue.push(geometry.spec.id);
            this._changeQueue.push(geometry.spec.type);
            this._changeQueue.push(geometry.spec.dynamic);
        }
        this._requestUpdate();
        this.value.geometry = geometry;
    }

    if (this._initialized) {
        if (this._node) {
            var i = this.value.geometry.spec.invalidations.length;
            if (i) this._requestUpdate();
            while (i--) {
                this.value.geometry.spec.invalidations.pop();
                this._changeQueue.push(Commands.GL_BUFFER_DATA);
                this._changeQueue.push(this.value.geometry.spec.id);
                this._changeQueue.push(this.value.geometry.spec.bufferNames[i]);
                this._changeQueue.push(this.value.geometry.spec.bufferValues[i]);
                this._changeQueue.push(this.value.geometry.spec.bufferSpacings[i]);
                this._changeQueue.push(this.value.geometry.spec.dynamic);
            }
        }
    }
    return this;
}
```
- example usage
```shell
...
        commands[++iterator]
    );
    return iterator;
}

function glSetGeometry (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setGeometry(
        path,
        commands[++iterator],
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setGlossiness"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setGlossiness (glossiness, strength)](#apidoc.element.famous.Mesh.prototype.setGlossiness)
- description and source-code
```javascript
function setGlossiness(glossiness, strength) {
    var isMaterial = glossiness.__isAMaterial__;
    var isColor = !!glossiness.getNormalizedRGB;

    if (isMaterial) {
        addMeshToMaterial(this, glossiness, 'glossiness');
        this.value.glossiness = [null, null];
        this.value.expressions.glossiness = glossiness;
    }
    else if (isColor) {
        this.value.expressions.glossiness = null;
        this.value.glossiness = [glossiness, strength || 20];
        glossiness = glossiness ? glossiness.getNormalizedRGB() : [0, 0, 0];
        glossiness.push(strength || 20);
    }

    if (this._initialized) {
        this._changeQueue.push(glossiness.__isAMaterial__ ? Commands.MATERIAL_INPUT : Commands.GL_UNIFORMS);
        this._changeQueue.push('u_glossiness');
        this._changeQueue.push(glossiness);
    }

    this._requestUpdate();
    return this;
}
```
- example usage
```shell
...
    if (value.color != null) this.setBaseColor(value.color);
    if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
    if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
    if (value.flatShading != null) this.setFlatShading(value.flatShading);

    if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
    if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
    if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
    if (value.expressions.positionOffset != null) this.setPositionOffset(value.expressions.positionOffset);

    this._inDraw = false;
};


function addMeshToMaterial(mesh, material, name) {
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setNormals"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setNormals (materialExpression)](#apidoc.element.famous.Mesh.prototype.setNormals)
- description and source-code
```javascript
function setNormals(materialExpression) {
    var isMaterial = materialExpression.__isAMaterial__;

    if (isMaterial) {
        addMeshToMaterial(this, materialExpression, 'normals');
        this.value.expressions.normals = materialExpression;
    }

    if (this._initialized) {
        this._changeQueue.push(materialExpression.__isAMaterial__ ? Commands.MATERIAL_INPUT : Commands.GL_UNIFORMS);
        this._changeQueue.push('u_normals');
        this._changeQueue.push(materialExpression);
    }

    this._requestUpdate();

    return this;
}
```
- example usage
```shell
...

    if (value.geometry != null) this.setGeometry(value.geometry);
    if (value.color != null) this.setBaseColor(value.color);
    if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
    if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
    if (value.flatShading != null) this.setFlatShading(value.flatShading);

    if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
    if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
    if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
    if (value.expressions.positionOffset != null) this.setPositionOffset(value.expressions.positionOffset);

    this._inDraw = false;
};
...
```

#### <a name="apidoc.element.famous.Mesh.prototype.setPositionOffset"></a>[function <span class="apidocSignatureSpan">famous.Mesh.prototype.</span>setPositionOffset (materialExpression)](#apidoc.element.famous.Mesh.prototype.setPositionOffset)
- description and source-code
```javascript
function positionOffset(materialExpression) {
    var uniformValue;
    var isMaterial = materialExpression.__isAMaterial__;

    if (isMaterial) {
        addMeshToMaterial(this, materialExpression, 'positionOffset');
        this.value.expressions.positionOffset = materialExpression;
        uniformValue = materialExpression;
    }
    else {
        this.value.expressions.positionOffset = null;
        this.value.positionOffset = materialExpression;
        uniformValue = this.value.positionOffset;
    }

    if (this._initialized) {
        this._changeQueue.push(materialExpression.__isAMaterial__ ? Commands.MATERIAL_INPUT : Commands.GL_UNIFORMS);
        this._changeQueue.push('u_positionOffset');
        this._changeQueue.push(uniformValue);
    }

    this._requestUpdate();

    return this;
}
```
- example usage
```shell
...
if (value.glossiness != null) this.setGlossiness.apply(this, value.glossiness);
if (value.drawOptions != null) this.setDrawOptions(value.drawOptions);
if (value.flatShading != null) this.setFlatShading(value.flatShading);

if (value.expressions.normals != null) this.setNormals(value.expressions.normals);
if (value.expressions.baseColor != null) this.setBaseColor(value.expressions.baseColor);
if (value.expressions.glossiness != null) this.setGlossiness(value.expressions.glossiness);
if (value.expressions.positionOffset != null) this.setPositionOffset(value.expressions.positionOffset);

this._inDraw = false;
};


function addMeshToMaterial(mesh, material, name) {
var expressions = mesh.value.expressions;
...
```



# <a name="apidoc.module.famous.MountPoint"></a>[module famous.MountPoint](#apidoc.module.famous.MountPoint)

#### <a name="apidoc.element.famous.MountPoint.MountPoint"></a>[function <span class="apidocSignatureSpan">famous.</span>MountPoint (node)](#apidoc.element.famous.MountPoint.MountPoint)
- description and source-code
```javascript
function MountPoint(node) {
    Position.call(this, node);

    var initial = node.getMountPoint();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.MountPoint.prototype"></a>[module famous.MountPoint.prototype](#apidoc.module.famous.MountPoint.prototype)

#### <a name="apidoc.element.famous.MountPoint.prototype.constructor"></a>[function <span class="apidocSignatureSpan">famous.MountPoint.prototype.</span>constructor (node)](#apidoc.element.famous.MountPoint.prototype.constructor)
- description and source-code
```javascript
function MountPoint(node) {
    Position.call(this, node);

    var initial = node.getMountPoint();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.MountPoint.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.MountPoint.prototype.</span>onUpdate ()](#apidoc.element.famous.MountPoint.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setMountPoint(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.MountPoint.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.MountPoint.prototype.</span>update ()](#apidoc.element.famous.MountPoint.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setMountPoint(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Node"></a>[module famous.Node](#apidoc.module.famous.Node)

#### <a name="apidoc.element.famous.Node.Node"></a>[function <span class="apidocSignatureSpan">famous.</span>Node ()](#apidoc.element.famous.Node.Node)
- description and source-code
```javascript
function Node() {
    this._requestingUpdate = false;
    this._inUpdate = false;
    this._mounted = false;
    this._shown = true;
    this._updater = null;
    this._opacity = 1;
    this._UIEvents = [];

    this._updateQueue = [];
    this._nextUpdateQueue = [];

    this._freedComponentIndicies = [];
    this._components = [];

    this._freedChildIndicies = [];
    this._children = [];

    this._fullChildren = [];

    this._parent = null;

    this._id = null;

    this._transformID = null;
    this._sizeID = null;

    if (!this.constructor.NO_DEFAULT_COMPONENTS) this._init();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Node.prototype"></a>[module famous.Node.prototype](#apidoc.module.famous.Node.prototype)

#### <a name="apidoc.element.famous.Node.prototype._init"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_init ()](#apidoc.element.famous.Node.prototype._init)
- description and source-code
```javascript
function _init() {
    this._transformID = this.addComponent(new Transform());
    this._sizeID = this.addComponent(new Size());
}
```
- example usage
```shell
...
    this._parent = null;

    this._id = null;

    this._transformID = null;
    this._sizeID = null;

    if (!this.constructor.NO_DEFAULT_COMPONENTS) this._init();
}

Node.RELATIVE_SIZE = 0;
Node.ABSOLUTE_SIZE = 1;
Node.RENDER_SIZE = 2;
Node.DEFAULT_SIZE = 0;
Node.NO_DEFAULT_COMPONENTS = false;
...
```

#### <a name="apidoc.element.famous.Node.prototype._requestUpdate"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_requestUpdate (force)](#apidoc.element.famous.Node.prototype._requestUpdate)
- description and source-code
```javascript
function _requestUpdate(force) {
    if (force || !this._requestingUpdate) {
        if (this._updater)
            this._updater.requestUpdate(this);
        this._requestingUpdate = true;
    }
}
```
- example usage
```shell
...
* @return {Node} this
*/
Node.prototype.requestUpdate = function requestUpdate (requester) {
   if (this._inUpdate || !this.isMounted())
       return this.requestUpdateOnNextTick(requester);
   if (this._updateQueue.indexOf(requester) === -1) {
       this._updateQueue.push(requester);
       if (!this._requestingUpdate) this._requestUpdate();
   }
   return this;
};

/**
* Schedules an update on the next tick. Similarily to
* {@link Node#requestUpdate}, 'requestUpdateOnNextTick' schedules the node's
...
```

#### <a name="apidoc.element.famous.Node.prototype._setMounted"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setMounted (mounted, path)](#apidoc.element.famous.Node.prototype._setMounted)
- description and source-code
```javascript
function _setMounted(mounted, path) {
    this._mounted = mounted;
    this._id = path ? path : null;
}
```
- example usage
```shell
...
);

    var children = node.getChildren();
    var components = node.getComponents();
    var i;
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
...
```

#### <a name="apidoc.element.famous.Node.prototype._setParent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setParent (parent)](#apidoc.element.famous.Node.prototype._setParent)
- description and source-code
```javascript
function _setParent(parent) {
    if (this._parent && this._parent.getChildren().indexOf(this) !== -1) {
        this._parent.removeChild(this);
    }
    this._parent = parent;
}
```
- example usage
```shell
...
    var i;
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onMount)
        components[i].onMount(node, i);

for (i = 0, len = children.length ; i < len ; i++)
...
```

#### <a name="apidoc.element.famous.Node.prototype._setShown"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setShown (shown)](#apidoc.element.famous.Node.prototype._setShown)
- description and source-code
```javascript
function _setShown(shown) {
    this._shown = shown;
}
```
- example usage
```shell
...

    var children = node.getChildren();
    var components = node.getComponents();
    var i;
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onMount)
...
```

#### <a name="apidoc.element.famous.Node.prototype._setUpdater"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_setUpdater (updater)](#apidoc.element.famous.Node.prototype._setUpdater)
- description and source-code
```javascript
function _setUpdater(updater) {
    this._updater = updater;
    if (this._requestingUpdate) this._updater.requestUpdate(this);
}
```
- example usage
```shell
...
* @param {FamousEngine} updater The updater which will be passed through the scene graph
*
* @return {undefined} undefined
*/
Dispatch.prototype._setUpdater = function _setUpdater (updater) {
   this._updater = updater;

   for (var key in this._nodes) this._nodes[key]._setUpdater(updater);
};

/**
* Enque the children of a node within the dispatcher. Does not clear
* the dispatchers queue first.
*
* @method addChildrenToQueue
...
```

#### <a name="apidoc.element.famous.Node.prototype._vecOptionalSet"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>_vecOptionalSet (vec, index, val)](#apidoc.element.famous.Node.prototype._vecOptionalSet)
- description and source-code
```javascript
function _vecOptionalSet(vec, index, val) {
    if (val != null && vec[index] !== val) {
        vec[index] = val;
        if (!this._requestingUpdate) this._requestUpdate();
        return true;
    }
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.addChild"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>addChild (child)](#apidoc.element.famous.Node.prototype.addChild)
- description and source-code
```javascript
function addChild(child) {
    var index = child ? this._children.indexOf(child) : -1;
    child = child ? child : new Node();

    if (index === -1) {
        index = this._freedChildIndicies.length ?
                this._freedChildIndicies.pop() : this._children.length;

        this._children[index] = child;
        this._fullChildren.push(child);
    }

    if (this.isMounted())
        child.mount(this.getLocation() + '/' + index);

    return child;
}
```
- example usage
```shell
...
'''js
var FamousEngine = require('famous/core/FamousEngine');
var DOMElement = require('famous/dom-renderables/DOMElement');

FamousEngine.init();
var scene = FamousEngine.createScene();

var node = scene.addChild();
var domEl = new DOMElement(node, {
    content: 'Hello World',
    properties: {
        fontFamily: 'Arial'
    }
});
'''
...
```

#### <a name="apidoc.element.famous.Node.prototype.addComponent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>addComponent (component)](#apidoc.element.famous.Node.prototype.addComponent)
- description and source-code
```javascript
function addComponent(component) {
    var index = this._components.indexOf(component);
    if (index === -1) {
        index = this._freedComponentIndicies.length ? this._freedComponentIndicies.pop() : this._components.length;
        this._components[index] = component;

        if (this.isMounted() && component.onMount)
            component.onMount(this, index);

        if (this.isShown() && component.onShow)
            component.onShow();
    }

    return index;
}
```
- example usage
```shell
...
function Camera(node) {
    this._node = node;
    this._projectionType = Camera.ORTHOGRAPHIC_PROJECTION;
    this._focalDepth = 0;
    this._near = 0;
    this._far = 0;
    this._requestingUpdate = false;
    this._id = node.addComponent(this);
    this._viewTransform = new Float32Array([1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1]);
    this._viewDirty = false;
    this._perspectiveDirty = false;
    this.setFlat();
}

Camera.FRUSTUM_PROJECTION = 0;
...
```

#### <a name="apidoc.element.famous.Node.prototype.addUIEvent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>addUIEvent (eventName)](#apidoc.element.famous.Node.prototype.addUIEvent)
- description and source-code
```javascript
function addUIEvent(eventName) {
    var UIEvents = this.getUIEvents();
    var components = this._components;
    var component;

    var added = UIEvents.indexOf(eventName) !== -1;
    if (!added) {
        UIEvents.push(eventName);
        for (var i = 0, len = components.length ; i < len ; i++) {
            component = components[i];
            if (component && component.onAddUIEvent) component.onAddUIEvent(eventName);
        }
    }

    return this;
}
```
- example usage
```shell
...

    if (events) {
        for (i = 0, len = events.length; i < len; i++) {
            this.on(events[i], events[i].callback);
        }
    }

    node.addUIEvent('touchstart');
    node.addUIEvent('mousedown');
    node.addUIEvent('touchmove');
    node.addUIEvent('mousemove');
    node.addUIEvent('touchend');
    node.addUIEvent('mouseup');
    node.addUIEvent('mouseleave');
}
...
```

#### <a name="apidoc.element.famous.Node.prototype.dismount"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>dismount ()](#apidoc.element.famous.Node.prototype.dismount)
- description and source-code
```javascript
function dismount() {
    if (!this.isMounted())
        throw new Error('Node is not mounted');

    var path = this.getLocation();

    TransformSystem.deregisterTransformAtPath(path);
    SizeSystem.deregisterSizeAtPath(path);
    Dispatch.dismount(path);

    if (!this._requestingUpdate) this._requestUpdate();
}
```
- example usage
```shell
...
        components[i].onHide();
    }

    if (node.isMounted()) {
if (node.onDismount) node.onDismount(path);

for (i = 0, len = children.length ; i < len ; i++)
    if (children[i] && children[i].dismount) children[i].dismount();
    else if (children[i]) this.dismount(path + '/' + i);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onDismount)
        components[i].onDismount();

node._setMounted(false);
...
```

#### <a name="apidoc.element.famous.Node.prototype.emit"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>emit (event, payload)](#apidoc.element.famous.Node.prototype.emit)
- description and source-code
```javascript
function emit(event, payload) {
    Dispatch.dispatch(this.getLocation(), event, payload);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.getAbsoluteSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getAbsoluteSize ()](#apidoc.element.famous.Node.prototype.getAbsoluteSize)
- description and source-code
```javascript
function getAbsoluteSize() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._sizeID).getAbsolute();
    else if (this.isMounted())
        return SizeSystem.get(this.getLocation()).getAbsolute();
    else throw new Error('This node does not have access to a size component');
}
```
- example usage
```shell
...
function Size(node) {
this._node = node;
this._id = node.addComponent(this);
this._requestingUpdate = false;

var initialProportionalSize = node.getProportionalSize();
var initialDifferentialSize = node.getDifferentialSize();
var initialAbsoluteSize = node.getAbsoluteSize();

this._proportional = {
    x: new Transitionable(initialProportionalSize[0]),
    y: new Transitionable(initialProportionalSize[1]),
    z: new Transitionable(initialProportionalSize[2])
};
this._differential = {
...
```

#### <a name="apidoc.element.famous.Node.prototype.getAlign"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getAlign ()](#apidoc.element.famous.Node.prototype.getAlign)
- description and source-code
```javascript
function getAlign() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._transformID).getAlign();
    else if (this.isMounted())
        return TransformSystem.get(this.getLocation()).getAlign();
    else throw new Error('This node does not have access to a transform component');
}
```
- example usage
```shell
...
 * @augments Position
 *
 * @param {Node} node Node that the Align component will be attached to
 */
function Align(node) {
    Position.call(this, node);

    var initial = node.getAlign();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}

/**
...
```

#### <a name="apidoc.element.famous.Node.prototype.getChildren"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getChildren ()](#apidoc.element.famous.Node.prototype.getChildren)
- description and source-code
```javascript
function getChildren() {
    return this._fullChildren;
}
```
- example usage
```shell
...
 *
 * @method addChildrenToQueue
 * @return {void}
 *
 * @param {Node} node from which to add children to the queue
 */
Dispatch.prototype.addChildrenToQueue = function addChildrenToQueue (node) {
    var children = node.getChildren();
    var child;
    for (var i = 0, len = children.length ; i < len ; i++) {
        child = children[i];
        if (child) this._queue.push(child);
    }
};
...
```

#### <a name="apidoc.element.famous.Node.prototype.getComponent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getComponent (index)](#apidoc.element.famous.Node.prototype.getComponent)
- description and source-code
```javascript
function getComponent(index) {
    return this._components[index];
}
```
- example usage
```shell
...
*
* @method getMountPoint
*
* @return {Float32Array}   An array representing the mount point.
*/
Node.prototype.getMountPoint = function getMountPoint () {
   if (!this.constructor.NO_DEFAULT_COMPONENTS)
       return this.getComponent(this._transformID).getMountPoint();
   else if (this.isMounted())
       return TransformSystem.get(this.getLocation()).getMountPoint();
   else throw new Error('This node does not have access to a transform component');
};

/**
* Determines the node's previously set align.
...
```

#### <a name="apidoc.element.famous.Node.prototype.getComponents"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getComponents ()](#apidoc.element.famous.Node.prototype.getComponents)
- description and source-code
```javascript
function getComponents() {
    return this._components;
}
```
- example usage
```shell
...
if (!parent)
    throw new Error(
            'Parent to path: ' + path +
            ' doesn\'t exist at expected path: ' + parentPath
    );

var children = node.getChildren();
var components = node.getComponents();
var i;
var len;

if (parent.isMounted()) node._setMounted(true, path);
if (parent.isShown()) node._setShown(true);

if (parent.isMounted()) {
...
```

#### <a name="apidoc.element.famous.Node.prototype.getComputedValue"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getComputedValue ()](#apidoc.element.famous.Node.prototype.getComputedValue)
- description and source-code
```javascript
function getComputedValue() {
    console.warn('Node.getComputedValue is depricated. Use Node.getValue instead');
    var numberOfChildren = this._children.length;

    var value = {
        location: this.getId(),
        computedValues: {
            transform: this.isMounted() ? TransformSystem.get(this.getLocation()).getLocalTransform() : null,
            size: this.isMounted() ? SizeSystem.get(this.getLocation()).get() : null
        },
        children: []
    };

    for (var i = 0 ; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getComputedValue)
            value.children.push(this._children[i].getComputedValue());

    return value;
}
```
- example usage
```shell
...
           size: this.isMounted() ? SizeSystem.get(this.getLocation()).get() : null
       },
       children: []
   };

   for (var i = 0 ; i < numberOfChildren ; i++)
       if (this._children[i] && this._children[i].getComputedValue)
           value.children.push(this._children[i].getComputedValue());

   return value;
};

/**
* Retrieves all children of the current node.
*
...
```

#### <a name="apidoc.element.famous.Node.prototype.getDifferentialSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getDifferentialSize ()](#apidoc.element.famous.Node.prototype.getDifferentialSize)
- description and source-code
```javascript
function getDifferentialSize() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._sizeID).getDifferential();
    else if (this.isMounted())
        return SizeSystem.get(this.getLocation()).getDifferential();
    else throw new Error('This node does not have access to a size component');
}
```
- example usage
```shell
...
 */
function Size(node) {
this._node = node;
this._id = node.addComponent(this);
this._requestingUpdate = false;

var initialProportionalSize = node.getProportionalSize();
var initialDifferentialSize = node.getDifferentialSize();
var initialAbsoluteSize = node.getAbsoluteSize();

this._proportional = {
    x: new Transitionable(initialProportionalSize[0]),
    y: new Transitionable(initialProportionalSize[1]),
    z: new Transitionable(initialProportionalSize[2])
};
...
```

#### <a name="apidoc.element.famous.Node.prototype.getFrame"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getFrame ()](#apidoc.element.famous.Node.prototype.getFrame)
- description and source-code
```javascript
function getFrame() {
    return this._updater.getFrame();
}
```
- example usage
```shell
...
* Method for getting the current frame. Will be deprecated.
*
* @method
*
* @return {Number} current frame
*/
Node.prototype.getFrame = function getFrame () {
   return this._updater.getFrame();
};

/**
* returns an array of the components currently attached to this
* node.
*
* @method getComponents
...
```

#### <a name="apidoc.element.famous.Node.prototype.getId"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getId ()](#apidoc.element.famous.Node.prototype.getId)
- description and source-code
```javascript
function getLocation() {
    return this._id;
}
```
- example usage
```shell
...
 */
Node.prototype.getValue = function getValue () {
var numberOfChildren = this._children.length;
var numberOfComponents = this._components.length;
var i = 0;

var value = {
    location: this.getId(),
    spec: {
        location: this.getId(),
        showState: {
            mounted: this.isMounted(),
            shown: this.isShown(),
            opacity: this.getOpacity() || null
        },
...
```

#### <a name="apidoc.element.famous.Node.prototype.getLocation"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getLocation ()](#apidoc.element.famous.Node.prototype.getLocation)
- description and source-code
```javascript
function getLocation() {
    return this._id;
}
```
- example usage
```shell
...
 * @method
 *
 * @return {undefined} undefined
 */
Camera.prototype.onUpdate = function onUpdate() {
this._requestingUpdate = false;

var path = this._node.getLocation();

this._node
    .sendDrawCommand(Commands.WITH)
    .sendDrawCommand(path);

if (this._perspectiveDirty) {
    this._perspectiveDirty = false;
...
```

#### <a name="apidoc.element.famous.Node.prototype.getMountPoint"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getMountPoint ()](#apidoc.element.famous.Node.prototype.getMountPoint)
- description and source-code
```javascript
function getMountPoint() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._transformID).getMountPoint();
    else if (this.isMounted())
        return TransformSystem.get(this.getLocation()).getMountPoint();
    else throw new Error('This node does not have access to a transform component');
}
```
- example usage
```shell
...
 * @augments Position
 *
* @param {Node} node Node that the MountPoint component will be attached to
 */
function MountPoint(node) {
    Position.call(this, node);

    var initial = node.getMountPoint();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}

/**
...
```

#### <a name="apidoc.element.famous.Node.prototype.getOpacity"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getOpacity ()](#apidoc.element.famous.Node.prototype.getOpacity)
- description and source-code
```javascript
function getOpacity() {
    return this._opacity;
}
```
- example usage
```shell
...
    var value = {
location: this.getId(),
spec: {
    location: this.getId(),
    showState: {
        mounted: this.isMounted(),
        shown: this.isShown(),
        opacity: this.getOpacity() || null
    },
    offsets: {
        mountPoint: [0, 0, 0],
        align: [0, 0, 0],
        origin: [0, 0, 0]
    },
    vectors: {
...
```

#### <a name="apidoc.element.famous.Node.prototype.getOrigin"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getOrigin ()](#apidoc.element.famous.Node.prototype.getOrigin)
- description and source-code
```javascript
function getOrigin() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._transformID).getOrigin();
    else if (this.isMounted())
        return TransformSystem.get(this.getLocation()).getOrigin();
    else throw new Error('This node does not have access to a transform component');
}
```
- example usage
```shell
...
 * @augments Position
 *
 * @param {Node} node Node that the Origin component will be attached to
 */
function Origin(node) {
    Position.call(this, node);

    var initial = node.getOrigin();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}

/**
...
```

#### <a name="apidoc.element.famous.Node.prototype.getParent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getParent ()](#apidoc.element.famous.Node.prototype.getParent)
- description and source-code
```javascript
function getParent() {
    return this._parent;
}
```
- example usage
```shell
...
            components = node.getComponents();

            for (i = 0, len = components.length ; i < len ; i++)
                if (components[i] && components[i].onReceive)
                    components[i].onReceive(event, payload);

            if (payload.propagationStopped) break;
            parent = node.getParent();
            if (parent === node) return;
            node = parent;
        }
    }
};

/**
...
```

#### <a name="apidoc.element.famous.Node.prototype.getPosition"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getPosition ()](#apidoc.element.famous.Node.prototype.getPosition)
- description and source-code
```javascript
function getPosition() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._transformID).getPosition();
    else if (this.isMounted())
        return TransformSystem.get(this.getLocation()).getPosition();
    else throw new Error('This node does not have access to a transform component');
}
```
- example usage
```shell
...
 */
function Position(node) {
    this._node = node;
    this._id = node.addComponent(this);

    this._requestingUpdate = false;

    var initialPosition = node.getPosition();

    this._x = new Transitionable(initialPosition[0]);
    this._y = new Transitionable(initialPosition[1]);
    this._z = new Transitionable(initialPosition[2]);
}

/**
...
```

#### <a name="apidoc.element.famous.Node.prototype.getProportionalSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getProportionalSize ()](#apidoc.element.famous.Node.prototype.getProportionalSize)
- description and source-code
```javascript
function getProportionalSize() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._sizeID).getProportional();
    else if (this.isMounted())
        return SizeSystem.get(this.getLocation()).getProportional();
    else throw new Error('This node does not have access to a size component');
}
```
- example usage
```shell
...
 * @param {Node} node Node that the Size component is attached to
 */
function Size(node) {
this._node = node;
this._id = node.addComponent(this);
this._requestingUpdate = false;

var initialProportionalSize = node.getProportionalSize();
var initialDifferentialSize = node.getDifferentialSize();
var initialAbsoluteSize = node.getAbsoluteSize();

this._proportional = {
    x: new Transitionable(initialProportionalSize[0]),
    y: new Transitionable(initialProportionalSize[1]),
    z: new Transitionable(initialProportionalSize[2])
...
```

#### <a name="apidoc.element.famous.Node.prototype.getRawChildren"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getRawChildren ()](#apidoc.element.famous.Node.prototype.getRawChildren)
- description and source-code
```javascript
function getRawChildren() {
    return this._children;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.getRenderSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getRenderSize ()](#apidoc.element.famous.Node.prototype.getRenderSize)
- description and source-code
```javascript
function getRenderSize() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._sizeID).getRender();
    else if (this.isMounted())
        return SizeSystem.get(this.getLocation()).getRender();
    else throw new Error('This node does not have access to a size component');
}
```
- example usage
```shell
...
 * @param {Node} node Node to potentially call onRenderSizeChange on
 * @param {Array} components a list of the nodes' components
 * @param {Size} size the size class for the Node
 *
 * @return {undefined} undefined
 */
function renderSizeChanged (node, components, size) {
var renderSize = size.getRenderSize();
var x = renderSize[0];
var y = renderSize[1];
var z = renderSize[2];
if (node.onRenderSizeChange) node.onRenderSizeChange(x, y, z);
for (var i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onRenderSizeChange)
        components[i].onRenderSizeChange(x, y, z);
...
```

#### <a name="apidoc.element.famous.Node.prototype.getRotation"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getRotation ()](#apidoc.element.famous.Node.prototype.getRotation)
- description and source-code
```javascript
function getRotation() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._transformID).getRotation();
    else if (this.isMounted())
        return TransformSystem.get(this.getLocation()).getRotation();
    else throw new Error('This node does not have access to a transform component');
}
```
- example usage
```shell
...
 * @augments Position
 *
 * @param {Node} node Node that the Rotation component will be attached to
 */
function Rotation(node) {
Position.call(this, node);

var initial = node.getRotation();

var x = initial[0];
var y = initial[1];
var z = initial[2];
var w = initial[3];

var xx = x * x;
...
```

#### <a name="apidoc.element.famous.Node.prototype.getScale"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getScale ()](#apidoc.element.famous.Node.prototype.getScale)
- description and source-code
```javascript
function getScale() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._transformID).getScale();
    else if (this.isMounted())
        return TransformSystem.get(this.getLocation()).getScale();
    else throw new Error('This node does not have access to a transform component');
}
```
- example usage
```shell
...
    }
    this.align.set(x, y, z, options, callback);
    return this;
};

Transform.prototype.setScale = function setScale(x, y, z, options, callback) {
    if (!this.scale) {
        var v = this._node.getScale();
        this.scale = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.scale.set(x, y, z, options, callback);
    return this;
};

Transform.prototype.setPosition = function setPosition(x, y, z, options, callback) {
...
```

#### <a name="apidoc.element.famous.Node.prototype.getSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getSize ()](#apidoc.element.famous.Node.prototype.getSize)
- description and source-code
```javascript
function getSize() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._sizeID).get();
    else if (this.isMounted())
        return SizeSystem.get(this.getLocation()).get();
    else throw new Error('This node does not have access to a size component');
}
```
- example usage
```shell
...
* Retrieves the computed size applied to the underlying Node.
*
* @method
*
* @return {Array} size three dimensional computed size
*/
Size.prototype.get = function get () {
   return this._node.getSize();
};

/**
* Halts all currently active size transitions.
*
* @method
*
...
```

#### <a name="apidoc.element.famous.Node.prototype.getSizeMode"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getSizeMode ()](#apidoc.element.famous.Node.prototype.getSizeMode)
- description and source-code
```javascript
function getSizeMode() {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        return this.getComponent(this._sizeID).getSizeMode();
    else if (this.isMounted())
        return SizeSystem.get(this.getLocation()).getSizeMode();
    else throw new Error('This node does not have access to a size component');
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the internal state of the component
 */
Size.prototype.getValue = function getValue() {
return {
    sizeMode: SizeSystem.get(this._node.getLocation()).getSizeMode(),
    absolute: {
        x: this._absolute.x.get(),
        y: this._absolute.y.get(),
        z: this._absolute.z.get()
    },
    differential: {
        x: this._differential.x.get(),
...
```

#### <a name="apidoc.element.famous.Node.prototype.getTransform"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getTransform ()](#apidoc.element.famous.Node.prototype.getTransform)
- description and source-code
```javascript
function getTransform() {
    return TransformSystem.get(this.getLocation());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.getUIEvents"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getUIEvents ()](#apidoc.element.famous.Node.prototype.getUIEvents)
- description and source-code
```javascript
function getUIEvents() {
    return this._UIEvents;
}
```
- example usage
```shell
...
 * @method
 *
 * @param {String} eventName the name of the event
 *
 * @return {undefined} undefined
 */
Node.prototype.removeUIEvent = function removeUIEvent (eventName) {
var UIEvents = this.getUIEvents();
var components = this._components;
var component;

var index = UIEvents.indexOf(eventName);
if (index !== -1) {
    UIEvents.splice(index, 1);
    for (var i = 0, len = components.length ; i < len ; i++) {
...
```

#### <a name="apidoc.element.famous.Node.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>getValue ()](#apidoc.element.famous.Node.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    var numberOfChildren = this._children.length;
    var numberOfComponents = this._components.length;
    var i = 0;

    var value = {
        location: this.getId(),
        spec: {
            location: this.getId(),
            showState: {
                mounted: this.isMounted(),
                shown: this.isShown(),
                opacity: this.getOpacity() || null
            },
            offsets: {
                mountPoint: [0, 0, 0],
                align: [0, 0, 0],
                origin: [0, 0, 0]
            },
            vectors: {
                position: [0, 0, 0],
                rotation: [0, 0, 0, 1],
                scale: [1, 1, 1]
            },
            size: {
                sizeMode: [0, 0, 0],
                proportional: [1, 1, 1],
                differential: [0, 0, 0],
                absolute: [0, 0, 0],
                render: [0, 0, 0]
            }
        },
        UIEvents: this._UIEvents,
        components: [],
        children: []
    };

    if (value.location) {
        var transform = TransformSystem.get(this.getId());
        var size = SizeSystem.get(this.getId());

        for (i = 0 ; i < 3 ; i++) {
            value.spec.offsets.mountPoint[i] = transform.offsets.mountPoint[i];
            value.spec.offsets.align[i] = transform.offsets.align[i];
            value.spec.offsets.origin[i] = transform.offsets.origin[i];
            value.spec.vectors.position[i] = transform.vectors.position[i];
            value.spec.vectors.rotation[i] = transform.vectors.rotation[i];
            value.spec.vectors.scale[i] = transform.vectors.scale[i];
            value.spec.size.sizeMode[i] = size.sizeMode[i];
            value.spec.size.proportional[i] = size.proportionalSize[i];
            value.spec.size.differential[i] = size.differentialSize[i];
            value.spec.size.absolute[i] = size.absoluteSize[i];
            value.spec.size.render[i] = size.renderSize[i];
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Node.prototype.hide"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>hide ()](#apidoc.element.famous.Node.prototype.hide)
- description and source-code
```javascript
function hide() {
    Dispatch.hide(this.getLocation());
    this._shown = false;
    return this;
}
```
- example usage
```shell
...
           components[i].onHide();


   this.addChildrenToQueue(node);
   var child;

   while ((child = this.breadthFirstNext()))
       this.hide(child.getLocation());

};

/**
* lookupNode takes a path and returns the node at the location specified
* by the path, if one exists. If not, it returns undefined.
*
...
```

#### <a name="apidoc.element.famous.Node.prototype.isMounted"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>isMounted ()](#apidoc.element.famous.Node.prototype.isMounted)
- description and source-code
```javascript
function isMounted() {
    return this._mounted;
}
```
- example usage
```shell
...
);

    var children = node.getChildren();
    var components = node.getComponents();
    var i;
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
...
```

#### <a name="apidoc.element.famous.Node.prototype.isRendered"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>isRendered ()](#apidoc.element.famous.Node.prototype.isRendered)
- description and source-code
```javascript
function isRendered() {
    return this._mounted && this._shown;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.isShown"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>isShown ()](#apidoc.element.famous.Node.prototype.isShown)
- description and source-code
```javascript
function isShown() {
    return this._shown;
}
```
- example usage
```shell
...

    var children = node.getChildren();
    var components = node.getComponents();
    var i;
    var len;

    if (parent.isMounted()) node._setMounted(true, path);
    if (parent.isShown()) node._setShown(true);

    if (parent.isMounted()) {
node._setParent(parent);
if (node.onMount) node.onMount(path);

for (i = 0, len = components.length ; i < len ; i++)
    if (components[i] && components[i].onMount)
...
```

#### <a name="apidoc.element.famous.Node.prototype.mount"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>mount (path)](#apidoc.element.famous.Node.prototype.mount)
- description and source-code
```javascript
function mount(path) {
    if (this.isMounted())
        throw new Error('Node is already mounted at: ' + this.getLocation());

    if (!this.constructor.NO_DEFAULT_COMPONENTS){
        TransformSystem.registerTransformAtPath(path, this.getComponent(this._transformID));
        SizeSystem.registerSizeAtPath(path, this.getComponent(this._sizeID));
    }
    else {
        TransformSystem.registerTransformAtPath(path);
        SizeSystem.registerSizeAtPath(path);
    }
    Dispatch.mount(path, this);

    if (!this._requestingUpdate) this._requestUpdate();
    return this;

}
```
- example usage
```shell
...
    if (node.onMount) node.onMount(path);

    for (i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onMount)
            components[i].onMount(node, i);

    for (i = 0, len = children.length ; i < len ; i++)
        if (children[i] && children[i].mount) children[i].mount(path + '/' + i);
        else if (children[i]) this.mount(path + '/' + i, children[i]);
}

if (parent.isShown()) {
    if (node.onShow) node.onShow();
    for (i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onShow)
...
```

#### <a name="apidoc.element.famous.Node.prototype.removeChild"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>removeChild (child)](#apidoc.element.famous.Node.prototype.removeChild)
- description and source-code
```javascript
function removeChild(child) {
    var index = this._children.indexOf(child);

    if (index > - 1) {
        this._freedChildIndicies.push(index);

        this._children[index] = null;

        if (child.isMounted()) child.dismount();

        var fullChildrenIndex = this._fullChildren.indexOf(child);
        var len = this._fullChildren.length;
        var i = 0;

        for (i = fullChildrenIndex; i < len-1; i++)
            this._fullChildren[i] = this._fullChildren[i + 1];

        this._fullChildren.pop();

        return true;
    }
    else {
        return false;
    }
}
```
- example usage
```shell
...
*
* @param {Node} parent The node to set as the parent of this
*
* @return {undefined} undefined;
*/
Node.prototype._setParent = function _setParent (parent) {
   if (this._parent && this._parent.getChildren().indexOf(this) !== -1) {
       this._parent.removeChild(this);
   }
   this._parent = parent;
};

/**
* Protected method. Sets the mount state of the node. Should only be called
* by the dispatch
...
```

#### <a name="apidoc.element.famous.Node.prototype.removeComponent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>removeComponent (component)](#apidoc.element.famous.Node.prototype.removeComponent)
- description and source-code
```javascript
function removeComponent(component) {
    var index = this._components.indexOf(component);
    if (index !== -1) {
        this._freedComponentIndicies.push(index);
        if (this.isShown() && component.onHide)
            component.onHide();

        if (this.isMounted() && component.onDismount)
            component.onDismount();

        this._components[index] = null;
    }
    return component;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.removeUIEvent"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>removeUIEvent (eventName)](#apidoc.element.famous.Node.prototype.removeUIEvent)
- description and source-code
```javascript
function removeUIEvent(eventName) {
    var UIEvents = this.getUIEvents();
    var components = this._components;
    var component;

    var index = UIEvents.indexOf(eventName);
    if (index !== -1) {
        UIEvents.splice(index, 1);
        for (var i = 0, len = components.length ; i < len ; i++) {
            component = components[i];
            if (component && component.onRemoveUIEvent) component.onRemoveUIEvent(eventName);
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Node.prototype.requestUpdate"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>requestUpdate (requester)](#apidoc.element.famous.Node.prototype.requestUpdate)
- description and source-code
```javascript
function requestUpdate(requester) {
    if (this._inUpdate || !this.isMounted())
        return this.requestUpdateOnNextTick(requester);
    if (this._updateQueue.indexOf(requester) === -1) {
        this._updateQueue.push(requester);
        if (!this._requestingUpdate) this._requestUpdate();
    }
    return this;
}
```
- example usage
```shell
...
 * @param {Number} near the distance of the near clipping plane for a frustum projection
 * @param {Number} far the distance of the far clipping plane for a frustum projection
 *
 * @return {Boolean} status of the set
 */
Camera.prototype.set = function set(type, depth, near, far) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }
    this._projectionType = type;
    this._focalDepth = depth;
    this._near = near;
    this._far = far;
};
...
```

#### <a name="apidoc.element.famous.Node.prototype.requestUpdateOnNextTick"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>requestUpdateOnNextTick (requester)](#apidoc.element.famous.Node.prototype.requestUpdateOnNextTick)
- description and source-code
```javascript
function requestUpdateOnNextTick(requester) {
    if (this._nextUpdateQueue.indexOf(requester) === -1)
        this._nextUpdateQueue.push(requester);
    return this;
}
```
- example usage
```shell
...
 *
 * @return {undefined} undefined
 */
Opacity.prototype.update = function update () {
    this._node.setOpacity(this._value.get());

    if (this._value.isActive()) {
      this._node.requestUpdateOnNextTick(this._id);
    }
    else {
      this._requestingUpdate = false;
    }
};

Opacity.prototype.onUpdate = Opacity.prototype.update;
...
```

#### <a name="apidoc.element.famous.Node.prototype.sendDrawCommand"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>sendDrawCommand (message)](#apidoc.element.famous.Node.prototype.sendDrawCommand)
- description and source-code
```javascript
function sendDrawCommand(message) {
    this._updater.message(message);
    return this;
}
```
- example usage
```shell
...
 */
Camera.prototype.onUpdate = function onUpdate() {
    this._requestingUpdate = false;

    var path = this._node.getLocation();

    this._node
.sendDrawCommand(Commands.WITH)
.sendDrawCommand(path);

    if (this._perspectiveDirty) {
this._perspectiveDirty = false;

switch (this._projectionType) {
    case Camera.FRUSTUM_PROJECTION:
...
```

#### <a name="apidoc.element.famous.Node.prototype.setAbsoluteSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setAbsoluteSize (x, y, z)](#apidoc.element.famous.Node.prototype.setAbsoluteSize)
- description and source-code
```javascript
function setAbsoluteSize(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._sizeID).setAbsolute(x, y, z);
    else if (this.isMounted())
        SizeSystem.get(this.getLocation()).setAbsolute(x, y, z);
    else throw new Error('This node does not have access to a size component');
    return this;
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {undefined} undefined
 */
Size.prototype.onUpdate = function onUpdate() {
var abs = this._absolute;
this._node.setAbsoluteSize(
    abs.x.get(),
    abs.y.get(),
    abs.z.get()
);
var prop = this._proportional;
var diff = this._differential;
this._node.setProportionalSize(
...
```

#### <a name="apidoc.element.famous.Node.prototype.setAlign"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setAlign (x, y, z)](#apidoc.element.famous.Node.prototype.setAlign)
- description and source-code
```javascript
function setAlign(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._transformID).setAlign(x, y, z);
    else if (this.isMounted())
        TransformSystem.get(this.getLocation()).setAlign(x, y, z);
    else throw new Error('This node does not have access to a transform component');
    return this;
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Node.prototype.setDifferentialSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setDifferentialSize (x, y, z)](#apidoc.element.famous.Node.prototype.setDifferentialSize)
- description and source-code
```javascript
function setDifferentialSize(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._sizeID).setDifferential(x, y, z);
    else if (this.isMounted())
        SizeSystem.get(this.getLocation()).setDifferential(x, y, z);
    else throw new Error('This node does not have access to a size component');
    return this;
}
```
- example usage
```shell
...
var prop = this._proportional;
var diff = this._differential;
this._node.setProportionalSize(
    prop.x.get(),
    prop.y.get(),
    prop.z.get()
);
this._node.setDifferentialSize(
    diff.x.get(),
    diff.y.get(),
    diff.z.get()
);

if (this.isActive()) this._node.requestUpdateOnNextTick(this._id);
else this._requestingUpdate = false;
...
```

#### <a name="apidoc.element.famous.Node.prototype.setMountPoint"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setMountPoint (x, y, z)](#apidoc.element.famous.Node.prototype.setMountPoint)
- description and source-code
```javascript
function setMountPoint(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._transformID).setMountPoint(x, y, z);
    else if (this.isMounted())
        TransformSystem.get(this.getLocation()).setMountPoint(x, y, z);
    else throw new Error('This node does not have access to a transform component');
    return this;
}
```
- example usage
```shell
...
 * of the Node's mount point.
 *
 * @method
 *
 * @return {undefined} undefined
 */
MountPoint.prototype.update = function update() {
    this._node.setMountPoint(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

MountPoint.prototype.onUpdate = MountPoint.prototype.update;

module.exports = MountPoint;
...
```

#### <a name="apidoc.element.famous.Node.prototype.setOpacity"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setOpacity (val)](#apidoc.element.famous.Node.prototype.setOpacity)
- description and source-code
```javascript
function setOpacity(val) {
    if (val !== this._opacity) {
        this._opacity = val;
        if (!this._requestingUpdate) this._requestUpdate();

        var i = 0;
        var list = this._components;
        var len = list.length;
        var item;
        for (; i < len ; i++) {
            item = list[i];
            if (item && item.onOpacityChange) item.onOpacityChange(val);
        }
    }
    return this;
}
```
- example usage
```shell
...
 * of the Node's opacity.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Opacity.prototype.update = function update () {
this._node.setOpacity(this._value.get());

if (this._value.isActive()) {
  this._node.requestUpdateOnNextTick(this._id);
}
else {
  this._requestingUpdate = false;
}
...
```

#### <a name="apidoc.element.famous.Node.prototype.setOrigin"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setOrigin (x, y, z)](#apidoc.element.famous.Node.prototype.setOrigin)
- description and source-code
```javascript
function setOrigin(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._transformID).setOrigin(x, y, z);
    else if (this.isMounted())
        TransformSystem.get(this.getLocation()).setOrigin(x, y, z);
    else throw new Error('This node does not have access to a transform component');
    return this;
}
```
- example usage
```shell
...
 * of the Node's origin
 *
 * @method
 *
 * @return {undefined} undefined
 */
Origin.prototype.update = function update() {
    this._node.setOrigin(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Origin.prototype.onUpdate = Origin.prototype.update;

module.exports = Origin;
...
```

#### <a name="apidoc.element.famous.Node.prototype.setPosition"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setPosition (x, y, z)](#apidoc.element.famous.Node.prototype.setPosition)
- description and source-code
```javascript
function setPosition(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._transformID).setPosition(x, y, z);
    else if (this.isMounted())
        TransformSystem.get(this.getLocation()).setPosition(x, y, z);
    else throw new Error('This node does not have access to a transform component');
    return this;
}
```
- example usage
```shell
...
* of the Node's position
*
* @method
*
* @return {undefined} undefined
*/
Position.prototype.update = function update () {
   this._node.setPosition(this._x.get(), this._y.get(), this._z.get());
   this._checkUpdate();
};

Position.prototype.onUpdate = Position.prototype.update;

/**
* Setter for X position
...
```

#### <a name="apidoc.element.famous.Node.prototype.setProportionalSize"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setProportionalSize (x, y, z)](#apidoc.element.famous.Node.prototype.setProportionalSize)
- description and source-code
```javascript
function setProportionalSize(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._sizeID).setProportional(x, y, z);
    else if (this.isMounted())
        SizeSystem.get(this.getLocation()).setProportional(x, y, z);
    else throw new Error('This node does not have access to a size component');
    return this;
}
```
- example usage
```shell
...
this._node.setAbsoluteSize(
    abs.x.get(),
    abs.y.get(),
    abs.z.get()
);
var prop = this._proportional;
var diff = this._differential;
this._node.setProportionalSize(
    prop.x.get(),
    prop.y.get(),
    prop.z.get()
);
this._node.setDifferentialSize(
    diff.x.get(),
    diff.y.get(),
...
```

#### <a name="apidoc.element.famous.Node.prototype.setRotation"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setRotation (x, y, z, w)](#apidoc.element.famous.Node.prototype.setRotation)
- description and source-code
```javascript
function setRotation(x, y, z, w) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._transformID).setRotation(x, y, z, w);
    else if (this.isMounted())
        TransformSystem.get(this.getLocation()).setRotation(x, y, z, w);
    else throw new Error('This node does not have access to a transform component');
    return this;
}
```
- example usage
```shell
...
 * of the Node's rotation
 *
 * @method
 *
 * @return {undefined} undefined
 */
Rotation.prototype.update = function update() {
    this._node.setRotation(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Rotation.prototype.onUpdate = Rotation.prototype.update;

module.exports = Rotation;
...
```

#### <a name="apidoc.element.famous.Node.prototype.setScale"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setScale (x, y, z)](#apidoc.element.famous.Node.prototype.setScale)
- description and source-code
```javascript
function setScale(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._transformID).setScale(x, y, z);
    else if (this.isMounted())
        TransformSystem.get(this.getLocation()).setScale(x, y, z);
    else throw new Error('This node does not have access to a transform component');
    return this;
}
```
- example usage
```shell
...
 * of the Node's scale.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Scale.prototype.update = function update() {
    this._node.setScale(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Scale.prototype.onUpdate = Scale.prototype.update;

module.exports = Scale;
...
```

#### <a name="apidoc.element.famous.Node.prototype.setSizeMode"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>setSizeMode (x, y, z)](#apidoc.element.famous.Node.prototype.setSizeMode)
- description and source-code
```javascript
function setSizeMode(x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._sizeID).setSizeMode(x, y, z);
    else if (this.isMounted())
        SizeSystem.get(this.getLocation()).setSizeMode(x, y, z);
    else throw new Error('This node does not have access to a size component');
    return this;
}
```
- example usage
```shell
...
* @param {Number} x the mode of size for the width
* @param {Number} y the mode of size for the height
* @param {Number} z the mode of size for the depth
*
* @return {Size} this
*/
Size.prototype.setMode = function setMode(x, y, z) {
   this._node.setSizeMode(x, y, z);
   return this;
};

/**
* Return the name of the Size component
*
* @method
...
```

#### <a name="apidoc.element.famous.Node.prototype.show"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>show ()](#apidoc.element.famous.Node.prototype.show)
- description and source-code
```javascript
function show() {
    Dispatch.show(this.getLocation());
    this._shown = true;
    return this;
}
```
- example usage
```shell
...
           components[i].onShow();


   this.addChildrenToQueue(node);
   var child;

   while ((child = this.breadthFirstNext()))
       this.show(child.getLocation());

};

/**
* Issues the onHide method to the node registered at the given path,
* and hides the entire subtree below that node. Throws if no node
* is registered to this path.
...
```

#### <a name="apidoc.element.famous.Node.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Node.prototype.</span>update (time)](#apidoc.element.famous.Node.prototype.update)
- description and source-code
```javascript
function update(time){
    this._inUpdate = true;
    var nextQueue = this._nextUpdateQueue;
    var queue = this._updateQueue;
    var item;

    while (nextQueue.length) queue.unshift(nextQueue.pop());

    while (queue.length) {
        item = this._components[queue.shift()];
        if (item && item.onUpdate) item.onUpdate(time);
    }

    this._inUpdate = false;
    this._requestingUpdate = false;

    if (!this.isMounted()) {
        // last update
        this._parent = null;
        this._id = null;
    }
    else if (this._nextUpdateQueue.length) {
        this._updater.requestUpdateOnNextTick(this);
        this._requestingUpdate = true;
    }
    return this;
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.OBJLoader"></a>[module famous.OBJLoader](#apidoc.module.famous.OBJLoader)

#### <a name="apidoc.element.famous.OBJLoader._onsuccess"></a>[function <span class="apidocSignatureSpan">famous.OBJLoader.</span>_onsuccess (url, options, text)](#apidoc.element.famous.OBJLoader._onsuccess)
- description and source-code
```javascript
function _onsuccess(url, options, text) {
    var buffers = format.call(this, text, options || {});
    this.cached[url] = buffers;

    for (var i = 0; i < this.requests[url].length; i++) {
        this.requests[url][i](buffers);
    }

    this.requests[url] = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.OBJLoader.formatText"></a>[function <span class="apidocSignatureSpan">famous.OBJLoader.</span>formatText (text, options)](#apidoc.element.famous.OBJLoader.formatText)
- description and source-code
```javascript
function format(text, options) {
    text = sanitize(text);

    var lines = text.split('\n');

    var geometries = [];
    options = options || {};

    var faceTexCoords = [];
    var faceVertices = [];
    var faceNormals = [];

    var normals = [];
    var texCoords = [];
    var vertices = [];

    var i1, i2, i3, i4;
    var split;
    var line;

    var length = lines.length;

    for (var i = 0; i < length; i++) {
        line = lines[i];
        split = lines[i].trim().split(' ');

        // Handle vertex positions

        if (line.indexOf('v ') !== -1) {
            vertices.push([
                parseFloat(split[1]),
                parseFloat(split[2]),
                parseFloat(split[3])
            ]);
        }

        // Handle texture coordinates

        else if(line.indexOf('vt ') !== -1) {
            texCoords.push([
                parseFloat(split[1]),
                parseFloat(split[2])
            ]);
        }

        // Handle vertex normals

        else if (line.indexOf('vn ') !== -1) {
            normals.push([
                parseFloat(split[1]),
                parseFloat(split[2]),
                parseFloat(split[3])
            ]);
        }

        // Handle face

        else if (line.indexOf('f ') !== -1) {

            // Vertex, Normal

            if (split[1].indexOf('//') !== -1) {
                i1 = split[1].split('//');
                i2 = split[2].split('//');
                i3 = split[3].split('//');

                faceVertices.push([
                    parseFloat(i1[0]) - 1,
                    parseFloat(i2[0]) - 1,
                    parseFloat(i3[0]) - 1
                ]);
                faceNormals.push([
                    parseFloat(i1[1]) - 1,
                    parseFloat(i2[1]) - 1,
                    parseFloat(i3[1]) - 1
                ]);

                // Handle quad

                if (split[4]) {
                    i4 = split[4].split('//');
                    faceVertices.push([
                        parseFloat(i1[0]) - 1,
                        parseFloat(i3[0]) - 1,
                        parseFloat(i4[0]) - 1
                    ]);
                    faceNormals.push([
                        parseFloat(i1[2]) - 1,
                        parseFloat(i3[2]) - 1,
                        parseFloat(i4[2]) - 1
                    ]);
                }
            }

            // Vertex, TexCoord, Normal

            else if (split[1].indexOf('/') !== -1) {
                i1 = split[1].split('/');
                i2 = split[2].split('/');
                i3 = split[3].split('/');

                faceVertices.push([
                    parseFloat(i1[0]) - 1,
                    parseFloat(i2[0]) - 1,
                    parseFloat(i3[0]) - 1
                ]);
                faceTexCoords.push([
                    parseFloat(i1[1]) - 1,
                    parseFloat(i2[1]) - 1,
                    parseFloat(i3[1]) - 1
                ]);
                faceNormals.push([
                    parseFloat(i1[2]) - 1,
                    parseFloat(i2[2]) - 1,
                    parseFloat(i3[2]) - 1
                ]);

                // Handle Quad

                if (split[4]) {
                    i4 = split[4].split('/');

                    faceVertices.push([
                        parseFloat(i1[0]) - 1,
                        parseFloat(i3[0]) - 1,
                        parseFloat(i4[0]) - 1
                    ]);
                    faceTexCoords.push([
                        parseFloat(i1[1]) - 1,
                        parseFloat(i3[1]) - 1,
                        parseFloat(i4[1]) - 1
                    ]);
                    faceNormals.push([
                        parseFloat(i1[2]) - 1,
                        parseFloat(i3[2]) - 1,
                        parseFloat(i4[2]) - 1
                    ]);
                }
            }

            // Vertex

            else {
                faceVertices.push([
                    parseFloat(split[1]) - 1,
                    parseFloat(spli ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.OBJLoader.load"></a>[function <span class="apidocSignatureSpan">famous.OBJLoader.</span>load (url, cb, options)](#apidoc.element.famous.OBJLoader.load)
- description and source-code
```javascript
function load(url, cb, options) {
    if (!this.cached[url]) {
        if (!this.requests[url]) {
            this.requests[url] = [cb];
            loadURL(
                url,
                this._onsuccess.bind(
                    this,
                    url,
                    options
                )
            );
        }
        else {
            this.requests[url].push(cb);
        }
    }
    else {
        cb(this.cached[url]);
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.ObjectManager"></a>[module famous.ObjectManager](#apidoc.module.famous.ObjectManager)

#### <a name="apidoc.element.famous.ObjectManager.disposeOf"></a>[function <span class="apidocSignatureSpan">famous.ObjectManager.</span>disposeOf (type)](#apidoc.element.famous.ObjectManager.disposeOf)
- description and source-code
```javascript
disposeOf = function (type) {
    var pool = this.pools[type];
    var i = pool.length;
    while (i--) pool.pop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.ObjectManager.freeDynamicGeometry"></a>[function <span class="apidocSignatureSpan">famous.ObjectManager.</span>freeDynamicGeometry (obj)](#apidoc.element.famous.ObjectManager.freeDynamicGeometry)
- description and source-code
```javascript
function free(obj) {
    pool.push(obj);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.ObjectManager.freeDynamicGeometryFeature"></a>[function <span class="apidocSignatureSpan">famous.ObjectManager.</span>freeDynamicGeometryFeature (obj)](#apidoc.element.famous.ObjectManager.freeDynamicGeometryFeature)
- description and source-code
```javascript
function free(obj) {
    pool.push(obj);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.ObjectManager.register"></a>[function <span class="apidocSignatureSpan">famous.ObjectManager.</span>register (type, Constructor)](#apidoc.element.famous.ObjectManager.register)
- description and source-code
```javascript
register = function (type, Constructor) {
    var pool = this.pools[type] = [];

    this['request' + type] = _request(pool, Constructor);
    this['free' + type] = _free(pool);
}
```
- example usage
```shell
...

'use strict';

var Vec3 = require('../math/Vec3');
var Mat33 = require('../math/Mat33');

var ObjectManager = require('../utilities/ObjectManager');
ObjectManager.register('DynamicGeometry', DynamicGeometry);
ObjectManager.register('DynamicGeometryFeature', DynamicGeometryFeature);
var oMRequestDynamicGeometryFeature = ObjectManager.requestDynamicGeometryFeature;
var oMFreeDynamicGeometryFeature = ObjectManager.freeDynamicGeometryFeature;

var TRIPLE_REGISTER = new Vec3();

/**
...
```

#### <a name="apidoc.element.famous.ObjectManager.requestDynamicGeometry"></a>[function <span class="apidocSignatureSpan">famous.ObjectManager.</span>requestDynamicGeometry ()](#apidoc.element.famous.ObjectManager.requestDynamicGeometry)
- description and source-code
```javascript
function request() {
    if (pool.length !== 0) return pool.pop();
    else return new Constructor();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.ObjectManager.requestDynamicGeometryFeature"></a>[function <span class="apidocSignatureSpan">famous.ObjectManager.</span>requestDynamicGeometryFeature ()](#apidoc.element.famous.ObjectManager.requestDynamicGeometryFeature)
- description and source-code
```javascript
function request() {
    if (pool.length !== 0) return pool.pop();
    else return new Constructor();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Opacity"></a>[module famous.Opacity](#apidoc.module.famous.Opacity)

#### <a name="apidoc.element.famous.Opacity.Opacity"></a>[function <span class="apidocSignatureSpan">famous.</span>Opacity (node)](#apidoc.element.famous.Opacity.Opacity)
- description and source-code
```javascript
function Opacity(node) {
    this._node = node;
    this._id = node.addComponent(this);
    this._value = new Transitionable(1);

    this._requestingUpdate = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Opacity.prototype"></a>[module famous.Opacity.prototype](#apidoc.module.famous.Opacity.prototype)

#### <a name="apidoc.element.famous.Opacity.prototype.get"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>get ()](#apidoc.element.famous.Opacity.prototype.get)
- description and source-code
```javascript
function get() {
    return this._value.get();
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>getValue ()](#apidoc.element.famous.Opacity.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return {
        component: this.toString(),
        value: this._value.get()
    };
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.halt"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>halt ()](#apidoc.element.famous.Opacity.prototype.halt)
- description and source-code
```javascript
function halt() {
    this._value.halt();
    return this;
}
```
- example usage
```shell
...
* Stops Opacity transition
*
* @method
*
* @return {Opacity} this
*/
Opacity.prototype.halt = function halt() {
   this._value.halt();
   return this;
};

/**
* Tells whether or not the opacity is in a transition
*
* @method
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.isActive"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>isActive ()](#apidoc.element.famous.Opacity.prototype.isActive)
- description and source-code
```javascript
function isActive(){
    return this._value.isActive();
}
```
- example usage
```shell
...
* Tells whether or not the opacity is in a transition
*
* @method
*
* @return {Boolean} whether or not the opacity is transitioning
*/
Opacity.prototype.isActive = function isActive(){
   return this._value.isActive();
};

/**
* When the node this component is attached to updates, update the value
* of the Node's opacity.
*
* @method
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>onUpdate ()](#apidoc.element.famous.Opacity.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setOpacity(this._value.get());

    if (this._value.isActive()) {
      this._node.requestUpdateOnNextTick(this._id);
    }
    else {
      this._requestingUpdate = false;
    }
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>set (value, transition, callback)](#apidoc.element.famous.Opacity.prototype.set)
- description and source-code
```javascript
function set(value, transition, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    this._value.set(value, transition, callback);
    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.setValue"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>setValue (value)](#apidoc.element.famous.Opacity.prototype.setValue)
- description and source-code
```javascript
function setValue(value) {
    if (this.toString() === value.component) {
        this.set(value.value);
        return true;
    }
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Opacity.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>toString ()](#apidoc.element.famous.Opacity.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'Opacity';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```

#### <a name="apidoc.element.famous.Opacity.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Opacity.prototype.</span>update ()](#apidoc.element.famous.Opacity.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setOpacity(this._value.get());

    if (this._value.isActive()) {
      this._node.requestUpdateOnNextTick(this._id);
    }
    else {
      this._requestingUpdate = false;
    }
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Origin"></a>[module famous.Origin](#apidoc.module.famous.Origin)

#### <a name="apidoc.element.famous.Origin.Origin"></a>[function <span class="apidocSignatureSpan">famous.</span>Origin (node)](#apidoc.element.famous.Origin.Origin)
- description and source-code
```javascript
function Origin(node) {
    Position.call(this, node);

    var initial = node.getOrigin();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Origin.prototype"></a>[module famous.Origin.prototype](#apidoc.module.famous.Origin.prototype)

#### <a name="apidoc.element.famous.Origin.prototype.constructor"></a>[function <span class="apidocSignatureSpan">famous.Origin.prototype.</span>constructor (node)](#apidoc.element.famous.Origin.prototype.constructor)
- description and source-code
```javascript
function Origin(node) {
    Position.call(this, node);

    var initial = node.getOrigin();

    this._x.set(initial[0]);
    this._y.set(initial[1]);
    this._z.set(initial[2]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Origin.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Origin.prototype.</span>onUpdate ()](#apidoc.element.famous.Origin.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setOrigin(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Origin.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Origin.prototype.</span>update ()](#apidoc.element.famous.Origin.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setOrigin(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Path"></a>[module famous.Path](#apidoc.module.famous.Path)

#### <a name="apidoc.element.famous.Path.depth"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>depth (path)](#apidoc.element.famous.Path.depth)
- description and source-code
```javascript
function depth(path) {
    var count = 0;
    var length = path.length;
    var len = this.hasTrailingSlash(path) ? length - 1 : length;
    var i = 0;
    for (; i < len ; i++) count += path[i] === '/' ? 1 : 0;
    return count;
}
```
- example usage
```shell
...
 *
 * @param {String} child the path that may be a child
 * @param {String} parent the path that may be a parent
 *
 * @return {Boolean} whether or not the first argument path is a child of the second argument path
 */
isChildOf: function isChildOf (child, parent) {
    return this.isDescendentOf(child, parent) && this.depth(child) === this.depth(parent) + 1;
},

/**
 * Returns true if the first argument path is a descendent of the second argument path.
 *
 * @method
 *
...
```

#### <a name="apidoc.element.famous.Path.getSelector"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>getSelector (path)](#apidoc.element.famous.Path.getSelector)
- description and source-code
```javascript
function getSelector(path) {
    var index = path.indexOf('/');
    return index === -1 ? path : path.substring(0, index);
}
```
- example usage
```shell
...
* @return {FamousEngine} this
*/
FamousEngine.prototype.addScene = function addScene (scene) {
   var selector = scene._selector;

   var current = this._scenes[selector];
   if (current && current !== scene) current.dismount();
   if (!scene.isMounted()) scene.mount(scene.getSelector());
   this._scenes[selector] = scene;
   return this;
};

/**
* Remove a scene.
*
...
```

#### <a name="apidoc.element.famous.Path.hasTrailingSlash"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>hasTrailingSlash (path)](#apidoc.element.famous.Path.hasTrailingSlash)
- description and source-code
```javascript
function hasTrailingSlash(path) {
    return path[path.length - 1] === '/';
}
```
- example usage
```shell
...
 * @param {String} path the path
 *
 * @return {Number} the depth in the tree that this path represents
 */
depth: function depth (path) {
    var count = 0;
    var length = path.length;
    var len = this.hasTrailingSlash(path) ? length - 1 : length;
    var i = 0;
    for (; i < len ; i++) count += path[i] === '/' ? 1 : 0;
    return count;
},

/**
 * Gets the position of this path in relation to its siblings.
...
```

#### <a name="apidoc.element.famous.Path.index"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>index (path)](#apidoc.element.famous.Path.index)
- description and source-code
```javascript
function index(path) {
    var length = path.length;
    var len = this.hasTrailingSlash(path) ? length - 1 : length;
    while (len--) if (path[len] === '/') break;
    var result = parseInt(path.substring(len + 1));
    return isNaN(result) ? 0 : result;
}
```
- example usage
```shell
...
var paths = this.paths;
var index = paths.indexOf(path);
if (index !== -1)
    throw new Error('item already exists at path: ' + path);

var i = 0;
var targetDepth = PathUtils.depth(path);
var targetIndex = PathUtils.index(path);

// The item will be inserted at a point in the array
// such that it is within its own breadth in the tree
// that the paths represent
while (
    paths[i] &&
    targetDepth >= PathUtils.depth(paths[i])
...
```

#### <a name="apidoc.element.famous.Path.indexAtDepth"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>indexAtDepth (path, depth)](#apidoc.element.famous.Path.indexAtDepth)
- description and source-code
```javascript
function indexAtDepth(path, depth) {
    var i = 0;
    var len = path.length;
    var index = 0;
    for (; i < len ; i++) {
        if (path[i] === '/') index++;
        if (index === depth) {
            path = path.substring(i ? i + 1 : i);
            index = path.indexOf('/');
            path = index === -1 ? path : path.substring(0, index);
            index = parseInt(path);
            return isNaN(index) ? path : index;
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Path.isChildOf"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>isChildOf (child, parent)](#apidoc.element.famous.Path.isChildOf)
- description and source-code
```javascript
function isChildOf(child, parent) {
    return this.isDescendentOf(child, parent) && this.depth(child) === this.depth(parent) + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Path.isDescendentOf"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>isDescendentOf (child, parent)](#apidoc.element.famous.Path.isDescendentOf)
- description and source-code
```javascript
function isDescendentOf(child, parent) {
    if (child === parent) return false;
    child = this.hasTrailingSlash(child) ? child : child + '/';
    parent = this.hasTrailingSlash(parent) ? parent : parent + '/';
    return this.depth(parent) < this.depth(child) && child.indexOf(parent) === 0;
}
```
- example usage
```shell
...
 *
 * @param {String} child the path that may be a child
 * @param {String} parent the path that may be a parent
 *
 * @return {Boolean} whether or not the first argument path is a child of the second argument path
 */
isChildOf: function isChildOf (child, parent) {
    return this.isDescendentOf(child, parent) && this.depth(child) === this.depth(parent) + 1;
},

/**
 * Returns true if the first argument path is a descendent of the second argument path.
 *
 * @method
 *
...
```

#### <a name="apidoc.element.famous.Path.parent"></a>[function <span class="apidocSignatureSpan">famous.Path.</span>parent (path)](#apidoc.element.famous.Path.parent)
- description and source-code
```javascript
function parent(path) {
    return path.substring(0, path.lastIndexOf('/', path.length - 2));
}
```
- example usage
```shell
...
Dispatch.prototype.mount = function mount (path, node) {
if (!node) throw new Error('Dispatch: no node passed to mount at: ' + path);
if (this._nodes[path])
    throw new Error('Dispatch: there is a node already registered at: ' + path);

node._setUpdater(this._updater);
this._nodes[path] = node;
var parentPath = PathUtils.parent(path);

// scenes are their own parents
var parent = !parentPath ? node : this._nodes[parentPath];

if (!parent)
    throw new Error(
            'Parent to path: ' + path +
...
```



# <a name="apidoc.module.famous.PathStore"></a>[module famous.PathStore](#apidoc.module.famous.PathStore)

#### <a name="apidoc.element.famous.PathStore.PathStore"></a>[function <span class="apidocSignatureSpan">famous.</span>PathStore ()](#apidoc.element.famous.PathStore.PathStore)
- description and source-code
```javascript
function PathStore() {
    this.items = [];
    this.paths = [];
    this.memo = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.PathStore.prototype"></a>[module famous.PathStore.prototype](#apidoc.module.famous.PathStore.prototype)

#### <a name="apidoc.element.famous.PathStore.prototype.get"></a>[function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>get (path)](#apidoc.element.famous.PathStore.prototype.get)
- description and source-code
```javascript
function get(path) {
    if (this.memo[path]) return this.items[this.memo[path]];

    var index = this.paths.indexOf(path);

    if (index === -1) return void 0;

    this.memo[path] = index;

    return this.items[index];
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.PathStore.prototype.getItems"></a>[function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>getItems ()](#apidoc.element.famous.PathStore.prototype.getItems)
- description and source-code
```javascript
function getItems() {
    return this.items;
}
```
- example usage
```shell
...
 * Updates the sizes in the scene graph. Called internally by the famous engine.
 *
 * @method
 *
 * @return {undefined} undefined
 */
SizeSystem.prototype.update = function update () {
var sizes = this.pathStore.getItems();
var paths = this.pathStore.getPaths();
var node;
var size;
var i;
var len;
var components;
...
```

#### <a name="apidoc.element.famous.PathStore.prototype.getPaths"></a>[function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>getPaths ()](#apidoc.element.famous.PathStore.prototype.getPaths)
- description and source-code
```javascript
function getPaths() {
    return this.paths;
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {undefined} undefined
 */
SizeSystem.prototype.update = function update () {
var sizes = this.pathStore.getItems();
var paths = this.pathStore.getPaths();
var node;
var size;
var i;
var len;
var components;

for (i = 0, len = sizes.length ; i < len ; i++) {
...
```

#### <a name="apidoc.element.famous.PathStore.prototype.insert"></a>[function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>insert (path, item)](#apidoc.element.famous.PathStore.prototype.insert)
- description and source-code
```javascript
function insert(path, item) {
    var paths = this.paths;
    var index = paths.indexOf(path);
    if (index !== -1)
        throw new Error('item already exists at path: ' + path);

    var i = 0;
    var targetDepth = PathUtils.depth(path);
    var targetIndex = PathUtils.index(path);

    // The item will be inserted at a point in the array
    // such that it is within its own breadth in the tree
    // that the paths represent
    while (
        paths[i] &&
        targetDepth >= PathUtils.depth(paths[i])
    ) i++;

    // The item will be sorted within its breadth by index
    // in regard to its siblings.
    while (
        paths[i] &&
        targetDepth === PathUtils.depth(paths[i]) &&
        targetIndex < PathUtils.index(paths[i])
    ) i++;

    // insert the items in the path
    paths.splice(i, 0, path);
    this.items.splice(i, 0, item);

    // store the relationship between path and index in the memo
    this.memo[path] = i;

    // all items behind the inserted item are now no longer
    // accurately stored in the memo. Thus the memo must be cleared for
    // these items.
    for (var len = this.paths.length ; i < len ; i++)
        this.memo[this.paths[i]] = null;
}
```
- example usage
```shell
...
 *
 * @param {String} path The path at which to register the size component
 * @param {Size | undefined} size The size component to be registered or undefined.
 *
 * @return {undefined} undefined
 */
SizeSystem.prototype.registerSizeAtPath = function registerSizeAtPath (path, size) {
if (!PathUtils.depth(path)) return this.pathStore.insert(path, size ? size : new Size());

var parent = this.pathStore.get(PathUtils.parent(path));

if (!parent) throw new Error(
        'No parent size registered at expected path: ' + PathUtils.parent(path)
);
...
```

#### <a name="apidoc.element.famous.PathStore.prototype.remove"></a>[function <span class="apidocSignatureSpan">famous.PathStore.prototype.</span>remove (path)](#apidoc.element.famous.PathStore.prototype.remove)
- description and source-code
```javascript
function remove(path) {
    var paths = this.paths;
    var index = this.memo[path] ? this.memo[path] : paths.indexOf(path);
    if (index === -1)
        throw new Error('Cannot remove. No item exists at path: ' + path);

    paths.splice(index, 1);
    this.items.splice(index, 1);

    this.memo[path] = null;

    for (var len = this.paths.length ; index < len ; index++)
        this.memo[this.paths[index]] = null;
}
```
- example usage
```shell
...
* @method
*
* @param {String} path The path at which to remove the size.
*
* @return {undefined} undefined
*/
SizeSystem.prototype.deregisterSizeAtPath = function deregisterSizeAtPath(path) {
   this.pathStore.remove(path);
};

/**
* Returns the size component stored at a given path. Returns undefined if no
* size component is registered to that path.
*
* @method
...
```



# <a name="apidoc.module.famous.PhysicsEngine"></a>[module famous.PhysicsEngine](#apidoc.module.famous.PhysicsEngine)

#### <a name="apidoc.element.famous.PhysicsEngine.PhysicsEngine"></a>[function <span class="apidocSignatureSpan">famous.</span>PhysicsEngine (options)](#apidoc.element.famous.PhysicsEngine.PhysicsEngine)
- description and source-code
```javascript
function PhysicsEngine(options) {
    this.events = new CallbackStore();

    options = options || {};
<span class="apidocCodeCommentSpan">    /** @prop bodies The bodies currently active in the engine. */
</span>    this.bodies = [];
    /** @prop forces The forces currently active in the engine. */
    this.forces = [];
    /** @prop constraints The constraints currently active in the engine. */
    this.constraints = [];

    /** @prop step The time between frames in the engine. */
    this.step = options.step || 1000/60;
    /** @prop iterations The number of times each constraint is solved per frame. */
    this.iterations = options.iterations || 10;
    /** @prop _indexPool Pools of indicies to track holes in the arrays. */
    this._indexPools = {
        bodies: [],
        forces: [],
        constraints: []
    };

    this._entityMaps = {
        bodies: {},
        forces: {},
        constraints: {}
    };

    this.speed = options.speed || 1.0;
    this.time = 0;
    this.delta = 0;

    this.origin = options.origin || new Vec3();
    this.orientation = options.orientation ? options.orientation.normalize() :  new Quaternion();

    this.frameDependent = options.frameDependent || false;

    this.transformBuffers = {
        position: [0, 0, 0],
        rotation: [0, 0, 0, 1]
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.PhysicsEngine.prototype"></a>[module famous.PhysicsEngine.prototype](#apidoc.module.famous.PhysicsEngine.prototype)

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.add"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>add ()](#apidoc.element.famous.PhysicsEngine.prototype.add)
- description and source-code
```javascript
function add() {
    for (var j = 0, lenj = arguments.length; j < lenj; j++) {
        var entity = arguments[j];
        if (entity instanceof Array) {
            for (var i = 0, len = entity.length; i < len; i++) {
                var e = entity[i];
                this.add(e);
            }
        }
        else {
            if (entity instanceof Particle) this.addBody(entity);
            else if (entity instanceof Constraint) this.addConstraint(entity);
            else if (entity instanceof Force) this.addForce(entity);
        }
    }
    return this;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.addBody"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>addBody (body)](#apidoc.element.famous.PhysicsEngine.prototype.addBody)
- description and source-code
```javascript
function addBody(body) {
    _addElement(this, body, 'bodies');
}
```
- example usage
```shell
...
        if (entity instanceof Array) {
            for (var i = 0, len = entity.length; i < len; i++) {
                var e = entity[i];
                this.add(e);
            }
        }
        else {
            if (entity instanceof Particle) this.addBody(entity);
            else if (entity instanceof Constraint) this.addConstraint(entity);
            else if (entity instanceof Force) this.addForce(entity);
        }
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.addConstraint"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>addConstraint (constraint)](#apidoc.element.famous.PhysicsEngine.prototype.addConstraint)
- description and source-code
```javascript
function addConstraint(constraint) {
    _addElement(this, constraint, 'constraints');
}
```
- example usage
```shell
...
            for (var i = 0, len = entity.length; i < len; i++) {
                var e = entity[i];
                this.add(e);
            }
        }
        else {
            if (entity instanceof Particle) this.addBody(entity);
            else if (entity instanceof Constraint) this.addConstraint(entity);
            else if (entity instanceof Force) this.addForce(entity);
        }
    }
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.addForce"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>addForce (force)](#apidoc.element.famous.PhysicsEngine.prototype.addForce)
- description and source-code
```javascript
function addForce(force) {
    _addElement(this, force, 'forces');
}
```
- example usage
```shell
...
               var e = entity[i];
               this.add(e);
           }
       }
       else {
           if (entity instanceof Particle) this.addBody(entity);
           else if (entity instanceof Constraint) this.addConstraint(entity);
           else if (entity instanceof Force) this.addForce(entity);
       }
   }
   return this;
};

/**
* Remove a group of bodies, force, or constraints from the engine.
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.getTransform"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>getTransform (body)](#apidoc.element.famous.PhysicsEngine.prototype.getTransform)
- description and source-code
```javascript
function getTransform(body) {
    var o = this.origin;
    var oq = this.orientation;
    var transform = this.transformBuffers;

    var p = body.position;
    var q = body.orientation;
    var rot = q;
    var loc = p;

    if (oq.w !== 1) {
        rot = Quaternion.multiply(q, oq, QUAT_REGISTER);
        loc = oq.rotateVector(p, VEC_REGISTER);
    }

    transform.position[0] = o.x+loc.x;
    transform.position[1] = o.y+loc.y;
    transform.position[2] = o.z+loc.z;

    transform.rotation[0] = rot.x;
    transform.rotation[1] = rot.y;
    transform.rotation[2] = rot.z;
    transform.rotation[3] = rot.w;

    return transform;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.off"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>off (key, callback)](#apidoc.element.famous.PhysicsEngine.prototype.off)
- description and source-code
```javascript
function off(key, callback) {
    this.events.off(key, callback);
    return this;
}
```
- example usage
```shell
...
*
* @param  {String}   path      Path at which the listener function has been
*                              registered.
* @param  {Function} callback  Callback function to be deregistered.
* @return {DOMRenderer}        this
*/
DOMRenderer.prototype.offInsertEl = function offInsertEl(path, callback) {
   this._insertElCallbackStore.off(path, callback);
   return this;
};

/**
* Registers an event handler to be triggered as soon as an element at the
* specified path is being removed.
*
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.on"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>on (key, callback)](#apidoc.element.famous.PhysicsEngine.prototype.on)
- description and source-code
```javascript
function on(key, callback) {
    this.events.on(key, callback);
    return this;
}
```
- example usage
```shell
...
this.trackedGestures = {};

var i;
var len;

if (events) {
    for (i = 0, len = events.length; i < len; i++) {
        this.on(events[i], events[i].callback);
    }
}

node.addUIEvent('touchstart');
node.addUIEvent('mousedown');
node.addUIEvent('touchmove');
node.addUIEvent('mousemove');
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.remove"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>remove ()](#apidoc.element.famous.PhysicsEngine.prototype.remove)
- description and source-code
```javascript
function remove() {
    for (var j = 0, lenj = arguments.length; j < lenj; j++) {
        var entity = arguments[j];
        if (entity instanceof Array) {
            for (var i = 0, len = entity.length; i < len; i++) {
                var e = entity[i];
                this.add(e);
            }
        }
        else {
            if (entity instanceof Particle) this.removeBody(entity);
            else if (entity instanceof Constraint) this.removeConstraint(entity);
            else if (entity instanceof Force) this.removeForce(entity);
        }
    }
    return this;
}
```
- example usage
```shell
...
* @method
*
* @param {String} path The path at which to remove the size.
*
* @return {undefined} undefined
*/
SizeSystem.prototype.deregisterSizeAtPath = function deregisterSizeAtPath(path) {
   this.pathStore.remove(path);
};

/**
* Returns the size component stored at a given path. Returns undefined if no
* size component is registered to that path.
*
* @method
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.removeBody"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>removeBody (body)](#apidoc.element.famous.PhysicsEngine.prototype.removeBody)
- description and source-code
```javascript
function removeBody(body) {
    _removeElement(this, body, 'bodies');
}
```
- example usage
```shell
...
        if (entity instanceof Array) {
            for (var i = 0, len = entity.length; i < len; i++) {
                var e = entity[i];
                this.add(e);
            }
        }
        else {
            if (entity instanceof Particle) this.removeBody(entity);
            else if (entity instanceof Constraint) this.removeConstraint(entity);
            else if (entity instanceof Force) this.removeForce(entity);
        }
    }
    return this;
};
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.removeConstraint"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>removeConstraint (constraint)](#apidoc.element.famous.PhysicsEngine.prototype.removeConstraint)
- description and source-code
```javascript
function removeConstraint(constraint) {
    _removeElement(this, constraint, 'constraints');
}
```
- example usage
```shell
...
            for (var i = 0, len = entity.length; i < len; i++) {
                var e = entity[i];
                this.add(e);
            }
        }
        else {
            if (entity instanceof Particle) this.removeBody(entity);
            else if (entity instanceof Constraint) this.removeConstraint(entity);
            else if (entity instanceof Force) this.removeForce(entity);
        }
    }
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.removeForce"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>removeForce (force)](#apidoc.element.famous.PhysicsEngine.prototype.removeForce)
- description and source-code
```javascript
function removeForce(force) {
    _removeElement(this, force, 'forces');
}
```
- example usage
```shell
...
               var e = entity[i];
               this.add(e);
           }
       }
       else {
           if (entity instanceof Particle) this.removeBody(entity);
           else if (entity instanceof Constraint) this.removeConstraint(entity);
           else if (entity instanceof Force) this.removeForce(entity);
       }
   }
   return this;
};

/**
* Begin tracking a body.
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.setOrientation"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>setOrientation (w, x, y, z)](#apidoc.element.famous.PhysicsEngine.prototype.setOrientation)
- description and source-code
```javascript
function setOrientation(w, x, y, z) {
    this.orientation.set(w, x, y, z).normalize();
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.setOrigin"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>setOrigin (x, y, z)](#apidoc.element.famous.PhysicsEngine.prototype.setOrigin)
- description and source-code
```javascript
function setOrigin(x, y, z) {
    this.origin.set(x, y, z);
    return this;
}
```
- example usage
```shell
...
 * of the Node's origin
 *
 * @method
 *
 * @return {undefined} undefined
 */
Origin.prototype.update = function update() {
    this._node.setOrigin(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Origin.prototype.onUpdate = Origin.prototype.update;

module.exports = Origin;
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.trigger"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>trigger (key, payload)](#apidoc.element.famous.PhysicsEngine.prototype.trigger)
- description and source-code
```javascript
function trigger(key, payload) {
    this.events.trigger(key, payload);
    return this;
}
```
- example usage
```shell
...
GestureHandler.prototype.triggerGestures = function() {
var payload = this.event;
for (var i = 0, len = this.gestures.length; i < len; i++) {
    var gesture = this.gestures[i];
    switch (gesture) {
        case 'rotate':
        case 'pinch':
            if (payload.points === 2) this.trigger(gesture, payload);
            break;
        case 'tap':
            if (payload.status === 'start') {
                if (this.options.tap) {
                    var pts = this.options.tap.points || 1;
                    if(this.multiTap >= pts && payload.points >= pts) this.trigger(gesture, payload);
                }
...
```

#### <a name="apidoc.element.famous.PhysicsEngine.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.PhysicsEngine.prototype.</span>update (time)](#apidoc.element.famous.PhysicsEngine.prototype.update)
- description and source-code
```javascript
function update(time) {
    if (this.time === 0) this.time = time;

    var bodies = this.bodies;
    var forces = this.forces;
    var constraints = this.constraints;

    var frameDependent = this.frameDependent;
    var step = this.step;
    var dt = step * 0.001;
    var speed = this.speed;

    var delta = this.delta;
    delta += (time - this.time) * speed;
    this.time = time;

    var i, len;
    var force, body, constraint;

    while(delta > step) {
        this.events.trigger('prestep', time);

        // Update Forces on particles
        for (i = 0, len = forces.length; i < len; i++) {
            force = forces[i];
            if (force === null) continue;
            force.update(time, dt);
        }

        // Tentatively update velocities
        for (i = 0, len = bodies.length; i < len; i++) {
            body = bodies[i];
            if (body === null) continue;
            _integrateVelocity(body, dt);
        }

        // Prep constraints for solver
        for (i = 0, len = constraints.length; i < len; i++) {
            constraint = constraints[i];
            if (constraint === null) continue;
            constraint.update(time, dt);
        }

        // Iteratively resolve constraints
        for (var j = 0, numIterations = this.iterations; j < numIterations; j++) {
            for (i = 0, len = constraints.length; i < len; i++) {
                constraint = constraints[i];
                if (constraint === null) continue;
                constraint.resolve(time, dt);
            }
        }

        // Increment positions and orientations
        for (i = 0, len = bodies.length; i < len; i++) {
            body = bodies[i];
            if (body === null) continue;
            _integratePose(body, dt);
        }

        this.events.trigger('poststep', time);

        if (frameDependent) delta = 0;
        else delta -= step;
    }

    this.delta = delta;
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Position"></a>[module famous.Position](#apidoc.module.famous.Position)

#### <a name="apidoc.element.famous.Position.Position"></a>[function <span class="apidocSignatureSpan">famous.</span>Position (node)](#apidoc.element.famous.Position.Position)
- description and source-code
```javascript
function Position(node) {
    this._node = node;
    this._id = node.addComponent(this);

    this._requestingUpdate = false;

    var initialPosition = node.getPosition();

    this._x = new Transitionable(initialPosition[0]);
    this._y = new Transitionable(initialPosition[1]);
    this._z = new Transitionable(initialPosition[2]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Position.prototype"></a>[module famous.Position.prototype](#apidoc.module.famous.Position.prototype)

#### <a name="apidoc.element.famous.Position.prototype._checkUpdate"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>_checkUpdate ()](#apidoc.element.famous.Position.prototype._checkUpdate)
- description and source-code
```javascript
function _checkUpdate() {
    if (this.isActive()) this._node.requestUpdateOnNextTick(this._id);
    else this._requestingUpdate = false;
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Position.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getValue ()](#apidoc.element.famous.Position.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return {
        component: this.toString(),
        x: this._x.get(),
        y: this._y.get(),
        z: this._z.get()
    };
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Position.prototype.getX"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getX ()](#apidoc.element.famous.Position.prototype.getX)
- description and source-code
```javascript
function getX() {
    return this._x.get();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.getY"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getY ()](#apidoc.element.famous.Position.prototype.getY)
- description and source-code
```javascript
function getY() {
    return this._y.get();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.getZ"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>getZ ()](#apidoc.element.famous.Position.prototype.getZ)
- description and source-code
```javascript
function getZ() {
    return this._z.get();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.halt"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>halt ()](#apidoc.element.famous.Position.prototype.halt)
- description and source-code
```javascript
function halt() {
    this._x.halt();
    this._y.halt();
    this._z.halt();
    return this;
}
```
- example usage
```shell
...
* Stops Opacity transition
*
* @method
*
* @return {Opacity} this
*/
Opacity.prototype.halt = function halt() {
   this._value.halt();
   return this;
};

/**
* Tells whether or not the opacity is in a transition
*
* @method
...
```

#### <a name="apidoc.element.famous.Position.prototype.isActive"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>isActive ()](#apidoc.element.famous.Position.prototype.isActive)
- description and source-code
```javascript
function isActive() {
    return this._x.isActive() || this._y.isActive() || this._z.isActive();
}
```
- example usage
```shell
...
* Tells whether or not the opacity is in a transition
*
* @method
*
* @return {Boolean} whether or not the opacity is transitioning
*/
Opacity.prototype.isActive = function isActive(){
   return this._value.isActive();
};

/**
* When the node this component is attached to updates, update the value
* of the Node's opacity.
*
* @method
...
```

#### <a name="apidoc.element.famous.Position.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>onUpdate ()](#apidoc.element.famous.Position.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setPosition(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Position.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>set (x, y, z, transition, callback)](#apidoc.element.famous.Position.prototype.set)
- description and source-code
```javascript
function set(x, y, z, transition, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    var xCallback;
    var yCallback;
    var zCallback;

    if (z != null) {
        zCallback = callback;
    }
    else if (y != null) {
        yCallback = callback;
    }
    else if (x != null) {
        xCallback = callback;
    }

    if (x != null) this._x.set(x, transition, xCallback);
    if (y != null) this._y.set(y, transition, yCallback);
    if (z != null) this._z.set(z, transition, zCallback);

    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Position.prototype.setValue"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setValue (state)](#apidoc.element.famous.Position.prototype.setValue)
- description and source-code
```javascript
function setValue(state) {
    if (this.toString() === state.component) {
        this.set(state.x, state.y, state.z);
        return true;
    }
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.setX"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setX (val, transition, callback)](#apidoc.element.famous.Position.prototype.setX)
- description and source-code
```javascript
function setX(val, transition, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    this._x.set(val, transition, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.setY"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setY (val, transition, callback)](#apidoc.element.famous.Position.prototype.setY)
- description and source-code
```javascript
function setY(val, transition, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    this._y.set(val, transition, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.setZ"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>setZ (val, transition, callback)](#apidoc.element.famous.Position.prototype.setZ)
- description and source-code
```javascript
function setZ(val, transition, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    this._z.set(val, transition, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Position.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>toString ()](#apidoc.element.famous.Position.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'Position';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```

#### <a name="apidoc.element.famous.Position.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Position.prototype.</span>update ()](#apidoc.element.famous.Position.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setPosition(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Program"></a>[module famous.Program](#apidoc.module.famous.Program)

#### <a name="apidoc.element.famous.Program.Program"></a>[function <span class="apidocSignatureSpan">famous.</span>Program (gl, options)](#apidoc.element.famous.Program.Program)
- description and source-code
```javascript
function Program(gl, options) {
    this.gl = gl;
    this.options = options || {};

    this.registeredMaterials = {};
    this.cachedUniforms = {};
    this.uniformTypes = [];

    this.definitionVec4 = [];
    this.definitionVec3 = [];
    this.definitionFloat = [];
    this.applicationVec3 = [];
    this.applicationVec4 = [];
    this.applicationFloat = [];
    this.applicationVert = [];
    this.definitionVert = [];

    if (this.options.debug) {
        this.gl.compileShader = Debug.call(this);
    }

    this.resetProgram();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Program.prototype"></a>[module famous.Program.prototype](#apidoc.module.famous.Program.prototype)

#### <a name="apidoc.element.famous.Program.prototype.compileShader"></a>[function <span class="apidocSignatureSpan">famous.Program.prototype.</span>compileShader (shader, source)](#apidoc.element.famous.Program.prototype.compileShader)
- description and source-code
```javascript
function compileShader(shader, source) {
    var i = 1;

    this.gl.shaderSource(shader, source);
    this.gl.compileShader(shader);
    if (!this.gl.getShaderParameter(shader, this.gl.COMPILE_STATUS)) {
        console.error('compile error: ' + this.gl.getShaderInfoLog(shader));
        console.error('1: ' + source.replace(/\n/g, function () {
            return '\n' + (i+=1) + ': ';
        }));
    }

    return shader;
}
```
- example usage
```shell
...
    .replace('#float_definitions', this.definitionFloat.join('\n'))
    .replace('#float_applications', this.applicationFloat.join('\n'));

program = this.gl.createProgram();

this.gl.attachShader(
    program,
    this.compileShader(this.gl.createShader(VERTEX_SHADER), vertexSource)
);

this.gl.attachShader(
    program,
    this.compileShader(this.gl.createShader(FRAGMENT_SHADER), fragmentSource)
);
...
```

#### <a name="apidoc.element.famous.Program.prototype.getUniformTypeFromValue"></a>[function <span class="apidocSignatureSpan">famous.Program.prototype.</span>getUniformTypeFromValue (value)](#apidoc.element.famous.Program.prototype.getUniformTypeFromValue)
- description and source-code
```javascript
function getUniformTypeFromValue(value) {
    if (Array.isArray(value) || value instanceof Float32Array) {
        switch (value.length) {
            case 1:  return 'uniform1fv';
            case 2:  return 'uniform2fv';
            case 3:  return 'uniform3fv';
            case 4:  return 'uniform4fv';
            case 9:  return 'uniformMatrix3fv';
            case 16: return 'uniformMatrix4fv';
        }
    }
    else if (!isNaN(parseFloat(value)) && isFinite(value)) {
        return 'uniform1f';
    }

    throw 'cant load uniform "' + name + '" with value:' + JSON.stringify(value);
}
```
- example usage
```shell
...
// Check if the value is already set for the
// given uniform.
if (this.uniformIsCached(name, value)) continue;

// Determine the correct function and pass the uniform
// value to WebGL.
if (!this.uniformTypes[name]) {
    this.uniformTypes[name] = this.getUniformTypeFromValue(value);
}

// Call uniform setter function on WebGL context with correct value

switch (this.uniformTypes[name]) {
    case 'uniform4fv': gl.uniform4fv(location, value); break;
    case 'uniform3fv': gl.uniform3fv(location, value); break;
...
```

#### <a name="apidoc.element.famous.Program.prototype.registerMaterial"></a>[function <span class="apidocSignatureSpan">famous.Program.prototype.</span>registerMaterial (name, material)](#apidoc.element.famous.Program.prototype.registerMaterial)
- description and source-code
```javascript
function registerMaterial(name, material) {
    var compiled = material;
    var type = inputTypes[name];
    var mask = masks[type];

    if ((this.registeredMaterials[material._id] & mask) === mask) return this;

    var k;

    for (k in compiled.uniforms) {
        if (uniforms.keys.indexOf(k) === -1) {
            uniforms.keys.push(k);
            uniforms.values.push(compiled.uniforms[k]);
        }
    }

    for (k in compiled.varyings) {
        if (varyings.keys.indexOf(k) === -1) {
            varyings.keys.push(k);
            varyings.values.push(compiled.varyings[k]);
        }
    }

    for (k in compiled.attributes) {
        if (attributes.keys.indexOf(k) === -1) {
            attributes.keys.push(k);
            attributes.values.push(compiled.attributes[k]);
        }
    }

    this.registeredMaterials[material._id] |= mask;

    if (type === 'float') {
        this.definitionFloat.push(material.defines);
        this.definitionFloat.push('float fa_' + material._id + '() {\n '  + compiled.glsl + ' \n}');
        this.applicationFloat.push('if (int(abs(ID)) == ' + material._id + ') return fa_' + material._id  + '();');
    }

    if (type === 'vec3') {
        this.definitionVec3.push(material.defines);
        this.definitionVec3.push('vec3 fa_' + material._id + '() {\n '  + compiled.glsl + ' \n}');
        this.applicationVec3.push('if (int(abs(ID.x)) == ' + material._id + ') return fa_' + material._id + '();');
    }

    if (type === 'vec4') {
        this.definitionVec4.push(material.defines);
        this.definitionVec4.push('vec4 fa_' + material._id + '() {\n '  + compiled.glsl + ' \n}');
        this.applicationVec4.push('if (int(abs(ID.x)) == ' + material._id + ') return fa_' + material._id + '();');
    }

    if (type === 'vert') {
        this.definitionVert.push(material.defines);
        this.definitionVert.push('vec3 fa_' + material._id + '() {\n '  + compiled.glsl + ' \n}');
        this.applicationVert.push('if (int(abs(ID.x)) == ' + material._id + ') return fa_' + material._id + '();');
    }

    return this.resetProgram();
}
```
- example usage
```shell
...
       mesh.textures.push(
           this.textureManager.register(material.textures[i], mesh.textures.length + i)
       );
   }

   // Register material!

   this.program.registerMaterial(name, material);

   return this.updateSize();
};

/**
* Changes the geometry data of a mesh
*
...
```

#### <a name="apidoc.element.famous.Program.prototype.resetProgram"></a>[function <span class="apidocSignatureSpan">famous.Program.prototype.</span>resetProgram ()](#apidoc.element.famous.Program.prototype.resetProgram)
- description and source-code
```javascript
function resetProgram() {
    var vertexHeader = [header];
    var fragmentHeader = [header];

    var fragmentSource;
    var vertexSource;
    var program;
    var name;
    var value;
    var i;

    this.uniformLocations   = [];
    this.attributeLocations = {};

    this.uniformTypes = {};

    this.attributeNames = clone(attributes.keys);
    this.attributeValues = clone(attributes.values);

    this.varyingNames = clone(varyings.keys);
    this.varyingValues = clone(varyings.values);

    this.uniformNames = clone(uniforms.keys);
    this.uniformValues = clone(uniforms.values);

    this.cachedUniforms = {};

    fragmentHeader.push('uniform sampler2D u_textures[7];\n');

    if (this.applicationVert.length) {
        vertexHeader.push('uniform sampler2D u_textures[7];\n');
    }

    for(i = 0; i < this.uniformNames.length; i++) {
        name = this.uniformNames[i];
        value = this.uniformValues[i];
        vertexHeader.push('uniform ' + TYPES[value.length] + name + ';\n');
        fragmentHeader.push('uniform ' + TYPES[value.length] + name + ';\n');
    }

    for(i = 0; i < this.attributeNames.length; i++) {
        name = this.attributeNames[i];
        value = this.attributeValues[i];
        vertexHeader.push('attribute ' + TYPES[value.length] + name + ';\n');
    }

    for(i = 0; i < this.varyingNames.length; i++) {
        name = this.varyingNames[i];
        value = this.varyingValues[i];
        vertexHeader.push('varying ' + TYPES[value.length]  + name + ';\n');
        fragmentHeader.push('varying ' + TYPES[value.length] + name + ';\n');
    }

    vertexSource = vertexHeader.join('') + vertexWrapper
        .replace('#vert_definitions', this.definitionVert.join('\n'))
        .replace('#vert_applications', this.applicationVert.join('\n'));

    fragmentSource = fragmentHeader.join('') + fragmentWrapper
        .replace('#vec3_definitions', this.definitionVec3.join('\n'))
        .replace('#vec3_applications', this.applicationVec3.join('\n'))
        .replace('#vec4_definitions', this.definitionVec4.join('\n'))
        .replace('#vec4_applications', this.applicationVec4.join('\n'))
        .replace('#float_definitions', this.definitionFloat.join('\n'))
        .replace('#float_applications', this.applicationFloat.join('\n'));

    program = this.gl.createProgram();

    this.gl.attachShader(
        program,
        this.compileShader(this.gl.createShader(VERTEX_SHADER), vertexSource)
    );

    this.gl.attachShader(
        program,
        this.compileShader(this.gl.createShader(FRAGMENT_SHADER), fragmentSource)
    );

    this.gl.linkProgram(program);

    if (! this.gl.getProgramParameter(program, this.gl.LINK_STATUS)) {
        console.error('link error: ' + this.gl.getProgramInfoLog(program));
        this.program = null;
    }
    else {
        this.program = program;
        this.gl.useProgram(this.program);
    }

    this.setUniforms(this.uniformNames, this.uniformValues);

    var textureLocation = this.gl.getUniformLocation(this.program, 'u_textures[0]');
    this.gl.uniform1iv(textureLocation, [0, 1, 2, 3, 4, 5, 6]);

    return this;
}
```
- example usage
```shell
...
   this.applicationVert = [];
   this.definitionVert = [];

   if (this.options.debug) {
       this.gl.compileShader = Debug.call(this);
   }

   this.resetProgram();
}

/**
* Determines whether a material has already been registered to
* the shader program.
*
* @method
...
```

#### <a name="apidoc.element.famous.Program.prototype.setUniforms"></a>[function <span class="apidocSignatureSpan">famous.Program.prototype.</span>setUniforms (uniformNames, uniformValue)](#apidoc.element.famous.Program.prototype.setUniforms)
- description and source-code
```javascript
setUniforms = function (uniformNames, uniformValue) {
    var gl = this.gl;
    var location;
    var value;
    var name;
    var len;
    var i;

    if (!this.program) return this;

    len = uniformNames.length;
    for (i = 0; i < len; i++) {
        name = uniformNames[i];
        value = uniformValue[i];

        // Retreive the cached location of the uniform,
        // requesting a new location from the WebGL context
        // if it does not yet exist.

        location = this.uniformLocations[name];

        if (location === null) continue;
        if (location === undefined) {
            location = gl.getUniformLocation(this.program, name);
            this.uniformLocations[name] = location;
        }

        // Check if the value is already set for the
        // given uniform.
        if (this.uniformIsCached(name, value)) continue;

        // Determine the correct function and pass the uniform
        // value to WebGL.
        if (!this.uniformTypes[name]) {
            this.uniformTypes[name] = this.getUniformTypeFromValue(value);
        }

        // Call uniform setter function on WebGL context with correct value

        switch (this.uniformTypes[name]) {
            case 'uniform4fv': gl.uniform4fv(location, value); break;
            case 'uniform3fv': gl.uniform3fv(location, value); break;
            case 'uniform2fv': gl.uniform2fv(location, value); break;
            case 'uniform1fv': gl.uniform1fv(location, value); break;
            case 'uniform1f' : gl.uniform1f(location, value); break;
            case 'uniformMatrix3fv': gl.uniformMatrix3fv(location, false, value); break;
            case 'uniformMatrix4fv': gl.uniformMatrix4fv(location, false, value); break;
        }
    }

    return this;
}
```
- example usage
```shell
...
        this.program = null;
    }
    else {
        this.program = program;
        this.gl.useProgram(this.program);
    }

    this.setUniforms(this.uniformNames, this.uniformValues);

    var textureLocation = this.gl.getUniformLocation(this.program, 'u_textures[0]');
    this.gl.uniform1iv(textureLocation, [0, 1, 2, 3, 4, 5, 6]);

    return this;
};
...
```

#### <a name="apidoc.element.famous.Program.prototype.uniformIsCached"></a>[function <span class="apidocSignatureSpan">famous.Program.prototype.</span>uniformIsCached (targetName, value)](#apidoc.element.famous.Program.prototype.uniformIsCached)
- description and source-code
```javascript
uniformIsCached = function (targetName, value) {
    if(this.cachedUniforms[targetName] == null) {
        if (value.length) {
            this.cachedUniforms[targetName] = new Float32Array(value);
        }
        else {
            this.cachedUniforms[targetName] = value;
        }
        return false;
    }
    else if (value.length) {
        var i = value.length;
        while (i--) {
            if(value[i] !== this.cachedUniforms[targetName][i]) {
                i = value.length;
                while(i--) this.cachedUniforms[targetName][i] = value[i];
                return false;
            }
        }
    }

    else if (this.cachedUniforms[targetName] !== value) {
        this.cachedUniforms[targetName] = value;
        return false;
    }

    return true;
}
```
- example usage
```shell
...
if (location === undefined) {
    location = gl.getUniformLocation(this.program, name);
    this.uniformLocations[name] = location;
}

// Check if the value is already set for the
// given uniform.
if (this.uniformIsCached(name, value)) continue;

// Determine the correct function and pass the uniform
// value to WebGL.
if (!this.uniformTypes[name]) {
    this.uniformTypes[name] = this.getUniformTypeFromValue(value);
}
...
```



# <a name="apidoc.module.famous.Quaternion"></a>[module famous.Quaternion](#apidoc.module.famous.Quaternion)

#### <a name="apidoc.element.famous.Quaternion.Quaternion"></a>[function <span class="apidocSignatureSpan">famous.</span>Quaternion (w, x, y, z)](#apidoc.element.famous.Quaternion.Quaternion)
- description and source-code
```javascript
function Quaternion(w, x, y, z) {
    this.w = w || 1;
    this.x = x || 0;
    this.y = y || 0;
    this.z = z || 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.clone"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.</span>clone (q)](#apidoc.element.famous.Quaternion.clone)
- description and source-code
```javascript
function clone(q) {
    return new Quaternion(q.w, q.x, q.y, q.z);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.conjugate"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.</span>conjugate (q, output)](#apidoc.element.famous.Quaternion.conjugate)
- description and source-code
```javascript
function conjugate(q, output) {
    output.w = q.w;
    output.x = -q.x;
    output.y = -q.y;
    output.z = -q.z;
    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.dot"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.</span>dot (q1, q2)](#apidoc.element.famous.Quaternion.dot)
- description and source-code
```javascript
function dot(q1, q2) {
    return q1.w * q2.w + q1.x * q2.x + q1.y * q2.y + q1.z * q2.z;
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Quaternion.multiply"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.</span>multiply (q1, q2, output)](#apidoc.element.famous.Quaternion.multiply)
- description and source-code
```javascript
function multiply(q1, q2, output) {
    var w1 = q1.w || 0;
    var x1 = q1.x;
    var y1 = q1.y;
    var z1 = q1.z;

    var w2 = q2.w || 0;
    var x2 = q2.x;
    var y2 = q2.y;
    var z2 = q2.z;

    output.w = w1 * w2 - x1 * x2 - y1 * y2 - z1 * z2;
    output.x = x1 * w2 + x2 * w1 + y2 * z1 - y1 * z2;
    output.y = y1 * w2 + y2 * w1 + x1 * z2 - x2 * z1;
    output.z = z1 * w2 + z2 * w1 + x2 * y1 - x1 * y2;
    return output;
}
```
- example usage
```shell
...
}
else {
    rotQ.fromEuler(x, y, z);
    callback = options;
    options = w;
}

var q = referenceQ.multiply(rotQ);
this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
return this;
};

Transform.prototype.clean = function clean() {
var node = this._node;
var c;
...
```

#### <a name="apidoc.element.famous.Quaternion.normalize"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.</span>normalize (q, output)](#apidoc.element.famous.Quaternion.normalize)
- description and source-code
```javascript
function normalize(q, output) {
    var w = q.w;
    var x = q.x;
    var y = q.y;
    var z = q.z;
    var length = sqrt(w * w + x * x + y * y + z * z);
    if (length === 0) return this;
    length = 1 / length;
    output.w *= length;
    output.x *= length;
    output.y *= length;
    output.z *= length;
    return output;
}
```
- example usage
```shell
...
var c = frontierEdges[j][1];
var B = vertices[b].vertex;
var C = vertices[c].vertex;

var AB = Vec3.subtract(B, A, AB_REGISTER);
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
...
```



# <a name="apidoc.module.famous.Quaternion.prototype"></a>[module famous.Quaternion.prototype](#apidoc.module.famous.Quaternion.prototype)

#### <a name="apidoc.element.famous.Quaternion.prototype.clear"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>clear ()](#apidoc.element.famous.Quaternion.prototype.clear)
- description and source-code
```javascript
function clear() {
    this.w = 1;
    this.x = 0;
    this.y = 0;
    this.z = 0;
    return this;
}
```
- example usage
```shell
...
    }
    this.event.current = 1;
    this.event.points = 1;
    id = t[0].identifier;
    this.trackedPointerIDs[0] = id;

    this.last1.set(t[0].pageX, t[0].pageY);
    this.velocity1.clear();
    this.delta1.clear();
    this.event.pointers.push(this.pointer1);
}
if (t[1] && this.trackedPointerIDs[1] !== t[1].identifier) {
    if (this.trackedGestures.tap) {
        threshold = (this.options.tap && this.options.tap.threshold) || 250;
        if (this.event.time - this.timeOfPointer < threshold) this.multiTap = 2;
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.conjugate"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>conjugate ()](#apidoc.element.famous.Quaternion.prototype.conjugate)
- description and source-code
```javascript
function conjugate() {
    this.x = -this.x;
    this.y = -this.y;
    this.z = -this.z;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.prototype.copy"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>copy (q)](#apidoc.element.famous.Quaternion.prototype.copy)
- description and source-code
```javascript
function copy(q) {
    this.w = q.w;
    this.x = q.x;
    this.y = q.y;
    this.z = q.z;
    return this;
}
```
- example usage
```shell
...
        this.event.rotationVelocity = 0;
    }
    this.event.pointers.push(this.pointer2);
}

this.event.status = 'start';
if (this.event.points === 1) {
    this.center.copy(this.last1);
    this.centerDelta.clear();
    this.centerVelocity.clear();
    if (this.trackedGestures.pinch) {
        this.event.scale = 1;
        this.event.scaleDelta = 0;
        this.event.scaleVelocity = 0;
    }
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.dot"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>dot (q)](#apidoc.element.famous.Quaternion.prototype.dot)
- description and source-code
```javascript
function dot(q) {
    return this.w * q.w + this.x * q.x + this.y * q.y + this.z * q.z;
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.fromAngleAxis"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>fromAngleAxis (angle, x, y, z)](#apidoc.element.famous.Quaternion.prototype.fromAngleAxis)
- description and source-code
```javascript
function fromAngleAxis(angle, x, y, z) {
    var len = sqrt(x * x + y * y + z * z);
    if (len === 0) {
        this.w = 1;
        this.x = this.y = this.z = 0;
    }
    else {
        len = 1 / len;
        var halfTheta = angle * 0.5;
        var s = sin(halfTheta);
        this.w = cos(halfTheta);
        this.x = s * x * len;
        this.y = s * y * len;
        this.z = s * z * len;
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.prototype.fromEuler"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>fromEuler (x, y, z)](#apidoc.element.famous.Quaternion.prototype.fromEuler)
- description and source-code
```javascript
function fromEuler(x, y, z) {
    var hx = x * 0.5;
    var hy = y * 0.5;
    var hz = z * 0.5;

    var sx = sin(hx);
    var sy = sin(hy);
    var sz = sin(hz);
    var cx = cos(hx);
    var cy = cos(hy);
    var cz = cos(hz);

    this.w = cx * cy * cz - sx * sy * sz;
    this.x = sx * cy * cz + cx * sy * sz;
    this.y = cx * sy * cz - sx * cy * sz;
    this.z = cx * cy * sz + sx * sy * cz;

    return this;
}
```
- example usage
```shell
...
        this.rotation = new QuatTransitionable(v[0], v[1], v[2], v[3], this);
    }
    var q = Q_REGISTER;
    if (typeof w === 'number') {
        q.set(w, x, y, z);
    }
    else {
        q.fromEuler(x, y, z);
        callback = options;
        options = w;
    }
    this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
    return this;
};
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.invert"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>invert ()](#apidoc.element.famous.Quaternion.prototype.invert)
- description and source-code
```javascript
function invert() {
    this.w = -this.w;
    this.x = -this.x;
    this.y = -this.y;
    this.z = -this.z;
    return this;
}
```
- example usage
```shell
...
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
    this.addFeature(distance, ABC, [a, b, c]);
}
else {
    var reference = Vec3.subtract(referencePoint, A, VEC_REGISTER);
    if (Vec3.dot(ABC, reference) > -0.001) ABC.invert();
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.leftMultiply"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>leftMultiply (q)](#apidoc.element.famous.Quaternion.prototype.leftMultiply)
- description and source-code
```javascript
function leftMultiply(q) {
    var x1 = q.x;
    var y1 = q.y;
    var z1 = q.z;
    var w1 = q.w || 0;
    var x2 = this.x;
    var y2 = this.y;
    var z2 = this.z;
    var w2 = this.w;

    this.w = w1*w2 - x1*x2 - y1*y2 - z1*z2;
    this.x = x1*w2 + x2*w1 + y2*z1 - y1*z2;
    this.y = y1*w2 + y2*w1 + x1*z2 - x2*z1;
    this.z = z1*w2 + z2*w1 + x2*y1 - x1*y2;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.prototype.length"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>length ()](#apidoc.element.famous.Quaternion.prototype.length)
- description and source-code
```javascript
function length() {
    var w = this.w;
    var x = this.x;
    var y = this.y;
    var z = this.z;
    return sqrt(w * w + x * x + y * y + z * z);
}
```
- example usage
```shell
...
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
if (this.trackedGestures.rotate) {
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.multiply"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>multiply (q)](#apidoc.element.famous.Quaternion.prototype.multiply)
- description and source-code
```javascript
function multiply(q) {
    var x1 = this.x;
    var y1 = this.y;
    var z1 = this.z;
    var w1 = this.w;
    var x2 = q.x;
    var y2 = q.y;
    var z2 = q.z;
    var w2 = q.w || 0;

    this.w = w1 * w2 - x1 * x2 - y1 * y2 - z1 * z2;
    this.x = x1 * w2 + x2 * w1 + y2 * z1 - y1 * z2;
    this.y = y1 * w2 + y2 * w1 + x1 * z2 - x2 * z1;
    this.z = z1 * w2 + z2 * w1 + x2 * y1 - x1 * y2;
    return this;
}
```
- example usage
```shell
...
}
else {
    rotQ.fromEuler(x, y, z);
    callback = options;
    options = w;
}

var q = referenceQ.multiply(rotQ);
this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
return this;
};

Transform.prototype.clean = function clean() {
var node = this._node;
var c;
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.normalize"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>normalize ()](#apidoc.element.famous.Quaternion.prototype.normalize)
- description and source-code
```javascript
function normalize() {
    var w = this.w;
    var x = this.x;
    var y = this.y;
    var z = this.z;
    var length = sqrt(w * w + x * x + y * y + z * z);
    if (length === 0) return this;
    length = 1 / length;
    this.w *= length;
    this.x *= length;
    this.y *= length;
    this.z *= length;
    return this;
}
```
- example usage
```shell
...
var c = frontierEdges[j][1];
var B = vertices[b].vertex;
var C = vertices[c].vertex;

var AB = Vec3.subtract(B, A, AB_REGISTER);
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.rotateVector"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>rotateVector (v, output)](#apidoc.element.famous.Quaternion.prototype.rotateVector)
- description and source-code
```javascript
function rotateVector(v, output) {
    var cw = this.w;
    var cx = -this.x;
    var cy = -this.y;
    var cz = -this.z;

    var vx = v.x;
    var vy = v.y;
    var vz = v.z;

    var tw = -cx * vx - cy * vy - cz * vz;
    var tx = vx * cw + vy * cz - cy * vz;
    var ty = vy * cw + cx * vz - vx * cz;
    var tz = vz * cw + vx * cy - cx * vy;

    var w = cw;
    var x = -cx;
    var y = -cy;
    var z = -cz;

    output.x = tx * w + x * tw + y * tz - ty * z;
    output.y = ty * w + y * tw + tx * z - x * tz;
    output.z = tz * w + z * tw + x * ty - tx * y;
    return output;
}
```
- example usage
```shell
...
var p = body.position;
var q = body.orientation;
var rot = q;
var loc = p;

if (oq.w !== 1) {
    rot = Quaternion.multiply(q, oq, QUAT_REGISTER);
    loc = oq.rotateVector(p, VEC_REGISTER);
}

transform.position[0] = o.x+loc.x;
transform.position[1] = o.y+loc.y;
transform.position[2] = o.z+loc.z;

transform.rotation[0] = rot.x;
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>set (w, x , y, z)](#apidoc.element.famous.Quaternion.prototype.set)
- description and source-code
```javascript
function set(w, x , y, z) {
    if (w != null) this.w = w;
    if (x != null) this.x = x;
    if (y != null) this.y = y;
    if (z != null) this.z = z;
    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Quaternion.prototype.slerp"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>slerp (q, t, output)](#apidoc.element.famous.Quaternion.prototype.slerp)
- description and source-code
```javascript
function slerp(q, t, output) {
    var w = this.w;
    var x = this.x;
    var y = this.y;
    var z = this.z;

    var qw = q.w;
    var qx = q.x;
    var qy = q.y;
    var qz = q.z;

    var omega;
    var cosomega;
    var sinomega;
    var scaleFrom;
    var scaleTo;

    cosomega = w * qw + x * qx + y * qy + z * qz;
    if ((1.0 - cosomega) > 1e-5) {
        omega = acos(cosomega);
        sinomega = sin(omega);
        scaleFrom = sin((1.0 - t) * omega) / sinomega;
        scaleTo = sin(t * omega) / sinomega;
    }
    else {
        scaleFrom = 1.0 - t;
        scaleTo = t;
    }

    output.w = w * scaleFrom + qw * scaleTo;
    output.x = x * scaleFrom + qx * scaleTo;
    output.y = y * scaleFrom + qy * scaleTo;
    output.z = z * scaleFrom + qz * scaleTo;

    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.prototype.toEuler"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>toEuler (output)](#apidoc.element.famous.Quaternion.prototype.toEuler)
- description and source-code
```javascript
function toEuler(output) {
    var w = this.w;
    var x = this.x;
    var y = this.y;
    var z = this.z;

    var xx = x * x;
    var yy = y * y;
    var zz = z * z;

    var ty = 2 * (x * z + y * w);
    ty = ty < -1 ? -1 : ty > 1 ? 1 : ty;

    output.x = atan2(2 * (x * w - y * z), 1 - 2 * (xx + yy));
    output.y = asin(ty);
    output.z = atan2(2 * (z * w - x * y), 1 - 2 * (yy + zz));

    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Quaternion.prototype.toMatrix"></a>[function <span class="apidocSignatureSpan">famous.Quaternion.prototype.</span>toMatrix (output)](#apidoc.element.famous.Quaternion.prototype.toMatrix)
- description and source-code
```javascript
function toMatrix(output) {
    var w = this.w;
    var x = this.x;
    var y = this.y;
    var z = this.z;

    var xx = x*x;
    var yy = y*y;
    var zz = z*z;
    var xy = x*y;
    var xz = x*z;
    var yz = y*z;

    return output.set([
        1 - 2 * (yy + zz), 2 * (xy - w*z), 2 * (xz + w*y),
        2 * (xy + w*z), 1 - 2 * (xx + zz), 2 * (yz - w*x),
        2 * (xz - w*y), 2 * (yz + w*x), 1 - 2 * (xx + yy)
    ]);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Registry"></a>[module famous.Registry](#apidoc.module.famous.Registry)

#### <a name="apidoc.element.famous.Registry.Registry"></a>[function <span class="apidocSignatureSpan">famous.</span>Registry ()](#apidoc.element.famous.Registry.Registry)
- description and source-code
```javascript
function Registry() {
    this._keyToValue = {};
    this._values = [];
    this._keys = [];
    this._keyToIndex = {};
    this._freedIndices = [];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Registry.prototype"></a>[module famous.Registry.prototype](#apidoc.module.famous.Registry.prototype)

#### <a name="apidoc.element.famous.Registry.prototype.get"></a>[function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>get (key)](#apidoc.element.famous.Registry.prototype.get)
- description and source-code
```javascript
function get(key) {
    return this._keyToValue[key];
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Registry.prototype.getKeyToValue"></a>[function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>getKeyToValue ()](#apidoc.element.famous.Registry.prototype.getKeyToValue)
- description and source-code
```javascript
function getKeyToValue() {
    return this._keyToValue;
}
```
- example usage
```shell
...
 */
WebGLRenderer.prototype.draw = function draw(renderState) {
    var time = this.compositor.getTime();

    this.gl.clear(this.gl.COLOR_BUFFER_BIT | this.gl.DEPTH_BUFFER_BIT);
    this.textureManager.update(time);

    this.meshRegistryKeys = sorter(this.meshRegistry.getKeys(), this.meshRegistry.getKeyToValue());

    this.setGlobalUniforms(renderState);
    this.drawCutouts();
    this.drawMeshes();
};

/**
...
```

#### <a name="apidoc.element.famous.Registry.prototype.getKeys"></a>[function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>getKeys ()](#apidoc.element.famous.Registry.prototype.getKeys)
- description and source-code
```javascript
function getKeys() {
    return this._keys;
}
```
- example usage
```shell
...
 */
WebGLRenderer.prototype.draw = function draw(renderState) {
    var time = this.compositor.getTime();

    this.gl.clear(this.gl.COLOR_BUFFER_BIT | this.gl.DEPTH_BUFFER_BIT);
    this.textureManager.update(time);

    this.meshRegistryKeys = sorter(this.meshRegistry.getKeys(), this.meshRegistry.getKeyToValue());

    this.setGlobalUniforms(renderState);
    this.drawCutouts();
    this.drawMeshes();
};

/**
...
```

#### <a name="apidoc.element.famous.Registry.prototype.getValues"></a>[function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>getValues ()](#apidoc.element.famous.Registry.prototype.getValues)
- description and source-code
```javascript
function getValues() {
    return this._values;
}
```
- example usage
```shell
...
 * @return {undefined} undefined
 */
WebGLRenderer.prototype.drawMeshes = function drawMeshes() {
    var gl = this.gl;
    var buffers;
    var mesh;

    var meshes = this.meshRegistry.getValues();

    for(var i = 0; i < meshes.length; i++) {
mesh = meshes[i];

if (!mesh) continue;

buffers = this.bufferRegistry.registry[mesh.geometry];
...
```

#### <a name="apidoc.element.famous.Registry.prototype.register"></a>[function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>register (key, value)](#apidoc.element.famous.Registry.prototype.register)
- description and source-code
```javascript
function register(key, value) {
    var index = this._keyToIndex[key];
    if (index == null) {
        index = this._freedIndices.pop();
        if (index === undefined) index = this._values.length;

        this._values[index] = value;
        this._keys[index] = key;

        this._keyToIndex[key] = index;
        this._keyToValue[key] = value;
    }
    else {
        this._keyToValue[key] = value;
        this._values[index] = value;
    }
}
```
- example usage
```shell
...

'use strict';

var Vec3 = require('../math/Vec3');
var Mat33 = require('../math/Mat33');

var ObjectManager = require('../utilities/ObjectManager');
ObjectManager.register('DynamicGeometry', DynamicGeometry);
ObjectManager.register('DynamicGeometryFeature', DynamicGeometryFeature);
var oMRequestDynamicGeometryFeature = ObjectManager.requestDynamicGeometryFeature;
var oMFreeDynamicGeometryFeature = ObjectManager.freeDynamicGeometryFeature;

var TRIPLE_REGISTER = new Vec3();

/**
...
```

#### <a name="apidoc.element.famous.Registry.prototype.unregister"></a>[function <span class="apidocSignatureSpan">famous.Registry.prototype.</span>unregister (key)](#apidoc.element.famous.Registry.prototype.unregister)
- description and source-code
```javascript
function unregister(key) {
    var index = this._keyToIndex[key];

    if (index != null) {
        this._freedIndices.push(index);
        this._keyToValue[key] = null;
        this._keyToIndex[key] = null;
        this._values[index] = null;
        this._keys[index] = null;
    }
}
```
- example usage
```shell
...
*
* @method
* @param {String} path Path used as id of target mesh.
*
* @return {undefined} undefined
*/
WebGLRenderer.prototype.removeMesh = function removeMesh(path) {
   this.meshRegistry.unregister(path);
};

/**
* Creates or retreives cutout
*
* @method
* @param {String} path Path used as id of cutout in cutout registry.
...
```



# <a name="apidoc.module.famous.RequestAnimationFrameLoop"></a>[module famous.RequestAnimationFrameLoop](#apidoc.module.famous.RequestAnimationFrameLoop)

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.RequestAnimationFrameLoop"></a>[function <span class="apidocSignatureSpan">famous.</span>RequestAnimationFrameLoop ()](#apidoc.element.famous.RequestAnimationFrameLoop.RequestAnimationFrameLoop)
- description and source-code
```javascript
function RequestAnimationFrameLoop() {
    var _this = this;

    // References to objects to be updated on next frame.
    this._updates = [];

    this._looper = function(time) {
        _this.loop(time);
    };
    this._time = 0;
    this._stoppedAt = 0;
    this._sleep = 0;

    // Indicates whether the engine should be restarted when the tab/ window is
    // being focused again (visibility change).
    this._startOnVisibilityChange = true;

    // requestId as returned by requestAnimationFrame function;
    this._rAF = null;

    this._sleepDiff = true;

    // The engine is being started on instantiation.
    // TODO(alexanderGugel)
    this.start();

    // The RequestAnimationFrameLoop supports running in a non-browser
    // environment (e.g. Worker).
    if (DOCUMENT_ACCESS) {
        document.addEventListener(VENDOR_VISIBILITY_CHANGE, function() {
            _this._onVisibilityChange();
        });
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.RequestAnimationFrameLoop.prototype"></a>[module famous.RequestAnimationFrameLoop.prototype](#apidoc.module.famous.RequestAnimationFrameLoop.prototype)

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype._onFocus"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_onFocus ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._onFocus)
- description and source-code
```javascript
function _onFocus() {
    if (this._startOnVisibilityChange) {
        this._start();
    }
}
```
- example usage
```shell
...
* @return {undefined} undefined
*/
RequestAnimationFrameLoop.prototype._onVisibilityChange = function _onVisibilityChange() {
   if (document[VENDOR_HIDDEN]) {
       this._onUnfocus();
   }
   else {
       this._onFocus();
   }
};

/**
* Internal helper function to be invoked as soon as the window/ tab is being
* focused after a visibiltiy change.
*
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype._onUnfocus"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_onUnfocus ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._onUnfocus)
- description and source-code
```javascript
function _onUnfocus() {
    this._stop();
}
```
- example usage
```shell
...
 * @method
 * @private
 *
 * @return {undefined} undefined
 */
RequestAnimationFrameLoop.prototype._onVisibilityChange = function _onVisibilityChange() {
    if (document[VENDOR_HIDDEN]) {
        this._onUnfocus();
    }
    else {
        this._onFocus();
    }
};

/**
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype._onVisibilityChange"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_onVisibilityChange ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._onVisibilityChange)
- description and source-code
```javascript
function _onVisibilityChange() {
    if (document[VENDOR_HIDDEN]) {
        this._onUnfocus();
    }
    else {
        this._onFocus();
    }
}
```
- example usage
```shell
...
   // TODO(alexanderGugel)
   this.start();

   // The RequestAnimationFrameLoop supports running in a non-browser
   // environment (e.g. Worker).
   if (DOCUMENT_ACCESS) {
       document.addEventListener(VENDOR_VISIBILITY_CHANGE, function() {
           _this._onVisibilityChange();
       });
   }
}

/**
* Handle the switching of tabs.
*
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype._start"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_start ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._start)
- description and source-code
```javascript
function _start() {
    this._running = true;
    this._sleepDiff = true;
    this._rAF = rAF(this._looper);
}
```
- example usage
```shell
...
* @method
* @private
*
* @return {undefined} undefined
*/
RequestAnimationFrameLoop.prototype._onFocus = function _onFocus() {
   if (this._startOnVisibilityChange) {
       this._start();
   }
};

/**
* Internal helper function to be invoked as soon as the window/ tab is being
* unfocused (hidden) after a visibiltiy change.
*
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype._stop"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>_stop ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype._stop)
- description and source-code
```javascript
function _stop() {
    this._running = false;
    this._stoppedAt = this._time;

    // Bug in old versions of Fx. Explicitly cancel.
    cAF(this._rAF);
}
```
- example usage
```shell
...
*
* @method  _onFocus
* @private
*
* @return {undefined} undefined
*/
RequestAnimationFrameLoop.prototype._onUnfocus = function _onUnfocus() {
   this._stop();
};

/**
* Starts the RequestAnimationFrameLoop. When switching to a differnt tab/
* window (changing the visibiltiy), the engine will be retarted when switching
* back to a visible state.
*
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.isRunning"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>isRunning ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.isRunning)
- description and source-code
```javascript
function isRunning() {
    return this._running;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.loop"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>loop (time)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.loop)
- description and source-code
```javascript
function loop(time) {
    this.step(time);
    this._rAF = rAF(this._looper);
    return this;
}
```
- example usage
```shell
...
function RequestAnimationFrameLoop() {
var _this = this;

// References to objects to be updated on next frame.
this._updates = [];

this._looper = function(time) {
    _this.loop(time);
};
this._time = 0;
this._stoppedAt = 0;
this._sleep = 0;

// Indicates whether the engine should be restarted when the tab/ window is
// being focused again (visibility change).
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.noLongerUpdate"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>noLongerUpdate (updateable)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.noLongerUpdate)
- description and source-code
```javascript
function noLongerUpdate(updateable) {
    var index = this._updates.indexOf(updateable);
    if (index > -1) {
        this._updates.splice(index, 1);
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.start"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>start ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.start)
- description and source-code
```javascript
function start() {
    if (!this._running) {
        this._startOnVisibilityChange = true;
        this._start();
    }
    return this;
}
```
- example usage
```shell
...
// requestId as returned by requestAnimationFrame function;
this._rAF = null;

this._sleepDiff = true;

// The engine is being started on instantiation.
// TODO(alexanderGugel)
this.start();

// The RequestAnimationFrameLoop supports running in a non-browser
// environment (e.g. Worker).
if (DOCUMENT_ACCESS) {
    document.addEventListener(VENDOR_VISIBILITY_CHANGE, function() {
        _this._onVisibilityChange();
    });
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.step"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>step (time)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.step)
- description and source-code
```javascript
function step(time) {
    this._time = time;
    if (this._sleepDiff) {
        this._sleep += time - this._stoppedAt;
        this._sleepDiff = false;
    }

    // The same timetamp will be emitted immediately before and after visibility
    // change.
    var normalizedTime = time - this._sleep;
    for (var i = 0, len = this._updates.length ; i < len ; i++) {
        this._updates[i].update(normalizedTime);
    }
    return this;
}
```
- example usage
```shell
...
*
* @return {FamousEngine} this
*/
FamousEngine.prototype.handleFrame = function handleFrame (messages) {
   if (!messages) throw new Error('handleFrame must be called with an array of messages');
   if (!messages.length) throw new Error('FRAME must be sent with a time');

   this.step(messages.shift());
   return this;
};

/**
* step updates the clock and the scene graph and then sends the draw commands
* that accumulated in the update to the renderers.
*
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.stop"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>stop ()](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.stop)
- description and source-code
```javascript
function stop() {
    if (this._running) {
        this._startOnVisibilityChange = false;
        this._stop();
    }
    return this;
}
```
- example usage
```shell
...
var message = ev.data ? ev.data : ev;
if (message[0] === Commands.ENGINE) {
    switch (message[1]) {
        case Commands.START:
            _this._engine.start();
            break;
        case Commands.STOP:
            _this._engine.stop();
            break;
        default:
            console.error(
                'Unknown ENGINE command "' + message[1] + '"'
            );
            break;
    }
...
```

#### <a name="apidoc.element.famous.RequestAnimationFrameLoop.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.RequestAnimationFrameLoop.prototype.</span>update (updateable)](#apidoc.element.famous.RequestAnimationFrameLoop.prototype.update)
- description and source-code
```javascript
function update(updateable) {
    if (this._updates.indexOf(updateable) === -1) {
        this._updates.push(updateable);
    }
    return this;
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Rotation"></a>[module famous.Rotation](#apidoc.module.famous.Rotation)

#### <a name="apidoc.element.famous.Rotation.Rotation"></a>[function <span class="apidocSignatureSpan">famous.</span>Rotation (node)](#apidoc.element.famous.Rotation.Rotation)
- description and source-code
```javascript
function Rotation(node) {
    Position.call(this, node);

    var initial = node.getRotation();

    var x = initial[0];
    var y = initial[1];
    var z = initial[2];
    var w = initial[3];

    var xx = x * x;
    var yy = y * y;
    var zz = z * z;

    var ty = 2 * (x * z + y * w);
    ty = ty < -1 ? -1 : ty > 1 ? 1 : ty;

    var rx = Math.atan2(2 * (x * w - y * z), 1 - 2 * (xx + yy));
    var ry = Math.asin(ty);
    var rz = Math.atan2(2 * (z * w - x * y), 1 - 2 * (yy + zz));

    this._x.set(rx);
    this._y.set(ry);
    this._z.set(rz);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Rotation.prototype"></a>[module famous.Rotation.prototype](#apidoc.module.famous.Rotation.prototype)

#### <a name="apidoc.element.famous.Rotation.prototype.constructor"></a>[function <span class="apidocSignatureSpan">famous.Rotation.prototype.</span>constructor (node)](#apidoc.element.famous.Rotation.prototype.constructor)
- description and source-code
```javascript
function Rotation(node) {
    Position.call(this, node);

    var initial = node.getRotation();

    var x = initial[0];
    var y = initial[1];
    var z = initial[2];
    var w = initial[3];

    var xx = x * x;
    var yy = y * y;
    var zz = z * z;

    var ty = 2 * (x * z + y * w);
    ty = ty < -1 ? -1 : ty > 1 ? 1 : ty;

    var rx = Math.atan2(2 * (x * w - y * z), 1 - 2 * (xx + yy));
    var ry = Math.asin(ty);
    var rz = Math.atan2(2 * (z * w - x * y), 1 - 2 * (yy + zz));

    this._x.set(rx);
    this._y.set(ry);
    this._z.set(rz);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Rotation.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Rotation.prototype.</span>onUpdate ()](#apidoc.element.famous.Rotation.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setRotation(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Rotation.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Rotation.prototype.</span>update ()](#apidoc.element.famous.Rotation.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setRotation(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Scale"></a>[module famous.Scale](#apidoc.module.famous.Scale)

#### <a name="apidoc.element.famous.Scale.Scale"></a>[function <span class="apidocSignatureSpan">famous.</span>Scale (node)](#apidoc.element.famous.Scale.Scale)
- description and source-code
```javascript
function Scale(node) {
    Position.call(this, node);

    this._x.set(1);
    this._y.set(1);
    this._z.set(1);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Scale.prototype"></a>[module famous.Scale.prototype](#apidoc.module.famous.Scale.prototype)

#### <a name="apidoc.element.famous.Scale.prototype.constructor"></a>[function <span class="apidocSignatureSpan">famous.Scale.prototype.</span>constructor (node)](#apidoc.element.famous.Scale.prototype.constructor)
- description and source-code
```javascript
function Scale(node) {
    Position.call(this, node);

    this._x.set(1);
    this._y.set(1);
    this._z.set(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Scale.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Scale.prototype.</span>onUpdate ()](#apidoc.element.famous.Scale.prototype.onUpdate)
- description and source-code
```javascript
function update() {
    this._node.setScale(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Scale.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.Scale.prototype.</span>update ()](#apidoc.element.famous.Scale.prototype.update)
- description and source-code
```javascript
function update() {
    this._node.setScale(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Scene"></a>[module famous.Scene](#apidoc.module.famous.Scene)

#### <a name="apidoc.element.famous.Scene.Scene"></a>[function <span class="apidocSignatureSpan">famous.</span>Scene (selector, updater)](#apidoc.element.famous.Scene.Scene)
- description and source-code
```javascript
function Scene(selector, updater) {
    if (!selector) throw new Error('Scene needs to be created with a DOM selector');
    if (!updater) throw new Error('Scene needs to be created with a class like Famous');

    Node.call(this);         // Scene inherits from node

    this._globalUpdater = updater; // The updater that will both
                                   // send messages to the renderers
                                   // and update dirty nodes

    this._selector = selector; // reference to the DOM selector
                               // that represents the element
                               // in the dom that this context
                               // inhabits

    this.mount(selector); // Mount the context to itself
                          // (it is its own parent)

    this._globalUpdater                  // message a request for the dom
        .message(Commands.NEED_SIZE_FOR)  // size of the context so that
        .message(selector);               // the scene graph has a total size

    this.show(); // the context begins shown (it's already present in the dom)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Scene.prototype"></a>[module famous.Scene.prototype](#apidoc.module.famous.Scene.prototype)

#### <a name="apidoc.element.famous.Scene.prototype.constructor"></a>[function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>constructor (selector, updater)](#apidoc.element.famous.Scene.prototype.constructor)
- description and source-code
```javascript
function Scene(selector, updater) {
    if (!selector) throw new Error('Scene needs to be created with a DOM selector');
    if (!updater) throw new Error('Scene needs to be created with a class like Famous');

    Node.call(this);         // Scene inherits from node

    this._globalUpdater = updater; // The updater that will both
                                   // send messages to the renderers
                                   // and update dirty nodes

    this._selector = selector; // reference to the DOM selector
                               // that represents the element
                               // in the dom that this context
                               // inhabits

    this.mount(selector); // Mount the context to itself
                          // (it is its own parent)

    this._globalUpdater                  // message a request for the dom
        .message(Commands.NEED_SIZE_FOR)  // size of the context so that
        .message(selector);               // the scene graph has a total size

    this.show(); // the context begins shown (it's already present in the dom)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Scene.prototype.getDispatch"></a>[function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>getDispatch ()](#apidoc.element.famous.Scene.prototype.getDispatch)
- description and source-code
```javascript
function getDispatch() {
    console.warn('Scene#getDispatch is deprecated, require the dispatch directly');
    return Dispatch;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Scene.prototype.getSelector"></a>[function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>getSelector ()](#apidoc.element.famous.Scene.prototype.getSelector)
- description and source-code
```javascript
function getSelector() {
    return this._selector;
}
```
- example usage
```shell
...
* @return {FamousEngine} this
*/
FamousEngine.prototype.addScene = function addScene (scene) {
   var selector = scene._selector;

   var current = this._scenes[selector];
   if (current && current !== scene) current.dismount();
   if (!scene.isMounted()) scene.mount(scene.getSelector());
   this._scenes[selector] = scene;
   return this;
};

/**
* Remove a scene.
*
...
```

#### <a name="apidoc.element.famous.Scene.prototype.getUpdater"></a>[function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>getUpdater ()](#apidoc.element.famous.Scene.prototype.getUpdater)
- description and source-code
```javascript
function getUpdater() {
    return this._updater;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Scene.prototype.mount"></a>[function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>mount (path)](#apidoc.element.famous.Scene.prototype.mount)
- description and source-code
```javascript
function mount(path) {
    if (this.isMounted())
        throw new Error('Scene is already mounted at: ' + this.getLocation());
    Dispatch.mount(path, this);
    this._id = path;
    this._mounted = true;
    this._parent = this;
    TransformSystem.registerTransformAtPath(path);
    SizeSystem.registerSizeAtPath(path);
}
```
- example usage
```shell
...
    if (node.onMount) node.onMount(path);

    for (i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onMount)
            components[i].onMount(node, i);

    for (i = 0, len = children.length ; i < len ; i++)
        if (children[i] && children[i].mount) children[i].mount(path + '/' + i);
        else if (children[i]) this.mount(path + '/' + i, children[i]);
}

if (parent.isShown()) {
    if (node.onShow) node.onShow();
    for (i = 0, len = components.length ; i < len ; i++)
        if (components[i] && components[i].onShow)
...
```

#### <a name="apidoc.element.famous.Scene.prototype.onReceive"></a>[function <span class="apidocSignatureSpan">famous.Scene.prototype.</span>onReceive (event, payload)](#apidoc.element.famous.Scene.prototype.onReceive)
- description and source-code
```javascript
function onReceive(event, payload) {
    // TODO: In the future the dom element that the context is attached to
    // should have a representation as a component. It would be render sized
    // and the context would receive its size the same way that any render size
    // component receives its size.
    if (event === 'CONTEXT_RESIZE') {
        if (payload.length < 2)
            throw new Error(
                    'CONTEXT_RESIZE\'s payload needs to be at least a pair' +
                    ' of pixel sizes'
            );

        this.setSizeMode('absolute', 'absolute', 'absolute');
        this.setAbsoluteSize(payload[0],
                             payload[1],
                             payload[2] ? payload[2] : 0);

        this._updater.message(Commands.WITH).message(this._selector).message(Commands.READY);
    }
}
```
- example usage
```shell
...
   if (!node) return;

   this.addChildrenToQueue(node);
   var child;

   while ((child = this.breadthFirstNext()))
       if (child && child.onReceive)
           child.onReceive(event, payload);

};

/**
* dispatchUIevent takes a path, an event name, and a payload and dispatches them in
* a manner anologous to DOM bubbling. It first traverses down to the node specified at
* the path. That node receives the event first, and then every ancestor receives the event
...
```



# <a name="apidoc.module.famous.Size"></a>[module famous.Size](#apidoc.module.famous.Size)

#### <a name="apidoc.element.famous.Size.Size"></a>[function <span class="apidocSignatureSpan">famous.</span>Size (node)](#apidoc.element.famous.Size.Size)
- description and source-code
```javascript
function Size(node) {
    this._node = node;
    this._id = node.addComponent(this);
    this._requestingUpdate = false;

    var initialProportionalSize = node.getProportionalSize();
    var initialDifferentialSize = node.getDifferentialSize();
    var initialAbsoluteSize = node.getAbsoluteSize();

    this._proportional = {
        x: new Transitionable(initialProportionalSize[0]),
        y: new Transitionable(initialProportionalSize[1]),
        z: new Transitionable(initialProportionalSize[2])
    };
    this._differential = {
        x: new Transitionable(initialDifferentialSize[0]),
        y: new Transitionable(initialDifferentialSize[1]),
        z: new Transitionable(initialDifferentialSize[2])
    };
    this._absolute = {
        x: new Transitionable(initialAbsoluteSize[0]),
        y: new Transitionable(initialAbsoluteSize[1]),
        z: new Transitionable(initialAbsoluteSize[2])
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Size.prototype"></a>[module famous.Size.prototype](#apidoc.module.famous.Size.prototype)

#### <a name="apidoc.element.famous.Size.prototype._isActive"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>_isActive (type)](#apidoc.element.famous.Size.prototype._isActive)
- description and source-code
```javascript
function _isActive(type) {
    return type.x.isActive() || type.y.isActive() || type.z.isActive();
}
```
- example usage
```shell
...
* @param {String} type Type of size
*
* @return {Boolean} boolean indicating whether the new state has been applied
*/

Size.prototype.isActive = function isActive(){
   return (
       this._isActive(this._absolute) ||
       this._isActive(this._proportional) ||
       this._isActive(this._differential)
   );
};

/**
* When the node this component is attached to updates, update the value
...
```

#### <a name="apidoc.element.famous.Size.prototype.get"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>get ()](#apidoc.element.famous.Size.prototype.get)
- description and source-code
```javascript
function get() {
    return this._node.getSize();
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Size.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>getValue ()](#apidoc.element.famous.Size.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return {
        sizeMode: SizeSystem.get(this._node.getLocation()).getSizeMode(),
        absolute: {
            x: this._absolute.x.get(),
            y: this._absolute.y.get(),
            z: this._absolute.z.get()
        },
        differential: {
            x: this._differential.x.get(),
            y: this._differential.y.get(),
            z: this._differential.z.get()
        },
        proportional: {
            x: this._proportional.x.get(),
            y: this._proportional.y.get(),
            z: this._proportional.z.get()
        }
    };
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Size.prototype.halt"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>halt ()](#apidoc.element.famous.Size.prototype.halt)
- description and source-code
```javascript
function halt() {
    this._proportional.x.halt();
    this._proportional.y.halt();
    this._proportional.z.halt();
    this._differential.x.halt();
    this._differential.y.halt();
    this._differential.z.halt();
    this._absolute.x.halt();
    this._absolute.y.halt();
    this._absolute.z.halt();
    return this;
}
```
- example usage
```shell
...
* Stops Opacity transition
*
* @method
*
* @return {Opacity} this
*/
Opacity.prototype.halt = function halt() {
   this._value.halt();
   return this;
};

/**
* Tells whether or not the opacity is in a transition
*
* @method
...
```

#### <a name="apidoc.element.famous.Size.prototype.isActive"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>isActive ()](#apidoc.element.famous.Size.prototype.isActive)
- description and source-code
```javascript
function isActive(){
    return (
        this._isActive(this._absolute) ||
        this._isActive(this._proportional) ||
        this._isActive(this._differential)
    );
}
```
- example usage
```shell
...
* Tells whether or not the opacity is in a transition
*
* @method
*
* @return {Boolean} whether or not the opacity is transitioning
*/
Opacity.prototype.isActive = function isActive(){
   return this._value.isActive();
};

/**
* When the node this component is attached to updates, update the value
* of the Node's opacity.
*
* @method
...
```

#### <a name="apidoc.element.famous.Size.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>onUpdate ()](#apidoc.element.famous.Size.prototype.onUpdate)
- description and source-code
```javascript
function onUpdate() {
    var abs = this._absolute;
    this._node.setAbsoluteSize(
        abs.x.get(),
        abs.y.get(),
        abs.z.get()
    );
    var prop = this._proportional;
    var diff = this._differential;
    this._node.setProportionalSize(
        prop.x.get(),
        prop.y.get(),
        prop.z.get()
    );
    this._node.setDifferentialSize(
        diff.x.get(),
        diff.y.get(),
        diff.z.get()
    );

    if (this.isActive()) this._node.requestUpdateOnNextTick(this._id);
    else this._requestingUpdate = false;
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Size.prototype.setAbsolute"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setAbsolute (x, y, z, options, callback)](#apidoc.element.famous.Size.prototype.setAbsolute)
- description and source-code
```javascript
function setAbsolute(x, y, z, options, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    var xCallback;
    var yCallback;
    var zCallback;

    if (z != null) {
        zCallback = callback;
    }
    else if (y != null) {
        yCallback = callback;
    }
    else if (x != null) {
        xCallback = callback;
    }

    var abs = this._absolute;
    if (x != null) {
        abs.x.set(x, options, xCallback);
    }
    if (y != null) {
        abs.y.set(y, options, yCallback);
    }
    if (z != null) {
        abs.z.set(z, options, zCallback);
    }
}
```
- example usage
```shell
...
 *
 * @return {Boolean} boolean indicating whether the new state has been applied
 */
Size.prototype.setValue = function setValue(state) {
if (this.toString() === state.component) {
    this.setMode.apply(this, state.sizeMode);
    if (state.absolute) {
        this.setAbsolute(state.absolute.x, state.absolute.y, state.absolute.z);
    }
    if (state.differential) {
        this.setAbsolute(state.differential.x, state.differential.y, state.differential.z);
    }
    if (state.proportional) {
        this.setAbsolute(state.proportional.x, state.proportional.y, state.proportional.z);
    }
...
```

#### <a name="apidoc.element.famous.Size.prototype.setDifferential"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setDifferential (x, y, z, options, callback)](#apidoc.element.famous.Size.prototype.setDifferential)
- description and source-code
```javascript
function setDifferential(x, y, z, options, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    var xCallback;
    var yCallback;
    var zCallback;

    if (z != null) {
        zCallback = callback;
    }
    else if (y != null) {
        yCallback = callback;
    }
    else if (x != null) {
        xCallback = callback;
    }

    var diff = this._differential;
    if (x != null) {
        diff.x.set(x, options, xCallback);
    }
    if (y != null) {
        diff.y.set(y, options, yCallback);
    }
    if (z != null) {
        diff.z.set(z, options, zCallback);
    }
    return this;
}
```
- example usage
```shell
...
 * @param {Number} z    z-Size to be added to the relatively sized node in
 *                      pixels ("depth").
 *
 * @return {Node} this
 */
Node.prototype.setDifferentialSize = function setDifferentialSize (x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._sizeID).setDifferential(x, y, z);
    else if (this.isMounted())
        SizeSystem.get(this.getLocation()).setDifferential(x, y, z);
    else throw new Error('This node does not have access to a size component');
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.Size.prototype.setMode"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setMode (x, y, z)](#apidoc.element.famous.Size.prototype.setMode)
- description and source-code
```javascript
function setMode(x, y, z) {
    this._node.setSizeMode(x, y, z);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Size.prototype.setProportional"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setProportional (x, y, z, options, callback)](#apidoc.element.famous.Size.prototype.setProportional)
- description and source-code
```javascript
function setProportional(x, y, z, options, callback) {
    if (!this._requestingUpdate) {
        this._node.requestUpdate(this._id);
        this._requestingUpdate = true;
    }

    var xCallback;
    var yCallback;
    var zCallback;

    if (z != null) {
        zCallback = callback;
    }
    else if (y != null) {
        yCallback = callback;
    }
    else if (x != null) {
        xCallback = callback;
    }

    var prop = this._proportional;
    if (x != null) {
        prop.x.set(x, options, xCallback);
    }
    if (y != null) {
        prop.y.set(y, options, yCallback);
    }
    if (z != null) {
        prop.z.set(z, options, zCallback);
    }
    return this;
}
```
- example usage
```shell
...
 * @param {Number} y    y-Size in pixels ("height").
 * @param {Number} z    z-Size in pixels ("depth").
 *
 * @return {Node} this
 */
Node.prototype.setProportionalSize = function setProportionalSize (x, y, z) {
    if (!this.constructor.NO_DEFAULT_COMPONENTS)
        this.getComponent(this._sizeID).setProportional(x, y, z);
    else if (this.isMounted())
        SizeSystem.get(this.getLocation()).setProportional(x, y, z);
    else throw new Error('This node does not have access to a size component');
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.Size.prototype.setValue"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>setValue (state)](#apidoc.element.famous.Size.prototype.setValue)
- description and source-code
```javascript
function setValue(state) {
    if (this.toString() === state.component) {
        this.setMode.apply(this, state.sizeMode);
        if (state.absolute) {
            this.setAbsolute(state.absolute.x, state.absolute.y, state.absolute.z);
        }
        if (state.differential) {
            this.setAbsolute(state.differential.x, state.differential.y, state.differential.z);
        }
        if (state.proportional) {
            this.setAbsolute(state.proportional.x, state.proportional.y, state.proportional.z);
        }
    }
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Size.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.Size.prototype.</span>toString ()](#apidoc.element.famous.Size.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'Size';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```



# <a name="apidoc.module.famous.Texture"></a>[module famous.Texture](#apidoc.module.famous.Texture)

#### <a name="apidoc.element.famous.Texture.Texture"></a>[function <span class="apidocSignatureSpan">famous.</span>Texture (gl, options)](#apidoc.element.famous.Texture.Texture)
- description and source-code
```javascript
function Texture(gl, options) {
    options = options || {};
    this.id = gl.createTexture();
    this.width = options.width || 0;
    this.height = options.height || 0;
    this.mipmap = options.mipmap;
    this.format = options.format || 'RGBA';
    this.type = options.type || 'UNSIGNED_BYTE';
    this.gl = gl;

    this.bind();

    gl.pixelStorei(gl.UNPACK_FLIP_Y_WEBGL, options.flipYWebgl || false);
    gl.pixelStorei(gl.UNPACK_PREMULTIPLY_ALPHA_WEBGL, options.premultiplyAlphaWebgl || false);

    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_MAG_FILTER, gl[options.magFilter] || gl.NEAREST);
    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_MIN_FILTER, gl[options.minFilter] || gl.NEAREST);

    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_S, gl[options.wrapS] || gl.CLAMP_TO_EDGE);
    gl.texParameteri(gl.TEXTURE_2D, gl.TEXTURE_WRAP_T, gl[options.wrapT] || gl.CLAMP_TO_EDGE);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Texture.prototype"></a>[module famous.Texture.prototype](#apidoc.module.famous.Texture.prototype)

#### <a name="apidoc.element.famous.Texture.prototype.bind"></a>[function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>bind ()](#apidoc.element.famous.Texture.prototype.bind)
- description and source-code
```javascript
function bind() {
    this.gl.bindTexture(this.gl.TEXTURE_2D, this.id);
    return this;
}
```
- example usage
```shell
...
 */
OBJLoader.load = function load(url, cb, options) {
if (!this.cached[url]) {
    if (!this.requests[url]) {
        this.requests[url] = [cb];
        loadURL(
            url,
            this._onsuccess.bind(
                this,
                url,
                options
            )
        );
    }
    else {
...
```

#### <a name="apidoc.element.famous.Texture.prototype.readBack"></a>[function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>readBack (x, y, width, height)](#apidoc.element.famous.Texture.prototype.readBack)
- description and source-code
```javascript
function readBack(x, y, width, height) {
    var gl = this.gl;
    var pixels;
    x = x || 0;
    y = y || 0;
    width = width || this.width;
    height = height || this.height;
    var fb = gl.createFramebuffer();
    gl.bindFramebuffer(gl.FRAMEBUFFER, fb);
    gl.framebufferTexture2D(gl.FRAMEBUFFER, gl.COLOR_ATTACHMENT0, gl.TEXTURE_2D, this.id, 0);
    if (gl.checkFramebufferStatus(gl.FRAMEBUFFER) === gl.FRAMEBUFFER_COMPLETE) {
        pixels = new Uint8Array(width * height * 4);
        gl.readPixels(x, y, width, height, gl.RGBA, gl.UNSIGNED_BYTE, pixels);
    }
    return pixels;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Texture.prototype.setArray"></a>[function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>setArray (input)](#apidoc.element.famous.Texture.prototype.setArray)
- description and source-code
```javascript
function setArray(input) {
    this.gl.texImage2D(this.gl.TEXTURE_2D, 0, this.gl[this.format], this.width, this.height, 0, this.gl[this.format], this.gl[this
.type], input);
    return this;
}
```
- example usage
```shell
...
    slot: slot
};

// Handle array

if (Array.isArray(source) || source instanceof Uint8Array || source instanceof Float32Array) {
    this.bindTexture(textureId);
    texture.setArray(source);
    spec.isLoaded = true;
}

// Handle video

else if (source instanceof HTMLVideoElement) {
    source.addEventListener('loadeddata', function() {
...
```

#### <a name="apidoc.element.famous.Texture.prototype.setImage"></a>[function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>setImage (img)](#apidoc.element.famous.Texture.prototype.setImage)
- description and source-code
```javascript
function setImage(img) {
    this.gl.texImage2D(this.gl.TEXTURE_2D, 0, this.gl[this.format], this.gl[this.format], this.gl[this.type], img);
    if (this.mipmap) this.gl.generateMipmap(this.gl.TEXTURE_2D);
    return this;
}
```
- example usage
```shell
...
    var options = input.options || {};
    var texture = this.registry[textureId];
    var spec;

    if (!texture) {

texture = new Texture(this.gl, options);
texture.setImage(this._checkerboard);

// Add texture to registry

spec = this.registry[textureId] = {
    resampleRate: options.resampleRate || null,
    lastResample: null,
    isLoaded: false,
...
```

#### <a name="apidoc.element.famous.Texture.prototype.unbind"></a>[function <span class="apidocSignatureSpan">famous.Texture.prototype.</span>unbind ()](#apidoc.element.famous.Texture.prototype.unbind)
- description and source-code
```javascript
function unbind() {
    this.gl.bindTexture(this.gl.TEXTURE_2D, null);
    return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.TextureManager"></a>[module famous.TextureManager](#apidoc.module.famous.TextureManager)

#### <a name="apidoc.element.famous.TextureManager.TextureManager"></a>[function <span class="apidocSignatureSpan">famous.</span>TextureManager (gl)](#apidoc.element.famous.TextureManager.TextureManager)
- description and source-code
```javascript
function TextureManager(gl) {
    this.registry = [];
    this._needsResample = [];

    this._activeTexture = 0;
    this._boundTexture = null;

    this._checkerboard = createCheckerboard();

    this.gl = gl;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.TextureManager.prototype"></a>[module famous.TextureManager.prototype](#apidoc.module.famous.TextureManager.prototype)

#### <a name="apidoc.element.famous.TextureManager.prototype.bindTexture"></a>[function <span class="apidocSignatureSpan">famous.TextureManager.prototype.</span>bindTexture (id)](#apidoc.element.famous.TextureManager.prototype.bindTexture)
- description and source-code
```javascript
function bindTexture(id) {
    var spec = this.registry[id];

    if (this._activeTexture !== spec.slot) {
        this.gl.activeTexture(this.gl.TEXTURE0 + spec.slot);
        this._activeTexture = spec.slot;
    }

    if (this._boundTexture !== id) {
        this._boundTexture = id;
        spec.texture.bind();
    }

    if (this._needsResample[spec.id]) {

        // TODO: Account for resampling of arrays.

        spec.texture.setImage(spec.source);
        this._needsResample[spec.id] = false;
    }
}
```
- example usage
```shell
...
/**
* Binds this texture as the selected target.
*
* @method
* @return {Object} Current texture instance.
*/
Texture.prototype.bind = function bind() {
   this.gl.bindTexture(this.gl.TEXTURE_2D, this.id);
   return this;
};

/**
* Erases the texture data in the given texture slot.
*
* @method
...
```

#### <a name="apidoc.element.famous.TextureManager.prototype.register"></a>[function <span class="apidocSignatureSpan">famous.TextureManager.prototype.</span>register (input, slot)](#apidoc.element.famous.TextureManager.prototype.register)
- description and source-code
```javascript
function register(input, slot) {
    var _this = this;

    var source = input.data;
    var textureId = input.id;
    var options = input.options || {};
    var texture = this.registry[textureId];
    var spec;

    if (!texture) {

        texture = new Texture(this.gl, options);
        texture.setImage(this._checkerboard);

        // Add texture to registry

        spec = this.registry[textureId] = {
            resampleRate: options.resampleRate || null,
            lastResample: null,
            isLoaded: false,
            texture: texture,
            source: source,
            id: textureId,
            slot: slot
        };

        // Handle array

        if (Array.isArray(source) || source instanceof Uint8Array || source instanceof Float32Array) {
            this.bindTexture(textureId);
            texture.setArray(source);
            spec.isLoaded = true;
        }

        // Handle video

        else if (source instanceof HTMLVideoElement) {
            source.addEventListener('loadeddata', function() {
                _this.bindTexture(textureId);
                texture.setImage(source);

                spec.isLoaded = true;
                spec.source = source;
            });
        }

        // Handle image url

        else if (typeof source === 'string') {
            loadImage(source, function (img) {
                _this.bindTexture(textureId);
                texture.setImage(img);

                spec.isLoaded = true;
                spec.source = img;
            });
        }
    }

    return textureId;
}
```
- example usage
```shell
...

'use strict';

var Vec3 = require('../math/Vec3');
var Mat33 = require('../math/Mat33');

var ObjectManager = require('../utilities/ObjectManager');
ObjectManager.register('DynamicGeometry', DynamicGeometry);
ObjectManager.register('DynamicGeometryFeature', DynamicGeometryFeature);
var oMRequestDynamicGeometryFeature = ObjectManager.requestDynamicGeometryFeature;
var oMFreeDynamicGeometryFeature = ObjectManager.freeDynamicGeometryFeature;

var TRIPLE_REGISTER = new Vec3();

/**
...
```

#### <a name="apidoc.element.famous.TextureManager.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.TextureManager.prototype.</span>update (time)](#apidoc.element.famous.TextureManager.prototype.update)
- description and source-code
```javascript
function update(time) {
    var registryLength = this.registry.length;

    for (var i = 1; i < registryLength; i++) {
        var texture = this.registry[i];

        if (texture && texture.isLoaded && texture.resampleRate) {
            if (!texture.lastResample || time - texture.lastResample > texture.resampleRate) {
                if (!this._needsResample[texture.id]) {
                    this._needsResample[texture.id] = true;
                    texture.lastResample = time;
                }
            }
        }
    }
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.TextureRegistry"></a>[module famous.TextureRegistry](#apidoc.module.famous.TextureRegistry)

#### <a name="apidoc.element.famous.TextureRegistry.get"></a>[function <span class="apidocSignatureSpan">famous.TextureRegistry.</span>get (accessor)](#apidoc.element.famous.TextureRegistry.get)
- description and source-code
```javascript
function get(accessor) {
    if (!this.registry[accessor]) {
        throw 'Texture "' + accessor + '" not found!';
    }
    else {
        return this.registry[accessor];
    }
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.TextureRegistry.register"></a>[function <span class="apidocSignatureSpan">famous.TextureRegistry.</span>register (accessor, data, options)](#apidoc.element.famous.TextureRegistry.register)
- description and source-code
```javascript
function register(accessor, data, options) {
    if (accessor) {
        this.registry[accessor] = { id: this.textureIds++, __isATexture__: true, data: data, options: options };
        return this.registry[accessor];
    }
	else {
        return { id: this.textureIds++, data: data, __isATexture__: true, options: options };
    }
}
```
- example usage
```shell
...

'use strict';

var Vec3 = require('../math/Vec3');
var Mat33 = require('../math/Mat33');

var ObjectManager = require('../utilities/ObjectManager');
ObjectManager.register('DynamicGeometry', DynamicGeometry);
ObjectManager.register('DynamicGeometryFeature', DynamicGeometryFeature);
var oMRequestDynamicGeometryFeature = ObjectManager.requestDynamicGeometryFeature;
var oMFreeDynamicGeometryFeature = ObjectManager.freeDynamicGeometryFeature;

var TRIPLE_REGISTER = new Vec3();

/**
...
```



# <a name="apidoc.module.famous.Transform"></a>[module famous.Transform](#apidoc.module.famous.Transform)

#### <a name="apidoc.element.famous.Transform.Transform"></a>[function <span class="apidocSignatureSpan">famous.</span>Transform (node)](#apidoc.element.famous.Transform.Transform)
- description and source-code
```javascript
function Transform(node) {
    this._node = node;
    this._id = node.addComponent(this);
    this.origin = null;
    this.mountPoint = null;
    this.align = null;
    this.scale = null;
    this.position = null;
    this.rotation = null;

    this._dirty = false;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Transform.prototype"></a>[module famous.Transform.prototype](#apidoc.module.famous.Transform.prototype)

#### <a name="apidoc.element.famous.Transform.prototype.clean"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>clean ()](#apidoc.element.famous.Transform.prototype.clean)
- description and source-code
```javascript
function clean() {
    var node = this._node;
    var c;
    var isDirty = false;
    if ((c = this.origin) && c._dirty) {
        node.setOrigin(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.mountPoint) && c._dirty) {
        node.setMountPoint(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.align) && c._dirty) {
        node.setAlign(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.scale) && c._dirty) {
        node.setScale(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.position) && c._dirty) {
        node.setPosition(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.rotation) && c._dirty) {
        var q = c.get();
        node.setRotation(q[0], q[1], q[2], q[3]);
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if (isDirty) this._node.requestUpdateOnNextTick(this._id);
    else this._dirty = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Transform.prototype.getValue"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>getValue ()](#apidoc.element.famous.Transform.prototype.getValue)
- description and source-code
```javascript
function getValue() {
    return {
        component: this.toString(),
        origin: this.origin && this.origin.get(),
        mountPoint: this.mountPoint && this.mountPoint.get(),
        align: this.align && this.align.get(),
        scale: this.scale && this.scale.get(),
        position: this.position && this.position.get(),
        rotation: this.rotation && this.rotation.get()
    };
}
```
- example usage
```shell
...
        }

        value.spec.vectors.rotation[3] = transform.vectors.rotation[3];
    }

    for (i = 0; i < numberOfChildren ; i++)
        if (this._children[i] && this._children[i].getValue)
            value.children.push(this._children[i].getValue());

    for (i = 0 ; i < numberOfComponents ; i++)
        if (this._components[i] && this._components[i].getValue)
            value.components.push(this._components[i].getValue());

    return value;
};
...
```

#### <a name="apidoc.element.famous.Transform.prototype.onUpdate"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>onUpdate ()](#apidoc.element.famous.Transform.prototype.onUpdate)
- description and source-code
```javascript
function clean() {
    var node = this._node;
    var c;
    var isDirty = false;
    if ((c = this.origin) && c._dirty) {
        node.setOrigin(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.mountPoint) && c._dirty) {
        node.setMountPoint(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.align) && c._dirty) {
        node.setAlign(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.scale) && c._dirty) {
        node.setScale(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.position) && c._dirty) {
        node.setPosition(c.x.get(), c.y.get(), c.z.get());
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if ((c = this.rotation) && c._dirty) {
        var q = c.get();
        node.setRotation(q[0], q[1], q[2], q[3]);
        c._dirty = c.isActive();
        isDirty = isDirty || c._dirty;
    }
    if (isDirty) this._node.requestUpdateOnNextTick(this._id);
    else this._dirty = false;
}
```
- example usage
```shell
...
   TransformSystem.update();

   while (nextQueue.length) queue.unshift(nextQueue.pop());

   while (queue.length) {
       item = queue.shift();
       if (item && item.update) item.update(time);
       if (item && item.onUpdate) item.onUpdate(time);
   }

   this._inUpdate = false;
};

/**
* requestUpdates takes a class that has an onUpdate method and puts it
...
```

#### <a name="apidoc.element.famous.Transform.prototype.rotate"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>rotate (x, y, z, w, options, callback)](#apidoc.element.famous.Transform.prototype.rotate)
- description and source-code
```javascript
function rotate(x, y, z, w, options, callback) {
    if (!this.rotation) {
        var v = this._node.getRotation();
        this.rotation = new QuatTransitionable(v[0], v[1], v[2], v[3], this);
    }
    var queue = this.rotation._t._queue;
    var len = queue.length;
    var referenceQ;
    var arr;
    if (len !== 0) arr = queue[len - 5];
    else arr = this.rotation._t._state;
    referenceQ = Q2_REGISTER.set(arr[3], arr[0], arr[1], arr[2]);

    var rotQ = Q_REGISTER;
    if (typeof w === 'number') {
        rotQ.set(w, x, y, z);
    }
    else {
        rotQ.fromEuler(x, y, z);
        callback = options;
        options = w;
    }

    var q = referenceQ.multiply(rotQ);
    this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Transform.prototype.setAlign"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setAlign (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setAlign)
- description and source-code
```javascript
function setAlign(x, y, z, options, callback) {
    if (!this.align) {
        var v = this._node.getAlign();
        this.align = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.align.set(x, y, z, options, callback);
    return this;
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Transform.prototype.setMountPoint"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setMountPoint (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setMountPoint)
- description and source-code
```javascript
function setMountPoint(x, y, z, options, callback) {
    if (!this.mountPoint) {
        var v = this._node.getMountPoint();
        this.mountPoint = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.mountPoint.set(x, y, z, options, callback);
    return this;
}
```
- example usage
```shell
...
 * of the Node's mount point.
 *
 * @method
 *
 * @return {undefined} undefined
 */
MountPoint.prototype.update = function update() {
    this._node.setMountPoint(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

MountPoint.prototype.onUpdate = MountPoint.prototype.update;

module.exports = MountPoint;
...
```

#### <a name="apidoc.element.famous.Transform.prototype.setOrigin"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setOrigin (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setOrigin)
- description and source-code
```javascript
function setOrigin(x, y, z, options, callback) {
    if (!this.origin) {
        var v = this._node.getOrigin();
        this.origin = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.origin.set(x, y, z, options, callback);
    return this;
}
```
- example usage
```shell
...
 * of the Node's origin
 *
 * @method
 *
 * @return {undefined} undefined
 */
Origin.prototype.update = function update() {
    this._node.setOrigin(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Origin.prototype.onUpdate = Origin.prototype.update;

module.exports = Origin;
...
```

#### <a name="apidoc.element.famous.Transform.prototype.setPosition"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setPosition (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setPosition)
- description and source-code
```javascript
function setPosition(x, y, z, options, callback) {
    if (!this.position) {
        var v = this._node.getPosition();
        this.position = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.position.set(x, y, z, options, callback);
    return this;
}
```
- example usage
```shell
...
* of the Node's position
*
* @method
*
* @return {undefined} undefined
*/
Position.prototype.update = function update () {
   this._node.setPosition(this._x.get(), this._y.get(), this._z.get());
   this._checkUpdate();
};

Position.prototype.onUpdate = Position.prototype.update;

/**
* Setter for X position
...
```

#### <a name="apidoc.element.famous.Transform.prototype.setRotation"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setRotation (x, y, z, w, options, callback)](#apidoc.element.famous.Transform.prototype.setRotation)
- description and source-code
```javascript
function setRotation(x, y, z, w, options, callback) {
    if (!this.rotation) {
        var v = this._node.getRotation();
        this.rotation = new QuatTransitionable(v[0], v[1], v[2], v[3], this);
    }
    var q = Q_REGISTER;
    if (typeof w === 'number') {
        q.set(w, x, y, z);
    }
    else {
        q.fromEuler(x, y, z);
        callback = options;
        options = w;
    }
    this.rotation.set(q.x, q.y, q.z, q.w, options, callback);
    return this;
}
```
- example usage
```shell
...
 * of the Node's rotation
 *
 * @method
 *
 * @return {undefined} undefined
 */
Rotation.prototype.update = function update() {
    this._node.setRotation(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Rotation.prototype.onUpdate = Rotation.prototype.update;

module.exports = Rotation;
...
```

#### <a name="apidoc.element.famous.Transform.prototype.setScale"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setScale (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.setScale)
- description and source-code
```javascript
function setScale(x, y, z, options, callback) {
    if (!this.scale) {
        var v = this._node.getScale();
        this.scale = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    this.scale.set(x, y, z, options, callback);
    return this;
}
```
- example usage
```shell
...
 * of the Node's scale.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Scale.prototype.update = function update() {
    this._node.setScale(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Scale.prototype.onUpdate = Scale.prototype.update;

module.exports = Scale;
...
```

#### <a name="apidoc.element.famous.Transform.prototype.setState"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>setState (state)](#apidoc.element.famous.Transform.prototype.setState)
- description and source-code
```javascript
function setState(state) {
    if (this.toString() === state.component) {
        if (state.origin) {
            this.setOrigin(state.origin.x, state.origin.y, state.origin.z);
        }
        if (state.mountPoint) {
            this.setMountPoint(state.mountPoint.x, state.mountPoint.y, state.mountPoint.z);
        }
        if (state.align) {
            this.setAlign(state.align.x, state.align.y, state.align.z);
        }
        if (state.scale) {
            this.setScale(state.scale.x, state.scale.y, state.scale.z);
        }
        if (state.position) {
            this.setPosition(state.position.x, state.position.y, state.position.z);
        }
        if (state.rotation) {
            this.setRotation(state.rotation.x, state.rotation.y, state.rotation.z, state.rotation.w);
        }
        return true;
    }
    return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Transform.prototype.toString"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>toString ()](#apidoc.element.famous.Transform.prototype.toString)
- description and source-code
```javascript
function toString() {
    return 'Transform';
}
```
- example usage
```shell
...
 *
 * @method
 *
 * @return {Object} the state of the component
 */
Camera.prototype.getValue = function getValue() {
    return {
        component: this.toString(),
        projectionType: this._projectionType,
        focalDepth: this._focalDepth,
        near: this._near,
        far: this._far
    };
};
...
```

#### <a name="apidoc.element.famous.Transform.prototype.translate"></a>[function <span class="apidocSignatureSpan">famous.Transform.prototype.</span>translate (x, y, z, options, callback)](#apidoc.element.famous.Transform.prototype.translate)
- description and source-code
```javascript
function translate(x, y, z, options, callback) {
    if (!this.position) {
        var v = this._node.getPosition();
        this.position = new Vec3Transitionable(v[0], v[1], v[2], this);
    }
    var p = this.position;
    var xq = p.x._queue;
    var yq = p.y._queue;
    var zq = p.z._queue;
    var xEnd = x == null ? null : x + (xq.length > 0 ? xq[xq.length - 5] : p.x._state);
    var yEnd = y == null ? null : y + (yq.length > 0 ? yq[yq.length - 5] : p.y._state);
    var zEnd = z == null ? null : z + (zq.length > 0 ? zq[zq.length - 5] : p.z._state);
    this.position.set(xEnd, yEnd, zEnd, options, callback);
    return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Transitionable"></a>[module famous.Transitionable](#apidoc.module.famous.Transitionable)

#### <a name="apidoc.element.famous.Transitionable.Transitionable"></a>[function <span class="apidocSignatureSpan">famous.</span>Transitionable (initialState)](#apidoc.element.famous.Transitionable.Transitionable)
- description and source-code
```javascript
function Transitionable(initialState) {
    this._queue = [];
    this._from = null;
    this._state = null;
    this._startedAt = null;
    this._pausedAt = null;
    if (initialState != null) this.from(initialState);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.Transitionable.prototype"></a>[module famous.Transitionable.prototype](#apidoc.module.famous.Transitionable.prototype)

#### <a name="apidoc.element.famous.Transitionable.prototype._interpolate"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>_interpolate (output, from, to, progress, method)](#apidoc.element.famous.Transitionable.prototype._interpolate)
- description and source-code
```javascript
function _interpolate(output, from, to, progress, method) {
    if (to instanceof Object) {
        if (method === 'slerp') {
            var x, y, z, w;
            var qx, qy, qz, qw;
            var omega, cosomega, sinomega, scaleFrom, scaleTo;

            x = from[0];
            y = from[1];
            z = from[2];
            w = from[3];

            qx = to[0];
            qy = to[1];
            qz = to[2];
            qw = to[3];

            if (progress === 1) {
                output[0] = qx;
                output[1] = qy;
                output[2] = qz;
                output[3] = qw;
                return output;
            }

            cosomega = w * qw + x * qx + y * qy + z * qz;
            if ((1.0 - cosomega) > 1e-5) {
                omega = Math.acos(cosomega);
                sinomega = Math.sin(omega);
                scaleFrom = Math.sin((1.0 - progress) * omega) / sinomega;
                scaleTo = Math.sin(progress * omega) / sinomega;
            }
            else {
                scaleFrom = 1.0 - progress;
                scaleTo = progress;
            }

            output[0] = x * scaleFrom + qx * scaleTo;
            output[1] = y * scaleFrom + qy * scaleTo;
            output[2] = z * scaleFrom + qz * scaleTo;
            output[3] = w * scaleFrom + qw * scaleTo;
        }
        else if (to instanceof Array) {
            for (var i = 0, len = to.length; i < len; i++) {
                output[i] = this._interpolate(output[i], from[i], to[i], progress, method);
            }
        }
        else {
            for (var key in to) {
                output[key] = this._interpolate(output[key], from[key], to[key], progress, method);
            }
        }
    }
    else {
        output = from + progress * (to - from);
    }
    return output;
}
```
- example usage
```shell
...
    output[0] = x * scaleFrom + qx * scaleTo;
    output[1] = y * scaleFrom + qy * scaleTo;
    output[2] = z * scaleFrom + qz * scaleTo;
    output[3] = w * scaleFrom + qw * scaleTo;
}
else if (to instanceof Array) {
    for (var i = 0, len = to.length; i < len; i++) {
        output[i] = this._interpolate(output[i], from[i], to[i], progress, method);
    }
}
else {
    for (var key in to) {
        output[key] = this._interpolate(output[key], from[key], to[key], progress, method);
    }
}
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype._sync"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>_sync (output, input)](#apidoc.element.famous.Transitionable.prototype._sync)
- description and source-code
```javascript
function _sync(output, input) {
    if (typeof input === 'number') output = input;
    else if (input instanceof Array) {
        if (output == null) output = [];
        for (var i = 0, len = input.length; i < len; i++) {
            output[i] = _sync(output[i], input[i]);
        }
    }
    else if (input instanceof Object) {
        if (output == null) output = {};
        for (var key in input) {
            output[key] = _sync(output[key], input[key]);
        }
    }
    return output;
}
```
- example usage
```shell
...
 *
 * @param  {Number|Array.Number}    initialState    initial state to
 *                                                  transition from
 * @return {Transitionable}         this
 */
Transitionable.prototype.from = function from(initialState) {
    this._state = initialState;
    this._from = this._sync(null, this._state);
    this._queue.length = 0;
    this._startedAt = this.constructor.Clock.now();
    this._pausedAt = null;
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.delay"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>delay (duration, callback)](#apidoc.element.famous.Transitionable.prototype.delay)
- description and source-code
```javascript
function delay(duration, callback) {
    var endState = this._queue.length > 0 ? this._queue[this._queue.length - 5] : this._state;
    return this.to(endState, Curves.flat, duration, callback);
}
```
- example usage
```shell
...
*    time and are the only way to trigger callbacks and mutate the internal
*    transition queue.
*
* @example
* var t = new Transitionable([0, 0]);
* t
*     .to([100, 0], 'linear', 1000)
*     .delay(1000)
*     .to([200, 0], 'outBounce', 1000);
*
* var div = document.createElement('div');
* div.style.background = 'blue';
* div.style.width = '100px';
* div.style.height = '100px';
* document.body.appendChild(div);
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.from"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>from (initialState)](#apidoc.element.famous.Transitionable.prototype.from)
- description and source-code
```javascript
function from(initialState) {
    this._state = initialState;
    this._from = this._sync(null, this._state);
    this._queue.length = 0;
    this._startedAt = this.constructor.Clock.now();
    this._pausedAt = null;
    return this;
}
```
- example usage
```shell
...
*/
function Transitionable(initialState) {
   this._queue = [];
   this._from = null;
   this._state = null;
   this._startedAt = null;
   this._pausedAt = null;
   if (initialState != null) this.from(initialState);
}

/**
* Internal Clock used for determining the current time for the ongoing
* transitions.
*
* @type {Performance|Date|Clock}
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.get"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>get (t)](#apidoc.element.famous.Transitionable.prototype.get)
- description and source-code
```javascript
function get(t) {
    if (this._queue.length === 0) return this._state;

    t = this._pausedAt ? this._pausedAt : t;
    t = t ? t : this.constructor.Clock.now();

    var progress = (t - this._startedAt) / this._queue[2];
    this._state = this._interpolate(
        this._state,
        this._from,
        this._queue[0],
        this._queue[1](progress > 1 ? 1 : progress),
        this._queue[4]
    );
    var state = this._state;
    if (progress >= 1) {
        this._startedAt = this._startedAt + this._queue[2];
        this._from = this._sync(this._from, this._state);
        this._queue.shift();
        this._queue.shift();
        this._queue.shift();
        var callback = this._queue.shift();
        this._queue.shift();
        if (callback) callback();
    }
    return progress > 1 ? this.get() : state;
}
```
- example usage
```shell
...
 * of the Node's align.
 *
 * @method
 *
 * @return {undefined} undefined
 */
Align.prototype.update = function update() {
    this._node.setAlign(this._x.get(), this._y.get(), this._z.get());
    this._checkUpdate();
};

Align.prototype.onUpdate = Align.prototype.update;

module.exports = Align;
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.halt"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>halt ()](#apidoc.element.famous.Transitionable.prototype.halt)
- description and source-code
```javascript
function halt() {
    return this.from(this.get());
}
```
- example usage
```shell
...
* Stops Opacity transition
*
* @method
*
* @return {Opacity} this
*/
Opacity.prototype.halt = function halt() {
   this._value.halt();
   return this;
};

/**
* Tells whether or not the opacity is in a transition
*
* @method
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.isActive"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>isActive ()](#apidoc.element.famous.Transitionable.prototype.isActive)
- description and source-code
```javascript
function isActive() {
    return this._queue.length > 0;
}
```
- example usage
```shell
...
* Tells whether or not the opacity is in a transition
*
* @method
*
* @return {Boolean} whether or not the opacity is transitioning
*/
Opacity.prototype.isActive = function isActive(){
   return this._value.isActive();
};

/**
* When the node this component is attached to updates, update the value
* of the Node's opacity.
*
* @method
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.isPaused"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>isPaused ()](#apidoc.element.famous.Transitionable.prototype.isPaused)
- description and source-code
```javascript
function isPaused() {
    return !!this._pausedAt;
}
```
- example usage
```shell
...
* var div = document.createElement('div');
* div.style.background = 'blue';
* div.style.width = '100px';
* div.style.height = '100px';
* document.body.appendChild(div);
*
* div.addEventListener('click', function() {
*     t.isPaused() ? t.resume() : t.pause();
* });
*
* requestAnimationFrame(function loop() {
*     div.style.transform = 'translateX(' + t.get()[0] + 'px)' + ' translateY(' + t.get()[1] + 'px)';
*     requestAnimationFrame(loop);
* });
*
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.override"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>override (finalState, curve, duration, callback, method)](#apidoc.element.famous.Transitionable.prototype.override)
- description and source-code
```javascript
function override(finalState, curve, duration, callback, method) {
    if (this._queue.length > 0) {
        if (finalState != null) this._queue[0] = finalState;
        if (curve != null)      this._queue[1] = curve.constructor === String ? Curves[curve] : curve;
        if (duration != null)   this._queue[2] = duration;
        if (callback != null)   this._queue[3] = callback;
        if (method != null)     this._queue[4] = method;
    }
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Transitionable.prototype.pause"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>pause ()](#apidoc.element.famous.Transitionable.prototype.pause)
- description and source-code
```javascript
function pause() {
    this._pausedAt = this.constructor.Clock.now();
    return this;
}
```
- example usage
```shell
...
};

Vec3Transitionable.prototype.isActive = function isActive() {
return this.x.isActive() || this.y.isActive() || this.z.isActive();
};

Vec3Transitionable.prototype.pause = function pause() {
this.x.pause();
this.y.pause();
this.z.pause();
return this;
};

Vec3Transitionable.prototype.resume = function resume() {
this.x.resume();
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.reset"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>reset (start)](#apidoc.element.famous.Transitionable.prototype.reset)
- description and source-code
```javascript
reset = function (start) {
    return this.from(start);
}
```
- example usage
```shell
...
* @param {Number} distance The distance of the feature from the origin.
* @param {Vec3} normal The facet normal.
* @param {Number[]} vertexIndices The indices of the vertices which compose the feature.
* @return {undefined} undefined
*/
DynamicGeometry.prototype.addFeature = function(distance, normal, vertexIndices) {
   var index = this._IDPool.features.length ? this._IDPool.features.pop() : this.features.length;
   this.features[index] = oMRequestDynamicGeometryFeature().reset(distance, normal, vertexIndices);
   this.numFeatures++;
};

/**
* Remove a feature and push its location in the feature array to the IDPool for later use.
*
* @method
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.resume"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>resume ()](#apidoc.element.famous.Transitionable.prototype.resume)
- description and source-code
```javascript
function resume() {
    var diff = this._pausedAt - this._startedAt;
    this._startedAt = this.constructor.Clock.now() - diff;
    this._pausedAt = null;
    return this;
}
```
- example usage
```shell
...
this.x.pause();
this.y.pause();
this.z.pause();
return this;
};

Vec3Transitionable.prototype.resume = function resume() {
this.x.resume();
this.y.resume();
this.z.resume();
return this;
};

Vec3Transitionable.prototype.halt = function halt() {
this.x.halt();
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>set (state, transition, callback)](#apidoc.element.famous.Transitionable.prototype.set)
- description and source-code
```javascript
set = function (state, transition, callback) {
    if (transition == null) {
        this.from(state);
        if (callback) callback();
    }
    else {
        this.to(state, transition.curve, transition.duration, callback, transition.method);
    }
    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Transitionable.prototype.to"></a>[function <span class="apidocSignatureSpan">famous.Transitionable.prototype.</span>to (finalState, curve, duration, callback, method)](#apidoc.element.famous.Transitionable.prototype.to)
- description and source-code
```javascript
function to(finalState, curve, duration, callback, method) {
    curve = curve != null && curve.constructor === String ? Curves[curve] : curve;
    if (this._queue.length === 0) {
        this._startedAt = this.constructor.Clock.now();
        this._pausedAt = null;
    }
    this._queue.push(
        finalState,
        curve != null ? curve : Curves.linear,
        duration != null ? duration : 100,
        callback,
        method
    );
    return this;
}
```
- example usage
```shell
...
*    are the only way to find state projected to the current (or provided)
*    time and are the only way to trigger callbacks and mutate the internal
*    transition queue.
*
* @example
* var t = new Transitionable([0, 0]);
* t
*     .to([100, 0], 'linear', 1000)
*     .delay(1000)
*     .to([200, 0], 'outBounce', 1000);
*
* var div = document.createElement('div');
* div.style.background = 'blue';
* div.style.width = '100px';
* div.style.height = '100px';
...
```



# <a name="apidoc.module.famous.UIManager"></a>[module famous.UIManager](#apidoc.module.famous.UIManager)

#### <a name="apidoc.element.famous.UIManager.UIManager"></a>[function <span class="apidocSignatureSpan">famous.</span>UIManager (thread, compositor, renderLoop)](#apidoc.element.famous.UIManager.UIManager)
- description and source-code
```javascript
function UIManager(thread, compositor, renderLoop) {
    this._thread = thread;
    this._compositor = compositor;
    this._renderLoop = renderLoop;

    this._renderLoop.update(this);

    var _this = this;
    this._thread.onmessage = function (ev) {
        var message = ev.data ? ev.data : ev;
        if (message[0] === Commands.ENGINE) {
            switch (message[1]) {
                case Commands.START:
                    _this._engine.start();
                    break;
                case Commands.STOP:
                    _this._engine.stop();
                    break;
                default:
                    console.error(
                        'Unknown ENGINE command "' + message[1] + '"'
                    );
                    break;
            }
        }
        else {
            _this._compositor.receiveCommands(message);
        }
    };
    this._thread.onerror = function (error) {
        console.error(error);
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.UIManager.prototype"></a>[module famous.UIManager.prototype](#apidoc.module.famous.UIManager.prototype)

#### <a name="apidoc.element.famous.UIManager.prototype.getCompositor"></a>[function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getCompositor ()](#apidoc.element.famous.UIManager.prototype.getCompositor)
- description and source-code
```javascript
function getCompositor() {
    return this._compositor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.UIManager.prototype.getEngine"></a>[function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getEngine ()](#apidoc.element.famous.UIManager.prototype.getEngine)
- description and source-code
```javascript
function getEngine() {
    return this._renderLoop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.UIManager.prototype.getRenderLoop"></a>[function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getRenderLoop ()](#apidoc.element.famous.UIManager.prototype.getRenderLoop)
- description and source-code
```javascript
function getRenderLoop() {
    return this._renderLoop;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.UIManager.prototype.getThread"></a>[function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>getThread ()](#apidoc.element.famous.UIManager.prototype.getThread)
- description and source-code
```javascript
function getThread() {
    return this._thread;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.UIManager.prototype.update"></a>[function <span class="apidocSignatureSpan">famous.UIManager.prototype.</span>update (time)](#apidoc.element.famous.UIManager.prototype.update)
- description and source-code
```javascript
function update(time) {
    this._thread.postMessage([Commands.FRAME, time]);
    var threadMessages = this._compositor.drawCommands();
    this._thread.postMessage(threadMessages);
    this._compositor.clearCommands();
}
```
- example usage
```shell
...
var time = this._clock.now();
var nextQueue = this._nextUpdateQueue;
var queue = this._updateQueue;
var item;

this._messages[1] = time;

SizeSystem.update();
TransformSystem.update();

while (nextQueue.length) queue.unshift(nextQueue.pop());

while (queue.length) {
    item = queue.shift();
    if (item && item.update) item.update(time);
...
```



# <a name="apidoc.module.famous.Vec2"></a>[module famous.Vec2](#apidoc.module.famous.Vec2)

#### <a name="apidoc.element.famous.Vec2.Vec2"></a>[function <span class="apidocSignatureSpan">famous.</span>Vec2 (x, y)](#apidoc.element.famous.Vec2.Vec2)
- description and source-code
```javascript
Vec2 = function (x, y) {
    if (x instanceof Array || x instanceof Float32Array) {
        this.x = x[0] || 0;
        this.y = x[1] || 0;
    }
    else {
        this.x = x || 0;
        this.y = y || 0;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec2.add"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>add (v1, v2, output)](#apidoc.element.famous.Vec2.add)
- description and source-code
```javascript
function add(v1, v2, output) {
    output.x = v1.x + v2.x;
    output.y = v1.y + v2.y;

    return output;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec2.clone"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>clone (v)](#apidoc.element.famous.Vec2.clone)
- description and source-code
```javascript
function clone(v) {
    return new Vec2(v.x, v.y);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec2.cross"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>cross (v1, v2)](#apidoc.element.famous.Vec2.cross)
- description and source-code
```javascript
cross = function (v1, v2) {
    return v1.x * v2.y - v1.y * v2.x;
}
```
- example usage
```shell
...
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}

var dist = VEC_REGISTER.length();
...
```

#### <a name="apidoc.element.famous.Vec2.dot"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>dot (v1, v2)](#apidoc.element.famous.Vec2.dot)
- description and source-code
```javascript
function dot(v1, v2) {
    return v1.x * v2.x + v1.y * v2.y;
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Vec2.normalize"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>normalize (v, output)](#apidoc.element.famous.Vec2.normalize)
- description and source-code
```javascript
function normalize(v, output) {
    var x = v.x;
    var y = v.y;

    var length = Math.sqrt(x * x + y * y) || 1;
    length = 1 / length;
    output.x = v.x * length;
    output.y = v.y * length;

    return output;
}
```
- example usage
```shell
...
var c = frontierEdges[j][1];
var B = vertices[b].vertex;
var C = vertices[c].vertex;

var AB = Vec3.subtract(B, A, AB_REGISTER);
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
...
```

#### <a name="apidoc.element.famous.Vec2.scale"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>scale (v, s, output)](#apidoc.element.famous.Vec2.scale)
- description and source-code
```javascript
function scale(v, s, output) {
    output.x = v.x * s;
    output.y = v.y * s;
    return output;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec2.subtract"></a>[function <span class="apidocSignatureSpan">famous.Vec2.</span>subtract (v1, v2, output)](#apidoc.element.famous.Vec2.subtract)
- description and source-code
```javascript
function subtract(v1, v2, output) {
    output.x = v1.x - v2.x;
    output.y = v1.y - v2.y;
    return output;
}
```
- example usage
```shell
...
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
...
```



# <a name="apidoc.module.famous.Vec2.prototype"></a>[module famous.Vec2.prototype](#apidoc.module.famous.Vec2.prototype)

#### <a name="apidoc.element.famous.Vec2.prototype.add"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>add (v)](#apidoc.element.famous.Vec2.prototype.add)
- description and source-code
```javascript
function add(v) {
    this.x += v.x;
    this.y += v.y;
    return this;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.clear"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>clear ()](#apidoc.element.famous.Vec2.prototype.clear)
- description and source-code
```javascript
function clear() {
    this.x = 0;
    this.y = 0;
    return this;
}
```
- example usage
```shell
...
    }
    this.event.current = 1;
    this.event.points = 1;
    id = t[0].identifier;
    this.trackedPointerIDs[0] = id;

    this.last1.set(t[0].pageX, t[0].pageY);
    this.velocity1.clear();
    this.delta1.clear();
    this.event.pointers.push(this.pointer1);
}
if (t[1] && this.trackedPointerIDs[1] !== t[1].identifier) {
    if (this.trackedGestures.tap) {
        threshold = (this.options.tap && this.options.tap.threshold) || 250;
        if (this.event.time - this.timeOfPointer < threshold) this.multiTap = 2;
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.copy"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>copy (v)](#apidoc.element.famous.Vec2.prototype.copy)
- description and source-code
```javascript
function copy(v) {
    this.x = v.x;
    this.y = v.y;
    return this;
}
```
- example usage
```shell
...
        this.event.rotationVelocity = 0;
    }
    this.event.pointers.push(this.pointer2);
}

this.event.status = 'start';
if (this.event.points === 1) {
    this.center.copy(this.last1);
    this.centerDelta.clear();
    this.centerVelocity.clear();
    if (this.trackedGestures.pinch) {
        this.event.scale = 1;
        this.event.scaleDelta = 0;
        this.event.scaleVelocity = 0;
    }
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.cross"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>cross (v)](#apidoc.element.famous.Vec2.prototype.cross)
- description and source-code
```javascript
cross = function (v) {
    return this.x * v.y - this.y * v.x;
}
```
- example usage
```shell
...
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}

var dist = VEC_REGISTER.length();
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.dot"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>dot (v)](#apidoc.element.famous.Vec2.prototype.dot)
- description and source-code
```javascript
dot = function (v) {
    return this.x * v.x + this.y * v.y;
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.invert"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>invert ()](#apidoc.element.famous.Vec2.prototype.invert)
- description and source-code
```javascript
function invert() {
    this.x *= -1;
    this.y *= -1;
    return this;
}
```
- example usage
```shell
...
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
    this.addFeature(distance, ABC, [a, b, c]);
}
else {
    var reference = Vec3.subtract(referencePoint, A, VEC_REGISTER);
    if (Vec3.dot(ABC, reference) > -0.001) ABC.invert();
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.isZero"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>isZero ()](#apidoc.element.famous.Vec2.prototype.isZero)
- description and source-code
```javascript
function isZero() {
    if (this.x !== 0 || this.y !== 0) return false;
    else return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec2.prototype.length"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>length ()](#apidoc.element.famous.Vec2.prototype.length)
- description and source-code
```javascript
function length() {
    var x = this.x;
    var y = this.y;

    return Math.sqrt(x * x + y * y);
}
```
- example usage
```shell
...
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
if (this.trackedGestures.rotate) {
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.map"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>map (fn)](#apidoc.element.famous.Vec2.prototype.map)
- description and source-code
```javascript
function map(fn) {
    this.x = fn(this.x);
    this.y = fn(this.y);
    return this;
}
```
- example usage
```shell
...
    var k;
    var pos;
    var tex;

    while (triangleIndex--) {
face = indices.slice(triangleIndex * 3, triangleIndex * 3 + 3);

pos = face.map(function(vertIndex) {
    return new Vec3(vertices[vertIndex * 3], vertices[vertIndex * 3 + 1], vertices[vertIndex * 3 + 2]);
});
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[1], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[1], pos[2], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[2], outputs[0]), 0.5, outputs[1]).toArray());

if (textureCoords) {
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.rotate"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>rotate (theta)](#apidoc.element.famous.Vec2.prototype.rotate)
- description and source-code
```javascript
rotate = function (theta) {
    var x = this.x;
    var y = this.y;

    var cosTheta = Math.cos(theta);
    var sinTheta = Math.sin(theta);

    this.x = x * cosTheta - y * sinTheta;
    this.y = x * sinTheta + y * cosTheta;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec2.prototype.scale"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>scale (s)](#apidoc.element.famous.Vec2.prototype.scale)
- description and source-code
```javascript
function scale(s) {
    if (s instanceof Vec2) {
        this.x *= s.x;
        this.y *= s.y;
    }
    else {
        this.x *= s;
        this.y *= s;
    }
    return this;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>set (x, y)](#apidoc.element.famous.Vec2.prototype.set)
- description and source-code
```javascript
function set(x, y) {
    if (x != null) this.x = x;
    if (y != null) this.y = y;
    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.subtract"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>subtract (v)](#apidoc.element.famous.Vec2.prototype.subtract)
- description and source-code
```javascript
function subtract(v) {
    this.x -= v.x;
    this.y -= v.y;
    return this;
}
```
- example usage
```shell
...
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
...
```

#### <a name="apidoc.element.famous.Vec2.prototype.toArray"></a>[function <span class="apidocSignatureSpan">famous.Vec2.prototype.</span>toArray ()](#apidoc.element.famous.Vec2.prototype.toArray)
- description and source-code
```javascript
function toArray() {
    return [this.x, this.y];
}
```
- example usage
```shell
...

    while (triangleIndex--) {
face = indices.slice(triangleIndex * 3, triangleIndex * 3 + 3);

pos = face.map(function(vertIndex) {
    return new Vec3(vertices[vertIndex * 3], vertices[vertIndex * 3 + 1], vertices[vertIndex * 3 + 2]);
});
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[1], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[1], pos[2], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[2], outputs[0]), 0.5, outputs[1]).toArray());

if (textureCoords) {
    tex = face.map(function(vertIndex) {
        return new Vec2(textureCoords[vertIndex * 2], textureCoords[vertIndex * 2 + 1]);
    });
...
```



# <a name="apidoc.module.famous.Vec3"></a>[module famous.Vec3](#apidoc.module.famous.Vec3)

#### <a name="apidoc.element.famous.Vec3.Vec3"></a>[function <span class="apidocSignatureSpan">famous.</span>Vec3 (x , y, z)](#apidoc.element.famous.Vec3.Vec3)
- description and source-code
```javascript
Vec3 = function (x , y, z){
    this.x = x || 0;
    this.y = y || 0;
    this.z = z || 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.add"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>add (v1, v2, output)](#apidoc.element.famous.Vec3.add)
- description and source-code
```javascript
function add(v1, v2, output) {
    output.x = v1.x + v2.x;
    output.y = v1.y + v2.y;
    output.z = v1.z + v2.z;
    return output;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec3.applyRotation"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>applyRotation (v, q, output)](#apidoc.element.famous.Vec3.applyRotation)
- description and source-code
```javascript
function applyRotation(v, q, output) {
    var cw = q.w;
    var cx = -q.x;
    var cy = -q.y;
    var cz = -q.z;

    var vx = v.x;
    var vy = v.y;
    var vz = v.z;

    var tw = -cx * vx - cy * vy - cz * vz;
    var tx = vx * cw + vy * cz - cy * vz;
    var ty = vy * cw + cx * vz - vx * cz;
    var tz = vz * cw + vx * cy - cx * vy;

    var w = cw;
    var x = -cx;
    var y = -cy;
    var z = -cz;

    output.x = tx * w + x * tw + y * tz - ty * z;
    output.y = ty * w + y * tw + tx * z - x * tz;
    output.z = tz * w + z * tw + x * ty - tx * y;
    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.clone"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>clone (v)](#apidoc.element.famous.Vec3.clone)
- description and source-code
```javascript
function clone(v) {
    return new Vec3(v.x, v.y, v.z);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.cross"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>cross (v1, v2, output)](#apidoc.element.famous.Vec3.cross)
- description and source-code
```javascript
function cross(v1, v2, output) {
    var x1 = v1.x;
    var y1 = v1.y;
    var z1 = v1.z;
    var x2 = v2.x;
    var y2 = v2.y;
    var z2 = v2.z;

    output.x = y1 * z2 - z1 * y2;
    output.y = z1 * x2 - x1 * z2;
    output.z = x1 * y2 - y1 * x2;
    return output;
}
```
- example usage
```shell
...
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}

var dist = VEC_REGISTER.length();
...
```

#### <a name="apidoc.element.famous.Vec3.dot"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>dot (v1, v2)](#apidoc.element.famous.Vec3.dot)
- description and source-code
```javascript
function dot(v1, v2) {
    return v1.x * v2.x + v1.y * v2.y + v1.z * v2.z;
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Vec3.normalize"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>normalize (v, output)](#apidoc.element.famous.Vec3.normalize)
- description and source-code
```javascript
function normalize(v, output) {
    var x = v.x;
    var y = v.y;
    var z = v.z;

    var length = Math.sqrt(x * x + y * y + z * z) || 1;
    length = 1 / length;

    output.x = x * length;
    output.y = y * length;
    output.z = z * length;
    return output;
}
```
- example usage
```shell
...
var c = frontierEdges[j][1];
var B = vertices[b].vertex;
var C = vertices[c].vertex;

var AB = Vec3.subtract(B, A, AB_REGISTER);
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
...
```

#### <a name="apidoc.element.famous.Vec3.project"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>project (v1, v2, output)](#apidoc.element.famous.Vec3.project)
- description and source-code
```javascript
function project(v1, v2, output) {
    var x1 = v1.x;
    var y1 = v1.y;
    var z1 = v1.z;
    var x2 = v2.x;
    var y2 = v2.y;
    var z2 = v2.z;

    var scale = x1 * x2 + y1 * y2 + z1 * z2;
    scale /= x2 * x2 + y2 * y2 + z2 * z2;

    output.x = x2 * scale;
    output.y = y2 * scale;
    output.z = z2 * scale;

    return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.scale"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>scale (v, s, output)](#apidoc.element.famous.Vec3.scale)
- description and source-code
```javascript
function scale(v, s, output) {
    output.x = v.x * s;
    output.y = v.y * s;
    output.z = v.z * s;
    return output;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec3.subtract"></a>[function <span class="apidocSignatureSpan">famous.Vec3.</span>subtract (v1, v2, output)](#apidoc.element.famous.Vec3.subtract)
- description and source-code
```javascript
function subtract(v1, v2, output) {
    output.x = v1.x - v2.x;
    output.y = v1.y - v2.y;
    output.z = v1.z - v2.z;
    return output;
}
```
- example usage
```shell
...
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
...
```



# <a name="apidoc.module.famous.Vec3.prototype"></a>[module famous.Vec3.prototype](#apidoc.module.famous.Vec3.prototype)

#### <a name="apidoc.element.famous.Vec3.prototype.add"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>add (v)](#apidoc.element.famous.Vec3.prototype.add)
- description and source-code
```javascript
function add(v) {
    this.x += v.x;
    this.y += v.y;
    this.z += v.z;

    return this;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.applyMatrix"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>applyMatrix (matrix)](#apidoc.element.famous.Vec3.prototype.applyMatrix)
- description and source-code
```javascript
function applyMatrix(matrix) {
    var M = matrix.get();

    var x = this.x;
    var y = this.y;
    var z = this.z;

    this.x = M[0]*x + M[1]*y + M[2]*z;
    this.y = M[3]*x + M[4]*y + M[5]*z;
    this.z = M[6]*x + M[7]*y + M[8]*z;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.applyRotation"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>applyRotation (q)](#apidoc.element.famous.Vec3.prototype.applyRotation)
- description and source-code
```javascript
function applyRotation(q) {
    var cw = q.w;
    var cx = -q.x;
    var cy = -q.y;
    var cz = -q.z;

    var vx = this.x;
    var vy = this.y;
    var vz = this.z;

    var tw = -cx * vx - cy * vy - cz * vz;
    var tx = vx * cw + vy * cz - cy * vz;
    var ty = vy * cw + cx * vz - vx * cz;
    var tz = vz * cw + vx * cy - cx * vy;

    var w = cw;
    var x = -cx;
    var y = -cy;
    var z = -cz;

    this.x = tx * w + x * tw + y * tz - ty * z;
    this.y = ty * w + y * tw + tx * z - x * tz;
    this.z = tz * w + z * tw + x * ty - tx * y;
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.clear"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>clear ()](#apidoc.element.famous.Vec3.prototype.clear)
- description and source-code
```javascript
function clear() {
    this.x = 0;
    this.y = 0;
    this.z = 0;
    return this;
}
```
- example usage
```shell
...
    }
    this.event.current = 1;
    this.event.points = 1;
    id = t[0].identifier;
    this.trackedPointerIDs[0] = id;

    this.last1.set(t[0].pageX, t[0].pageY);
    this.velocity1.clear();
    this.delta1.clear();
    this.event.pointers.push(this.pointer1);
}
if (t[1] && this.trackedPointerIDs[1] !== t[1].identifier) {
    if (this.trackedGestures.tap) {
        threshold = (this.options.tap && this.options.tap.threshold) || 250;
        if (this.event.time - this.timeOfPointer < threshold) this.multiTap = 2;
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.copy"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>copy (v)](#apidoc.element.famous.Vec3.prototype.copy)
- description and source-code
```javascript
function copy(v) {
    this.x = v.x;
    this.y = v.y;
    this.z = v.z;
    return this;
}
```
- example usage
```shell
...
        this.event.rotationVelocity = 0;
    }
    this.event.pointers.push(this.pointer2);
}

this.event.status = 'start';
if (this.event.points === 1) {
    this.center.copy(this.last1);
    this.centerDelta.clear();
    this.centerVelocity.clear();
    if (this.trackedGestures.pinch) {
        this.event.scale = 1;
        this.event.scaleDelta = 0;
        this.event.scaleVelocity = 0;
    }
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.cross"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>cross (v)](#apidoc.element.famous.Vec3.prototype.cross)
- description and source-code
```javascript
function cross(v) {
    var x = this.x;
    var y = this.y;
    var z = this.z;

    var vx = v.x;
    var vy = v.y;
    var vz = v.z;

    this.x = y * vz - z * vy;
    this.y = z * vx - x * vz;
    this.z = x * vy - y * vx;
    return this;
}
```
- example usage
```shell
...
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}

var dist = VEC_REGISTER.length();
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.dot"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>dot (v)](#apidoc.element.famous.Vec3.prototype.dot)
- description and source-code
```javascript
function dot(v) {
    return this.x*v.x + this.y*v.y + this.z*v.z;
}
```
- example usage
```shell
...
Vec2.subtract(VEC_REGISTER, this.center, this.centerDelta);
Vec2.add(this.velocity1, this.velocity2, this.centerVelocity).scale(0.5);
this.center.copy(VEC_REGISTER);

Vec2.subtract(this.last2, this.last1, VEC_REGISTER);

if (this.trackedGestures.rotate) {
    var dot = VEC_REGISTER.dot(this.diff12);
    var cross = VEC_REGISTER.cross(this.diff12);
    var theta = -Math.atan2(cross, dot);
    this.event.rotation += theta;
    this.event.rotationDelta = theta;
    this.event.rotationVelocity = theta * invDt;
}
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.invert"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>invert ()](#apidoc.element.famous.Vec3.prototype.invert)
- description and source-code
```javascript
function invert() {
    this.x = -this.x;
    this.y = -this.y;
    this.z = -this.z;

    return this;
}
```
- example usage
```shell
...
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
    this.addFeature(distance, ABC, [a, b, c]);
}
else {
    var reference = Vec3.subtract(referencePoint, A, VEC_REGISTER);
    if (Vec3.dot(ABC, reference) > -0.001) ABC.invert();
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.isZero"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>isZero ()](#apidoc.element.famous.Vec3.prototype.isZero)
- description and source-code
```javascript
function isZero() {
    return this.x === 0 && this.y === 0 && this.z === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.length"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>length ()](#apidoc.element.famous.Vec3.prototype.length)
- description and source-code
```javascript
function length() {
    var x = this.x;
    var y = this.y;
    var z = this.z;

    return Math.sqrt(x * x + y * y + z * z);
}
```
- example usage
```shell
...
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
if (this.trackedGestures.rotate) {
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.lengthSq"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>lengthSq ()](#apidoc.element.famous.Vec3.prototype.lengthSq)
- description and source-code
```javascript
function lengthSq() {
    var x = this.x;
    var y = this.y;
    var z = this.z;

    return x * x + y * y + z * z;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.map"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>map (fn)](#apidoc.element.famous.Vec3.prototype.map)
- description and source-code
```javascript
function map(fn) {
    this.x = fn(this.x);
    this.y = fn(this.y);
    this.z = fn(this.z);

    return this;
}
```
- example usage
```shell
...
    var k;
    var pos;
    var tex;

    while (triangleIndex--) {
face = indices.slice(triangleIndex * 3, triangleIndex * 3 + 3);

pos = face.map(function(vertIndex) {
    return new Vec3(vertices[vertIndex * 3], vertices[vertIndex * 3 + 1], vertices[vertIndex * 3 + 2]);
});
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[1], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[1], pos[2], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[2], outputs[0]), 0.5, outputs[1]).toArray());

if (textureCoords) {
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.normalize"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>normalize ()](#apidoc.element.famous.Vec3.prototype.normalize)
- description and source-code
```javascript
function normalize() {
    var x = this.x;
    var y = this.y;
    var z = this.z;

    var len = Math.sqrt(x * x + y * y + z * z) || 1;
    len = 1 / len;

    this.x *= len;
    this.y *= len;
    this.z *= len;
    return this;
}
```
- example usage
```shell
...
var c = frontierEdges[j][1];
var B = vertices[b].vertex;
var C = vertices[c].vertex;

var AB = Vec3.subtract(B, A, AB_REGISTER);
var AC = Vec3.subtract(C, A, AC_REGISTER);
var ABC = Vec3.cross(AB, AC, new Vec3());
ABC.normalize();

if (!referencePoint) {
    var distance = Vec3.dot(ABC, A);
    if (distance < 0) {
        ABC.invert();
        distance *= -1;
    }
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.rotateX"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>rotateX (theta)](#apidoc.element.famous.Vec3.prototype.rotateX)
- description and source-code
```javascript
function rotateX(theta) {
    var y = this.y;
    var z = this.z;

    var cosTheta = Math.cos(theta);
    var sinTheta = Math.sin(theta);

    this.y = y * cosTheta - z * sinTheta;
    this.z = y * sinTheta + z * cosTheta;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.rotateY"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>rotateY (theta)](#apidoc.element.famous.Vec3.prototype.rotateY)
- description and source-code
```javascript
function rotateY(theta) {
    var x = this.x;
    var z = this.z;

    var cosTheta = Math.cos(theta);
    var sinTheta = Math.sin(theta);

    this.x = z * sinTheta + x * cosTheta;
    this.z = z * cosTheta - x * sinTheta;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.rotateZ"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>rotateZ (theta)](#apidoc.element.famous.Vec3.prototype.rotateZ)
- description and source-code
```javascript
function rotateZ(theta) {
    var x = this.x;
    var y = this.y;

    var cosTheta = Math.cos(theta);
    var sinTheta = Math.sin(theta);

    this.x = x * cosTheta - y * sinTheta;
    this.y = x * sinTheta + y * cosTheta;

    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.Vec3.prototype.scale"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>scale (s)](#apidoc.element.famous.Vec3.prototype.scale)
- description and source-code
```javascript
function scale(s) {
    this.x *= s;
    this.y *= s;
    this.z *= s;

    return this;
}
```
- example usage
```shell
...
id = t[1].identifier;
this.trackedPointerIDs[1] = id;

this.last2.set(t[1].pageX, t[1].pageY);
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.set"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>set (x, y, z)](#apidoc.element.famous.Vec3.prototype.set)
- description and source-code
```javascript
function set(x, y, z) {
    if (x != null) this.x = x;
    if (y != null) this.y = y;
    if (z != null) this.z = z;

    return this;
}
```
- example usage
```shell
...
* @param {Node} node Node that the Align component will be attached to
*/
function Align(node) {
   Position.call(this, node);

   var initial = node.getAlign();

   this._x.set(initial[0]);
   this._y.set(initial[1]);
   this._z.set(initial[2]);
}

/**
* Return the name of the Align component
*
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.subtract"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>subtract (v)](#apidoc.element.famous.Vec3.prototype.subtract)
- description and source-code
```javascript
function subtract(v) {
    this.x -= v.x;
    this.y -= v.y;
    this.z -= v.z;

    return this;
}
```
- example usage
```shell
...
this.velocity2.clear();
this.delta2.clear();

Vec2.add(this.last1, this.last2, this.center).scale(0.5);
this.centerDelta.clear();
this.centerVelocity.clear();

Vec2.subtract(this.last2, this.last1, this.diff12);
this.dist = this.diff12.length();

if (this.trackedGestures.pinch) {
    this.event.scale = this.event.scale || 1;
    this.event.scaleDelta = 0;
    this.event.scaleVelocity = 0;
}
...
```

#### <a name="apidoc.element.famous.Vec3.prototype.toArray"></a>[function <span class="apidocSignatureSpan">famous.Vec3.prototype.</span>toArray ()](#apidoc.element.famous.Vec3.prototype.toArray)
- description and source-code
```javascript
function toArray() {
    return [this.x, this.y, this.z];
}
```
- example usage
```shell
...

    while (triangleIndex--) {
face = indices.slice(triangleIndex * 3, triangleIndex * 3 + 3);

pos = face.map(function(vertIndex) {
    return new Vec3(vertices[vertIndex * 3], vertices[vertIndex * 3 + 1], vertices[vertIndex * 3 + 2]);
});
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[1], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[1], pos[2], outputs[0]), 0.5, outputs[1]).toArray());
vertices.push.apply(vertices, Vec3.scale(Vec3.add(pos[0], pos[2], outputs[0]), 0.5, outputs[1]).toArray());

if (textureCoords) {
    tex = face.map(function(vertIndex) {
        return new Vec2(textureCoords[vertIndex * 2], textureCoords[vertIndex * 2 + 1]);
    });
...
```



# <a name="apidoc.module.famous.WebGLRenderer"></a>[module famous.WebGLRenderer](#apidoc.module.famous.WebGLRenderer)

#### <a name="apidoc.element.famous.WebGLRenderer.WebGLRenderer"></a>[function <span class="apidocSignatureSpan">famous.</span>WebGLRenderer (canvas, compositor)](#apidoc.element.famous.WebGLRenderer.WebGLRenderer)
- description and source-code
```javascript
function WebGLRenderer(canvas, compositor) {
    canvas.classList.add('famous-webgl-renderer');

    this.canvas = canvas;
    this.compositor = compositor;

    var gl = this.gl = this.getWebGLContext(this.canvas);

    gl.clearColor(0.0, 0.0, 0.0, 0.0);
    gl.polygonOffset(0.1, 0.1);
    gl.enable(gl.POLYGON_OFFSET_FILL);
    gl.enable(gl.DEPTH_TEST);
    gl.enable(gl.BLEND);
    gl.depthFunc(gl.LEQUAL);
    gl.blendFunc(gl.SRC_ALPHA, gl.ONE_MINUS_SRC_ALPHA);
    gl.enable(gl.CULL_FACE);
    gl.cullFace(gl.BACK);

    this.meshRegistry = new Registry();
    this.cutoutRegistry = new Registry();
    this.lightRegistry = new Registry();

    this.numLights = 0;
    this.ambientLightColor = [0, 0, 0];
    this.lightPositions = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
    this.lightColors = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0];

    this.textureManager = new TextureManager(gl);
    this.bufferRegistry = new BufferRegistry(gl);
    this.program = new Program(gl, { debug: true });

    this.state = {
        boundArrayBuffer: null,
        boundElementBuffer: null,
        lastDrawn: null,
        enabledAttributes: {},
        enabledAttributesKeys: []
    };

    this.resolutionName = ['u_resolution'];
    this.resolutionValues = [[0, 0, 0]];

    this.cachedSize = [];

<span class="apidocCodeCommentSpan">    /*
    The projectionTransform has some constant components, i.e. the z scale, and the x and y translation.

    The z scale keeps the final z position of any vertex within the clip's domain by scaling it by an
    arbitrarily small coefficient. This has the advantage of being a useful default in the event of the
    user forgoing a near and far plane, an alien convention in dom space as in DOM overlapping is
    conducted via painter's algorithm.

    The x and y translation transforms the world space origin to the top left corner of the screen.

    The final component (this.projectionTransform[15]) is initialized as 1 because certain projection models,
    e.g. the WC3 specified model, keep the XY plane as the projection hyperplane.
    */
</span>    this.projectionTransform = [1, 0, 0, 0, 0, 1, 0, 0, 0, 0, -0.000001, 0, -1, 1, 0, 1];

    // TODO: remove this hack

    var cutout = this.cutoutGeometry = {
        spec: {
            id: -1,
            bufferValues: [[-1, -1, 0, 1, -1, 0, -1, 1, 0, 1, 1, 0]],
            bufferNames: ['a_pos'],
            type: 'TRIANGLE_STRIP'
        }
    };

    this.bufferRegistry.allocate(
        this.cutoutGeometry.spec.id,
        cutout.spec.bufferNames[0],
        cutout.spec.bufferValues[0],
        3
    );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.famous.WebGLRenderer.prototype"></a>[module famous.WebGLRenderer.prototype](#apidoc.module.famous.WebGLRenderer.prototype)

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.bufferData"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>bufferData (geometryId, bufferName, bufferValue, bufferSpacing, isDynamic)](#apidoc.element.famous.WebGLRenderer.prototype.bufferData)
- description and source-code
```javascript
function bufferData(geometryId, bufferName, bufferValue, bufferSpacing, isDynamic) {
    this.bufferRegistry.allocate(geometryId, bufferName, bufferValue, bufferSpacing, isDynamic);
}
```
- example usage
```shell
...
    commands[++iterator]
);
return iterator;
}

function glBufferData (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.bufferData(
    commands[++iterator],
    commands[++iterator],
    commands[++iterator],
    commands[++iterator],
    commands[++iterator]
);
return iterator;
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.createLight"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>createLight (path)](#apidoc.element.famous.WebGLRenderer.prototype.createLight)
- description and source-code
```javascript
function createLight(path) {
    this.numLights++;
    var light = {
        color: [0, 0, 0],
        position: [0, 0, 0]
    };
    this.lightRegistry.register(path, light);
    return light;
}
```
- example usage
```shell
...
 * @param {Number} x x position
 * @param {Number} y y position
 * @param {Number} z z position
 *
 * @return {WebGLRenderer} this
 */
WebGLRenderer.prototype.setLightPosition = function setLightPosition(path, x, y, z) {
    var light = this.lightRegistry.get(path) || this.createLight(path);
    light.position[0] = x;
    light.position[1] = y;
    light.position[2] = z;
    return this;
};

/**
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.createMesh"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>createMesh (path)](#apidoc.element.famous.WebGLRenderer.prototype.createMesh)
- description and source-code
```javascript
function createMesh(path) {
    var uniforms = keyValueToArrays({
        u_opacity: 1,
        u_transform: identity,
        u_size: [0, 0, 0],
        u_baseColor: [0.5, 0.5, 0.5, 1],
        u_positionOffset: [0, 0, 0],
        u_normals: [0, 0, 0],
        u_flatShading: 0,
        u_glossiness: [0, 0, 0, 0]
    });
    var mesh = {
        depth: null,
        uniformKeys: uniforms.keys,
        uniformValues: uniforms.values,
        buffers: {},
        geometry: null,
        drawType: null,
        textures: [],
        visible: true
    };

    this.meshRegistry.register(path, mesh);
    return mesh;
}
```
- example usage
```shell
...
* @method
* @param {String} path Path used as id of target mesh.
* @param {Boolean} visibility Indicates the visibility of target mesh.
*
* @return {undefined} undefined
*/
WebGLRenderer.prototype.setMeshVisibility = function setMeshVisibility(path, visibility) {
   var mesh = this.meshRegistry.get(path) || this.createMesh(path);

   mesh.visible = visibility;
};

/**
* Deletes a mesh from the meshRegistry.
*
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.draw"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>draw (renderState)](#apidoc.element.famous.WebGLRenderer.prototype.draw)
- description and source-code
```javascript
function draw(renderState) {
    var time = this.compositor.getTime();

    this.gl.clear(this.gl.COLOR_BUFFER_BIT | this.gl.DEPTH_BUFFER_BIT);
    this.textureManager.update(time);

    this.meshRegistryKeys = sorter(this.meshRegistry.getKeys(), this.meshRegistry.getKeyToValue());

    this.setGlobalUniforms(renderState);
    this.drawCutouts();
    this.drawMeshes();
}
```
- example usage
```shell
...
*/
DOMElement.prototype.onMount = function onMount(node, id) {
   this._node = node;
   this._id = id;
   this._UIEvents = node.getUIEvents().slice(0);
   TransformSystem.makeBreakPointAt(node.getLocation());
   this.onSizeModeChange.apply(this, node.getSizeMode());
   this.draw();
   this.setAttribute('data-fa-path', node.getLocation());
};

/**
* Method to be invoked by the Node as soon as the node is being dismounted
* either directly or by dismounting one of its ancestors.
*
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.drawBuffers"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>drawBuffers (vertexBuffers, mode, id)](#apidoc.element.famous.WebGLRenderer.prototype.drawBuffers)
- description and source-code
```javascript
function drawBuffers(vertexBuffers, mode, id) {
    var gl = this.gl;
    var length = 0;
    var attribute;
    var location;
    var spacing;
    var offset;
    var buffer;
    var iter;
    var j;
    var i;

    iter = vertexBuffers.keys.length;
    for (i = 0; i < iter; i++) {
        attribute = vertexBuffers.keys[i];

        // Do not set vertexAttribPointer if index buffer.

        if (attribute === 'indices') {
            j = i; continue;
        }

        // Retreive the attribute location and make sure it is enabled.

        location = this.program.attributeLocations[attribute];

        if (location === -1) continue;
        if (location === undefined) {
            location = gl.getAttribLocation(this.program.program, attribute);
            this.program.attributeLocations[attribute] = location;
            if (location === -1) continue;
        }

        if (!this.state.enabledAttributes[attribute]) {
            gl.enableVertexAttribArray(location);
            this.state.enabledAttributes[attribute] = true;
            this.state.enabledAttributesKeys.push(attribute);
        }

        // Retreive buffer information used to set attribute pointer.

        buffer = vertexBuffers.values[i];
        spacing = vertexBuffers.spacing[i];
        offset = vertexBuffers.offset[i];
        length = vertexBuffers.length[i];

        // Skip bindBuffer if buffer is currently bound.

        if (this.state.boundArrayBuffer !== buffer) {
            gl.bindBuffer(buffer.target, buffer.buffer);
            this.state.boundArrayBuffer = buffer;
        }

        if (this.state.lastDrawn !== id) {
            gl.vertexAttribPointer(location, spacing, gl.FLOAT, gl.FALSE, 0, 4 * offset);
        }
    }

    // Disable any attributes that not currently being used.

    var len = this.state.enabledAttributesKeys.length;
    for (i = 0; i < len; i++) {
        var key = this.state.enabledAttributesKeys[i];
        if (this.state.enabledAttributes[key] && vertexBuffers.keys.indexOf(key) === -1) {
            gl.disableVertexAttribArray(this.program.attributeLocations[key]);
            this.state.enabledAttributes[key] = false;
        }
    }

    if (length) {

        // If index buffer, use drawElements.

        if (j !== undefined) {
            buffer = vertexBuffers.values[j];
            offset = vertexBuffers.offset[j];
            spacing = vertexBuffers.spacing[j];
            length = vertexBuffers.length[j];

            // Skip bindBuffer if buffer is currently bound.

            if (this.state.boundElementBuffer !== buffer) {
                gl.bindBuffer(buffer.target, buffer.buffer);
                this.state.boundElementBuffer = buffer;
            }

            gl.drawElements(gl[mode], length, gl.UNSIGNED_SHORT, 2 * offset);
        }
        else {
            gl.drawArrays(gl[mode], 0, length);
        }
    }

    this.state.lastDrawn = id;
}
```
- example usage
```shell
...

       var j = mesh.textures.length;
       while (j--) this.textureManager.bindTexture(mesh.textures[j]);

       if (mesh.options) this.handleOptions(mesh.options, mesh);

       this.program.setUniforms(mesh.uniformKeys, mesh.uniformValues);
       this.drawBuffers(buffers, mesh.drawType, mesh.geometry);

       if (mesh.options) this.resetOptions(mesh.options);
   }
};

/**
* Iterates through and draws all registered cutout meshes. Blending
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.drawCutouts"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>drawCutouts ()](#apidoc.element.famous.WebGLRenderer.prototype.drawCutouts)
- description and source-code
```javascript
function drawCutouts() {
    var cutout;
    var buffers;
    var cutouts = this.cutoutRegistry.getValues();
    var len = cutouts.length;

    this.gl.disable(this.gl.CULL_FACE);
    this.gl.enable(this.gl.BLEND);
    this.gl.depthMask(true);

    for (var i = 0; i < len; i++) {
        cutout = cutouts[i];

        if (!cutout) continue;

        buffers = this.bufferRegistry.registry[cutout.geometry];

        if (!cutout.visible) continue;

        this.program.setUniforms(cutout.uniformKeys, cutout.uniformValues);
        this.drawBuffers(buffers, cutout.drawType, cutout.geometry);
    }

    this.gl.enable(this.gl.CULL_FACE);
}
```
- example usage
```shell
...

   this.gl.clear(this.gl.COLOR_BUFFER_BIT | this.gl.DEPTH_BUFFER_BIT);
   this.textureManager.update(time);

   this.meshRegistryKeys = sorter(this.meshRegistry.getKeys(), this.meshRegistry.getKeyToValue());

   this.setGlobalUniforms(renderState);
   this.drawCutouts();
   this.drawMeshes();
};

/**
* Iterates through and draws all registered meshes. This includes
* binding textures, handling draw options, setting mesh uniforms
* and drawing mesh buffers.
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.drawMeshes"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>drawMeshes ()](#apidoc.element.famous.WebGLRenderer.prototype.drawMeshes)
- description and source-code
```javascript
function drawMeshes() {
    var gl = this.gl;
    var buffers;
    var mesh;

    var meshes = this.meshRegistry.getValues();

    for(var i = 0; i < meshes.length; i++) {
        mesh = meshes[i];

        if (!mesh) continue;

        buffers = this.bufferRegistry.registry[mesh.geometry];

        if (!mesh.visible) continue;

        if (mesh.uniformValues[0] < 1) {
            gl.depthMask(false);
            gl.enable(gl.BLEND);
        }
        else {
            gl.depthMask(true);
            gl.disable(gl.BLEND);
        }

        if (!buffers) continue;

        var j = mesh.textures.length;
        while (j--) this.textureManager.bindTexture(mesh.textures[j]);

        if (mesh.options) this.handleOptions(mesh.options, mesh);

        this.program.setUniforms(mesh.uniformKeys, mesh.uniformValues);
        this.drawBuffers(buffers, mesh.drawType, mesh.geometry);

        if (mesh.options) this.resetOptions(mesh.options);
    }
}
```
- example usage
```shell
...
   this.gl.clear(this.gl.COLOR_BUFFER_BIT | this.gl.DEPTH_BUFFER_BIT);
   this.textureManager.update(time);

   this.meshRegistryKeys = sorter(this.meshRegistry.getKeys(), this.meshRegistry.getKeyToValue());

   this.setGlobalUniforms(renderState);
   this.drawCutouts();
   this.drawMeshes();
};

/**
* Iterates through and draws all registered meshes. This includes
* binding textures, handling draw options, setting mesh uniforms
* and drawing mesh buffers.
*
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.getOrSetCutout"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>getOrSetCutout (path)](#apidoc.element.famous.WebGLRenderer.prototype.getOrSetCutout)
- description and source-code
```javascript
function getOrSetCutout(path) {
    var cutout = this.cutoutRegistry.get(path);

    if (!cutout) {
        var uniforms = keyValueToArrays({
            u_opacity: 0,
            u_transform: identity.slice(),
            u_size: [0, 0, 0],
            u_origin: [0, 0, 0],
            u_baseColor: [0, 0, 0, 1]
        });

        cutout = {
            uniformKeys: uniforms.keys,
            uniformValues: uniforms.values,
            geometry: this.cutoutGeometry.spec.id,
            drawType: this.cutoutGeometry.spec.type,
            visible: true
        };

        this.cutoutRegistry.register(path, cutout);
    }

    return cutout;
}
```
- example usage
```shell
...
 */
Context.prototype.getWebGLRenderer = function getWebGLRenderer() {
return this._webGLRenderer;
};

// Command Callbacks
function preventDefault (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.preventDefault(commands[++iterator]);
return iterator;
}

function allowDefault (context, path, commands, iterator) {
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.allowDefault(commands[++iterator]);
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.getWebGLContext"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>getWebGLContext (canvas)](#apidoc.element.famous.WebGLRenderer.prototype.getWebGLContext)
- description and source-code
```javascript
function getWebGLContext(canvas) {
    var names = ['webgl', 'experimental-webgl', 'webkit-3d', 'moz-webgl'];
    var context;

    for (var i = 0, len = names.length; i < len; i++) {
        try {
            context = canvas.getContext(names[i]);
        }
        catch (error) {
            console.error('Error creating WebGL context: ' + error.toString());
        }
        if (context) return context;
    }

    if (!context) {
        console.error('Could not retrieve WebGL context. Please refer to https://www.khronos.org/webgl/ for requirements');
        return false;
    }

}
```
- example usage
```shell
...
 */
function WebGLRenderer(canvas, compositor) {
canvas.classList.add('famous-webgl-renderer');

this.canvas = canvas;
this.compositor = compositor;

var gl = this.gl = this.getWebGLContext(this.canvas);

gl.clearColor(0.0, 0.0, 0.0, 0.0);
gl.polygonOffset(0.1, 0.1);
gl.enable(gl.POLYGON_OFFSET_FILL);
gl.enable(gl.DEPTH_TEST);
gl.enable(gl.BLEND);
gl.depthFunc(gl.LEQUAL);
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.handleMaterialInput"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>handleMaterialInput (path, name, material)](#apidoc.element.famous.WebGLRenderer.prototype.handleMaterialInput)
- description and source-code
```javascript
function handleMaterialInput(path, name, material) {
    var mesh = this.meshRegistry.get(path) || this.createMesh(path);
    material = compileMaterial(material, mesh.textures.length);

    // Set uniforms to enable texture!

    mesh.uniformValues[mesh.uniformKeys.indexOf(name)][0] = -material._id;

    // Register textures!

    var i = material.textures.length;
    while (i--) {
        mesh.textures.push(
            this.textureManager.register(material.textures[i], mesh.textures.length + i)
        );
    }

    // Register material!

    this.program.registerMaterial(name, material);

    return this.updateSize();
}
```
- example usage
```shell
...
        commands[++iterator]
    );
    return iterator;
}

function materialInput (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.handleMaterialInput(
        path,
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.handleOptions"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>handleOptions (options, mesh)](#apidoc.element.famous.WebGLRenderer.prototype.handleOptions)
- description and source-code
```javascript
function handleOptions(options, mesh) {
    var gl = this.gl;
    if (!options) return;

    if (options.blending) gl.enable(gl.BLEND);

    switch (options.side) {
        case 'double':
            this.gl.cullFace(this.gl.FRONT);
            this.drawBuffers(this.bufferRegistry.registry[mesh.geometry], mesh.drawType, mesh.geometry);
            this.gl.cullFace(this.gl.BACK);
            break;
        case 'back':
            gl.cullFace(gl.FRONT);
            break;
    }
}
```
- example usage
```shell
...
        }

        if (!buffers) continue;

        var j = mesh.textures.length;
        while (j--) this.textureManager.bindTexture(mesh.textures[j]);

        if (mesh.options) this.handleOptions(mesh.options, mesh);

        this.program.setUniforms(mesh.uniformKeys, mesh.uniformValues);
        this.drawBuffers(buffers, mesh.drawType, mesh.geometry);

        if (mesh.options) this.resetOptions(mesh.options);
    }
};
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.removeMesh"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>removeMesh (path)](#apidoc.element.famous.WebGLRenderer.prototype.removeMesh)
- description and source-code
```javascript
function removeMesh(path) {
    this.meshRegistry.unregister(path);
}
```
- example usage
```shell
...
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setMeshVisibility(path, commands[++iterator]);
return iterator;
}

function glRemoveMesh (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.removeMesh(path);
return iterator;
}

function pinholeProjection (context, path, commands, iterator) {
context._renderState.projectionType = Camera.PINHOLE_PROJECTION;
context._renderState.perspectiveTransform[11] = -1 / commands[++iterator];
context._renderState.perspectiveDirty = true;
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.resetOptions"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>resetOptions (options)](#apidoc.element.famous.WebGLRenderer.prototype.resetOptions)
- description and source-code
```javascript
function resetOptions(options) {
    var gl = this.gl;
    if (!options) return;
    if (options.blending) gl.disable(gl.BLEND);
    if (options.side === 'back') gl.cullFace(gl.BACK);
}
```
- example usage
```shell
...
       while (j--) this.textureManager.bindTexture(mesh.textures[j]);

       if (mesh.options) this.handleOptions(mesh.options, mesh);

       this.program.setUniforms(mesh.uniformKeys, mesh.uniformValues);
       this.drawBuffers(buffers, mesh.drawType, mesh.geometry);

       if (mesh.options) this.resetOptions(mesh.options);
   }
};

/**
* Iterates through and draws all registered cutout meshes. Blending
* is disabled, cutout uniforms are set and finally buffers are drawn.
*
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setAmbientLightColor"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setAmbientLightColor (path, r, g, b)](#apidoc.element.famous.WebGLRenderer.prototype.setAmbientLightColor)
- description and source-code
```javascript
function setAmbientLightColor(path, r, g, b) {
    this.ambientLightColor[0] = r;
    this.ambientLightColor[1] = g;
    this.ambientLightColor[2] = b;
    return this;
}
```
- example usage
```shell
...
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setMeshOptions(path, commands[++iterator]);
    return iterator;
}

function glAmbientLight (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setAmbientLightColor(
        path,
        commands[++iterator],
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setCutoutState"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setCutoutState (path, usesCutout)](#apidoc.element.famous.WebGLRenderer.prototype.setCutoutState)
- description and source-code
```javascript
function setCutoutState(path, usesCutout) {
    var cutout = this.getOrSetCutout(path);

    cutout.visible = usesCutout;
}
```
- example usage
```shell
...

   if (options.properties)
       for (key in options.properties)
           this.setProperty(key, options.properties[key]);

   if (options.id) this.setId(options.id);
   if (options.content) this.setContent(options.content);
   if (options.cutout === false) this.setCutoutState(options.cutout);
}

/**
* Serializes the state of the DOMElement.
*
* @method
*
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setCutoutUniform"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setCutoutUniform (path, uniformName, uniformValue)](#apidoc.element.famous.WebGLRenderer.prototype.setCutoutUniform)
- description and source-code
```javascript
function setCutoutUniform(path, uniformName, uniformValue) {
    var cutout = this.getOrSetCutout(path);

    var index = cutout.uniformKeys.indexOf(uniformName);

    if (uniformValue.length) {
        for (var i = 0, len = uniformValue.length; i < len; i++) {
            cutout.uniformValues[index][i] = uniformValue[i];
        }
    }
    else {
        cutout.uniformValues[index] = uniformValue;
    }
}
```
- example usage
```shell
...
temp[13] = commands[++iterator];
temp[14] = commands[++iterator];
temp[15] = commands[++iterator];

context._domRenderer.setMatrix(temp);

if (context._webGLRenderer)
    context._webGLRenderer.setCutoutUniform(path, 'u_transform', temp);

return iterator;
}

function changeSize (context, path, commands, iterator) {
var width = commands[++iterator];
var height = commands[++iterator];
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setGeometry"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setGeometry (path, geometry, drawType, dynamic)](#apidoc.element.famous.WebGLRenderer.prototype.setGeometry)
- description and source-code
```javascript
function setGeometry(path, geometry, drawType, dynamic) {
    var mesh = this.meshRegistry.get(path) || this.createMesh(path);

    mesh.geometry = geometry;
    mesh.drawType = drawType;
    mesh.dynamic = dynamic;

    return this;
}
```
- example usage
```shell
...
        commands[++iterator]
    );
    return iterator;
}

function glSetGeometry (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setGeometry(
        path,
        commands[++iterator],
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setGlobalUniforms"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setGlobalUniforms (renderState)](#apidoc.element.famous.WebGLRenderer.prototype.setGlobalUniforms)
- description and source-code
```javascript
function setGlobalUniforms(renderState) {
    var light;
    var stride;
    var lights = this.lightRegistry.getValues();
    var len = lights.length;

    for (var i = 0; i < len; i++) {
        light = lights[i];

        if (!light) continue;

        stride = i * 4;

        // Build the light positions' 4x4 matrix

        this.lightPositions[0 + stride] = light.position[0];
        this.lightPositions[1 + stride] = light.position[1];
        this.lightPositions[2 + stride] = light.position[2];

        // Build the light colors' 4x4 matrix

        this.lightColors[0 + stride] = light.color[0];
        this.lightColors[1 + stride] = light.color[1];
        this.lightColors[2 + stride] = light.color[2];
    }

    globalUniforms.values[0] = this.numLights;
    globalUniforms.values[1] = this.ambientLightColor;
    globalUniforms.values[2] = this.lightPositions;
    globalUniforms.values[3] = this.lightColors;

<span class="apidocCodeCommentSpan">    /*
     * Set time and projection uniforms
     * projecting world space into a 2d plane representation of the canvas.
     * The x and y scale (this.projectionTransform[0] and this.projectionTransform[5] respectively)
     * convert the projected geometry back into clipspace.
     * The perpective divide (this.projectionTransform[11]), adds the z value of the point
     * multiplied by the perspective divide to the w value of the point. In the process
     * of converting from homogenous coordinates to NDC (normalized device coordinates)
     * the x and y values of the point are divided by w, which implements perspective.
     */
</span>    this.projectionTransform[0] = 1 / (this.cachedSize[0] * 0.5);
    this.projectionTransform[5] = -1 / (this.cachedSize[1] * 0.5);
    this.projectionTransform[11] = renderState.perspectiveTransform[11];

    globalUniforms.values[4] = this.projectionTransform;
    globalUniforms.values[5] = this.compositor.getTime() * 0.001;
    globalUniforms.values[6] = renderState.viewTransform;

    this.program.setUniforms(globalUniforms.keys, globalUniforms.values);
}
```
- example usage
```shell
...
   var time = this.compositor.getTime();

   this.gl.clear(this.gl.COLOR_BUFFER_BIT | this.gl.DEPTH_BUFFER_BIT);
   this.textureManager.update(time);

   this.meshRegistryKeys = sorter(this.meshRegistry.getKeys(), this.meshRegistry.getKeyToValue());

   this.setGlobalUniforms(renderState);
   this.drawCutouts();
   this.drawMeshes();
};

/**
* Iterates through and draws all registered meshes. This includes
* binding textures, handling draw options, setting mesh uniforms
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setLightColor"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setLightColor (path, r, g, b)](#apidoc.element.famous.WebGLRenderer.prototype.setLightColor)
- description and source-code
```javascript
function setLightColor(path, r, g, b) {
    var light = this.lightRegistry.get(path) || this.createLight(path);

    light.color[0] = r;
    light.color[1] = g;
    light.color[2] = b;
    return this;
}
```
- example usage
```shell
...
        commands[++iterator]
    );
    return iterator;
}

function glLightColor (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setLightColor(
        path,
        commands[++iterator],
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setLightPosition"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setLightPosition (path, x, y, z)](#apidoc.element.famous.WebGLRenderer.prototype.setLightPosition)
- description and source-code
```javascript
function setLightPosition(path, x, y, z) {
    var light = this.lightRegistry.get(path) || this.createLight(path);
    light.position[0] = x;
    light.position[1] = y;
    light.position[2] = z;
    return this;
}
```
- example usage
```shell
...
        commands[++iterator]
    );
    return iterator;
}

function glLightPosition (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setLightPosition(
        path,
        commands[++iterator],
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setMeshOptions"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setMeshOptions (path, options)](#apidoc.element.famous.WebGLRenderer.prototype.setMeshOptions)
- description and source-code
```javascript
setMeshOptions = function (path, options) {
    var mesh = this.meshRegistry.get(path) || this.createMesh(path);

    mesh.options = options;
    return this;
}
```
- example usage
```shell
...
if (context._webGLRenderer) context._webGLRenderer.getOrSetCutout(path);
context._domRenderer.unsubscribe(commands[++iterator]);
return iterator;
}

function glSetDrawOptions (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setMeshOptions(path, commands[++iterator]);
return iterator;
}

function glAmbientLight (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setAmbientLightColor(
    path,
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setMeshUniform"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setMeshUniform (path, uniformName, uniformValue)](#apidoc.element.famous.WebGLRenderer.prototype.setMeshUniform)
- description and source-code
```javascript
function setMeshUniform(path, uniformName, uniformValue) {
    var mesh = this.meshRegistry.get(path) || this.createMesh(path);

    var index = mesh.uniformKeys.indexOf(uniformName);

    if (index === -1) {
        mesh.uniformKeys.push(uniformName);
        mesh.uniformValues.push(uniformValue);
    }
    else {
        mesh.uniformValues[index] = uniformValue;
    }
}
```
- example usage
```shell
...
        commands[++iterator]
    );
    return iterator;
}

function glUniforms (context, path, commands, iterator) {
    if (!context._webGLRenderer) context._initWebGLRenderer();
    context._webGLRenderer.setMeshUniform(
        path,
        commands[++iterator],
        commands[++iterator]
    );
    return iterator;
}
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.setMeshVisibility"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>setMeshVisibility (path, visibility)](#apidoc.element.famous.WebGLRenderer.prototype.setMeshVisibility)
- description and source-code
```javascript
function setMeshVisibility(path, visibility) {
    var mesh = this.meshRegistry.get(path) || this.createMesh(path);

    mesh.visible = visibility;
}
```
- example usage
```shell
...
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setCutoutState(path, commands[++iterator]);
return iterator;
}

function glMeshVisibility (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.setMeshVisibility(path, commands[++iterator]);
return iterator;
}

function glRemoveMesh (context, path, commands, iterator) {
if (!context._webGLRenderer) context._initWebGLRenderer();
context._webGLRenderer.removeMesh(path);
return iterator;
...
```

#### <a name="apidoc.element.famous.WebGLRenderer.prototype.updateSize"></a>[function <span class="apidocSignatureSpan">famous.WebGLRenderer.prototype.</span>updateSize (size)](#apidoc.element.famous.WebGLRenderer.prototype.updateSize)
- description and source-code
```javascript
function updateSize(size) {
    if (size) {
        var pixelRatio = window.devicePixelRatio || 1;
        var displayWidth = ~~(size[0] * pixelRatio);
        var displayHeight = ~~(size[1] * pixelRatio);
        this.canvas.width = displayWidth;
        this.canvas.height = displayHeight;
        this.gl.viewport(0, 0, displayWidth, displayHeight);

        this.cachedSize[0] = size[0];
        this.cachedSize[1] = size[1];
        this.cachedSize[2] = (size[0] > size[1]) ? size[0] : size[1];
        this.resolutionValues[0] = this.cachedSize;
    }

    this.program.setUniforms(this.resolutionName, this.resolutionValues);

    return this;
}
```
- example usage
```shell
...
       _this.onResize();
   });
}

Compositor.prototype.onResize = function onResize () {
   this._resized = true;
   for (var selector in this._contexts) {
       this._contexts[selector].updateSize();
   }
};

/**
* Retrieves the time being used by the internal clock managed by
* 'FamousEngine'.
*
...
```



# <a name="apidoc.module.famous.animationFrame"></a>[module famous.animationFrame](#apidoc.module.famous.animationFrame)

#### <a name="apidoc.element.famous.animationFrame.cancelAnimationFrame"></a>[function <span class="apidocSignatureSpan">famous.animationFrame.</span>cancelAnimationFrame (id)](#apidoc.element.famous.animationFrame.cancelAnimationFrame)
- description and source-code
```javascript
cancelAnimationFrame = function (id) {
    clearTimeout(id);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.famous.animationFrame.requestAnimationFrame"></a>[function <span class="apidocSignatureSpan">famous.animationFrame.</span>requestAnimationFrame (callback)](#apidoc.element.famous.animationFrame.requestAnimationFrame)
- description and source-code
```javascript
requestAnimationFrame = function (callback) {
    var currTime = now();
    var timeToCall = Math.max(0, 16 - (currTime - lastTime));
    var id = setTimeout(function () {
        callback(currTime + timeToCall);
    }, timeToCall);
    lastTime = currTime + timeToCall;
    return id;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
