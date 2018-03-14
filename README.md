# `fadebetweencolours-gml`

* A script for `.gml`, [YoYo Games'](https://www.yoyogames.com/) proprietary language which forms part of their [Gamemaker: Studio](https://www.yoyogames.com/gamemaker) software.
* Use this script to fade between two RGB colours at a certain `rate` every game step.
* The `rate` refers to how much the RGB values (ranging from 0-255) change each step. A `rate` of `5` would change the `R`, `G` and `B` values of the original colour by 5 each step until it reached the `R`, `G` and `B` values of the target colour.
* Free (£ and *libre*) to use without attribution.
* Download the text file above, or copy and paste from below.

```
///GoBetweenColoursAuto(colour1r, colour1g, colour1b, colour2r, colour2g, colour2b, rate)

OriginalR = argument0
OriginalG = argument1
OriginalB = argument2

TargetR = argument3
TargetG = argument4
TargetB = argument5

RDiff = abs(argument0 - argument3)
GDiff = abs(argument1 - argument4)
BDiff = abs(argument2 - argument5)

Rate = round(argument6)

//----------------------------

if CurrentR < TargetR {
CurrentR += (Rate)
} else if CurrentR > TargetR {
CurrentR -= (Rate)
}

if CurrentG < TargetG {
CurrentG += (Rate)
} else if CurrentG > TargetG {
CurrentG -= (Rate)
}

if CurrentB < TargetB {
CurrentB += (Rate)
} else if CurrentB > TargetB {
CurrentB -= (Rate)
}


CurrentColour = make_colour_rgb(CurrentR,CurrentG,CurrentB)

return CurrentColour
```
