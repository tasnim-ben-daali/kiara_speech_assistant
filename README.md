# Kiara – Assistant Vocal en Python

Kiara est un assistant vocal simple développé en Python qui écoute des commandes vocales, les transcrit, puis répond à voix haute. Ce projet a été réalisé à titre personnel, en s'inspirant de Travelsy Media.

## Fonctionnalités

- **Reconnaissance vocale (speech-to-text)** : capture l'audio depuis le microphone et le transcrit via l'API de reconnaissance vocale de Google
- **Synthèse vocale (text-to-speech)** : répond à voix haute grâce à gTTS (Google Text-to-Speech), l'audio étant joué avec `playsound`
- **Commandes vocales disponibles** :
  - Demander le nom de l'assistant
  - Demander l'heure actuelle
  - Faire une recherche Google par la voix ("search for ...")
  - Trouver un lieu sur Google Maps par la voix ("find location ...")
  - Quitter l'assistant ("exit")

## Technologies utilisées

- Python 3.11
- [SpeechRecognition](https://pypi.org/project/SpeechRecognition/) + PyAudio (capture et transcription audio)
- [gTTS](https://pypi.org/project/gTTS/) (synthèse vocale)
- [playsound](https://pypi.org/project/playsound/) 1.2.2 (lecture audio)
- `webbrowser` (module intégré) pour ouvrir les résultats de recherche/maps

## Installation

1. Cloner le dépôt :
   ```
   git clone https://github.com/<ton-nom-utilisateur>/<nom-du-depot>.git
   cd <nom-du-depot>
   ```

2. Créer et activer un environnement virtuel :
   ```
   py -m venv venv
   venv\Scripts\activate
   ```
   *(Sur macOS/Linux : `source venv/bin/activate`)*

3. Installer les dépendances :
   ```
   pip install SpeechRecognition pyaudio gtts playsound==1.2.2
   ```

## Utilisation

Une fois l'environnement virtuel activé, lance :
```
python main.py
```

Prononce une commande quand le message "Say something!" s'affiche. Kiara la transcrit, y répond à voix haute, et agit en conséquence si elle correspond à une commande connue.

## Structure du projet

```
.
├── main.py         # Logique principale de l'assistant
├── requirements.txt (optionnel, voir remarque ci-dessous)
├── .gitignore
└── README.md
```

## Remarques

- Les fichiers `.mp3` temporaires générés pour la synthèse vocale sont supprimés automatiquement après chaque réponse.
- `venv/`, `__pycache__/` et `*.mp3` sont exclus du suivi git via `.gitignore`.

## Licence

Projet réalisé à des fins personnelles et éducatives.
