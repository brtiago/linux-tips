# How to hold packages on linux

> There are different ways of holding back packages: with dpkg, apt, dselect, aptitude or Synaptic.

> _Ler em:_ [_Português_](README.pt-BR.md).

1. **dpkg**
- Put a package on hold:
```
echo "<package-name> hold" | sudo dpkg --set-selections
```

- Remove the hold:
```
echo "<package-name> install" | sudo dpkg --set-selections
```

- Display the status of all your packages:
```
dpkg --get-selections
```

- Display the status of a single package:
```
dpkg --get-selections <package-name>
```

- Show all packages on hold:
```
dpkg --get-selections | grep "+//0<hold$"
```

2. **apt**
- Hold a package:
```
sudo apt-mark hold <package-name>
```

- Remove the hold:
```
sudo apt-mark unhold <package-name>
```

- Show all packages on hold:
```
sudo apt-mark showhold
```