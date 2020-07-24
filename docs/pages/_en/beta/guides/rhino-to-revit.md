---
title: Rhino Geometry to Revit
order: 21
---

{% include ltr/en/wip_note.html %}

In this guide we will take a look at how to send Rhino geometry to Revit using Grasshopper. {{ site.terms.rir }} allows Rhino shapes and forms to be encoded into structured Revit elements.  It is important to note that the easiest and quickest way of moving geometry into Revit may not be the best method. Determining which the final goal of the forms in Revit can improve the quality of the final Revit data structure and improve project efficiency.

### Rhino objects as DirectShapes

This is the most obvious and many times the easiest way to get Geometry from Rhino into Revit. It is where everyone starts. But only in very specific situations is it ever the best.  For instance good reasons for Directshapes might be:
1. Temporary models for quick printing for a competition submission
1. Placeholders for part of the building that is still changing during design development.  For instance while the floor plates might be done, the facade might be in flux in Grasshopper.  Using a directshape as a placeholder may be right.
1. A completely bespoke component or assembly that cannot be modeled using Revit native Families.

{% include youtube_player.html id="7kNYSJ3kdqw" %}

### Rhino objects as Loadable Families

Revit defines loadable families as:
* Building components that would usually be purchased, delivered, and installed in and around a building, such as windows, doors, casework, fixtures, furniture, and planting
* System components that would usually be purchased, delivered, and installed in and around a building, such as boilers, water heaters, air handlers, and plumbing fixtures
* Some annotation elements that are routinely customized, such as symbols and title blocks

Wrapping Rhino gemoetry inside Loadable Families have many advantages:
* Repeated objects can be inserted mutiple times allowing forms to be scheduled and counted correctly
* Forms in loadable families can be edited by Revit if needed.

### Using Revit built-in System Families

Trying to work within Categories of objects whic include built-in Revit systems Families such as Walls, Floors, Ceiling and Roofs can take the most amount of thought.
