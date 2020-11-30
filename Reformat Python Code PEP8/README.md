# Batch file to reformat Python Script as (PEP8) in Notepad++
### This procedure will creates a menu item in Notepad++ to format Python file as PEP8.

## Requirement
1. Python installed
2. Install https://pypi.org/project/autopep8/
    
    > pip install --upgrade autopep8

## Steps to add menu item to Notepad++
1.  Install autopep8 
        > pip install --upgrade autopep8

2.  Create text file, named autopep8.bat, save file any where, say at :-
        C:\my_bat_files\autopep8.bat
    
3.  Add the following text in autopep8

    path=C:\<your_python_path>\Scripts;C:\<your_python_path>\
    C:\<your_python_path>\Scripts\autopep8 --in-place --aggressive --aggressive %1
    pause
    
4. In Notepad++, select Menu - Run.

5. Dialog box will be shown, type in Program to Run :-
    C:\my_bat_files\autopep8.bat "$(FULL_CURRENT_PATH)"

6. Click Save, in Name text box type "PEP8", then click OK.

7. Open Python file, then to re-formatted, select Run - PEP8

