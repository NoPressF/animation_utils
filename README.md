# fiAnimation
With this script you will be able to work with the OnPlayerFinishAnimation event

# Example:
```pawn
new time_point = 0.5; // A time point between 0.0 and 1.0 calls OnPlayerFinishAnimation when, for example, the animation is halfway complete (0.5)
au_ApplyAnimation(playerid, "BOMBER", "BOM_PLANT_CROUCH_IN", 4.1, false, false, false, false, 0, true, time_point);

```
```pawn
public OnPlayerFinishAnimation(playerid, animationid, finishedMilseconds)
{
    // Animationid - get value a played id animation.
    // finishedMilseconds - get value a how long the animation has been completed in milliseconds since it started.
    // Example:
    if(animationid == 165)
    {
        SendClientMessage(playerid, -1, !"Animation finished!");
        printf("Animation finished in [ %i ] milseconds!", finishedMilseconds); // Result = Animation finished in [ 850~ ] milseconds!
    }
    return true;
}
```
