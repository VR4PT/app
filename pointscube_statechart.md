```mermaid
stateDiagram-v2
[*] -->idle
idle --> idle: overlapWithPlayer/<br/>viewportOverlay("Good job") for 5 seconds,<br/>totalReps++

idle: Idle<br/>enter/spawnElvis, spawnCube<br/>exit/destroyElvis, destoryCube
```
