# How to implement the IncrementalBackColor and IncrementalForeColor properties


<p>When a user performs an incremental search within the XtraGrid, the colors used to highlight the matching text are obtained from the current skin. It's possible to create your own skin and provide your own background and foreground colors. If you don't want to create a new skin, you can accomplish this task by creating a descendant to the existing in-place editor and introducing properties allowing you to manually specify these colors. Then create a descendant of the corresponding ViewInfo class and override the GetSystemColor method.</p>


<h3>Description</h3>

<p>Starting from version 10.2, the TextEditPainter.DrawMatchedString method retrieves the appearance for the matching string from the current Skin. Therefore, the code responsible for replacing the default colors with custom ones was moved into the TextEditPainter class.</p>

<br/>


