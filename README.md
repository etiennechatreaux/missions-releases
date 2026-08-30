# Missions — releases

Binaires et flux de mise à jour de **Missions**, une palette de tâches flottante pour
macOS. Le code source vit dans un dépôt privé ; ici on ne trouve que ce que l'app
et son site ont besoin de lire publiquement.

**→ [Page de téléchargement](https://etiennechatreaux.github.io/missions-releases/)**

- `index.html` — la page de téléchargement, servie par GitHub Pages.
- `appcast.xml` — le flux [Sparkle](https://sparkle-project.org) que l'app
  interroge pour savoir si une version plus récente existe.
- [Releases](../../releases) — les `.dmg` signés Developer ID et notarisés par
  Apple. Chaque release porte le même fichier deux fois : `Missions-<build>.dmg`,
  que l'appcast vise nommément, et `Missions.dmg`, dont le nom ne change jamais —
  c'est lui qui rend l'adresse
  [`releases/latest/download/Missions.dmg`](../../releases/latest/download/Missions.dmg)
  stable.

## Installation

Télécharge le `.dmg` de la dernière release, glisse **Missions** dans
**Applications**, puis lance-la. Un écran d'accueil explique le raccourci et la
permission au premier démarrage.

**macOS 26 ou plus récent.** L'app est notarisée par Apple : elle s'ouvre sans
avertissement de sécurité.

## Ce que fait l'app

- **Une palette flottante**, appelée par **⌥ droite + ⌘ droite** depuis n'importe
  quelle app. Elle suit tous les bureaux et ne vole jamais le focus.
- **Des listes configurables**, un onglet chacune, plus un onglet *Aujourd'hui* :
  ce qui y est coché disparaît au changement de jour, ce qui ne l'est pas reste.
- **Un mode Focus** : une tâche peut ouvrir une session pendant laquelle les apps
  que tu n'as pas autorisées sont **recouvertes d'un voile** dès qu'elles passent
  au premier plan. Rien n'est jamais fermé ni quitté, et le voile se lève avec la
  session.

## Permission

Missions demande la permission **Accessibilité**, et rien d'autre : macOS ne
laisse entendre un raccourci global qu'aux apps autorisées. Refusée, l'app reste
utilisable — le raccourci ne marche alors que quand la palette a déjà le focus, et
un clic sur l'icône du Dock la ramène toujours.

## Mises à jour

Automatiques, depuis l'app : elle lit `appcast.xml` et propose la version plus
récente quand il y en a une. Rien n'est installé sans ton accord.

## Données

Tout est local, dans `~/Library/Application Support/Missions` — pas de compte, pas
de serveur, aucune statistique d'usage. Pour désinstaller : jeter
`Missions.app` à la corbeille et supprimer ce dossier.

## Un problème ?

[Ouvre un ticket](../../issues) — c'est ici que le support se passe, le dépôt du
code étant privé.
