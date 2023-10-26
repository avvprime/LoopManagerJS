# LoopManagerJS
Proper game loop for javascript. You can add and remove update and draw functions to the loop.

```
LoopManager.setSimulationDepth(120) // Default is 60 simulation per second. Use higher numbers for physics related jobs with the cost of performance.

const myUpdateId = LoopManager.addUpdate(update);
const myDrawId = LoopManager.addDraw(draw);

LoopManager.start(); // start game loop

// LoopManager.stop();

function update(delta)
{
  x += 10 * delta
  y += 10 * delta
}
function draw()
{
  ctx.fillStyle = 'red';
  ctx.fillRect(x, y, 100, 100);
}

// Use LoopManager.removeUpdate(myUpdateId) and LoopManager.removeDraw(myDrawId) to remove functions from game loop
```
