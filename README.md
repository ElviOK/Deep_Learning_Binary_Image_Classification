# Deep Learning Binary Image Classification

## Projektübersicht
Dieses Repository enthält die Dateien und Ergebnisse meines Projekts zur binären Klassifikation von Bildern mithilfe von Deep Learning (**PyTorch**). 
- **`pitch.pdf`**: Eine kurze Präsentation, die die Zielsetzung des Projekts beschreibt.
- **`DL_experiments.ipynb`**: Das Hauptnotebook mit allen Experimenten und Analysen.
- **Tensorboard-Bilder (`Accuracy_Eval.png`, `Loss_Eval.png`, `Low_Dropout.png`)**: Visualisierungen, die den Lernfortschritt des Modells zeigen.

---

## Projektbeschreibung
In diesem Projekt wurde ein neuronales Netzwerk entwickelt, um eine binäre Klassifikation von Bildern durchzuführen. Der Fokus lag auf:
- Implementierung eines benutzerdefinierten CNN-Modells.
- Einsatz von Techniken wie **Early Stopping**, **Dropout** und **Tensorboard** zur Modelloptimierung und Visualisierung.
- Evaluation der Modellleistung mit **Loss- und Genauigkeitsmetriken**.

---

## Methodik
### 1. **EDA und Preprocessing**
- **EDA**: Analyse der Klassenverteilung, Bildformate und Pixelintensitäten.
- **Preprocessing**: Vereinheitlichung der Bildgrößen und Farbschemata, Bereinigung von Duplikaten und Normalisierung der Bilddaten.

### 2. **Baseline-Modelle**
- **Heuristik-Baseline**: Klassifikation nach der häufigsten Klasse (*Neutral*), Accuracy: **52,16%**.
- **Random Forest Baseline**: Training auf flachen Pixelwerten, Accuracy: **83,79%**.

### 3. **CNN-Modell**
- Benutzerdefinierte Architektur mit:
  - 3 **Convolutional Layers** mit Batch Normalization.
  - **Dropout** (0,7) zur Regularisierung.
  - Dynamische Fully Connected Layer zur flexiblen Verarbeitung der Eingabe.
- **Hyperparameter-Optimierung**: Random Search auf Dropout-Werten, Lernrate und Batchgröße.

### 4. **Training und Evaluierung**
- Einsatz von **Early Stopping**, um Überanpassung zu vermeiden.
- Verwendung von **Tensorboard**, um den Fortschritt in Echtzeit zu verfolgen.
- Finale Testgenauigkeit: **89,41%**.
