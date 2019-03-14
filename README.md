# FileConvert
Quickly and easily convert between filetypes on macOS using the CloudConvert service

Created by Arjun Barrett

Contact arjunbarrett@gmail.com for any inquiries.




PRE-REQUISITES

Install XCode Command Line Tools (CLT) by running the command `xcode-select —-install` in the Terminal. Simply running the .app installer should install all other necessary components.




INSTALLATION

Use the installer.




DOCUMENTATION

The app will ask you for arguments. Separate arguments with the space key. There are two modes - auto and standard. No need to designate that it’s standard mode; simply type in a filepath as your first argument (surround the path with quotes if there are any spaces). Your second argument should be the desired filetype. for example, type


mp3


to designate that you want to convert to mp3. The service supports hundreds of file extensions. If you try something silly, like converting a .pdf file to .aiff, FileConvert should throw an error. Your third argument is optional, but is the file download path. If none is provided, the new file is placed in the same directory as the old one. The old file is moved to Trash, but not deleted, after every run. This functionality can be customized in the python code.


If you want to use auto mode, put auto as your first argument. It will parse your Downloads directory for the most recently created file. If there is nothing there, it will check for a directory named Convert on your desktop. If it exists, and there are files inside, it will convert the most recently created file. Your second argument is, again, the desired filetype. Third argument is the optional file download path. Old file is moved to Trash.


I added my own custom mode, spanishconvert, in the python code. I use it all the time when my Spanish instructor gives me horrific file formats. Feel free to replace it with whatever you would like - it essentially runs auto mode but also moves the file to the directory of your choice and opens it.




TWEAKING

If you want to fiddle with the code, open the application in Automator. (P.S. Extremely sorry I forgot to add comments! The shell script is pretty straightforward but the Python code is a mess.)




UNINSTALLATION

Paste the following into Terminal:

rm -r /Applications/FileConvert.app && rm -r /Applications/.CloudConvertFiles | true



That's it!




THANK YOU
for taking the time to read this wall of text. I rarely read READMEs so I congratulate you. Have fun with the application!
