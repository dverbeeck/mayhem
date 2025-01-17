# Mayhem 📝

A minimal TUI based task tracker

<a href="./altscreen-toggle/main.go">
  <img src="gifs/Navigation.gif"/>
</a>

<br></br>


<a href="./altscreen-toggle/main.go">
  <img src="gifs/Editing.gif"/>
</a>



## Installation

- You can download a pre-compiled binary for your system for the [latest release](https://github.com/BOTbkcd/mayhem/releases)
- Or if you have go installed on your system you can use the following command to install this package: 

```
go install github.com/BOTbkcd/mayhem@latest
```

*SQLite is a dependency for this tool, make sure it is installed beforehand (it is fairly ubiquitous & should already be present on your system).*




## Features

- Three pane responsive layout, auto adjusts when terminal is resized

- Vim key bindings for navigation

- Tasks:

  - Completion Status:
    - Tasks can be marked finished/unfinished using `Tab` key
    - Each stack has a label which denotes the number of unfinished tasks in that stack
  - A task can be broken down into associated *<u>steps</u>* 
    - Individual steps can be marked as finished as progress is made

  - Task can be moved to a new stack after creation without any loss of data
    
  - Recurring tasks:
    - A recurring task will begin from the specified start time & repeat after the recurrence interval until the deadline is reached
    - A recurring task can only be temporarily marked as finished. It will resurface after the recurrence interval.
    - The deadline can be extended as per requirement
    - They are marked in task table using `📌` icon

- Sorting:

  - Stacks are sorted alphabetically by default
  - Tasks are sorted by completion status, then deadline, then priority & then by title
    - Unscheduled tasks have less precedence than scheduled tasks

- Pane Footer: each pane has a footer which your relative position in the pane

- Dynamic help section at the bottom shows the relevant key bindings available at a given instance

  

## Navigation

| Key                   | Description                        |
| --------------------- | ---------------------------------- |
| <kbd>k or up</kbd>    | Move up                            |
| <kbd>j or down</kbd>  | Move down                          |
| <kbd>l or right</kbd> | Switch focus to the pane on right  |
| <kbd>h or left</kbd>  | Switch focus to the pane on left   |
| <kbd>g</kbd>          | Jump to top of the pane            |
| <kbd>G</kbd>          | Jump to bottom of the pane         |
| <kbd>e</kbd>          | Edit                               |
| <kbd>tab</kbd>        | Toggle task/step completion status |
| <kbd>esc</kbd>        | Return                             |
| <kbd>m</kbd>          | Move task to new stack             |
| <kbd>?</kbd>          | Toggle Help                        |
| <kbd>q</kbd> / <kbd>ctrl+c</kbd>          | Quit                               |

