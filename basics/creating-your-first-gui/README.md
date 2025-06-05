---
description: In this guide, you will be taught how to create your first GUI
---

# 🌇 Creating your first GUI

## Important

The only thing you need for a GUI to work is the `id` and the `title` .

#### Example:

```yaml
id: myfirstgui
title: My very first GUI using NotionMenus
```

This creates a simple GUI with the ID "myfirstgui" and title "My very first GUI using NotionMenus"

this gui will have 54 slots and will only be accessible using the command `/nm gui myfirstgui YourName`&#x20;

#### But how do I add a command to open it?

To add a command for opening the GUI you simply add a command field with either a single command, or multiple. Like this:

```yaml
id: guiwithcommand
title: My cool GUI with a command
command: guicommand
# or for multiple commands you'd do:
# command:
# - firstcommand
# - secondcommand
```

To open this gui, you'd either run the nm command as before, or this time just `/guicommand`&#x20;

#### What if I wanna change the size of the GUI?

Changing the size of your is very simple actually, you just need to add it like this:

```yaml
id: sizedgui
title: A GUI with 18 slots
size: 18 # this number can be anything from 9-54 with increments of 9 [9, 18, ..., 54]
```

This will make the GUI have 18 slots, aka 2 rows

Sadly because of minecraft limitations, this is onlly possible from 9 (1 row) to 54 (6 rows) in increments of 9

#### How would I let people move items in their inventory?

You can also make players be able to move items in their inventory, but not into the gui

to do this, you simply add a `lock-inventory: false`, like this:

```yaml
id: moveitems
title: Gui where you can rearrange your inventory
lock-inventory: false # this is set to true by default, meaning players can't move items
```

