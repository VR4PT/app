Could also add mirror

```mermaid
---
title: System-level Class Diagram
---
classDiagram
class PointsCube{
    Transform ElvisOriginalLocation
    OnComponentBeginOverlap()
}

class LevelFromAlpha { }

Level <| -- LevelFromAlpha

class VRPawn{
    tryTeleport()
    snapTurn()
    getGrabComponent()
    onEventBeginPlay()
    onEnhancedInputAction()
    onBeginOverlap()
    int myReps

}
class BigElvisWalking{
    onEventTick()
    Transform elvisOriginalLocation
    onBeginOverlap()
    spawnAt()
}

class Mirror { }

LateralRaiseLevel o-- Mirror





class Arms {
    Transform leftHandTransform
    Transform rightHandTransform
    onEventUpdateAnimation()
}

class Level {
    onEventBeginPlay()
    onEventTick()
    repsComplete()
    spawnLeftBlock()
    spawnRightBlock()
    int blocksTouched
    int setsCompleted
    int repsCompleted
    int constReps
    int constSets
}

class LateralRaiseLevel { }
Level <|-- LateralRaiseLevel

class Hand {
    Float poseAlphaGrasp
    Float poseAlphaPoint
    Float poseAlphaThumbUp
    onEventUpdateAnimation()
}



class HeadMountedDisplay{ }



VRPawn *-- Arms

VRPawn *-- Hand
VRPawn *-- HeadMountedDisplay
HeadMountedDisplay <-- Arms

LateralRaiseLevel o--BigElvisWalking
Level o-- PointsCube
Level o-- VRPawn

```
