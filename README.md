# Minimo Releases

Ce repository public distribue les binaires de Minimo et le manifest de mise a jour signe.

## Source de verite mise a jour

URL stable consommee par l'app:

- https://github.com/Sillapps/minimo-releases/releases/latest/download/update-manifest.json

Le manifest doit contenir au minimum:

- `latest`
- `download_urls.windows`
- `download_urls.macos`
- `signature_alg` (ed25519)
- `signature`

Optionnel:

- `notes_url`
- `signed_payload`

## Contrat de release

Chaque release doit inclure:

- `Minimo-x.y.z-Windows-Setup.exe` (ou fallback `.zip`)
- `Minimo-x.y.z-macOS.dmg`
- `SHA256SUMS.txt`
- `update-manifest.json`

## Verification integrite (recommande)

Exemple Windows (PowerShell):

```powershell
Get-FileHash .\Minimo-x.y.z-Windows-Setup.exe -Algorithm SHA256
```

Exemple macOS:

```bash
shasum -a 256 Minimo-x.y.z-macOS.dmg
```

Le hash calcule localement doit correspondre a la ligne du fichier `SHA256SUMS.txt`.

## Notes

- Le code source de l'application n'est pas dans ce repository.
- Les binaires restent publics; l'integrite du check de version repose sur la signature Ed25519 du manifest.
