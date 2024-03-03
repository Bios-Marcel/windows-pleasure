
## Disable language switching on Ctrl + Shift

I often switch languages by accident, since I have both german and english installed.

1.  Press **Windows Logo key + I**, to open **Settings**.
2.  Click on **Devices** and select **Typing** on the left pane.
3.  Scroll down and select **Advanced keyboard settings**.
4.  Click on **Input language hot keys.**
5.  Select the layout for which you have assigned the shortcut and click on **Change Key Sequence**.
6.  Under **Switch Keyboard Layout**, select **Not assigned**.
7.  Click on OK (Twice).

## Disable web search in start menu

Web search impacts performance, as the startmenu sometimes doesn't respond at all or even shows web results when local results would've been correct.

1. Open group policy editor
2. Navigate to `User Configuration > Administrative Templates > Windows Components > File Explorer`
3. Enable `Turn off display of recent search entries in the File Explorer search box`

There is no separate setting for web results. Classic Windows moment.

## Change default keyboard layout

Since I mainly use the laptop as a desktop, where I have a german keyboard layout, I changed the default.

1. Open `Advanced Keyboard Settings`.
2. Change preferred default layout.

## Disable Annoyance On Boot

Windows 11 thinks it's funny to force you to "finish setting up your system" every once in a while.
Meaning instead of letting you boot, it shows you a modal wizard where they try to sell you bullshit.

Settings > System > Notifications > Additional Settings > Remove All Checkmarks

## Pre-Win11 Context Menu

`.reg` to disable new menu:

```reg
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}]
@=""

[HKEY_CURRENT_USER\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32]
@=""
```

To undo:

```reg
Windows Registry Editor Version 5.00

[-HKEY_CURRENT_USER\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}]
```

## Powershell Autocomplete

```powershell
echo "# Shows navigable menu of all options when hitting Tab" >> $PROFILE.CurrentUserAllHosts
echo "Set-PSReadlineKeyHandler -Key Tab -Function MenuComplete" >> $PROFILE.CurrentUserAllHosts
```
## Disable double quote insertion

Time & Language -> Language & Region -> Choose Language -> Replace INTL layout with normal one

## Fix Win+Tab Sluggishnes

Windows, being the magnificient piece of trash that it is, can't render your
desktop background fast enough, so you need to set a solid as your background
color.

https://superuser.com/questions/1810772/windows-11-desktop-switching-is-slow-since-latest-update


