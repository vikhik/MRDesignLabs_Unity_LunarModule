# Mixed Reality Design Labs

This repo is where Microsoft's Windows Mixed Reality Design team publishes examples and explorations. The goal is to inspire creators and help them to build Mixed Reality experiences. We share sample app projects here that demonstrate how to use various types of common controls and patterns in Mixed Reality. Find out details about common controls and sample apps on https://developer.microsoft.com/en-us/windows/mixed-reality/design


# Lunar Module

<img src="https://github.com/Microsoft/MRDesignLabs_Unity_LunarModule/blob/master/External/ReadMeImages/LM_hero.jpg" alt="Lunar Module sample app">


Lunar Module is a open-source sample app from Microsoft's Mixed Reality Design Labs, it is a spiritual sequel to the 1979 Atari classic, *Lunar Lander*. This sample app will demonstrate how to extend Hololens' base gestures with two hand tracking and xbox controller input, reactive objects to surface mapping and plane finding, and simple menu systems. You can use this project's components to create your own mixed reality app experience. 

# Technical Details

**Local Hand Input** - *Assets/MRDesignLab/HUX/Scripts/Utilities/LocalHandInput.cs* - This script provides a convenient way to track left / right hand input in local space relative to the player's head. Once the player taps anywhere in space, that point is treated as the input origin and all translations are reported as X,Y and Z position / velocity in local space. This local translation survives world translations as well (eg, walking forward with your hand extended). Acceleration, clamping and dead zones are also provided.

<img src="https://github.com/Microsoft/MRDesignLabs_Unity_LunarModule/blob/master/External/ReadMeImages/LM_LocalHandInput.PNG" alt="Local hand input">

**Simple Menu Collection** - *Assets/MRDesignLab/HUX/Prefabs/Dialogs/SimpleMenuCollection* - Most of Lunar Module's menus are generated by the SimpleMenuCollection.cs script, which extends SimpleMenu.cs class and combines it with ObjectCollection to provide a way to rapidly assemble interfaces.

To use this prefab, drag it into your scene and assign a button prefab. Then enter the desired button names and targets into the inspector editor. Buttons will be instantiated at runtime and assigned to the specified Input Receivers. (For an example of an Input Receiver, check out Assets/MRDesignLab_LunarModule/Scripts/Screens/StartupScreen.cs.) SimpleMenu.cs and SimpleMenuCollection.cs could easily be extended to include transitions, animations and so on.

<img src="https://github.com/Microsoft/MRDesignLabs_Unity_LunarModule/blob/master/External/ReadMeImages/LM_SimpleMenuCollection.PNG" alt="Simple menu collection">

**Hand Coach** - *Assets/MRDesignLab_LunarModule/Prefabs/HandCoach* - this prefab enables devs to create standardized tutorials for their apps. It provides an interface for demonstrate left or right handed gestures, including directional motion. Visual options include ghosting, highlighting and color changes for lost tracking.

<img src="https://github.com/Microsoft/MRDesignLabs_Unity_LunarModule/blob/master/External/ReadMeImages/LM_HandCoach.PNG" alt="Hand coach">

# More from Mixed Reality Design Labs #

**Common Controls Examples**: https://github.com/Microsoft/MRDesignLabs_Unity

**Periodic Table of Elements sample app**: https://github.com/Microsoft/MRDesignLabs_Unity_PeriodicTable

# Contributing
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
