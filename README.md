# Missions — releases

Binaires et flux de mise à jour de **Missions**, une palette todo flottante pour
macOS. Le code source vit dans un dépôt privé ; ici on ne trouve que ce que
l'app a besoin de lire publiquement.

- `appcast.xml` — le flux [Sparkle](https://sparkle-project.org) que l'app
  interroge pour savoir si une version plus récente existe.
- [Releases](../../releases) — les `.dmg` signés Developer ID et notarisés par
  Apple.

## Installation

Télécharge le `.dmg` de la dernière release, glisse **Missions** dans
**Applications**, puis lance-la. Au premier démarrage macOS demandera la
permission **Accessibilité** (Réglages Système → Confidentialité et sécurité →
Accessibilité) : elle est nécessaire au raccourci global ⌥ droite + ⌘ droite,
qui affiche et masque la palette.

Les mises à jour suivantes se font toutes seules depuis l'app.
