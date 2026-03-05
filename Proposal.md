# Abstract
Game name : 

Group: 
- 曾衡昌 113590033
- 應尼歌 113590040

# Game Introduction

# Development Timeline

### Phase 1: Planning & Physics Foundations
**Week 2: Concept & Requirements**
* Define "Mario Logic": Gravity constants, terminal velocity, and jump impulse values.
* Setup C++ environment: SFML linking, directory structure, and CMake configuration.
* Sketch the "Game Loop": `HandleInput` → `Update(dt)` → `Render`.

**Week 3: OOP Design & Architecture**
* Create Class Diagram: `Entity`, `Player`, `Enemy`, `Tile`, `Camera`.
* Define Inheritance Hierarchy: `Entity` → `DynamicEntity` (Mario/Goomba) and `StaticEntity` (Blocks).

* Establish the `GameManager` to coordinate state transitions.

### Phase 2: Core Mechanics & Prototyping
**Week 4: The Kinematic Player**
* Implement horizontal movement with acceleration/deceleration logic.
* Implement the variable jump (height depends on button hold duration).

**Week 5: Tilemap & Static Collision**
* Implement a `TileMap` class for rendering levels efficiently using `sf::VertexArray`.
* Implement AABB Collision Detection for solid ground and walls.


**Week 6: Combat System (Stomp Logic)**
* Implement vertical collision checks: Detect if Player is falling while colliding with an enemy's top bound.
* Handle Player state changes (Small Mario vs. Big Mario hitbox scaling).

**Week 7: Items & Blocks**
* Implement `QuestionBlock` and `Brick` logic (breaking vs. bumping).
* Create item classes: Mushrooms and Coins with their own simple physics.

**Week 8: Level Scrolling (The Camera)**
* Implement an `sf::View` based camera system.
* Implement "Camera Locking" to prevent the screen from scrolling backward (classic NES style).

### Phase 3: Expansion & Polishing
**Week 9: Enemy Variety & AI**
* Add different enemy types (Goombas, Koopas) using polymorphism for unique behaviors.
* Implement "Pit Deaths" and boundary checking.

**Week 10: State Machine & UI**
* Add Start Menu, Pause, and Game Over screens.
* Display HUD: Score, Coin count, World number, and Timer using `sf::Font`.

**Week 11: Sprite Animations**
* Implement an `Animation` manager to handle frame-switching for run, jump, and idle cycles.
* Handle sprite flipping (texture rect mirroring) based on movement direction.

**Week 12: Level Expansion & Loading**
* Implement a File Parser to load level layouts from `.txt` or `.json`.

* Add the "Flagpole" logic to trigger level completion and score calculation.

**Week 13: Advanced Sound & Feedback**
* Integrate `sf::Sound` for jumps, stomps, and power-ups.
* Add background music using `sf::Music` with looping logic.

**Week 14: Debugging & Refactoring**
* Refactor code for Encapsulation (ensure no public member variables).
* Fix "Wall Clipping" and "Corner Catching" physics bugs.

### Phase 4: Testing & Finalization
**Week 15: Playtesting & Balance**
* Fine-tune physics constants (friction/gravity) for the best "game feel."
* Ensure level difficulty progression is balanced.

**Week 16: Optimization**
* Optimize draw calls for stable 60 FPS.
* Perform final memory leak checks using Valgrind or Visual Studio Debugger.

**Week 17: Final Touches**
* Add visual feedback (particle effects for breaking bricks).
* Ensure smooth transitions between Game States.

**Week 18: Submission**
* Prepare project package (Source code, Assets, CMakeLists.txt).
* Final Documentation: Technical manual and User guide.
