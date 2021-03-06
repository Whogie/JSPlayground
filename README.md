# JSGamework

A pre-built game loop to help start building a 2D JavaScript game.

##### Initial Setup
Set your desired resolution and frame rate in `start(width, height, fps)` provided in _index.html_. Then code your game in the provided functions in _game.js_.

##### Using _game.js_
The `initialize()` function is only called once at the start of the program. Good for setting up variables and assets.

Your game logic goes into `update(dt)`, while `draw()` is used for drawing the scene.


##### Fixed Frame Rate
`update(dt)` is called at the specified frame rate, but `draw()` is called when the computer is ready to draw a frame.

`dt` (delta time) passed through the update function will be the number of miliseconds for the frame rate.

##### Unlocked Frame Rate
If you set your frame rate to `0` in `start()` in _index.html_, the framerate will be unlocked. `dt` in `draw(dt)` is used to determine the number of miliseconds that passed in each frame.

Multiply any movement by `dt` to keep a consistent speed regardless of framerate. Be aware that this can add complications. A low framerate can cause larger movement than expected, and decimal imprecision can cause behavior to become non-deterministic.

##### Automatic Scaling
Program for one resolution. JSG will automatically scale your game to fit any browser window size. Just use the provided `JSG.canvas` and `JSG.context`.

##### Mouse
Use the provided `JSG.mouse.x` and `JSG.mouse.y` so that the mouse cursor plays nicely with the scalar.

Use `JSG.mouse.click` or `JSG.mouse.release` to listen for and handle clicks.

##### Keyboard
`JSG.keyboard.keyList` is an array of all the keys being pressed. If, for example, you want to check if 'A' is being pressed, use:
```javascript
        if (JSG.keyboard.keyList.includes(65))
```
