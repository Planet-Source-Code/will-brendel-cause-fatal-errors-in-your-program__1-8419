<div align="center">

## Cause Fatal Errors In Your Program


</div>

### Description

This code just causes those neat little errors Windows sends us every so often. I don't think there's a use for this, but here it is anyway. Just a note, it also closes the VB IDE when called so watch out!
 
### More Info
 
Buttons: cmdFatalAppExit, cmdFatalExit

Crashes VB IDE if called from within the IDE.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Will Brendel](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/will-brendel.md)
**Level**          |Intermediate
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/will-brendel-cause-fatal-errors-in-your-program__1-8419/archive/master.zip)

### API Declarations

```
Private Declare Sub FatalAppExit Lib "kernel32" Alias "FatalAppExitA" (ByVal uAction As Long, ByVal lpMessageText As String)
Private Declare Sub FatalExit Lib "kernel32" (ByVal code As Long)
```


### Source Code

```
Private Sub cmdFatalAppExit_Click()
 FatalAppExit 0, "You can replace this message with one of your own." & vbLf & vbLf & "Multiple lines are allowed too!"
End Sub
Private Sub cmdFatalExit_Click()
 FatalExit 1
End Sub
```

