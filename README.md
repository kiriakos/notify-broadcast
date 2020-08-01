# Broadcast desktop notifications via notify-send and dbus

`notify-broadcast` can send broadcst notifications via `notify-send` to all 
users on a desktop session

It utilizes `notify-send` and DBUS for this.

## Installation

Just copy the notify-broadcast into root's path.

## Usage

`notify-broadcast` is a wrapper around `notify-send` and passes arguments 
trasparently to itso it can be used  options
```
# notify-broadcast MESSAGE

# ./notify-broadcast 
./notify-broadcast needs at least a message.
For a full API description see notify-send
Usage:
  notify-broadcast [OPTION…] <SUMMARY> [BODY] - create a notification

Help Options:
  -?, --help                        Show help options

Application Options:
  -u, --urgency=LEVEL               Specifies the urgency level (low, normal, critical).
  -t, --expire-time=TIME            Specifies the timeout in milliseconds at which to expire the notification.
  -a, --app-name=APP_NAME           Specifies the app name for the icon
  -i, --icon=ICON[,ICON...]         Specifies an icon filename or stock icon to display.
  -c, --category=TYPE[,TYPE...]     Specifies the notification category.
  -h, --hint=TYPE:NAME:VALUE        Specifies basic extra data to pass. Valid types are int, double, string and byte.
  -v, --version                     Version of the package.


```

## Dependencies

The script is dependent on DBUS and the system having notify-send and a desktop
environment.

The used executables are `sed`, `who`, `cut`, `xargs`, `strings`, `grep` and of course `notify-send`

## Packages

AUR: tbd
