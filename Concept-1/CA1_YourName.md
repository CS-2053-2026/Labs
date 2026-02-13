# CS2053 - Concept Assignment 1
## Reyaansh Vohra

---

**1**:

Initialize()
  Create paddle, ball, bricks
  score = 0
  lives = 3

While the game is running:
  Process()
    Move paddle
    Launch the ball if isPressed(Space)

  Update()
    Update ball pos
    Check collision with wall, paddle, bricks
    if the ball falls
      lives--
    if lives == 0
      GAME OVER

**2-a**:

_ready() is used for scene initialization(when the node enters the scene).
_physics_process() is used for physics(like momentum) and movement.
_process() is used for the visuals, runs every frame.
ORDER: _ready() -> _physics_process() -> _process()

**2-b**:

After initializing the scene, the game loop handles different inputs and updates physics and logic.
_physics_process() handles the physics changes.
_process() takes care of the logic.

**2-c**:

The occurrence of physics can be changed in project settings.
_process() depends on the device's refresh rate.

**3**:
Buffering is used in 2D Game Graphics to prevent screen tearing and flickering. People usually disable it for debugging.

**4**:

We use TileMap to create the layout of one or more levels of the game.
TileSet is used to get different frames for different movements using image tiles.

**5-a**:

(6,6)

**5-b**:

var dir = (gameObject2.position - gameObject1.postion).normalized()

**6**:

Let A = Player pos
    B = Explosion pos

Dir = normalize(B-A)
Take a unit vector pointing to the right of A, X
C = DotProduct(Dir,X)
If C > 0 -> sound from right
   C = 0 -> centred sound
   C < 0 -> sound from left

**7-a**:

DotProduct(N, L) is the cos angle between the normal and light.
We multiply by DiffuseColor to apply material color.
L is a normalized directional vector.

**7-b**:

DotProduct(R, V) is the alignment between the reflection and the viewer.
We multiply the value of pow(DotProduct(R, V)` with SpecularColor to control the highlight colour.

**8-a**:

<9,12,2>

**8-b**:

<12,16,0>

**8-c**:

<-16,12,0>

**8-d**:

50

**9**:
Answer here

**10**:

We filter input to remove noise. If we don't filter input, the movement becomes jittery.
Ways of analog filtering: smoothing, deadzones.
Ways of digital filtering: timers, debouncing


---
