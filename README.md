# Projet-Tri-par-Couleur-UR3

Projet Arduino avec capteur TCS3200 pour détecter des couleurs (rouge, vert, bleu). Un code couleur est envoyé via port série à un robot UR3 via Modbus TCP/IP. Communication simple entre capteur et automate industriel. Matériel : Arduino UNO, TCS3200, UR3.


FONCTIONNEMENT

1. L’Arduino lit les valeurs RGB du capteur TCS3200.
2. L’Arduino calcule un code couleur :
   0 : ambigu
   1 : rouge
   2 : vert
   3 : bleu
   et l’envoie sur le port série.
3. L’application C# lit le port série, crée une trame Modbus TCP et envoie le code couleur à l’UR3.

---

PRÉREQUIS

- Arduino UNO (ou compatible)
- Capteur TCS3200
- UR3 avec Modbus TCP/IP activé
- Visual Studio ou .NET pour le code C#

---

BRANCHEMENT TCS3200 → ARDUINO

TCS3200 | Arduino
---------|--------
S0       | D8
S1       | D9
S2       | D10
S3       | D11
OUT      | D12
LED      | D7
GND      | GND
VCC      | 5V

---

CODE ARDUINO

Fichier : TCS3200_lecturedecouleur.txt
