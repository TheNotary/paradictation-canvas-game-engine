# Paradictation

Paradictation is a minimal 2D canvas engine useful for building projects that make heavy use of sprite drawing and even sprite animation.  It's designed to not abstract so much of the process that you need to throw away your existing programming knowedgle to study some random guy's framework idea for a few months only to realize that 'superior' solutions have since been published by other random guys an you need to start all over again.  You know?

## Usage

NPM/ Yarn is used as the versioning/ packaging agent for this source code.  As such, to use this code in your game, you would do

    # npm install paradictation
    yarn add paradictation

Directly in the folder consisting of your HTML/JS source code.  Then to pull in the engine, you would add:

    <html>

    <body>
      <canvas id="someCanvasPerhaps"></canvas>
    </body>

      <script src="node_modules/paradictation/engine/screen.js"></script>
      <script src="node_modules/paradictation/engine/gameLoop.js"></script>
      <script src="node_modules/paradictation/engine/userInput.js"></script>

      <script src="yourScreenClass.js"></script>
      <script src="yourGameClass.js"></script>
      <script src="anInitFilePerhaps.js"></script>

    </html>

Perhaps in the future I'll add `parcel` as a dependency to increase the complexity of the system and decreate the number of steps involved in adding the engine to a project...

## Core Concepts

###### asGameLoop

There's an `asGameLoop` that you extend your existing game loop with.  Thereafter, when you call `yourGame.start()` the game loop begins, consisting of a `draw()` method which is called at 60hz or so, and an `update()` which will be fired as soon as possible (this is a typicall aproach to game development).

###### screens

There's a `screen` concept.  For instance, the mario intro screen that shows copyright information and a menu selection would be considered a `screen`, and once you begin the game, perhaps you would be switching to a level screen that represents a different canvas element entirely and consists of a totally different javascript object with custom programming for dealing with level-specific stuff like mario running around, cameras moving, etc., etc.




