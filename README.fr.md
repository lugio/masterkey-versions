<p align="center"><img src="docs/images/masterkey.svg" width="96" alt="MasterKey"></p>

<h1 align="center">MasterKey — versions</h1>

<p align="center"><a href="README.md">English</a></p>

**MasterKey** est un gestionnaire de connexions de bureau écrit en Rust (Tauri 2, Vue 3) : SSH et RDP en onglets, carnet de
connexions, coffre local chiffré et liaison en lecture seule avec Bitwarden / Vaultwarden. Son code est privé jusqu'à la version 1.

Ce dépôt ne contient **aucun code**. Il publie les installeurs Windows signés, leurs signatures et la fiche `latest.json` que
MasterKey lit pour proposer les mises à jour.

## Mises à jour depuis l'application

Quand une version plus récente est publiée ici, son numéro apparaît à côté du logo, dans la barre de titre :

![Avis de mise à jour dans la barre de titre](docs/images/avis.png)

Un clic montre ce qui change et propose **Installer et relancer**. Rien ne s'installe sans ce clic, et les sessions ouvertes sont
rappelées avant la relance :

![Dialogue de mise à jour](docs/images/dialogue.png)

*(Captures prises sur le carnet d'exemple fourni avec l'application.)*

## Intégrité

- Chaque installeur est signé (minisign). La clé publique est intégrée à MasterKey, qui **refuse tout fichier dont la signature ne
  correspond pas**, d'où qu'il vienne.
- La clé privée ne quitte pas le poste du mainteneur ; l'intégration continue ne signe rien.
- Les installeurs ne sont pas encore signés Authenticode : Windows SmartScreen avertit à la première installation manuelle.

## Installation

1. Télécharger `MasterKey_x.y.z_x64-setup.exe` dans la [dernière version](https://github.com/lugio/masterkey-versions/releases/latest).
2. Le lancer (installation pour l'utilisateur, sans droits d'administrateur).
3. Les versions suivantes arrivent par l'avis de la barre de titre.

Jusqu'à la v1, chaque version est une **version d'essai**, pour évaluation (publiée comme version normale pour que la fiche de mise à jour la trouve).

## Licence

Voir [LICENSE](LICENSE) : privée jusqu'à la version 1, une licence libre est prévue ensuite.
