# Minimo Releases

Ce repository public sert uniquement a distribuer les binaires de Minimo.

## Telechargement

- Windows: [Derniere version](https://github.com/Sillapps/minimo-releases/releases/download/v0.0.11/Minimo-0.0.11-Windows-Setup.exe)
- macOS: [Derniere version](https://github.com/Sillapps/minimo-releases/releases/download/v0.0.11/Minimo-0.0.11-macOS.dmg)

## Verifier l'integrite (recommande)

Chaque release contient un fichier `SHA256SUMS.txt`.

Exemple Windows (PowerShell):

```powershell
Get-FileHash .\Minimo-Windows-Setup.exe -Algorithm SHA256
```

Exemple macOS:

```bash
shasum -a 256 Minimo-macOS.dmg
```

Le hash calcule localement doit correspondre a la ligne du fichier `SHA256SUMS.txt`.

## Notes

- Le code source de l'application n'est pas dans ce repository.
- Les liens sont stables pour permettre la verification de mise a jour dans l'app.
