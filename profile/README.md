# StrayMods

Hi! This is BassNuke, this organization is meant as an option to see the code behind my mods in case you want to see/learn how something is down specifically.\
[UE4-Project](https://github.com/Bass-StrayMods/UE4-Project) contains the full Unreal project which you can download and run directly (pay attention to README.md information). Releases of all my mods can be found in this repository for all as well as in their own mod repository.

Independent mods can be added to your project as submodules and that is the purpose of the [SetupTrainer](https://github.com/Bass-StrayMods/SetupTrainer), [InputDisplay](https://github.com/Bass-StrayMods/InputDisplay) and [NoLogo](https://github.com/Bass-StrayMods/NoLogo) repositories as well as to hold their independent releases.

## Include in your own project
Go to any mods repository and get the clone address, do `git submodule add -f <git@github.com...>` inside of Content/Mods in your UE project

## Packaging
In order to be able to package mods in your project, you need to change some settings.
- Go to `Editor Settings` and enable `Allow ChunkID Assignments`

<img src="https://github.com/Bass-StrayMods/.github/blob/main/profile/editorSettings.png" width="300">
<br/>

<img src="https://github.com/Bass-StrayMods/.github/blob/main/profile/generateChunks.png" width="600">
<br/>

- Go to `Project Settings` and enable `Generate Chunks`

<img src="https://github.com/Bass-StrayMods/.github/blob/main/profile/projectSettings.png" width="300">
<br/>

<img src="https://github.com/Bass-StrayMods/.github/blob/main/profile/generateChunks.png" width="800">
<br/>

Assign every item under the mod subfolder (i.e. SetupTrainer) to a packaging chunk you will remember (check image). Save all the elements after doing so to update their chunk information.

<img src="https://github.com/Bass-StrayMods/.github/blob/main/profile/assignChunk.png" width="800">
<br/>

Package the project under the `Pkg` folder in your root UE project directory (you will need to create it, does not have to be Pak, any name/directory works just remember where it is).\

<img src="https://github.com/Bass-StrayMods/.github/blob/main/profile/package.png" width="500">
<br/>

After the project is packaged, go to `Pkg\WindowsNoEditor\Hk_project\Content\Paks` and rename `pakchunk<pak#>-WindowsNoEditor.pak` to `YourModName.pak` (i.e. SetupTrainer.pak).\

Put your new pak file under the LogicMods folder and it should be loaded with Unreal Mod Loader.
