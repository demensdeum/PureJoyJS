# PureJoyJS
Virtual joystick with delegate function for JavaScript.

A simple, touch-friendly virtual joystick written in pure JavaScript, utilizing HTML Canvas for drawing and Pointer Events for input handling.

It's great for touch controls because it leverages the modern Pointer Events API, which unifies input from mouse, touch, and pen. This ensures a reliable and responsive experience across mobile devices, tablets, and even desktops with touchscreens, making it an ideal choice for implementing virtual game controls.

Usage example:  
```
<head>
</head>
<body>
<script type="module">
    import { Joystick } from './node_modules/purejoyjs/joystick.js'

    let currentX = 0;
    let currentY = 0;
    let isDragging = false;
    let joystickId = null;

    function handleJoystickMove(id, x, y, dragging) {
        joystickId = id;
        currentX = x;
        currentY = y;
        isDragging = dragging;
    }

    function gameLoop() {
        if (joystickId !== null) {
            console.log(`handleJoystickMove: ${joystickId} ${currentX} ${currentY} ${isDragging}`);
        }

        joystick.draw()
        requestAnimationFrame(gameLoop);
    }

    const joystick = new Joystick("joystick", handleJoystickMove, 240)
    joystick.placeJoystickAt(0,0,1000)

    requestAnimationFrame(gameLoop);
</script>
</body>
```

![Screenshot](screenshot.png "Screenshot")

Live Demo:
https://demensdeum.com/software/cube-art-project-2-online/
