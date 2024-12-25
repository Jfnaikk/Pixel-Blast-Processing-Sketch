Pixel Blast Effect

Pixel Blast Effect is an interactive visual art program written in Processing. The program generates a burst of colorful particles when the user clicks anywhere on the canvas. Each particle radiates outward in random directions, gradually fading out over time, creating a dynamic and vibrant explosion effect. Users can also save their creations as a screenshot by pressing the SPACEBAR.

Features
Interactive Pixel Blast: Click anywhere on the canvas to trigger a colorful explosion of pixels.
Dynamic Movement: Each particle moves outward in a random direction with randomized speed and size.
Gradual Fade-Out: Pixels fade away over time, enhancing the animation’s aesthetic.
Screenshot Functionality: Press the SPACEBAR to save the current canvas as a .png file.
On-Screen Instructions: Displays instructions at the bottom of the canvas for user guidance.

How It Works
Setup: The canvas initializes with a black background and waits for user interaction.
Mouse Interaction: Clicking on the canvas creates a pixel blast at the mouse position.

Blast Mechanics:
Each particle (pixel) has a random size, speed, direction, and lifetime.
Particles spread outward from the center of the blast and gradually fade as their lifetime decreases.

Screenshot:
Pressing the SPACEBAR saves the current frame as a .png file in the sketch folder.

Usage
Open the code in the Processing IDE.
Run the program by pressing the play button.
Click anywhere on the canvas to generate a colorful pixel blast.
Press the SPACEBAR to save a screenshot of the current canvas.
File Structure

This project includes the following files:

PixelBlast.pde: The main source code for the simulation.
README.md: Documentation for the project.
Mouse Click: Triggers a pixel blast at the clicked position.
SPACEBAR: Saves a screenshot of the current canvas.
Customization
You can modify the following aspects in the code to personalize the program:

Blast Intensity: Adjust the maxPixels parameter in the PixelBlast class to control the number of particles.
Particle Speed and Size: Modify the speed and size ranges in the Pixel class.
Canvas Size: Change the size() function in the setup() method.
Color Palette: Experiment with the colorMode(HSB) settings in the Pixel.display() method.
Author
This project was created by Jawad F. Naik as part of the course Elements of Media, taught by Professor Fred Wolflink at the Massachusetts College of Art and Design in Boston, Massachusetts, USA.

License
This project is open-source and licensed under the MIT License. See the LICENSE file for details.

Acknowledgments
Special thanks to the Processing Foundation for their excellent tools and resources, and to the Massachusetts College of Art and Design for fostering creativity and exploration.
