# Brighter Wisplight

Valheim mod (BepInEx) that makes the Wisplight actually light your way:
configurable brightness and range. Light only — the fog is untouched.

- Download: [Thunderstore](https://thunderstore.io/c/valheim/p/TaKeShI/BrighterWisplight/)
- What it does, options and screenshots: [`thunderstore/README.md`](thunderstore/README.md)
- Changes: [`thunderstore/CHANGELOG.md`](thunderstore/CHANGELOG.md)

## Build

Requires the .NET SDK (any recent one; the mod targets `net472`) and Valheim
installed.

```powershell
dotnet build -c Debug     # builds and copies the dll to the mod manager profile
dotnet build -c Release   # builds dist/BrighterWisplight-<version>.zip for Thunderstore
```

The game folder is detected on the usual Steam paths. If yours is elsewhere,
copy `Environment.props.example` to `Environment.props` (ignored by git) and set
`ValheimDir` and `ModDeployDir`.

## Release

1. Bump `<Version>` in `BrighterWisplight.csproj` and `version_number` in
   `thunderstore/manifest.json` (same number).
2. Add the entry to `thunderstore/CHANGELOG.md`.
3. `dotnet build -c Release` and upload `dist/BrighterWisplight-<version>.zip`
   on Thunderstore.
