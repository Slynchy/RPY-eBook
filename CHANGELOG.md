#RPY-PDF Changelog

#### v1.2.0
- Replaced chapter/act dividers with '\f' (page break)
	* This does not work with .txt->Kindle, but works with .txt->MSWord->MOBI->Kindle
- Added unknown character name detection
	* For when the character's name matches this pattern: 
		+ "Unknown" "This is speech."
	* Works with Katawa Shoujo script, not sure about other RPY scripts
- Lua implementation
	* Doesn't do anything yet
- Debug function examples (see DebugStrings.cpp)

#### v1.1.0
- Commenced support for KEY game script (e.g. Clannad)
	* By no means complete; has some weird bugs
- Added some samples
	* NOTE: These samples do not contain copyrighted content and are not intended for use with the tool but only to see how the tool can be used on existing scripts.
- Need to add support for $X functions in RPY script (e.g. note text)
- Maybe add a "straight to MS Word" mode, which automatically inserts ^m (new page) for chapter changes and formats titles?


#### v1.0.0
- Cleaned up the code, added comments
- Can now output chapter names if formatted correctly in "chapternames.txt"

#### v0.8.0
- Added better chapter recognition
- Added (but commented-out) support for chapter naming from "chapternames.txt"
- Many fixes/tweaks:
	* Everything is in unicode now
	* Added to_wstring and to_string functions
	* Added error-checking to file loading.
	* More that I've forgotten

#### v0.7.0
- Removed PDF support
	* Tough decision, but it makes the program much easier to compile, doesn't require any external libs, and the outputted PDFs didn't work anyway.
- Now outputs a .txt file for further formatting.
	* As well as another .txt file containing all the "garbage" strings, so you can see if strings were removed when they shouldn't be.
- Bug/Todo list:
	* Needs a configurable chapter/act divider?
	* Try compiling to Linux

#### v0.6.0
- Added unicode support
	* Still dislikes ellipses, but accentuations work now.
- Can now output to .TXT as well as .PDF
- PDF support complete and will be unsupported in future versions.
	* This is because I started this project to read RPY games on Kindle, but PDF doesn't work well on Kindle for non-graphical content.
- Software now entirely customizable via configurable text files.
- Bug list:
	* No distinguishment between scenes/chapters
	* Haven't checked to see what strings are removed, in case some important ones are.

#### v0.5.0
- First commit
- Bug list:
	* No configuration possible to the page layout
		+ i.e. still has hard-coded fonts, etc.
	* Probably more; can't remember.