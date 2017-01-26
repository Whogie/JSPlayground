# JSPlayground

A pre-built game loop to help start building a 2D JavaScript game.

##### Initial Setup
Set your desired resolution in `start(width,height)` provided in _index.html_. Then code your game in the provided functions in _game.js_.

##### Automatic Scaling
Program for one resolution. JSP will automatically scale your game to fit any browser window size. Just use the provided `JSP.canvas` and `JSP.context`.

##### Mouse
Use the provided `JSP.mouse.x` and `JSP.mouse.y` so that the mouse cursor plays nicely with the scalar.

##### Keyboard
`JSP.keyboard.keyList` is an array of all the keys being pressed. If, for example, you want to check if 'A' is being pressed, try the command:
```javascript
        if (JSP.keyboard.keyList.includes(65))
```

##### Delta Time
Multiply any increments to your game objects in the `update()` function by `dt` to help adjust to any framerate. Example:
```javascript
mainCharacter.x += 2
```
becomes
```javascript
mainCharacter.x += 2 * dt
```

`dt` multiplier caps at 3x (20fps). Any slower, and dt allows slowdown to occur.