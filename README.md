# 🎲 hex-tactics

Tactical 1v1 RPG su griglia esagonale. Duello a turni con dadi, slancio, asta nascosta sul movimento e meccaniche di carica/stance.

🎮 **Gioca subito**: <https://valeriodolci.github.io/hex-tactics-play/>

📦 **Sorgente** (privato): `ValerioDolci/hex-tactics` — TypeScript + Phaser 3 + Vite + Python (per training AI)

---

## Concetti chiave

- **Mappa esagonale** 24×14 hex con basette 7-hex per unità
- **Tre risorse** per ogni PG:
  - **Dadi azione** (pool 6→9): si spendono per attacchi/difese/ricariche
  - **Slancio**: mobilità + scudo passivo contro ranged
  - **Impeto**: timing nel round (chi più impeto gioca prima)
- **Architettura tiri** a due componenti: **Variabile** (d6) + **Fissa** (bonus statici). Schivata morde solo la variabile, parata morde il totale.
- **Asta nascosta sul movimento**: per attraversare la zona di reach di un nemico, si fa un'asta in slancio simultanea (mind game puro, niente dadi).
- **Combat hot-seat** o **vs AI** (Easy = Utility heuristic, Hard = Decision Tree distillato da PPO MaskablePPO trained 250k step self-play).

## Compatibilità

- **Desktop**: Chrome, Firefox, Safari (qualsiasi browser moderno)
- **Mobile**: iOS Safari, Android Chrome (touch nativo, viewport responsive Phaser Scale.FIT, UI scale x1.4 su mobile per essere tap-friendly)
- **Fullscreen**: tap sul bottone ⛶ in alto a destra. Su iPhone Safari (no Fullscreen API): usa "Condividi → Aggiungi a Home" per esperienza standalone.
- **Rotazione**: ottimizzato per landscape. In portrait appare un overlay che invita a ruotare il dispositivo.

## Cosa contiene il manuale in-game

13 capitoli completi navigabili dalla home:

1. Cos'è hex-tactics
2. Anatomia di un'unità
3. Round e turno
4. Le tre risorse + transfer impeto→slancio
5. Movimento
6. Architettura del tiro (variabile + fissa)
7. Combattimento mischia
8. Combattimento a distanza (con regola D-049 no-ranged-in-melee)
9. Schivata vs parata
10. Equipaggiamento (con impedimento variabile V2)
11. Skill system (con costi spec /2^N e lv up *2)
12. Meccaniche avanzate (carica, stance, asta zona controllo)
13. Strategie e build (con counter-ranged dettagliato)

## Aggiornamenti

Ogni nuovo build viene pubblicato qui automaticamente via `scripts/deploy_pages.sh` dal repo source.

## Crediti

- Game design: **ValerioDolci** (regole, balance, decisioni architetturali)
- Sviluppo: in collaborazione con Claude (Anthropic) come pair programmer

## Licenza

Free per playtest pubblico. Codice sorgente non disponibile.
