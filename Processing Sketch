/* 
 * Date: December 12, 2024
 * Author: Jawad F. Naik
 * Class/Professor: Elements of Media / Fred Wolflink
 * Institution: Massachusetts College of Art and Design
 * Location: Boston, Massachusetts, USA
 * 
 * Description:
 * This program generates a colorful pixel blast effect whenever the user clicks
 * on the canvas. Each blast consists of particles that move outward in random 
 * directions and fade out gradually over time. Press SPACEBAR to save a screenshot.
 */

ArrayList<PixelBlast> blasts = new ArrayList<>();
PFont font;

void setup() {
  size(800, 800); // Canvas size
  background(0);  // Black background
  font = createFont("Arial", 16, true); // Load font for instructions
}

void draw() {
  background(0); // Refresh the background to black

  // Update and display all pixel blasts
  for (PixelBlast blast : blasts) {
    blast.update();
    blast.display();
  }

  // Display instructions at the bottom
  displayInstructions();
}

void mousePressed() {
  // Create a new pixel blast at the mouse click position
  blasts.add(new PixelBlast(mouseX, mouseY));
}

void keyPressed() {
  if (key == ' ') { // If spacebar is pressed
    saveFrame("screenshot-####.png"); // Save the current frame as a PNG file
  }
}

void displayInstructions() {
  fill(255); // White text
  textFont(font);
  textAlign(CENTER);
  text("Click anywhere to trigger a colorful pixel blast. Press SPACEBAR to save a screenshot.", width / 2, height - 20);
}

class PixelBlast {
  float x, y; // Center of the blast
  ArrayList<Pixel> pixels = new ArrayList<>(); // Store the individual pixels
  int maxPixels; // Total number of pixels in the blast

  PixelBlast(float x, float y) {
    this.x = x;
    this.y = y;
    this.maxPixels = int(random(50, 100)); // Randomize the number of pixels
    // Create all pixels with random directions and speeds
    for (int i = 0; i < maxPixels; i++) {
      float angle = random(TWO_PI); // Random angle for direction
      float speed = random(1, 5);   // Random speed for each pixel
      pixels.add(new Pixel(x, y, angle, speed));
    }
  }

  void update() {
    // Update all pixels
    for (Pixel p : pixels) {
      p.update();
    }
  }

  void display() {
    // Display all pixels
    for (Pixel p : pixels) {
      p.display();
    }
  }
}

class Pixel {
  float x, y;      // Current position
  float angle;     // Direction of movement
  float speed;     // Speed of movement
  float size;      // Size of the pixel
  int colorHue;    // Color of the pixel
  float lifetime;  // How long the pixel lasts

  Pixel(float x, float y, float angle, float speed) {
    this.x = x; // Initial position (x)
    this.y = y; // Initial position (y)
    this.angle = angle; // Movement direction
    this.speed = speed; // Movement speed
    this.size = random(3, 8);       // Random size for the pixel
    this.colorHue = int(random(360)); // Random color
    this.lifetime = random(50, 100); // Random lifetime
  }

  void update() {
    // Move the pixel in its direction
    x += cos(angle) * speed;
    y += sin(angle) * speed;
    // Decrease lifetime gradually
    lifetime--;
  }

  void display() {
    if (lifetime > 0) { // Display only if the pixel is still "alive"
      colorMode(HSB, 360, 100, 100, 100);
      fill(colorHue, 100, 100, map(lifetime, 0, 100, 0, 100)); // Fade out
      noStroke();
      ellipse(x, y, size, size); // Draw the pixel
    }
  }
}
