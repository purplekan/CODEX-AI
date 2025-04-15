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

