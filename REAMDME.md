# Phonetcs Plugin for the Atto Editor
 This plugin adds a button to the Atto Text Editor to allow for teachers and students to add phonetic symbols.

Phonetic is a text editor tool that allows users to insert phonetic and linguistic symbols. To use this tool, users click on the Phonetic button on the Atto text editor menu bar. Clicking this button allows the selection of alphabetic symbols and delimiters from the International Phonetic Alphabet for insertion into running text. 

## Installation instructions:

1. Get the latest release source package (either as zip or tar.gz) from https://github.com/lsuonline/moodle_atto_phonetic.git/releases
1. Log in to Moodle as an Admin.
1. Navigate to **System Administration > Plugins > Install Plugins**
1. Drag the .zip of the latest release over the drag and drop section to install a plugin. 
1. Moodle should detect the new/upgraded plug-in and show "Plugins check" screen which prompts you to install/upgrade. Click  "Upgrade Moodle database now" button to proceed.
1. After installation is completed, visit **Site Administration > Plugins > Text Editors > Atto Toolbar Settings** and confirm that 'phonetic' has been added to the list of installed plugins for Atto.
1. On this same page, add 'phonetic' to the list of buttons following the heading 'accessibility' (it should now read something similar to 'accessibility = accessibilitychecker, accessibilityhelper, phonetic') and save changes.
1. The Phonetic button for Atto should now be installed and will appear on all rich text input windows throughout the Moodle site.

## Usage:

1. On a rich text input window on the Moodle site, navigate the cursor to the position at which you would like your content to be inserted and click the Phonetic button (the button that sorta looks like a dz and is after the accessibility checker and/or the screen reader buttons). 
1. A modal window will pop up and from there you can choose the symbol you need.
1. After selecting a symbol click on the "Save Phonetic" button to insert the symbol.

## Making changes to the code:

Any changes to the plugin code within 'button.js' must be processed using Grunt Shifter, documentation found at https://docs.moodle.org/dev/Grunt. To use Grunt Shifter please follow the following steps:

1. Install Node.js and npm.
1. Open a terminal and install Grunt `npm install -g grunt`.
1. Navigate the terminal to the root directory of the project.
1. Run `npm install`, this will install all dependencies needed for the grunt shifter command. 
1. After making any changes to button.js open a terminal to the root of the project directory and run 'grunt shifter -v'. -v allows error logs to show for any issues.  
1. Increment the version in version.php by 1 (e.g. change 2020061000 to 2020061001)
1. Add everything except the .git and node_modules folder to a zip archive
1. Treat the zip archive as a new release and follow the installation instructions above. As long as the version is higher than the currently installed version an update should trigger.