# Datos

Los datasets **no se suben a GitHub** (repo público + `.gitignore`). Quedan solo en tu PC.

## Estructura

```
data/
├── raw/          ← datos originales (no commitear)
├── processed/    ← derivados del pipeline (no commitear)
└── README.md     ← este archivo (sí va al repo)
```

## Archivos actuales (`raw/`)

| Archivo | Filas | Descripción |
|---------|------:|-------------|
| `X_val.csv` | ~20.861 | Features de validación (variables `ue_cah_*`) |
| `y_val.csv` | ~20.861 | Target binario (`target`) |

## Uso en Python

```python
from pathlib import Path

DATA = Path("../data/raw")  # desde notebooks/
X_val = pd.read_csv(DATA / "X_val.csv")
y_val = pd.read_csv(DATA / "y_val.csv")
```

## Agregar más archivos

Copiá train/test u otros splits a `data/raw/`:

```bash
cp /ruta/a/tus/archivos/*.csv ~/Projects/dea-comportamental/data/raw/
```

Si tenés `X_train.csv`, `y_train.csv`, etc., decime la ruta y los incorporamos.
