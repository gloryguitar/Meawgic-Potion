# Meawgic Potion

Meawgic Potion is a JavaFX 2D farming and potion-brewing game. Explore the map, buy and grow magical ingredients, brew potions from recipes, and sell requested items in the shop to earn coins.

## Features

- Pixel-art JavaFX game scene with outside and inside maps
- Player movement and object interaction
- Crop planting, watering, timed growth, and harvesting
- Potion brewing with ingredient recipes and brewing timers
- Inventory for ingredients and potions
- Shop quests for selling items and earning coins
- Music/effect toggles, reset button, and in-game potion guide

## Controls

| Key / Action | Description |
| --- | --- |
| `W` `A` `S` `D` | Move the player |
| `E` | Interact with highlighted objects |
| Mouse click | Use buttons, inventory items, shop quests, and brewing controls |

## Gameplay Loop

1. Start with coins and buy seeds from crop plots.
2. Fill the water bar at the pond.
3. Water planted crops and wait for them to grow.
4. Harvest ingredients into the inventory.
5. Enter the house and use a brewing pot to create potions.
6. Sell crops or potions at the shop to earn more coins.

## Project Structure

```text
src/application/   JavaFX entry point and start page
src/entity/        Item, crop, potion, stone, and recipe data
src/gui/           Inventory, shop, brewing, plant, and settings panes
src/inventory/     Ingredient and potion counters
src/logic/         Game controller, maps, player, objects, sound, and camera
res/               Images, fonts, and sound assets
UML/               UML diagrams
```

## Requirements

- Java JDK with JavaFX support, or a standalone JavaFX SDK added to the module path
- JavaFX modules used by this project include `javafx.controls`, `javafx.graphics`, `javafx.media`, and `javafx.fxml`

## Running

### Option 1: Run the included JAR

Download JavaFX, then run the JAR with JavaFX on the module path.

Windows example:

```bash
java --module-path "C:\path\to\openjfx-24_windows-x64_bin-sdk\javafx-sdk-24\lib" --add-modules javafx.controls,javafx.graphics,javafx.media,javafx.fxml -jar MeawgicPotion.jar
```

Generic example:

```bash
java --module-path <path-to-javafx-sdk>/lib --add-modules javafx.controls,javafx.graphics,javafx.media,javafx.fxml -jar MeawgicPotion.jar
```

### Option 2: Import in Eclipse

This repository includes Eclipse project files (`.project` and `.classpath`). Import the project into Eclipse and use a JavaFX-enabled JDK/JRE configuration, then run:

```text
application.Main
```

### Option 3: Compile manually

```bash
mkdir -p bin
javac --module-path <path-to-javafx-sdk>/lib --add-modules javafx.controls,javafx.graphics,javafx.media,javafx.fxml -d bin $(find src -name "*.java")
```

Run with the compiled classes and resources on the classpath:

```bash
java --module-path <path-to-javafx-sdk>/lib --add-modules javafx.controls,javafx.graphics,javafx.media,javafx.fxml -cp "bin;res" application.Main
```

> On macOS/Linux, use `bin:res` instead of `bin;res` for the classpath separator.

## Main Class

```text
application.Main
```

## Collaborator

- [Guitardesu](https://github.com/gloryguitar)
- [Ai_](https://github.com/AiSiriRak)
