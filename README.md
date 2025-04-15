# 🧠 CODEX – AI Debug Action Predictor

Codex est une **IA fine-tunée sur le modèle T5** qui **prédit automatiquement l’action de correction** à effectuer lorsqu’une erreur de code est détectée.  
> Exemple :  
> "missing colon in function definition" → `add_colon_to_function`

---

## 🚀 Objectif

Créer un **assistant IA intelligent** capable d’identifier le type d’erreur rencontrée dans du code, et de **suggérer automatiquement la correction la plus appropriée**.

---

## 📦 Fonctionnalités

- 🔮 Prédiction d'action correctrice à partir d’un message d’erreur
- 🧠 Modèle basé sur `t5-small` fine-tuné sur plus de 200 cas
- 📚 Données d'entraînement sous format `.jsonl`
- 🔁 Ré-entraînement possible et rapide via HuggingFace
- ✅ Évaluation automatique via `test_model.py`

---

## 📂 Structure du projet
CODEX-AI/ ├── train_model.py # Script d'entraînement du modèle ├── test_model.py # Script de test des prédictions ├── dataset.jsonl # Données d'entraînement (erreurs et actions) ├── debug_model/ # Répertoire contenant les checkpoints entraînés │ └── checkpoint-xxx/ # Derniers poids enregistrés └── README.md # Ce fichier de documentation

---

## ⚙️ Installation & Setup

### 1. Clone ce dépôt :
```bash
git clone https://github.com/purplekan/CODEX-AI.git
cd CODEX-AI
```
### 2. Crée un environnement virtuel :
```bash
python -m venv .venv
# Sur Windows :
.venv\Scripts\activate
# Sur Mac/Linux :
source .venv/bin/activate
```
### 3. Installe les dépendances

Installe les dépendances :

```bash
pip install -r requirements.txt
```
Si requirements.txt n’existe pas encore, tu peux installer manuellement :

```bash
pip install transformers datasets
```

## 🧪 Tester le modèle
```bash
python test_model.py
```
Le script affiche :
- 🔍 L’entrée (ex. : "function not defined")
- ✅ La sortie attendue (ex. : define_function)
- 🔮 La prédiction du modèle
- ✔️ Ou ❌ selon la correspondance

## 🧠 Entraîner le modèle
```bash
python train_model.py
```
Cela :
- Charge les données depuis dataset.jsonl
- Entraîne le modèle T5
- Sauvegarde les checkpoints dans debug_model/

Tu peux augmenter les performances en enrichissant dataset.jsonl avec plus de cas.

## 📈 Exemple de données d'entraînement (dataset.jsonl)
```json
{"input": "function not defined", "output": "define_function"}
{"input": "missing colon in function definition", "output": "add_colon_to_function"}
{"input": "list index out of range", "output": "check_list_index"}
```

🔧 Conseils pour de meilleurs résultats
- Entraîne sur un nombre plus grand d’exemples
- Augmente num_train_epochs dans TrainingArguments
- Utilise num_beams, temperature, et repetition_penalty pour des prédictions plus précises

## 📚 Ressources utilisées

- 🤗 [HuggingFace Transformers](https://github.com/huggingface/transformers)
- 🧠 Modèle `t5-small`
- 🔍 Fine-tuning basé sur `Trainer` + `Datasets`

------

## 🛡️ Licence

Ce projet est sous licence **MIT**.

------

## 🧠 À propos

Ce projet a été co-développé par [purplekan](https://github.com/purplekan) et son copilote IA ChatGPT 🤝
 Dans une vision partagée : **entraîner, tester, progresser.**

------

> "Ce projet est la première pierre d’un édifice plus grand : des IA collaboratives, spécialisées, et redoutables."











