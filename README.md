# EnglishHanZi
A custom input method schema for writing and learning English with Chinese ideograms.
Version 0.16

# Overview

English Hanzi is a user-defined schema that enables users to type in English and converts their input into Chinese characters.

# Installation
	1. Ensure you have Rime installed on your system.
	- If not, download from the Rime website or use commands.
		- For Linux/Ubuntu users use:
			sudo apt update
			sudo apt install ibus-rime
		- For Linux/Fedora users use:
			sudo dnf update
		sudo dnf install ibus-rime
		
	2. Restart IBus:
	ibus-daemon -drx
	or
	ibus restart
	
	3. Open IBus setup
	ibus-setup
	
	4. Go to the Input Method tab, click Add, and select Rime from the list.
	
	5. Deploy the Schema:
		Copy the two files "english.dict.yaml" and "english.schema.yaml" to Linux: ~/.config/ibus/rime/ or Windows: %APPDATA%\Rime\ or MacOS: ~/Library/Rime/
		In "default.custom.yaml" insert "- schema: english" just under "- schema: luna_pinyin" and make thus a comment "#    - schema: luna_pinyin".
			The result must be like this:
			  schema_list:
			#    - schema: luna_pinyin
			    - schema: english
		In "default.yaml" insert "  - schema: english"
			The result must be like this:
			schema_list:
			  - schema: luna_pinyin
			  (... other schema ...)
			  - schema: english
			  
	6. Deploy IBus
	ibus-daemon -drx   
	or
	ibus restart
	
	7. In Linux/Ubuntu go to Settings / Keyboard / + Add Input Source and choose Chinese (Rime) from the list.
	Now you can switch through your keyboard layouts and/or input methods using Super+Space or any other key combination you have.



Contact
For questions or feedback, please open an issue on the GitHub Issues page or write to me on eurasianlink@yandex.com

