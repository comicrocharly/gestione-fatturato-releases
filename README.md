# Gestione Fatturato — canale release

Repo pubblico di distribuzione per **Gestione Fatturato** (repo source:
`comicrocharly/gestione-fatturato`).

## Contenuto

Ogni release contiene i binari **firmati** e il manifest `latest.json`:

| File | Uso |
|---|---|
| `Gestione.Fatturato_*.exe` | Installatore Windows 11 (x64) — anche da installare a mano |
| `Gestione.Fatturato_*.exe.sig` | Firma del binario (verificata dall'updater in-app) |
| `Gestione.Fatturato.dmg` | macOS Universal (Apple Silicon + Intel) |
| `Gestione.Fatturato.app.tar.gz` | Bundle per l'updater in-app macOS |
| `Gestione.Fatturato.app.tar.gz.sig` | Firma del bundle |
| `latest.json` | Manifest interrogato dall'app al check di aggiornamento |

## Come si aggiorna l'app

- **Automaticamente**: l'app controlla questo canale all'avvio (una volta
  attivata) e propone l'installazione con "Installa e riavvia".
- **A mano**: scarica il `.exe` (Windows) o il `.dmg` (macOS) della release
  più recente e installa come di consueto.

## Note di sicurezza

I binari sono firmati con una chiave minisign dedicata al canale. La verifica
della firma avviene dentro l'app, al download dell'aggiornamento (mai in
questo repo). Le note di ogni release riportano il changelog completo.
