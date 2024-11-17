# Important Points

- This is a stepping stone to ease the transition to a new tool. It's not a long term programming strategy.

- Moving from Scratch
  - A LOT more power and control. No limitations
  - Things in the virtual world are like real world things.
    - In order to see something on the screen, we need a camera
  - Sub-scenes
  - Node heirarchy instead of flat list
    - Each scene must have one root node
  - There are 2D and 3D nodes that generally don't mix

# Steps

## Setting up the Scene - [YouTube Video](https://www.youtube.com/watch?v=1QdQrI2Og-g)

### Install the Block Coding plugin

1. Create a new Godot project
1. Select **AssetLib** from the top center
1. Search for **Block Codking** by _endless_
   1. Download
   1. Install into the project
1. In the AssetLib on the top right, select **Plugins**
1. Turn on Enabled for BlockCode
1. Switch from AssetLib to 2D view

### Creating the game world

1. Staring with a 2D scene, rename the root node to "PongGame"
1. Do **Save Scene** and again enter "PongGame"
1. Add a **Camera 2D** node. This will be in the center of the world.
1. Change the camera's zoom value from 1.0 to 0.5
1. Create the paddles
   1. Add a child node to the game and search for **Simple Character**
   1. Set the texture using _Quick Load_ **Paddle**
   1. Drag it to the left side and rename it to \*\*Left Paddle"
   1. Use CTRL+D to duplicate it
   1. Rename the new paddle to **Right Paddle**
   1. Drag this to the right side
1. Create the ball
   1. With the PongGame node selected, add a new child object that is a **Rigid Body 2D**
   1. Rename this to "Ball"
   1. To this, add another child which is a **Sprite 2D**
   1. In the texture, quick load the "Ball"
   1. Note the warning on the ball. It needs a collision shape. Add a child node that is a "Collision Shape 2D"
   1. Set the shape to a Cirlce Shape, and drag the size to be as big as the ball sprite

## Coding [YouTube Video](https://www.youtube.com/watch?v=WlUN7Zz0Djg)
