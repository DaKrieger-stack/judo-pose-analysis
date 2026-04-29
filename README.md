# KI-Porjeket - In Arbeit... #

# Judo Pose Analysis — Ippon-Seoi-nage Klassifikation

Dieses Projekt erkennt und klassifiziert die Judo-Technik **Ippon-Seoi-nage** anhand von Körper-Keypoints, die aus selbst aufgenommenen Videos extrahiert wurden.

---

## Über das Projekt

Mithilfe von **Pose Estimation** werden aus Videoaufnahmen Skelett-Keypoints extrahiert und anschließend mit einem Machine-Learning-Modell klassifiziert. Ziel ist es, die charakteristische Bewegungsstruktur des Ippon-Seoi-nage automatisch zu erkennen.

**Pipeline:**
```
Video → Frame-Extraktion → Keypoint-Erkennung (MediaPipe) → Feature-Aufbereitung → Klassifikation (scikit-learn)
```

---

## Technologien

| Library | Verwendung |
|---|---|
| [MediaPipe](https://mediapipe.dev/) | Pose Estimation & Keypoint-Extraktion |
| [OpenCV](https://opencv.org/) | Video-/Bildverarbeitung, Frame-Extraktion |
| [scikit-learn](https://scikit-learn.org/) | Klassifikationsmodell |
| [Jupyter Notebook](https://jupyter.org/) | Analyse & Entwicklung |

---

## Daten

Die Trainingsdaten wurden **selbst erhoben**:

1. Videos von Ippon-Seoi-nage-Ausführungen aufgenommen
2. Frames aus den Videos extrahiert (via OpenCV)
3. Körper-Keypoints pro Frame mit MediaPipe detektiert
4. Keypoints als strukturierte Datenpunkte gespeichert

Die aufbereiteten Daten liegen im Ordner [`Data/`](./Data/).

> ⚠️ Rohdaten (Videos/Originalbilder) sind nicht im Repository enthalten.

---

## Projektstruktur

```
judo-pose-analysis/
├── Data/               # Extrahierte Keypoint-Daten
├── *.ipynb             # Jupyter Notebooks (Analyse & Modell)
└── .gitignore
```

---

## Setup & Ausführung

### Voraussetzungen

- Python 3.8+
- Jupyter Notebook oder JupyterLab

### Installation

```bash
git clone https://github.com/DaKrieger-stack/judo-pose-analysis.git
cd judo-pose-analysis
pip install mediapipe opencv-python scikit-learn jupyter numpy pandas
```

### Starten

```bash
jupyter notebook
```

Dann das gewünschte Notebook im Browser öffnen und ausführen.

---

## Analysierte Technik

**Ippon-Seoi-nage** (一本背負投) ist ein klassischer Judo-Schulter-Wurf, bei dem der Angreifer den Gegner über die Schulter wirft. Die Analyse fokussiert sich auf die charakteristischen Körperpositionen und Gelenkwinkel während der Wurfbewegung.

---

## Lizenz

Privates Projekt – kein öffentlicher Einsatz vorgesehen.