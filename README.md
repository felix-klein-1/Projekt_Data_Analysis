# Themenextraktion aus Kundenbeschwerden (NLP)

Extraktion wiederkehrender Themen aus dem complaint-content-classification-nlp-Datensatz
mittels Vorverarbeitung, Vektorisierung (TF-IDF & Word2Vec) und Themenmodellierung (LDA & NMF).

## Pipeline

1. **Vorverarbeitung** – Kleinschreibung, Entfernen von Sonderzeichen/Zahlen/Stoppwörtern,
   Tokenisierung und Lemmatisierung; Beschwerden mit < 3 Wörtern werden entfernt.
2. **Vektorisierung** – TF-IDF (interpretierbar) und Word2Vec (semantisch).
3. **Themenextraktion** – LDA und NMF auf Basis der TF-IDF-Matrix.

## Setup

```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

## Nutzung

[Datensatz](https://github.com/halpert3/complaint-content-classification-nlp/blob/main/project_data/complaints_processed.csv) `complaints_processed.csv` ins Projektverzeichnis legen und das Notebook ausführen:

```bash
jupyter notebook complaints_topic_modeling.ipynb
```

## Benötigte Dateien

- `complaints_topic_modeling.ipynb` – Notebook mit der gesamten Analyse
- `requirements.txt` – benötigte Python-Bibliotheken
- `complaints_processed.csv` – Datensatz (nicht im Repository enthalten)
