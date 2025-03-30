# Asteroids: The Arcade Classic Game
*Implementation of the classic arcade game using JavaScript, HTML5 Canvas, and a save progress system*

## 🚀 Introduction

Welcome to the web version of the classic game *[Asteroids](https://en.wikipedia.org/wiki/Asteroids_(video_game))*! 
Originally developed by Atari in 1979, *Asteroids* became one of the most iconic arcade games of all time. 
Its simple yet addictive gameplay, featuring a spaceship navigating through an asteroid field while shooting obstacles 
into smaller fragments, captured the imagination of millions.

Did you know that *Asteroids* was one of the first games to use [vector graphics](https://www.youtube.com/watch?v=ywIpBSblBdA&t=31s)instead of pixel-based sprites? 
This gave it a crisp, futuristic look that set it apart from other games of its era. 
The game was so popular that arcade cabinets required frequent servicing because players would slam the buttons too hard in the heat of battle!

## 🕹️ Game Mechanics

- **Player-controlled rocket ship with movement and thrust**: The spaceship is maneuvered using the arrow keys: the `up arrow` applies thrust, while the `left` and `right` arrows rotate the ship. This precise control system allows players to navigate through the asteroid field with skillful movements. Also, the activation of the thrust is accompanied by a visual effect.

- **Asteroids of varying sizes and speeds**: Asteroids are generated dynamically, appearing in random positions and shapes using the `Math.random()` function. Upon destruction, each asteroid splits into smaller fragments until it reaches its smallest size, adding an element of challenge and unpredictability.

- **Laser beams fired from the rocket ship**: Players can shoot using the `spacebar`, firing laser beams that travel a fixed distance before disappearing. This mechanic ensures strategic shooting, as lasers do not persist indefinitely.

- **Collision detection between game objects**: The game calculates collisions using a circular bounding radius for each element. Additionally, a temporary invincibility (blinking) mode is activated upon respawn, preventing immediate asteroid collisions.

- **Lives system**: Players start with three lives, visually represented by small ship icons in the upper-left corner of the screen. Losing all lives results in a game over.

- **Redraw mechanics.** When an object moves beyond the screen’s boundaries, it reappears on the opposite side, simulating an infinite space environment.

- **Levels progression and scoring**: After clearing all the asteroids in a round, the next level begins. The following round adds +1 asteroid to the total and increases their speed, making the game more challenging. Scoring is based on the size of the destroyed asteroid. Larger asteroids grant fewer points, while smaller asteroids award the most points, rewarding players for clearing the more difficult, faster-moving obstacles.

- **Game over**: When the player runs out of lives, a game over screen appears. After five seconds, the game automatically restarts.

- **Sound effects**: The game features immersive sound effects for thrusting, laser firing, and collisions, enhancing the overall experience.

## 🔧 Installation & Setup

To run this game as a static webpage from GitHub, follow these steps:

1. **Clone the repository to your local machine**  
   First, clone the repository that contains the game files. Open a terminal or command prompt and run the following command:
   ```bash
   git clone https://github.com/eugene-bytko/asteroid-arcade-game.git
   ```
2. **Navigate to the project folder**  
   After cloning, change the directory to the folder that contains the game files:
   ```bash
   cd asteroid-arcade-game
   ```
3. **Set up GitHub Pages**  
   - On GitHub, go to the repository’s settings page. 
   - Scroll down to the GitHub Pages section. 
   - In the Source dropdown, select the main branch (or gh-pages if your repository uses that). 
   - Once you save the settings, GitHub will automatically publish the static website.
4. **Access the game**  
   After the GitHub Pages configuration, you can access the game through the following URL:
   ```bash
   https://eugene-bytko.github.io/asteroid-arcade-game
   ```
5. **Optional: Local Testing**  
   If you want to test it locally before deploying, you can use a simple HTTP server. If you have Python installed, run:
   ```bash
   python -m http.server 8000
   ```
   Then, open `http://localhost:8000` in your browser to see the game running locally.

## 💾 Saving Progress

The game automatically saves your best score in the browser's **local storage**, ensuring your high score is remembered between sessions. This allows you to track your progress and aim to beat your best score every time you play.

To clear the saved data (including your high score), follow these steps:

1. Open the **Developer Tools** in your browser (usually by pressing `F12` or `Ctrl+Shift+I`).

2. Go to the **Application** tab (in Chrome) or **Storage** tab (in Firefox).

3. In the left-hand menu, select **Local Storage**.

4. Find the entry related to the game (e.g., `score`) and delete it.

Alternatively, you can clear the entire browser's local storage by clicking **Clear all** in the local storage panel.

## 📜 Credits & References

This project draws inspiration from the fantastic [JavaScript Asteroids Tutorial](https://www.youtube.com/watch?v=H9CSWMxJx84) on YouTube, building upon its foundation with new features and enhancements.

## ⚖️ License

This game is licensed under the **MIT License**. You are free to modify, distribute, and use the code, as long as you include the original copyright and license notice in any copies of the game. The MIT License encourages creativity and collaboration, allowing you to improve and build upon this game.

For more details, refer to the full [MIT License](https://opensource.org/licenses/MIT).
