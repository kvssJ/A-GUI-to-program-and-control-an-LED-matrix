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

Since each frame created using the GUI is meant to be a frame of an animation, I added the option to control the number of seconds a frame woild last. If I set the time to 2 seconds, the frame would persist for two seconds By default, the time is set to 1 second.

# Frames




