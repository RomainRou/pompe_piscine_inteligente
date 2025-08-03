# 💧 Blueprint Home Assistant - Pompe de piscine intelligente

Ce blueprint Home Assistant permet une gestion intelligente de la **pompe de piscine**, avec plusieurs modes de fonctionnement :

## 🔧 Fonctions principales

- ⏱️ 4 plages horaires configurables (matin et après-midi)
- 🌡️ Calcul automatique du temps de filtration en fonction de la température de l’eau
- ❄️ Mode hiver avec filtration minimale (en cours de test et de developpement)
- 🌦️ Intégration météo : annulation ou report de filtration en cas de mauvais temps (en cours de developpement possibilité de rencontré quelques souci)
- 📲 Possibilitées de notifications Telegram au démarrage et arrêt
- 🧪 Modes de traitement spécifiques (anti-algues, chlore choc, floculant, etc.)
- 🔁 Retour automatique au mode normal après traitement

## 🛠️ Pré-requis

- Capteurs nécéssaire:
  - Température de la piscine
  - Température extérieure
  - Entité météo (integration meteo france par exemple)
  - Saison (integration season dans home assistant)
- Entités nécéssaire:
  - `switch` de la pompe
  - `input_select` pour les modes de traitement (a mettre dans le fichier input_select.yaml se référé au fichier fourni)
  - `input_boolean` pour le suivi du cycle ( a créé dans home assistant se référer au fichier fourni input_boolean.yaml)
  - `input_number` et `input_datetime` pour la durée/début ( a créé dans home assistant se référé au fichier fourni pour l'input _number)

## 📁 Fichier blueprint

📄 [`pompe_piscine_intelligente.yaml`](blueprints/automation/pompe_piscine_intelligente.yaml)
📄 [`input_select.yaml`](input_select.yaml)
📄 [`input_number.yaml`](input_number.yaml)
📄 [`input_boolean.yaml`](input_boolean.yaml)
## 🧪 Exemple de modes personnalisés

- Anti-calcaire curatif : 12 à 24h
- Floculant : 2 à 4h
- Brome : 12 à 24h
- Chlore choc : 8 à 12h
- ...
## Installation automatique du blueprint ##
<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FRomainRou%2Fpompe_piscine_inteligente%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fautomationpompe_piscine_intelligente.yaml" target="_blank" rel="noreferrer noopener"><img src="https://my.home-assistant.io/badges/blueprint_import.svg" alt="Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled." /></a>


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

mkdir -p blueprints/automation/RomainRou
cp /chemin/vers/ton/blueprint.yaml blueprints/automation/RomainRou/pompe_piscine_intelligente.yaml
touch README.md  # ou utilise le modèle ci-dessus

git add .
git commit -m "Ajout du blueprint pompe de piscine intelligente"
git push origin main



