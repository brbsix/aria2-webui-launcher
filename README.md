This is a launcher script for the [Aria2 WebUI](https://github.com/ziahamza/webui-aria2).

It launches the aria2 server in a `xfce4-terminal` window. The WebUI is launched via Chrome's kiosk mode in it's own profile (user directory) so as to not interfere with normal browsing. The aria2 server and WebUI communicate via RPC. A secret token is generated and configured upon each launch.

## Prerequisites

This assumes you have aria2 and Google's Chrome web browser installed. Error messages are displayed via `zenity` (assuming a TTY is not detected as would be the case when it is launched from an application window). `xfce4-terminal` is also required, though this can easily be changed by adjusting the `TERMINAL` value in the script.

## Installation

1. Clone the Aria2 WebUI into the desired installation directory:

        git clone https://github.com/ziahamza/webui-aria2.git

2. Copy the `aria2-webui` launcher script into the same directory as Aria2 WebUI

3. Copy `aria2-webui.desktop` into the appropriate directory, generally `~/.local/share/applications`

4. Create a symlink to `aria2-webui` in your PATH. For example:

        ln -s ~/Applications/aria2-webui/aria2-webui ~/.local/bin/

5. Launch it from your application menu!
