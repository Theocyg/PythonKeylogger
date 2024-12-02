# ReadMe

## Prérequis

Pour exécuter ce projet, vous aurez besoin de Python 3.x et des bibliothèques listées dans le fichier `requirements.txt`.

## Installation

1. Clonez ce dépôt sur votre machine locale.
2. Créez un environnement virtuel (optionnel mais recommandé) :
   ```bash
   python -m venv venv
   ```
3. Activez l'environnement virtuel :
     ```bash
     source venv/bin/activate
     ```
4. Installez les dépendances :
   ```bash
   pip install -r requirements.txt
   ```

## Utilisation

### Démarrer le serveur Flask

Pour démarrer le serveur Flask, exécutez le script `ecoute.py` :
```bash
python ecoute.py
```
Le serveur écoutera sur `http://0.0.0.0:8080`.

### Démarrer le keylogger

Pour démarrer le keylogger, exécutez le script `keylogger.py` :
```bash
python keylogger.py
```
Le keylogger enregistrera les frappes de clavier et les enverra périodiquement au serveur Flask.

## Fonctionnalités

### `ecoute.py`

- **Route** : `/`
- **Méthode** : `POST`
- **Description** : Reçoit les données JSON et les affiche dans la console.

### `keylogger.py`

- **Enregistrement des frappes** : Enregistre les frappes de clavier et les stocke dans une variable globale `text`.
- **Envoi des données** : Envoie les données enregistrées au serveur Flask toutes les 10 secondes.
- **Mapping AZERTY** : Convertit les frappes de clavier QWERTY en AZERTY.

## Remarques

- Assurez-vous que le serveur Flask est en cours d'exécution avant de démarrer le keylogger.
- Le keylogger enregistre toutes les frappes de clavier, y compris les touches spéciales comme Entrée, Tab, Espace, et Backspace.

## Avertissement

L'utilisation de keyloggers peut être illégale et contraire à l'éthique si elle est utilisée sans le consentement de l'utilisateur. Assurez-vous d'utiliser ce projet de manière responsable et conforme aux lois et règlements en vigueur.