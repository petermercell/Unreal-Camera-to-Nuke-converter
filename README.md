# Unreal Camera to Nuke Converter

A TCL script for converting Unreal Engine camera data to Foundry Nuke format.

## Overview

When exporting cameras from Unreal Engine to Nuke for VFX compositing, artists face a common challenge: the two applications use different coordinate systems. Unreal Engine uses a Z-up, left-handed coordinate system, while Nuke uses a Y-up, right-handed system. This converter handles the necessary transformations to ensure your Unreal cameras work correctly in Nuke.

## Features

- Converts Unreal Engine camera coordinate system to Nuke's coordinate system
- Handles rotation order and axis transformations automatically
- Preserves camera animation data
- Simple TCL-based integration with Nuke

## Installation

1. Download `Unreal_Nuke_Converter_PM.tcl`
2. Place it in your `.nuke` directory:
   - **Linux**: `~/.nuke/`
   - **macOS**: `~/.nuke/`
   - **Windows**: `C:\Users\<username>\.nuke\`
3. Add the following to your `menu.tcl` to add a menu item (optional):

```tcl
source "Unreal_Nuke_Converter_PM.tcl"
```

## Usage

1. Export your camera from Unreal Engine Sequencer
2. In Nuke, run the converter script
3. The script will create a properly transformed Camera node

## Example Files

The `UNREAL_NUKE_FILES` folder contains example files to help you get started with the workflow.

## Requirements

- Foundry Nuke (any version with TCL support)
- Camera data exported from Unreal Engine

## Common Workflow

1. **In Unreal Engine**: Set up your camera in Sequencer and export the camera animation
2. **Run Converter**: Use this script to convert the camera data
3. **In Nuke**: Import the converted camera for compositing work

## Why This Tool?

Manually converting cameras between Unreal and Nuke requires understanding both coordinate systems and applying the correct transformations. This script automates that process, saving time and reducing errors in VFX pipelines that combine real-time rendering with traditional compositing.

## License

MIT License - See [LICENSE.txt](LICENSE.txt) for details.

## Author

Peter Mercell  
[www.petermercell.com](https://www.petermercell.com)
