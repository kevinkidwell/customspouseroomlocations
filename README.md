# Custom Spouse Room Locations
A mod for Stardew Valley 1.6+

This mod was inspired by [Split Spouse Rooms](https://www.nexusmods.com/stardewvalley/mods/17699) that I used before 1.6 and my absolute need to move my spouse rooms around.

**----------------------------------------**

## What does it do?

- Replaces map files for (hopefully) seamless visuals when you move spouse rooms around
- Configuration options for where you want your spouse room(s) to move
- Config file to define what spouse rooms go where
- Configuration for minor visual fixes to apply along with these map edits

**----------------------------------------**

## What’s in the mod folder?

- Two folders, one for CP and one for PSR.
- The CP folder is required for map edits. Includes various visual assets, maps, and configuration setup.
- The PSR folder is required to move spouse rooms around. Includes a content file to edit spouse room locations.

**----------------------------------------**

## Dependencies:

**Required:**
- [Content Patcher](https://www.nexusmods.com/stardewvalley/mods/1915)
- [PolyamorySweet](”https://www.nexusmods.com/stardewvalley/mods/20599”), specifically Polyamory Sweet Rooms

**Recommended:**
- [GMCM](”https://www.nexusmods.com/stardewvalley/mods/5098”) for configuration
- [PolyamorySweet](”https://www.nexusmods.com/stardewvalley/mods/20599”) for multiple spouses

**----------------------------------------**

## Compatibility:

This mod has been updated to be compatible with the following mods:
- [Lnh's First Farmhouse](https://www.nexusmods.com/stardewvalley/mods/17526)
- [Seasonal Garden Farmhouse v2](https://www.nexusmods.com/stardewvalley/mods/17386)
- [Lune FarmHouse](https://www.nexusmods.com/stardewvalley/mods/17627)
- [Aimon's Tidy Cozy Farmhouse](https://www.nexusmods.com/stardewvalley/mods/16438)

Compatibility work in progress for the following mods, will be released when ready:
- [Aimon's Fancy Farmhouse](https://www.nexusmods.com/stardewvalley/mods/14411)

**----------------------------------------**

## How to Edit:

   1. Open the [PSR] Custom Spouse Room Locations folder
   2. Find the example-content.json file
   3. Duplicate that file and rename it content.json
   4. Follow the information provided here for the different variables, placement information, and examples.

    **General information:**
        1. All spouse rooms are 7 blocks wide (X) and 12 blocks tall (Y)
        2. Templated data shows the starter placement for each location that you can place a room
        3. If you are using farmhouse mods, look for that section to see the starting positions for your specific modded room locations
        4. Remove or comment out any unused placements

    **Placement Information:**
        All placements have this layout for informational purposes:
            // Mod name or vanilla
            // The location of this room, corresponds to config
            // How many rooms you can place in this location
            // Shell templates you can use here

        **Example:**
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
            },

        **Starting Position Variables:**
            **Vanilla:**
                **Upper**: X:68, Y:2
                **Lower Right**: X:49, Y:33
                **Lower Left**: X:30, Y:33

            **Seasonal Garden Farmhouse v2:**
                **Attic**: X:7, Y:56
                **Large Room**: X:69, Y:56
                **Main Floor Left**: X:8, Y:8
                **Main Floor Right**: X:69, Y:21

            **Lnh's First Farmhouse:**
                **Main Floor**: X:49, Y:0
                **South Room**: X:50, Y:92
                **Southeast Room Right**: X:39, Y:197
                **Southeast Room Upper Left**: X:10, Y:195
                **Southeast Room Lower Left**: X:10, Y:208

            **Lune FarmHouse:**
                **Upper Room**: X:7, Y:8
                **Kitchen Cellar - Small**: X:7, Y:30
                **Kitchen Cellar - Large**: X:7, Y:33
                **Upper Right Room**: X:61, Y:8
                **Southern Room - Small**: X:58, Y:30
                **Southern Room - Large**: X:58, Y:33

            **Aimon's Tidy Cozy Farmhouse:**
                **Left bedroom**: X:7, Y:19
                **Right bedroom**: X:46, Y:32


        **Shell Type Variables:**
            **custom_spouse_room_open_right**:
                Vanilla: Lower right or Upper, with another spouse room to the right of it.
                SGFv2: Large room or Main Floor Right, with another spouse room to the right of it.
                LNH: Main Floor, South Room, Southeast Room Right, with another spouse room to the right of it.
                Lune: Upper Right Room, Southern Room - Small, Southern Room - Large, with another spouse room to the right of it.
                ATC: Right bedroom, with another spouse room to the right of it.

            **custom_spouse_room_closed_right**:
                Vanilla: Lower right or Upper, AND it's the only or last spouse room in the row.
                SGFv2: Large Room or Main Floor Right, AND it's the only or last spouse room in the row.
                LNH: Main Floor, South Room, Southeast Room Right,  AND it's the only or last spouse room in the row.
                Lune: Upper Right Room, Southern Room - Small, Southern Room - Large,  AND it's the only or last spouse room in the row.
                ATC: Right bedroom, AND it's the only or last spouse room in the row.

            **custom_spouse_room_open_left**:
                Vanilla: Lower left, with another room to the left of it.
                SGFv2: Attic or Main Floor Left, with another room to the left of it.
                LNH: Southeast Room Upper Left or Southeast Room Lower Left, with another room to the left of it.
                Lune: Upper Room, Kitchen Cellar - Small, Kitchen Cellar - Large, with another room to the left of it.
                ATC: Left bedroom, with another room to the left of it.

            **custom_spouse_room_closed_left**:
                Vanilla: Lower left, AND it's the only or last spouse room in the row.
                SGFv2: Attic or Main Floor Left, AND it's the only or last spouse room in the row.
                LNH: Southeast Room Upper Left or Southeast Room Lower Left, AND it's the only or last spouse room.
                Lune: Upper Room, Kitchen Cellar - Small, Kitchen Cellar - Large,  AND it's the only or last spouse room in the row.
                ATC: Left bedroom, AND it's the only or last spouse room in the row.

**----------------------------------------**

## Notes:
- This was created primarily for my personal use and so may have some bugs. Let me know if you find any and I'm willing to try and fix them!
- This is intended for the fully upgraded farmhouse (including Southern Room and Expanded Upper Room, with edits for Cubby) but may work as long as you only have one of those sections. Compatibility for other mods may be added in the future.


**----------------------------------------**

## Get in Touch:
If you want to get in touch with me with any questions, concerns, suggestions, etc.:
- Feel free to post in the Discussion tab here
- Message me on Discord @kevinkidwell or tag me in the SDV Discord