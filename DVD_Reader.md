# Lire un DVD protégé sous Ubuntu 24.04 avec MPV Reader

Cette procédure est un guide pas à pas pour pouvoir **regarder un DVD commercial protégé** sur un PC sous Ubuntu 24.04, en utilisant le lecteur **MPV**.

## Mettre à jour l'historique des pacquets
- ```sudo apt update```

## Installer MPV Reader
- ```sudo apt install mpv```

## Ajouter les bibliothèques pour lire des DVD protégés (CSS)
- ```sudo apt install libdvd-pkg```
- ```sudo dpkg-reconfigure libdvd-pkg```

### 🔐 À propos de CSS

**CSS** signifie **Content Scramble System**.  
C’est un **système de chiffrement** utilisé sur certains DVD commerciaux pour empêcher la copie ou la lecture sur PC.<br>
Sans la bibliothèque adéquate (`libdvdcss2`), la plupart des lecteurs multimédia ne peuvent pas lire ces DVD.

## Acceder au DVD
- Branchez votre lecteur DVD USB si nécessaire.
- Insérez le DVD dans le lecteur.

## Lire le DVD avec MPV

- ```mpv dvd://```<br>
**ou** <br>
- ```mpv dvd:// --dvd-device=/dev/sr0```

En espérant que celà vous soit utile