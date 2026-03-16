# El Viaje de Juan

Projet **Unity** (jeu 2D) : *El Viaje de Juan*.

Le joueur contrôle Juan à travers plusieurs **tableaux / niveaux**. L’objectif est d’atteindre la **ligne d’arrivée** en évitant des obstacles (murs/objets mobiles, rotations, etc.).  
Le jeu affiche un **HUD** (morts, niveau, temps, collectibles) et propose un **menu** avec les règles et les crédits.

## Fonctionnalités principales

- **Menu titre** (`TitleMenu`)
  - Accès aux **Règles** et **Crédits** (navigation par clic)
- **Gameplay**
  - Déplacement du joueur (script `PlayerManager`)
  - **Téléportation** entre tableaux/niveaux (`Teleport` + `TableauManager`)
  - **Collectibles** (ex: compteur de "flammes")
  - **Chronomètre** + **compteur de morts**
  - **Fin de niveau/jeu** via une `FinishLine` (retour au menu après quelques secondes)
- **Obstacles**
  - Déplacements verticaux, boucles, murs animés (`VerticalMove`, `VerticalMoveLoop`, `RedWall`, etc.)
  - Rotations avec pause/angle (`Rotation`)
  - Effets visuels (opacité selon distance : `OpaqueNext`)

## Structure du projet

- `Assets/Scenes/` : scènes Unity (ex: `TitleMenu`, `SceneTest`, etc.)
- `Assets/Scripts/`
  - `Core/` : scripts principaux (joueur, HUD, téléportation, fin de jeu…)
  - `Menu/` : scripts de menu
  - `ObstacleBehaviours/` : comportements des obstacles
- `Assets/Audio/` : musiques/bruitages
- `Assets/Graphics/` : sprites/éléments visuels
- `Assets/Prefabs/` : prefabs Unity

## Installation / Lancement (Unity)

1. Cloner le repo :
   ```bash
   git clone https://github.com/Lucas33860/el-viaje-de-juan.git
   ```
2. Ouvrir le projet avec **Unity Hub** (version Unity à adapter selon le projet).
3. Ouvrir la scène `Assets/Scenes/TitleMenu.unity`.
4. Lancer avec **Play**.

## Contrôles

Les contrôles exacts dépendent de la configuration dans Unity (Input Manager).  
Le projet contient un script `PlayerManager` qui gère le mouvement et certaines mécaniques (freeze / dash, etc.).

## Crédits

Voir le menu “Crédits” dans le jeu (scène titre).

## Licence

Aucune licence n’est définie pour le moment. (Ajouter un fichier LICENSE si besoin.)
