# Legion - The Apex Legends Asset Extractor
Extracts various assets from the game "Apex Legends". This software is considered **Work-in-Progress** developed by [DTZxPorter](https://twitter.com/dtzxporter) & id-daemon.

_Download and version info:_

> **IMPORTANT:** By downloading this software you are agreeing to the **EULA** located inside of the archive (EULA.txt).

- Download Link: [Legion (v0.84)](https://mega.nz/#!ERxjmICB!-QCYh7HOVlidxKen9TjTJ0JtEklafklkaVfwLg0fYQo).
- Requires Visual Studio 2019 x64 Redist: [Redist](https://aka.ms/vs/16/release/vc_redist.x64.exe).
- Currently works as of 4/7/2019 updates.

## Donate:
- I take time out of my day to make this happen.
- Show your support: [HERE](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=686S5QL7Z4HKQ)

## Usage:
Using Legion is fairly simple as the tool only requires the files located within "Apex\paks\Win64" in order to function.
> **IMPORTANT:** Both the tool and the game **require** the entirety of the Win64 folder to be intact and must not be modified in any way.

- The tool supports Drag and Drop functionality, supported file formats are ONLY the **.rpak** extensions.

## Command Line:
- By default, Legion exports textures and data tables.
- To switch mode to models add:
  - `--exportmdl` as the first argument.
  - `--mdlfmt=obj` switches the model format.
    - Formats: [obj, smd, xnatxt, xnabin, maya] semodel is default.
- To switch mode to animations add:
  - `--exportanim` as the first argument.
- After these arguments, just pass the path to the rpak.
- Full example:
  - `--exportmdl --mdlfmt=smd "C:\path\to\apex\paks\Win64\common.rpak"`

> **IMPORTANT:** The tool **AUTO LOADS** the patch rpak files, just specify the base one and it will handle the rest.

> **NOTE:** Not all (0X).rpak files are patches, some can be loaded directly, just try them.

## Ripping:
- The **.rpak** files contain various encoded assets that Legion can export; and, as of now the currently supported assets are:
  - Textures in DDS format.
  - DataTables as a CSV file.
  - Models as [SEModel, OBJ, XNALara, SMD, Maya (Legacy)].
  - Animations as [SEAnim].
  
## Coming Soon
- Enhanced GUI.

## Known Bugs:
- A very small handfull of textures aren't supported yet.

## Versioning:
- 0.18 - Initial Release.
- 0.54 - Model export support, fixed patch_master crash, skip existing images.
- 0.60 - Patch rpak support, xmodel_export model format.
- 0.61 - Shadow fix for mp_rr* crash...
- 0.62 - Fixed SMD export when invalid normals exist, fixed materials in xmodel_export.
- 0.68 - Fixed season 1 rpak patches causing crashes.
- 0.84 - Initial support for animations, performance tweaks, maya (legacy) exporter.