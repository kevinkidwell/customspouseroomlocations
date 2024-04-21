# Custom Spouse Room Locations - Vanilla
A mod for Stardew Valley 1.6+

This mod was inspired by [Split Spouse Rooms](https://www.nexusmods.com/stardewvalley/mods/17699) that I used before 1.6 and my absolute need to move my spouse rooms around.

## Details:
- This is for the Vanilla version of the game. If you are using a modded farmhouse, download the corresponding version instead.

---

## What does it do?

- Replaces map files for (hopefully) seamless visuals when you move spouse rooms around
- Configuration options for where you want your spouse room(s) to move
- Config file to define what spouse rooms go where
- Configuration for minor visual fixes to apply along with these map edits

---

## What’s in the mod folder?

- Two folders, one for CP and one for PSR.
- The CP folder is required for map edits. Includes various visual assets, maps, and configuration setup.
- The PSR folder is required to move spouse rooms around. Includes a content file to edit spouse room locations.

---

## Dependencies:

### Required:
- [Content Patcher](https://www.nexusmods.com/stardewvalley/mods/1915)
- [PolyamorySweet](https://www.nexusmods.com/stardewvalley/mods/20599), specifically Polyamory Sweet Rooms

### Recommended:
- [GMCM](https://www.nexusmods.com/stardewvalley/mods/5098) for configuration
- [PolyamorySweet](https://www.nexusmods.com/stardewvalley/mods/20599) for multiple spouses

---

## How to Edit:
1. Open the [PSR] Custom Spouse Room Locations folder
2. Find the example-content.json file
3. Duplicate that file and rename it content.json
4. Follow the information provided here for the different variables, placement information, and examples.  

### General information:  
1. All spouse rooms are 7 blocks wide (X) and 12 blocks tall (Y)
2. Templated data shows the starter placement for each location that you can place a room
3. Remove or comment out any unused placements

### Placement Information:  
All placements have this layout for informational purposes:  
```
// Mod name or vanilla  
// The location of this room, corresponds to config  
// How many rooms you can place in this location  
// Shell templates you can use here
```

### Example:  
```
// VANILLA  
// UPPER  
// As many rooms to the right as you want  
// “custom_spouse_room_closed_right”, “custom_spouse_room_open_right  
{  
   “name”: “SpouseName”, <— This is the name of the spouse whose room you are placing  
   “startPos”: {  
      “X”: 68, <— This is the starting x-axis for this room  
      “Y”: 2 <— This is the starting y-axis for this room  
   },  
   “spousePosOffset”: { <— Sets the offset of the spouse within the room from PSR (I don’t tend to touch this)  
      X”: 3,  
      “Y”: 3  
   },  
   “shellType”: “custom_spouse_room_closed_right”, <— This is the type of room shell for this specific spouse room  
}
```

### Starting Position Variables: 
```
Vanilla:
    Upper: X:68, Y:2
    Lower Right: X:49, Y:33
    Lower Left: X:30, Y:33
```

### Shell Type Variables:
```
custom_spouse_room_open_right:
    Vanilla: Lower right or Upper, with another spouse room to the right of it.

custom_spouse_room_closed_right:
    Vanilla: Lower right or Upper, AND it's the only or last spouse room in the row.

custom_spouse_room_open_left:
    Vanilla: Lower left, with another room to the left of it.

custom_spouse_room_closed_left:
    Vanilla: Lower left, AND it's the only or last spouse room in the row.
```
---

## Get in Touch:
If you want to get in touch with me with any questions, concerns, suggestions, etc.:
- Post in the [Discussion tab on Nexus](https://www.nexusmods.com/stardewvalley/mods/21525/?tab=posts)
- Submit a bug report on [Nexus](https://www.nexusmods.com/stardewvalley/mods/21525/?tab=bugs) or [Github](https://github.com/kevinkidwell/customspouseroomlocations/issues)
- Message me on Discord @kevinkidwell or tag me in the SDV Discord
