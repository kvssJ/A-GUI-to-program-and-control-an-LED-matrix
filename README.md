# A-GUI-to-program-and-control-an-LED-matrix
I used tkinter to create a Graphical User Interface that can be used to create frames of an animation to play them on an LED matrix.


<img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/aefc98db-7462-4fcb-aa0b-773409813a2a" />


# The layout

Since I wanted the Graphical User Interface to provide a more visual and easy way to create frames for the LED matrix, I programmed the GUI such that it resembled the actual LED matrix. The GUI has 30 buttons arranged in a grid where each button was an LED. On the left side, the GUI has some additional options like a time box, a list box with a bunch of common colours, and even the option to choose a colour from an RGB colour chooser. Below the grid, there are options to create new frames, edit previous frames, and to submit all the frames. These different parts of the GUI are explained in more detail below:

# Choosing a colour

I added a colour listbox with a bunch of common colours and a colour chooser to choose any colour I want for a particular LED. Once I choose a colour, the Red, Green, and Blue hue values of the colour are stored in variables and even the colour of the button is changed to the selected colour to show how the LED should look like.


<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/488c4ca5-c91b-4f77-a382-821b99a13ca5" />


<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/570e71f1-641d-4a1d-b759-6d1bd8bd4025" />


# Time box

Since each frame created using the GUI is meant to be a frame of an animation, I added the option to control the number of seconds a frame would last. If I set the time to 2 seconds, the frame would persist for two seconds. By default, the time is set to 1 second.

# Brightness control

I added a scrollbar ranging from 0 to 15 to control the brightness of a particular LED. By default, the brightness is set to 15 (fully bright). I used something called Bit Angle Modulation to control the brightness. Since this repository is only for the GUI. I won't discuss how Bit Angle Modulation works here.

# Frames

As you can see above, I added several buttons below the grid like : "Next", "Previous", "Submit", and "Done". These buttons are meant to make it easier for me to create new frames, check or edit previous frames, and finally submit the frames once I'm happy with them.

In the background, whenever I submit a frame, the RGB values, brightness values and the time value of the frame are added to a list. 

I didn't want to use a multi-dimensional array to store multiple float or int values of all the rows of all the frames. Instead, I used a simple two-dimensional list. Each element of this 2D list is a list containing all the values of a frame. To simplify the lists, I concatenated the RGB values and brightness values of each row into a string. The six strings formed a list in the 2D list. 

Once I click submit, this list of strings would be added to the 2D list. Since I was using python anyways, this was pretty easy with the append function.

I also added the option to edit previous frames which had already been submitted. Whenever I move to a previous frame, the program would access the corresponding list and edit any changed values.

# Interfacing the GUI with the LED matrix

Once I click "Done", all the values of the 2D list is written to "led information text" text file. 

I wrote two other programs to read the text file and play the animation on the matrix. It was much harder to figure out how to read the values and play the animation than to create the GUI. I have another repository with these two programs. The actual LED control is explained in that repository.

Currently, once I write all the values to the text file, I'll need to run the other programs as two seperate programs. Once I'm done adding any more features or code, I'm planning to change the GUI such that as soon as I click "Done", it both writes the values to the text file and plays the animation on the LED matrix automatically.

# Future plans

There are a LOT of things you can do with an easy to use GUI and an LED matrix. You just need some creativity to figure them out. Currently, I'm planning to add a few simple features to the GUI so that I can do more than just play animations.

### Music player

I think it'll be really cool to find some way to interface music with the LED matrix, sort of like a visual representation for sound. Varying brightness or varying colours depending on auditory features like pitch or loudness are some ways I could do this. I'm hoping to add the option to upload songs to the GUI and play them on the matrix 

### Tetris and other simple games

The LED matrix is perfect for old or simple games like tetris, space invaders, or the clasic snake game. I could add levels or high scores to the GUI. 

### Video/image to pixel art

For a 5x6 LED matrix, even if I manage to get a really low resolution pixelated image, it'll be difficult to spot on the LED matrix. However, I'll still add such an option to the GUI so that once I make a larger matrix, I can use it.

I'm planning to use the open cv library in python to process images or videos into pixels, read the values from the pixels, and eventually write them to the LED Matrix.



