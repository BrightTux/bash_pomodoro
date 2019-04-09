# Hi there!

This is a simple pomodoro timer scripted using bash.
The bash script loops until the user decides not to restart the timer.

On my setup, i binded this tool to some keyboard shortcut for easy access.
To further simplify it, you could change the zenity tool to just a `notify-send` command.

```
function pomo {

	zenity --info --text="Starting Pomodoro Timer 💯!"
	sleep 1500 && zenity --info --text="⏰ Time to take a break?"
       	sleep 300 && zenity --question --text="Back to work! Restart timer? 🔃" --ok-label="No." --cancel-label="Yes, restart!"

}

pomo
while [ $? -ne 0 ]; do pomo; done
```

# Requirements:
zenity, bash, and probably the glyphs fonts... 


