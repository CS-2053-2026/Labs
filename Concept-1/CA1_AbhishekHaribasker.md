# CS2053 - Concept Assignment 1
## Abhishek Haribasker

---

**1**:


**2-a**:
_ready: Its used for initialization. It occurs once when the node enters the Scene Tree.
_physics_process: Its used for physics-related tasks like movement or collisions. It occurs at a fixed frequency.
_process: Used for non-physics tasks like UI or timers. It occurs on every frame.
Order: _ready first, then _physics_process. Finally, _process.

**2-b**:
These functions are used to iterate through all active nodes so that we don't have to write the while loop manually.

**2-c**:
_ready: It cannot be triggered again naturally unless we add the node to the tree again.
_process: Frequency depends on hardware performance. We can't strictly control it, but we can toggle it off using set_process(false).
_physics_process: Frequency is fixed.

**3**:
Buffering is used to prevent screen tearing and flickering. It is disabled to reduce input latency.

**4**:
The sprite-sheet equivalent for large, static things like environments are called Tilemaps.
These sprite-sheet equivalents are referenced to a particular image. These are called Tilesets.

**5-a**:
(6,6)

**5-b**:
var pos1 = Vector2(2, 2)
var pos2 = Vector2(8, 8)
var diff = pos2 - pos1
var direction = diff.normalized()

**6**:
To determine the speaker, first we find target vector.

T = E - C, where C is character position and E is explosion position.
Next, we find dot product.
d = T.R, where R is a vector.

Now, to determine speaker:
If d > 0: The explosion is to the right; play sound in the right speaker.
If d < 0: The explosion is to the left; play sound in the left speaker.
If d = 0: The explosion is centered.


**7-a**:
The meaning of dot product(N,L) is the dot product of a normal surface and directional light.
We multiply by DiffuseColor because the dot product acts as a scaling factor. For a directional light, L vector is the negated direction of light.

**7-b**:
The meaning of dot product(R,V) is the dot product of reflection and view/eye vector.

**8-a**:
<3,4,2> + <6,8,0> = <9,12,2>.

**8-b**:
2 . <6,8,0> = <12,16,0>.

**8-c**:
<3,4,2> X <6,8,0> = <-16,12,0>.

**8-d**:
<3,4,2> . <6,8,0> = 50.

**9**:
W = [(1,0,0,3),(0,0,-1,4),(0,1,0,2),(0,0,0,1)].

**10**:
We filter signals to remove noise, which can be any unwanted or meaningless signal that interferes with the desired input.

Ways to filter Analog inputs:
-> Dead Zone.

Ways to filter Digital inputs:
-> Low-pass filter


---
