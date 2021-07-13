# JBML
My mod loader for Unity (To be added to project)

# How to Use - As the Gamedev
Download and import JBML.unitypackage into your project. Create the JBMLObject prefab in the first loaded scene.
JBMLObject has some options that can be changed. Mod Tags To Be Loaded is a list of strings. The strings let the mod loader know what mod tags to load. "\*" means load all mod tags. If you're going to use this feature at all, I would recommend to make a settings menu in the game (under some kind of Advanced tab) where players can input the strings themselves.
By the way, make sure you add a Mods folder to the root of your assets folder and ship the game with a Mods folder in Game_Data
# How to Use - As the Modder
Download JBMLInterfaceManager.dll and create a new project (C# Class Library) in Visual Studio. Add a reference to JBMLInterfaceManager.dll.
In your script, add "using JBML.InterfaceManager;" and add make your class 'public class *ClassName* : MonoBehaviour, IMod'. In your class, create the method 'public string ModTag() {return "*ModTagHere*";}'. Then add the code you want (the script will be added to JBMLObject, by the way) and build the dll. Then put it in the Game_Data\Mods folder, and your mod should be loaded if you programmed it correctly.
