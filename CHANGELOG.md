# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

# Section Groups
* **Added** - for new features
* **Changed** - for changes in existing functionality
* **Deprecated** - for once-stable features removed in upcoming releases
* **Removed** - for deprecated features removed in this release
* **Fixed** - for any bug fixes
* **Security** - to invite users to upgrade in case of vulnerabilities
* **Unreleased** - shows changes as they occur - allows users to anticipate new functionality.

***

# Release History 
#### (For Details See Version Changes Below)
* [v2.0] - Classify feature; Export to CSV; Optimized Bootup refactoring; Java Preferences Extension Library; Tooltip Module
* [v1.1] - Configuration from Properties File
* [v1.0] - Drag-n-Drop of Fingerprints; Bubbles (terms), Contexts; Copy/Paste JSON; Freehand Expression Syntax
* [v0.9] - Pre-production

***

## [v2.0.2]
#### Removed
#### Added
* Added this specific Github project repository.
* New UI for Global Properties Editor accessed through the addition of new Main Menu item.
* New UI for Global Category Composer accessed through the addition of new Main Menu item.
* New Java Preferences extension libary enabling the saving of complex objects and
registration of event handlers to changes on those items.
* Ability to save (using the above new library); user created Categories which can be used
as Classification Filters.
* New Classification feature on the new "Classify" UI tab in OutputWindows allowing the visualization of 
many simultaneous filters together with inspection of their result metrics in textual and graphical form.
* New "Export to CSV File" feature to save Keywords, Tokens, and Slices to local disk.
* New Tooltip behavior module to enable current and future custom tooltip behavior.
* Ability to use <CTRL> + "W" to advance focus to all windows.
* Added Tooltip to ContextsDisplay to inform user that the elipsis (...) can be clicked on to expand the
list of context words to reveal their similar terms.
* Added new property to display the path of the properties file being currently used - to the Global
Properties Editor.
* Added new property to control the tooltip time delay.
* Added ability to globally enable/disable tooltips.
* Added ability to specify the default Operator (i.e. And, Or, Not etc) in the InputWindow ExpressionDisplay.
* Added Interactive Legend to the Fingerprint display of the new ClassifyDisplay feature.
* Added Global property to enable specifying Retina's to "exclude" from language detection. (i.e. needed for "en_synonymous")
* Externalized all custom libraries to their own Github projects (i.e. ExtendedClient, ExtendedPreferences, CorticalFX [widgets]) so now they are "trackable" in their own repositories.
* Added new "WeakIdentityHashmap" class which allows registration of listeners for Garbage Collection object queuing.
* Big refactoring of "bootup" process to allow clearer semantics and comprehension of startup code; plus enabling
detection of end of bootup with property notification allowing dependent start up code to "know" when all UI objects
are coherent and therefore able to be referenced. (Listeners can be added for quiescence detection)
* Use of the above to disable Main menu until the object node hierarchy and UI are fully initialized. (Previously could cause errors if user clicked on the menu before they were ready.)
#### Changed
* Greatly simplified pasting of Freehand expressions directly into the Expression UI. 
#### Fixed 
* TextDisplay: Retina drop-down list is now in sync with the Window's Retina selection in the ControlPanel's
WindowBoxes.
* Removed automatic deletion of Terms in the ExpressionDisplay when they are not present in the current Retina
being used. (Used to delete the user's input.)
* Fixed multiple "other" bugs throughout...
***

## [v1.1]  Main Feature: Configuration from Properties File
#### Removed
#### Added
* This CHANGLOG
* New 'ExtendedClient' code module and repository containing Endpoint abstraction to handle clients specialized for 'position lookups'
* RetianPropertyConfigurationTest in ExtendedClient repo - contains all unit tests for new Properties classes.
* OrderedProperties modified 3rd party class for ability to print out properties in 'encounter' order.
* PrefixedProperties - custom subclass of OrderedProperties to handle manipulation of properties by named groups.
* Application Menubar
* Ability to 'reset' configurations. (no more deleting the api key file) Allows ability to restate configuration to use upon next start up.
* Ability to print out example properties file to the user's home directory
* New "Load Properties File" button on the initial Overlay home screen and feature for selecting properties file to load from.
* API key loading method still remains the same. Properties file feature can not exist in tandem with previous method.
* System 'remembers' (stores in preferences) the file path of the previous loaded properties file and will auto-load it upon subsequent start ups so 
the don't have to be re-specified on every start up.
* Endpoint URL's are now explicitly and extensively checked for connection viability for each URL during startup to guarantee configuration is "sane".
* Added new deployment installer image and executable jar.
* Link to newly updated "User Guide"
#### Changed  
* README.md landing page to reflect new deployment version number.
* Links to new installer versions on README.md
#### Fixed

