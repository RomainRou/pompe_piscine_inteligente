# 💧 Blueprint Home Assistant - Pompe de piscine intelligente

Ce blueprint Home Assistant permet une gestion intelligente de la **pompe de piscine**, avec plusieurs modes de fonctionnement :

## 🔧 Fonctions principales

- ⏱️ 4 plages horaires configurables (matin et après-midi)
- 🌡️ Calcul automatique du temps de filtration en fonction de la température de l’eau
- ❄️ Mode hiver avec filtration minimale
- 🌦️ Intégration météo : annulation ou report de filtration en cas de mauvais temps
- 📲 Notifications Telegram au démarrage et arrêt
- 🧪 Modes de traitement spécifiques (anti-algues, chlore choc, floculant, etc.)
- 🔁 Retour automatique au mode normal après traitement

## 🛠️ Pré-requis

- Capteurs :
  - Température de la piscine
  - Température extérieure
  - Entité météo
  - Saison (sensor ou input_select)
- Entités :
  - `switch` de la pompe
  - `input_select` pour les modes de traitement
  - `input_boolean` pour le suivi du cycle
  - `input_number` et `input_datetime` pour la durée/début

## 📁 Fichier blueprint

📄 [`pompe_piscine_intelligente.yaml`](blueprints/automation/ton_nom_utilisateur/pompe_piscine_intelligente.yaml)

## 🧪 Exemple de modes personnalisés

- Anti-calcaire curatif : 12 à 24h
- Floculant : 2 à 4h
- Brome : 12 à 24h
- Chlore choc : 8 à 12h
- ...
## Installation automatique du blueprint ##
[![Importer dans Home Assistant](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?repository_url=https://raw.githubusercontent.com/RomainRou/pompe_piscine_inteligente/main/blueprints/automation/RomainRou/pompe_piscine_intelligente.yaml)


## 📦 Importer dans Home Assistant

1. Dans Home Assistant, va dans **Configuration > Automatisations > Blueprints**
2. Clique sur **Importer un blueprint**
3. Utilise ce lien :<br>
https://github.com/ton_utilisateur/home-assistant-blueprints/blob/main/blueprints/automation/RomainRou/pompe_piscine_intelligente.yaml

---

### ✅ 4. Ajoute et pousse tes fichiers

#### A. Via Git

```bash
git clone https://github.com/RomainRou/home-assistant-blueprints.git
cd home-assistant-blueprints

mkdir -p blueprints/automation/ton_nom_utilisateur
cp /chemin/vers/ton/blueprint.yaml blueprints/automation/ton_nom_utilisateur/pompe_piscine_intelligente.yaml
touch README.md  # ou utilise le modèle ci-dessus

git add .
git commit -m "Ajout du blueprint pompe de piscine intelligente"
git push origin main
