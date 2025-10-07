# PureJoyJS
Virtual joystick with delegate function for JavaScript

``
const joystick = new Joystick('left_stick', handleJoystickInput, joystickSize);
joystick.placeJoystickAt(xPosition, yPosition, zDepth);

function gameLoop() {
    // Update game logic here...
    joystick.draw();
}
``

![Screenshot](screenshot.png "Screenshot")

Live Demo:
https://demensdeum.com/software/cube-art-project-2-online/
