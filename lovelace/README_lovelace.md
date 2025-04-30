# MunnezzAssistant – Dashboard Lovelace

Questa cartella contiene la dashboard e i componenti visivi per integrare MunnezzAssistant in Home Assistant in modo grafico e professionale.

## 📁 Contenuto

- `munnezzassistant_dashboard.yaml`: dashboard completa con layout già pronto
- `munnezzassistant_card_today.yaml`: card animata per il rifiuto del giorno
- `munnezzassistant_card_confirm.yaml`: card per confermare il conferimento
- `munnezzassistant_card_trashbin.yaml`: card con cestino animato (usa immagini esterne)
- `munnezzassistant_light_theme.yaml`: tema chiaro ispirato allo stile MunnezzAssistant

## 🛠️ Istruzioni

### 1. Copia i file nella tua cartella Home Assistant:

- YAML: `/config/lovelace/`
- Immagini: `/config/www/munnezzassistant/`

### 2. Aggiungi le immagini cestino in `/www/munnezzassistant/`:

- `cestino_vuoto.png`
- `cestino_pieno.png`

Oppure usa URL pubblici da GitHub Pages:
```
https://vesuviocode.github.io/munnezzassistant-site/lovelace_assets/images/cestino_vuoto.png
```

### 3. Importa la dashboard

Vai in:  
**Impostazioni > Dashboard > Aggiungi dashboard > 3 puntini > Modifica in YAML**

Incolla il contenuto di `munnezzassistant_dashboard.yaml`

### 4. Attiva il tema (opzionale)

- Copia `munnezzassistant_light_theme.yaml` in `/config/themes/`
- Aggiungi nel `configuration.yaml`:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

- Riavvia Home Assistant
- Vai in **Impostazioni > Aspetto > Tema** e scegli `munnezzassistant_light`

## 🔄 Requisiti

- Home Assistant 2024.12.0 o superiore
- Componenti: `input_boolean.rifiuto_confermato`, `sensor.rifiuto_oggi`