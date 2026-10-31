# ErisEzioLauncher
Launcher pour ouvrir plusieurs fenêtres d'émulateurs
<p align="center"><img src="docs/logo.png" width="160" alt="Logo Eris Ezio"></p>

<h1 align="center">Eris Ezio's Launcher</h1>

<p align="center">
Le shiny hunting <b>multi-fenêtres</b>, en un clic.<br>
Ouvre jusqu'à 60 fenêtres d'émulateur, chacune avec sa propre horloge, et les range automatiquement au pixel près.
</p>

<p align="center">
<a href="https://twitch.tv/eris_ezio_live">Twitch</a> ·
<a href="https://www.youtube.com/@ERIS_EZIO_SH">YouTube</a>
</p>

---

## ✨ Ce que fait le launcher

- **Plusieurs émulateurs pris en charge** : melonDS, VisualBoyAdvance, mGBA et Azahar.
- **Une horloge différente par fenêtre** grâce à [RunAsDate](https://www.nirsoft.net/utils/run_as_date.html) : la fenêtre 1 démarre à l'heure choisie, la fenêtre 2 une minute plus tard, etc.
- **Rangement automatique** sur le plus grand écran : fenêtres collées bord à bord, lignes au choix alignées ou en quinconce (décalage d'une demi-fenêtre).
- **Glisser-déposer** : une ROM, une cartouche GBA (emplacement GBA de melonDS) ou une sauvegarde `.sav` / `.dsv`.
- **Bouton ARRÊTER** pour stopper l'ouverture des fenêtres à tout moment.
- **Interface inspirée du menu de la Nintendo DS**, nette en 1080p comme en 4K.

## 📥 Installation

1. Télécharge **ErisEzioLauncher.exe** dans la section [Releases](../../releases).
2. Télécharge **RunAsDate** (gratuit) sur le site de NirSoft : <https://www.nirsoft.net/utils/run_as_date.html>
   → prends la version **64 bits** pour melonDS, mGBA et Azahar.
3. Installe le ou les émulateurs que tu utilises.

Au premier lancement, le launcher cherche tout seul RunAsDate et les émulateurs sur le bureau (y compris via leurs raccourcis). S'il ne les trouve pas, il te demande où ils sont.

> ⚠️ Le programme n'est pas signé : Windows SmartScreen peut afficher un avertissement.
> Clique sur **Informations complémentaires** puis **Exécuter quand même**.

## 🎮 Utilisation

1. Choisis l'**émulateur**.
2. Règle le **nombre de fenêtres**, le **nombre par ligne**, la **date** et l'**heure** de départ.
3. Glisse ta **ROM** (et si besoin une cartouche GBA ou une sauvegarde) sur la fenêtre.
4. Clique sur **LANCER**.

### À propos des sauvegardes

- Une sauvegarde déposée est installée à côté de la ROM (même nom, en `.sav`) au moment du lancement.
- L'ancienne sauvegarde est **toujours mise de côté** (`nom.sav.bak-date-heure`) avant d'être remplacée.
- La sauvegarde déposée ne sert qu'**une seule fois**, pour ne jamais écraser ta progression.
- Toutes les fenêtres partagent le même fichier de sauvegarde : **ne sauvegarde que dans la fenêtre du shiny**.
- Azahar gère ses sauvegardes dans ses propres dossiers : la fonction est désactivée pour lui.

### Réglages avancés

Chaque émulateur a son fichier de réglages à côté de l'exe (`LanceurMelonDS.ini`, `LanceurVBA.ini`, `LanceurMGBA.ini`, `LanceurAzahar.ini`) :

| Clé | Rôle | Défaut |
|---|---|---|
| `pasVertical` | Décalage vertical entre deux lignes, en pixels (`0` = automatique) | `0` |
| `delaiLancement` | Pause entre deux fenêtres, en secondes | `2` |
| `tailleFenetre` | Taille imposée de la zone d'affichage (mGBA), ex. `320x326` | — |
| `retoucheBordures` | `1` = supprime le liseré gris de Windows 11 (déconseillé) | `0` |

## 🛠️ Compiler soi-même

Il faut [Go](https://go.dev/dl/) 1.21 ou plus récent.

```bat
cd src
build.bat
```

ou directement :

```bat
go build -ldflags "-s -w -H windowsgui" -o ErisEzioLauncher.exe .
```

Le fichier `rsrc_windows_amd64.syso` contient l'icône et le manifeste Windows ; il est pris en compte automatiquement par `go build`.

## 📜 Historique des versions

| Version | Nouveautés |
|---|---|
| **1.1.0** | Décalage des lignes au choix pour tous les émulateurs, bouton ARRÊTER |
| 1.0.2 | Affichage correct quand la fenêtre passe d'un écran 4K à un écran 1080p |
| 1.0.1 | Option de décalage des lignes pour melonDS |
| 1.0.0 | Nouvelle interface façon DS, sauvegardes par glisser-déposer, nouveau nom |
| 0.5.0 | Première interface graphique |
| 0.4.0 | ROM et cartouche GBA par glisser-déposer |
| 0.3.x | Lanceur unique : melonDS, VisualBoyAdvance, mGBA, Azahar |
| 0.0.x | Premières versions (melonDS + RunAsDate) |

## 🙏 Crédits

- Créé par **Eris Ezio** ([@ERIS_EZIO_SH](https://www.youtube.com/@ERIS_EZIO_SH)).
- Utilise [RunAsDate](https://www.nirsoft.net/utils/run_as_date.html) de NirSoft (non inclus, à télécharger séparément).
- melonDS, VisualBoyAdvance-M, mGBA et Azahar appartiennent à leurs auteurs respectifs. Ce projet n'est affilié à aucun d'eux, ni à Nintendo.
- Aucune ROM n'est fournie : utilise uniquement des copies de jeux que tu possèdes.

## 📄 Licence

Distribué sous licence **MIT** : tu peux utiliser, modifier et redistribuer ce programme librement, à condition de conserver le nom de l'auteur et la licence. Voir le fichier [LICENSE](LICENSE).
