# nol.csv

Encodage / décodage CSV (RFC 4180) en pur [Nolc](https://noliae-nolc.s3.gra.io.cloud.ovh.net/nolc-latest-linux-x86_64.tar.gz), sans dépendance.

## Installation

```toml
[dependances]
"nol-csv" = { git = "https://github.com/Noliae-France/nol-csv" }
```

## API

- Encodage (complet, conforme) : `csv_echappe(v)`, `csv_ligne(champs)`, `csv_document(lignes)` — guillemets quand nécessaire, guillemets internes doublés, terminaison `\r\n`.
- Décodage : `csv_analyse_ligne_simple(ligne)` (champs non guillemetés).

```nol
var champs: List<Text> = []
push(champs, "nom")
push(champs, "ville, pays")
csv_ligne(champs)          // => nom,"ville, pays"
```

## Feuille de route
- Décodage des champs guillemetés et multi-lignes (parseur à états)

## Licence

MIT © 2026 Bastien LANGUEDOC.
