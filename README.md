# Important Points

- Math Skills

  - Negative numbers
  - Decimal numbers
  - Multiplication
  - Heirarchy

- This is a stepping stone to ease the transition to a new tool. It's not a long term programming strategy.

- Moving from Scratch
  - A LOT more power and control. No limitations
  - Things in the virtual world are like real world things.
    - In order to see something on the screen, we need a camera
  - Sub-scenes
  - Node heirarchy instead of flat list
    - Each scene must have one root node
  - There are 2D and 3D nodes that generally don't mix
  - The visual and physical aspects of the virtual world are separate

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
1. Do **Save Scene** and again enter "PongGame" as the scene name
1. 🎥 Create the Camera
   1. Select the PongGame node, and add a child **Camera 2D** node. This will be in the center of the world.
   1. Change the camera's zoom value from 1.0 to 0.5
1. 🏓 Create the paddles
   1. Add a child node to the game and search for **Simple Character**
   1. Set the texture using _Quick Load_ **Paddle**
   1. Drag it to the left side and rename it to \*\*Left Paddle"
   1. Use CTRL+D to duplicate it
   1. Rename the new paddle to **Right Paddle**
   1. Drag this to the right side
1. ⚽ Create the ball
   1. With the PongGame node selected, add a new child object that is a **Rigid Body 2D**
   1. Rename this to "Ball"
   1. To this, add another child which is a **Sprite 2D**
   1. In the texture, quick load the "Ball"
   1. Note the warning on the ball. It needs a collision shape. Add a child node that is a "Collision Shape 2D"
   1. Set the shape to a Cirlce Shape, and drag the size to be as big as the ball sprite
   1. On the ball's **Rigidbody** create a new **Physics Material** with Frction=0 and Bounce=1, and set the GravityScale to 0
   1. In the **Linear** section, set the Velocity to X=400 and Y=400
1. 🧱 Create the walls
   1. From the PongGame node, add a child of type \*\*Static Body 2D" and rename this to "TopWall"
   1. To this, add a child node that is a **Collision Shape 2D** and set the shape to a new **Rectangle Shape**
   1. Drag and resize this shape to sit above the full play field
   1. Select the **TopWall** object and duplicate it.
   1. Rename this to \*\*BottomWall" and drag it to the bottom of the scene
1. 💯 Create the score display
   1. From the PongGame node, add a child node of type **Simple Scoring**
   1. In the **Canvas Layer** set the Transform Offset X=-1000 Y=-700
1. 🥅 Create Goals
   1. From the PongGame node, add an Area2D child
   1. Name this **LeftGoal**
   1. Add a child to it that is a **CollisionShape2D** with a rectagle shape
   1. Move this just off the left side of the camera's view
   1. Duplicate this LeftGoal and rename it RightGoal and move it off the right side
1. .🦋 Make it pretty
   1. Select the PongGame node, and add a **Sprite2D** child node
   1. On the Texture, Quick Load the "Space" graphic.
   1. Resize the sprite to fill the camera area
   1. Drag it to the top of the list so it doesn't block the other elements
   1. Select the **Ball - Sprite2D** and in the **Canvas Item - Visibility** Choose **Modulate** and pick a nice colour.
   1. Do the same for both of the Paddles

## Coding [YouTube Video](https://www.youtube.com/watch?v=WlUN7Zz0Djg)
