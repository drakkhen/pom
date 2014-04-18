pom
===

Command line pomodoro timer.

This is primarily to show the timer in my tmux statusbar.


Installation
------------

Copy `pom` somewhere in your $PATH, e.g. ~/bin.


Commands
--------

- `pom server`: start up the pom server that will keep track of the timer
- `pom start`: start a pomodoro of 25 minutes
- `pom pause`: pause the current pomodoro
- `pom stop`: stop the current pomodoro
- `pom shutdown`: shutdown the pom server
- `pom status`: information about the current pomodoro
- `pom tmux`: output suitable for the tmux status bar


Tmux Integration
----------------

Sample .tmux.conf bindings:

`bind m run 'pom stop'`
`bind v run 'pom pause'`
`bind b run 'pom start'`

Status bar integration:

`set -g status-right "#(pom tmux)"`

If you add pom to your status bar, you might want to increase its update rate:

`set -g status-interval 1`

