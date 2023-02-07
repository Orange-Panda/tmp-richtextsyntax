# Text Mesh Pro Rich Text Syntax Highlighter for Visual Studio Code

This Visual Studio Code Extension will highlight Text Mesh Pro [Rich Text](http://digitalnativestudios.com/textmeshpro/docs/rich-text/) to make writing text files used in the Unity Engine more legible at a glance.

## TODO: Features

TODO: There will be an animation of typing out rich text and it highlighting here

## TODO: Extension Settings

Include VS Code settings through the `contributes.configuration` extension point.

This extension contributes the following settings:

* `myExtension.enable`: Enable/disable this extension.
* `myExtension.thing`: Set to `blah` to do something.

## Known Issues
-

## Limitations
- By design the extension ends continuous tags when a newline begins. This is because some files are read and displayed line by line without the expectation for closing tags to be used.
	- You may opt to use the `<br>` tag to keep it all on one line if your text is not very long
	- This may become a preference in the future if it is possible.
- Starting a continuous Tag "A" then starting a continuous Tag "B" means that tag "A" can't be closed until tag "B" is closed.
	- Example: `<b>bold <i>bold and italic</b> italic</i>` will fail to close the bold tag because it was busy in the italics tag
	- This is occurs *only* in the code editor and TextMeshPro will render the text as expected.