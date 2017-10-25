# godot-data-structures
Godot Data Structures is a repository dedicated to collecting scripting-accessible `Reference` types that are not available by default in Godot's scripting [class API](http://docs.godotengine.org/en/latest/classes/index.html).

Godot starts out with `Array`, `Dictionary` (for HashMaps), and the `Node` and `SceneTree` types for multi-children tree structures. 

The intent is to create data types that fulfill new requirements at maximum efficiency and work out-of-the-box.

[Jump to Data Structure List](https://github.com/willnationsdev/godot-next#data-structures)

## How to Use

1. If godot-data-structures is on the Asset Library already, simply plugin the asset from the Asset Library browser. Otherwise, download the repository as a .zip from GitHub. Unzip the archive and copy the files into your project directory (you just need to put the `godot-data-structures` folder into the `res://addons/` directory for your project).

2. Create or open a project.

3. Create a script that will use the new data structure.

4. Let's assume the data structure is `DataType.gdns` located at `res://addons/godot-data-structures/DataType.gdns`. In the new script, type the following:

    const DataType = preload("res://addons/godot-data-structures/DataType.gdns")

5. Then, in another section of the script, type...

    var data_type = DataType.new()

This will give you an instance of the data structure called `DataType` in your script.

## How to Contribute

Note that this repo caters more strongly towards GDNative implementations, especially those in C++, D, or another efficiency-focused language. Feel free to contribute a GDScript or C# implementation, but we should make it a goal to eventually port these scripts to native implementations.

### Ideas
If you have an idea for a node that you would like to have added to the repository, create a new Issue.

### In Progress
Work-in-progress nodes should be kept in forked repositories until completed. Feel free to edit the README file's Work In Progress section with a link to your repository's content.

### Completed

If you would like to add your own data structure to the repository, do the following:

1. Fork the repository to your GitHub.

2. Clone the repository and switch to the branch (major.minor engine version) you are adding a data structure for.

3. Identify a place in the repository folder hierarchy that seems appropriate for your data structure. Folders should be named in association with a related topic. If you must create new directories, please follow a snake\_case naming scheme when creating topical directories.

4. Once you've found a suitable location, create a new directory, this time using UpperCamelCase.

5. Inside the new folder, attach the content necessary for your node. For GDScript, this would be a `.gd` file. For CSharp, this would be a `.cs` file. For GDNative scripts, the folder should contain the `.gdns` file, a GDNativeLibrary `.tres`, and one dynamic library file for each major desktop platform (Windows, Mac OS, Linux) along with any and all custom source code (not part of the bindings) that was used to generate the dynamic libraries. **For GDNative scripts, please attempt to acquire as many platforms as possible so that all data structures will be available to every user.**

- Be sure to include in your data structure a comment at the top saying "Contributors" along with a subsequent comment detailing your GitHub username after a hyphen. For example:
```
    # Contributors
    # - willnationsdev
```
- Please keep the content of your script in the appropriate style for the type of script you are making to maintain consistency. `.gd` files should use the established [GDScript style guide](http://docs.godotengine.org/en/latest/learning/scripting/gdscript/gdscript_styleguide.html). `.cs` files likewise should use UpperCamelCase for typenames and lowerCamelCase for variable and function names. Finally, any and all GDNative scripts should use the style conventions of the bound language. The exception to this would be GDNative C++, in which case, please use the style preferred in Godot Engine source code (snake\_case for variables/functions, UpperCamelCase for typenames). For example:
```
    # GDScript
    var my_var = null
    var ScriptType = preload("res://script.gd")

    // CSharp
    public int myVar = null;
    public class MyClass {};

    // GDNative C++ (if a different language, then you should use whatever convention is appropriate for that language)
    int my_var = null;
    class MyClass {};
```

6. Go to the README.md file and add the name of any added types to the list of included data structures along with any hashtags you would like to attach (please keep it to 3 or less). The name of the type should be a relative link to its location in the repository. If possible, try to find a space nearby other nodes of a similar type. For GDNative scripts, the description should specify what platforms have been made available.

7. Commit and push all of your changes

    1. the new directory with an UpperCamelCase name (and snake\_case parent directory names).
    2. the script-related file(s) with an UpperCamelCase name (with contributor credits).
    3. the modified README.md file to add your node to the description of the repository's content. (GDNative scripts should specify what platforms have been made available)

8. Submit a pull request to the original repository

If you would like to make edits to an existing data structure, don't forget to add your name to the list of contributors within that data structure's script.

If possible, please try to create working scripts for each version of the engine supported by the branches. One way that you as a community member can help is by porting existing types from one engine version to another.

If you find any problems with a particular plugin or have suggestions for improving it and would like to launch a discussion, please create an Issue and mention one of the active developers associated with it (you can click on the file and then click on the History button to see a list of commits that have edited the file. Common usernames will give you an idea of who to mention).

That's it! I hope you've got ideas of what you'd like to share with others.

# Data Structures

(Since no data structures have been created yet, please refer to the README content of [Godot NExt](https://github.com/willnationsdev/godot-next) for an idea of how to format this table.)

|Linkable Node Name|Description|Language|Tags
|-|-|-|-|

# Work In Progress Nodes

These are nodes that others are actively working to contribute to the repository. Clicking the link should take you to the new node's code so-far-implemented in their forked repository.

|Linkable Node Name|Description|Language|Tags
|-|-|-|-|

