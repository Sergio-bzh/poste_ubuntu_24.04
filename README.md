# Préparation d'un poste Ubuntu pour développer
Ce fichier décrit les étapes d'installation d'un environnement de développement.

## Prérequis :
- PC (_i386 X64_) de préférence sans OS
- Clef USB bootable (_image ISO Ubuntu 24.04 **LTS**_)
- Connexion internet (câble éthernet)
- Connaissance basique de gestionnaire des paquets apt et des commandes shell (_bash_)

## Objectifs :
La mise en place de cette configuration a pour but de disposer d'un poste de travail avec les outils nécessaires au suivi de ma formation Bachelor Python et à la production des livrables attendus pour la validations des différents blocs qui la composent.

## Étapes d'installation :

### 1. Installer Ubuntu LTS
- Allumez le PC et adaptez les paramètres du BIOS pour "_booter_" sur des périfériques USB
- Branchez la Clef USB
- Connectez le PC à une prise éthernet relié à votre router
- Démarrez le PC (_suivez les instructions d'installation selon vos envies ou besoins_)
- Notez et conservez vos identifiants
- A la fin de l'installation retirez la clef USB et redémarrez le PC
- Ovrez une session avec votre compte utilisateur
- Élevez les privilèges et mettez à jour votre système
    - ```sudo apt update && sudo apt upgrade```


### 2. Installer Git
- ```sudo apt install git```
- ```git config --global user.name "votre nom"```
- ```git config --global user.email "votre email"```

### 3. Installer Curl
- ```sudo apt install curl```

### 4. Installer Docker
- ```sudo apt install docker.io```
- ```sudo usermod -aG docker $USER```
- **Relancez la session ou redémarrez le poste**

### 5. Installer Node.js (npm et yarn)
- ```sudo apt install nodejs npm```
- ```npm install -g yarn```

### 6. Installer la CLI Heroku (_pour déployer en console_)
- ```npm install -g heroku```

### 7. Installer VSCode
- Allez dans le "**Centre d'applications**" et recherchez le snap "**VSCode**"
- Cliquez sur **Installez**<br>**OU en console**
- ```sudo snap install --classic code```

### 8. Installer le language de développement souhaité (_**Python 3**_ dans mon cas)
- ```sudo apt install python3```
- ```sudo apt install python3-pip```

### 9. **OPTIONNEL**

- #### a. Installer ZSH à la place de bash
    - ```sudo apt install zsh```

- #### b. Installer Oh_my_zsh (_change aussi le shell par défaut_)
    - ```sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"```


- #### c. Installer terminator (_pour remplacer le terminal par défaut_)
    - Allez dans le "**Centre d'applications**" et recherchez le snap "**Terminator**"
    - Cliquez sur **Installez**

- #### d. Installer Guake (Console "_effémère_")
    - ```sudo apt install guake```

## Vérifier les outils installé :
- ```git --version```
- ```curl --version```
- ```docker --version```
- ```node --version```
- ```python3 --version```
- ```heroku --version```
- ```code --version```

**_En espérant que ce mini how-to puisse vous être utile_**