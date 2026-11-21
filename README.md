# technicalteam774.github.io

Root site for the TechnicalTeam774 apps.

Its main job is `/.well-known/assetlinks.json` — the Digital Asset Links file
Android reads to confirm that an installed app owns this domain. When the check
passes, the app opens without a browser address bar.

## Adding another app

Append one object to the array in `.well-known/assetlinks.json`:

```json
{
  "relation": ["delegate_permission/common.handle_all_urls"],
  "target": {
    "namespace": "android_app",
    "package_name": "io.github.technicalteam774.<app>",
    "sha256_cert_fingerprints": ["<SHA-256 of that app's signing certificate>"]
  }
}
```

Get the fingerprint from the signing keystore:

```
keytool -list -v -keystore <file>.keystore -alias <alias>
```

Never remove an existing entry — each installed app depends on its own.

## Apps

| App | Path | Android package |
|-----|------|-----------------|
| ميزان | `/finance-dashboard/` | `io.github.technicalteam774.mizan` |
| ميعاد | `/miaad/` | — |
| لمّة | `/lamma/` | — |
