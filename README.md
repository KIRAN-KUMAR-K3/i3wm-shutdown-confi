# i3wm-shutdown-confi
#This config file is to be used only in i3wm for shutdown,reboot,and logout option
# i3wm-shutdown-options
> This is feature is for all the i3 users who have been struggling to set up customised shortcuts for shutdown,login and reboot options
The snippet of code can be found down.<br>
```bash
#bindsym $mod+x mode "exit: [l]ogout, [r]eboot, [s]hutdown"<br>
mode "exit: [l]ogout, [r]eboot, [s]hutdown" {<br>
<br>
  bindsym l exec i3-msg exit<br>
  bindsym r exec systemctl reboot<br>
  bindsym s exec systemctl poweroff<br>
  bindsym Escape mode "default"<br>
  bindsym Return mode "default"<br>
}<br>
bindsym $mod+x mode "exit: [l]ogout, [r]eboot, [s]hutdown" <br>

```




> This is code of snippet for setting up the shortcuts,update the above code using the config file of i3wm.<br>
> The path for the config file of i3wm is <br>

```bash
/home/_your_host_name/.config/i3/config  
```

> Using any text editor you can edit the config file. 
# If you need to set up customised shortcuts <br>

```bash
bindsym $Your_custom_shortcut exec command_name  
```