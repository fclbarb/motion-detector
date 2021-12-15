# motion_detect
# Use the onboard accelerometer to make a motion detector to protect your cool stuff!

## Step 1 @unplugged

Name your project so it flashes on start up.

## Step 1 @fullscreen

Place the ``||basic:show string||`` block in  ``||basic:on start||``. Replace "Hello" with your project's name.
```blocks
basic.showString("alarm")
```

## Step 2 @fullscreen

From Input, drag the ``||input:on shake||`` block to the workspace to monitor any movement of your @boardname@.
```blocks
input.onGesture(Gesture.Shake, () => {
})
```

## Step 3 @fullscreen
Drag a ``||basic.showIcon||`` block into the ``||input.on shake||`` block and select an angry face.
```blocks
input.onGesture(Gesture.Shake, () => {
basic.showIcon(IconNames.Angry)})
```
## Step 4 @fullscreen

Add some music to scare aware the intruder!
From Music, drag a ``||music.play melody at tempo||`` block below the ``||basic.showIcon(IconNames.Angry)||''.
You can make your own music or choose from the gallery by clicking on the music notes!

```blocks
input.onGesture(Gesture.Shake, () => {
basic.showIcon(IconNames.Angry)
music.playMelody("- - - - - - - - ", 120)})
```

## Step 5 @fullscreen

Add a ``||basic.clearScreen||`` below the ``||music.play melody at tempo||`` to reset the motion detector for the next time somebody moves it!

```blocks
input.onGesture(Gesture.Shake, () => {
basic.showIcon(IconNames.Angry)
music.playMelody("- - - - - - - - ", 120)
basic.clearScreen()})
```

## Step 6 @fullscreen
Click on the SHAKE button in the simulator. You should see an angry face and hear the music!

##Step 7 @fullscreen
``|Download|`` to transfer your code to your @boardname@!
    