# Introduction

This repository contains macros I've written for AvsP(mod), because why not. Descriptions for available macros below.

## QuickTrim Begin/Mid/Stop

QuickTrim is a collection of three macros intended to make writing trims faster. You should bind the macros to hotkeys like Ctrl+F1/F2/F3 or whatever (I personally use macro keys on my keyboard). Create a new line, make it a comment with `#` in the beginning and make sure the cursor is located after it. Then, open the video and start going through it. After that...

- Hit Begin when you want to open a trim and the macro will write `Trim(CURRENT_FRAME,`
- Hit Mid and the macro will write `PREVIOUS_FRAME)++Trim(CURRENT_FRAME,`
- Hit Stop and the macro will write `CURRENT_FRAME)++`

The end result is that you will be able to quickly trim a video with just the navigation keys and three hotkeys. After you're done, just uncomment the line and delete the `++` from the end of the line and you should end up with a pretty trim line similar to this example:

```
Trim(2,928)++Trim(929,3624)++Trim(5726,25145)++Trim(26945,43647)++Trim(43648,46004)++Trim(47804,48250)++Trim(48251,48519)
```