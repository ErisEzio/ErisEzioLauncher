<p align="center"><img src="docs/logo.png" width="170" alt="Logo Eris Ezio"></p>

<h1 align="center">Eris Ezio's Launcher</h1>

<p align="center">
🇫🇷 Français · 🇬🇧 <i>English, Deutsch, Italiano, Русский and 日本語 are available in the app.</i>
</p>

<p align="center">
<b>Le shiny hunting multi-fenêtres, en un clic.</b><br>
Ouvre jusqu'à 60 fenêtres d'émulateur, chacune avec sa propre horloge,<br>et range-les automatiquement au pixel près.
</p>

<p align="center">
<img src="https://img.shields.io/badge/version-1.4.0-3c6eb4" alt="Version 1.4.0">
<img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078d6" alt="Windows 10 | 11">
<img src="https://img.shields.io/badge/licence-MIT-2f8a4f" alt="Licence MIT">
<img src="https://img.shields.io/badge/langues-FR%20%7C%20EN%20%7C%20DE%20%7C%20IT%20%7C%20RU%20%7C%20JA-ce3c60" alt="Langues">
</p>

<p align="center">
<a href="../../releases/latest"><b>⬇ Télécharger la dernière version</b></a>
&nbsp;·&nbsp;
<a href="https://twitch.tv/eris_ezio_live">Twitch</a>
&nbsp;·&nbsp;
<a href="https://www.youtube.com/@ERIS_EZIO_SH">YouTube</a>
</p>

---

## Pourquoi ce launcher ?

En shiny hunting sur émulateur, chaque fenêtre doit démarrer avec une heure différente pour obtenir un tirage différent. À la main, ça veut dire régler 20 horloges, puis ranger 20 fenêtres une par une.

**Eris Ezio's Launcher** fait tout ça pour toi :

1. il ouvre les fenêtres via **RunAsDate**, chacune avec une horloge décalée (+1 minute par défaut, réglable) ;
2. il les **range automatiquement**, collées bord à bord, sur l'écran de ton choix ;
3. il charge directement ta **ROM**, ta **cartouche GBA** et ta **sauvegarde**.

## ✨ Fonctionnalités

- **5 émulateurs** : melonDS, DeSmuME, VisualBoyAdvance, mGBA et Azahar.
- **Une horloge différente par fenêtre**, avec un écart réglable en **secondes, minutes, heures, jours, mois ou années** (par défaut +1 minute : 14:00, 14:01, 14:02…).
- **Rangement au pixel près**, lignes alignées ou **en quinconce** (décalage d'une demi-fenêtre), toujours empilées dans le bon ordre (chaque ligne devant la précédente).
- **Pour la DS et la 3DS**, les lignes se chevauchent juste assez pour garder **l'écran du haut** entièrement visible.
- **Choix de l'écran** (ou automatiquement le plus grand).
- **Glisser-déposer** de la ROM, de la cartouche GBA et de la sauvegarde.
- **Bouton ARRÊTER** pour stopper l'ouverture à tout moment.
- **Interface inspirée du menu de la Nintendo DS**, nette en 1080p comme en 4K.
- **6 langues** : français, anglais, allemand, italien, russe et japonais, au choix dans la barre du haut.
- **Réglages mémorisés** séparément pour chaque émulateur.

## 🎮 Émulateurs pris en charge

| Émulateur | ROM | Cartouche GBA | Sauvegarde déposée | Quinconce par défaut |
|---|:-:|:-:|:-:|:-:|
| [melonDS](https://melonds.kuribo64.net/) | ✅ | ✅ | ✅ `.sav` | ✅ |
| [DeSmuME](http://desmume.org/) | ✅ | ✅ | ✅ `.dsv` | — |
| [VisualBoyAdvance-M](https://visualboyadvance-m.org/) | ✅ | — | ✅ `.sav` | — |
| [mGBA](https://mgba.io/) | ✅ | — | ✅ `.sav` | — |
| [Azahar](https://azahar-emu.org/) | ✅ | — | — | — |

Le décalage en quinconce peut être activé ou désactivé pour chaque émulateur.

## 📥 Installation

1. Télécharge le fichier **ErisEzioLauncher….exe** dans la page [Releases](../../releases/latest). Aucune installation n'est nécessaire.
2. Télécharge **RunAsDate** (gratuit) sur le site de NirSoft : <https://www.nirsoft.net/utils/run_as_date.html>.
   Prends la version **64 bits** si ton émulateur est en 64 bits, ce qui est le cas de la plupart aujourd'hui.
3. Installe le ou les émulateurs que tu utilises. Dans leurs réglages, l'horloge du jeu doit suivre **l'heure du PC**.

Au premier lancement, le launcher cherche tout seul RunAsDate et les émulateurs sur ton bureau, y compris via leurs raccourcis. S'il ne les trouve pas, il te demande simplement où ils sont.

> ⚠️ **Avertissement Windows** : le programme n'est pas signé, donc Windows SmartScreen peut afficher un message.
> Clique sur **Informations complémentaires** puis sur **Exécuter quand même**.

## 🚀 Prise en main

1. Choisis la **langue** dans la barre du haut si besoin, puis l'**émulateur** et l'**écran**.
2. Indique le **nombre de fenêtres** et le **nombre par ligne**.
3. Choisis la **date** et l'**heure** de la première fenêtre, puis l'**écart d'horloge** entre deux fenêtres.
4. Coche ou décoche le **décalage en quinconce**.
5. Glisse ta **ROM** sur la fenêtre (et si besoin une cartouche GBA ou une sauvegarde).
6. Clique sur **LANCER**.

Pendant l'ouverture, le bouton devient **ARRÊTER**. Si tu cliques dessus, plus aucune nouvelle fenêtre n'est lancée, et celles déjà ouvertes sont rangées normalement.

### Glisser-déposer

Dépose un fichier n'importe où sur la fenêtre, le launcher reconnaît son type tout seul :

| Fichier déposé | Va dans… |
|---|---|
| `.sav`, `.dsv`, `.srm` | **Sauvegarde** |
| `.gba`, `.gb`, `.gbc` (avec melonDS ou DeSmuME) | **Cartouche GBA** |
| tout autre fichier | **ROM du jeu** |

### Sauvegardes

- Une sauvegarde déposée est installée **au moment du lancement**, là où l'émulateur la lit :
  - à côté de la ROM, avec le même nom, en `.sav` (melonDS, VisualBoyAdvance, mGBA) ;
  - dans le dossier `Battery` de DeSmuME, en `.dsv`.
- **L'ancienne sauvegarde n'est jamais perdue** : elle est d'abord copiée en `nom.sav.bak-date-heure`.
- Elle ne sert **qu'une seule fois**, pour ne jamais écraser ta progression aux lancements suivants.
- Les `.dsv` de DeSmuME sont convertis automatiquement pour melonDS, VisualBoyAdvance et mGBA.
- Sans sauvegarde déposée, chaque émulateur utilise **sa sauvegarde habituelle**.

> 💡 Toutes les fenêtres partagent le même fichier de sauvegarde : **ne sauvegarde que dans la fenêtre du shiny**.

## ⚙️ Réglages avancés

Chaque émulateur a son fichier de réglages à côté de l'exe : `LanceurMelonDS.ini`, `LanceurDeSmuME.ini`, `LanceurVBA.ini`, `LanceurMGBA.ini` et `LanceurAzahar.ini`.

| Clé | Rôle | Défaut |
|---|---|---|
| `pasVertical` | Décalage vertical entre deux lignes, en pixels (`0` = automatique) | `0` |
| `delaiLancement` | Pause entre deux fenêtres, en secondes | `2` |
| `tailleFenetre` | Taille imposée de la zone d'affichage (mGBA), par ex. `320x326` | — |
| `retoucheBordures` | `1` = supprime le liseré gris de Windows 11 (déconseillé, peut rendre l'affichage instable) | `0` |

## 🧰 Dépannage

| Problème | Solution |
|---|---|
| Les fenêtres ont toutes la même heure | Dans l'émulateur, l'horloge du jeu doit suivre l'heure du PC, pas une date fixe. |
| « RunAsDate demande les droits administrateur » | Lance le launcher avec un clic droit > **Exécuter en tant qu'administrateur**. |
| RunAsDate n'a aucun effet | Utilise la version de RunAsDate (32 ou 64 bits) qui correspond à ton émulateur. |
| Le PC rame avec beaucoup de fenêtres | Coupe le son et la VSync dans l'émulateur, ou ouvre moins de fenêtres. |
| L'écran du haut est coupé ou trop espacé | Ajuste `pasVertical` dans le fichier `.ini` de l'émulateur. |
| Le launcher se ferme sans message | C'est sûrement l'antivirus (à cause de RunAsDate) : regarde l'historique de protection et ajoute le dossier du launcher et RunAsDate aux exclusions. |
| Une erreur s'affiche | Le détail est dans `ErisEzioLauncher.log`, à côté du programme : joins-le à ton signalement dans l'onglet [Issues](../../issues). |

## 🛠️ Compiler soi-même

Il faut [Go](https://go.dev/dl/) 1.21 ou plus récent.

```bat
cd src
build.bat
```

Ou directement :

```bat
go build -ldflags "-s -w -H windowsgui" -o ErisEzioLauncher.exe .
```

Le fichier `rsrc_windows_amd64.syso` contient l'icône et le manifeste Windows ; `go build` l'intègre automatiquement.

## 📜 Historique des versions

| Version | Nouveautés |
|---|---|
| **1.4.0** | Écart d'horloge réglable (secondes → années), ordre d'empilement des fenêtres corrigé |
| 1.3.0 | Interface en 6 langues : français, anglais, allemand, italien, russe, japonais |
| 1.2.2 | Correction : le launcher se fermait à l'ouverture d'une fenêtre « Ouvrir » (émulateur introuvable, bouton « … ») |
| 1.2.1 | Messages d'erreur et journal de diagnostic `ErisEzioLauncher.log` |
| 1.2.0 | Choix de l'écran, ajout de DeSmuME |
| 1.1.0 | Décalage en quinconce au choix pour tous les émulateurs, bouton ARRÊTER |
| 1.0.2 | Affichage correct en passant d'un écran 4K à un écran 1080p |
| 1.0.1 | Option de décalage des lignes pour melonDS |
| 1.0.0 | Nouvelle interface façon DS, sauvegardes par glisser-déposer, nouveau nom |
| 0.5.0 | Première interface graphique |
| 0.4.0 | ROM et cartouche GBA par glisser-déposer |
| 0.3.x | Lanceur unique : melonDS, VisualBoyAdvance, mGBA, Azahar |
| 0.0.x | Premières versions (melonDS + RunAsDate) |

## 🙏 Crédits

- Créé par **Eris Ezio** : [Twitch](https://twitch.tv/eris_ezio_live) · [YouTube](https://www.youtube.com/@ERIS_EZIO_SH).
- S'appuie sur [RunAsDate](https://www.nirsoft.net/utils/run_as_date.html) de NirSoft (non inclus, à télécharger séparément).
- melonDS, DeSmuME, VisualBoyAdvance-M, mGBA et Azahar appartiennent à leurs auteurs respectifs. Ce projet n'est affilié à aucun d'eux, ni à Nintendo.
- Aucune ROM n'est fournie : utilise uniquement des copies de jeux que tu possèdes.

## 📄 Licence

Distribué sous licence **MIT** : tu peux utiliser, modifier et redistribuer ce programme librement, à condition de conserver le nom de l'auteur et la licence. Voir le fichier [LICENSE](LICENSE).
## 📄 Licence

Distribué sous licence **MIT** : tu peux utiliser, modifier et redistribuer ce programme librement, à condition de conserver le nom de l'auteur et la licence. Voir le fichier [LICENSE](LICENSE).

