This document provides a summary of the available commands in the ValorVDC BIMTools Revit add-in.

---

## Commands

### Align Branches (Pipe, Duct, Fab Parts)
Aligns one or more branch pipes with a selected main pipe. 

### Copy Scope Boxes
Copies selected scope boxes from the current project to other open projects, simplifying the process of standardizing views.

### Copy Parameters
Copies shared Parameter from a Linked Project.

### Create Riser Pipe (Pipe Only)
Allows for the creation of a vertical pipe riser between two points, automatically handling connections.
Works only with Revit Native Pipe Families at the moment. Not Fabrication Pipe at the moment or Ducts.

### Disconnect Pipe (Pipe Only, No Fab Parts)
Disconnects a selected pipe/duct from its connected fittings or equipment.

### Fix Skewed Pipe (Pipe Only, No Fab Parts)
Corrects pipes that are drawn at a slight, unintended angle, realigning them to the nearest orthogonal or 45-degree axis.

### Floor Sleeve Round (Pipe, Duct, Fab Parts)
Places round sleeves in floors where pipes, ducts, or conduits penetrate them. It can place a single sleeve or multiple sleeves based on floor selection.

### Flow Arrow (Pipe, Duct, Fab Parts)
Manages the visibility and direction of flow arrows on duct and pipe systems to indicate the direction of flow.

### Realign Element Pipe, Duct, Fab Parts)
Realigns a single selected element (like a pipe or duct) to the nearest cardinal axis (horizontal or vertical).

### Realign Multi Elements (Pipe, Duct, Fab Parts)
Realigns multiple selected elements to the nearest cardinal axis.

### Specify Length (Pipe, Duct, Fab Parts)
Allows the user to input a specific length and apply it to a selected pipe or duct segment.

### Wall Sleeve Rectangular (Duct, Fab Duct)
Places rectangular sleeves in walls for duct or other rectangular MEP penetrations.

### Wall Sleeve Round (Pipe, Duct, Fab Parts)
Places round sleeves in walls for pipe or other round MEP penetrations.

### Zoom Object
Zooms the current view to fit the selected element(s) on the screen.


***---Known Issues ---***

Disconnect Element - will sometimes delete the installation and then disconnect the pipe

Align MEP elements - will connect to an open connector, but sometimes create another copy of the pipe. Usually, all you have to do is select a pipe and delete it. Additionally, if the connector is below or to the right of the element, it's connecting to weird things can happen. Just “Undo" the command and move whatever you're trying to connect to the left of the element or on top of it in a section view.

Extend and connect -  will work as long as the end of the pipe you're extending is not at or past the fitting you're connected to. Also, this is mostly designed for pipes that are already perfectly aligned, and you're having trouble making a final connection.

Place floor sleeves by floor- has an issue if you copied the floor from a linked model, not sure why this is happening. The floor is the floor, but I am working on it. It still works perfectly if you place them one by one; you just can't place them on the floor just yet.

Optimize segments - does work except sometimes on slope pipe, which will cause an undesirable condition of re-sloping the pipes at an extreme angle. I am currently investigating this first and have been for the last week or so, trying to figure out why it is doing this and how to resolve it. But for the most part, if the pipe is not slowed, it works perfectly.

