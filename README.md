# Custom Shutdown Options in i3wm Configuration

If you're an i3 user and want to easily set up personalized shortcuts for logout, reboot, and shutdown, here's a simple code snippet to add to your i3wm configuration file.

## Configuration File Location

The i3wm configuration file is typically located at:

```bash
/home/_your_host_name/.config/i3/config
```

You can edit this file using any text editor of your choice.

## Code Snippet

Add the following lines to your i3 configuration file:

```bash
# Customized shutdown options
bindsym $Your_custom_shortcut mode "exit: [l]ogout, [r]eboot, [s]hutdown"

mode "exit: [l]ogout, [r]eboot, [s]hutdown" {
  bindsym l exec i3-msg exit
  bindsym r exec systemctl reboot
  bindsym s exec systemctl poweroff
  bindsym Escape mode "default"
  bindsym Return mode "default"
}
```

Replace `$Your_custom_shortcut` with the key combination you want to use for accessing the shutdown options.

## Example Usage

For instance, if you want to use `Mod+x` as your shortcut, replace `$Your_custom_shortcut` with `$mod+x`:

```bash
bindsym $mod+x mode "exit: [l]ogout, [r]eboot, [s]hutdown"
```

Now, when you press `Mod+x`, a menu will appear with options to logout (`l`), reboot (`r`), and shutdown (`s`). You can customize this according to your preferences.

Remember to save the file and restart i3wm (or reload the configuration) for the changes to take effect:

```bash
i3-msg reload
```

Now, you have an easy and user-friendly way to perform these system actions in i3wm.