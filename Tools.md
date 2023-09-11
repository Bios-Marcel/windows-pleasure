
List of tools that help me preserve my sanity when on windows.

## Package manager

Using https://scoop.sh seems to be the best call, since `winget` manages to be even slower.

Install:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
irm get.scoop.sh | iex
```

Too also access additional tools, add the extras bucket:

```powershell
scoop bucket add extras
```

The nice thing is, that you can't only get all kinds of unix-y tools, but also graphical tools, even ones such as Teamspeak.

## Git Autocomplete

https://github.com/AnderssonPeter/PowerType

While posh-git is nice, it makes startup painfully slow.
## ShareX

https://github.com/ShareX/ShareX - Screenshots, video recording and more

Also less buggy than windows built-in stuff which cant even properly handle multiscreen / eGPU.

Also available via scoop:

```powershell
scoop install sharex
```
## CLI tool recommends

Install via scoop:

```powershell
scoop install ripgrep gsudo 7zip curl
```

## PowerToys

This is a reboot of an old concept from Microsoft by Microsoft. It contains a multitude of little helper tools, many of which should be part of windows.

https://github.com/microsoft/PowerToys

## Open-Shell-Menu

Brings back the old startmenu, no websearch, no ads, no bullshit.

https://github.com/Open-Shell/Open-Shell-Menu
