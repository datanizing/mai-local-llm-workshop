# Lokale Sprachmodelle effizient betreiben

Repository zum Workshop.

## Pakete
Folgende Basispakete sollten installiert sein:

* `numpy`
* `pandas`
* `tqdm`
* `sklearn`
* `matplotlib`
* `seaborn`

Für die Vorverarbeitung der Daten brauchen wir `spacy`.

Das Finden von Informationen geschieht mit:

* `sentence_transformers`
* `tantivy`
* `usearch`

Für die Inferenz der generativen Modelle wird folgendes benötigt:
* `vllm`
* `sglang`
* `openai`

Alternativ gern `pyproject.toml` verwenden. Für `unsloth` und `vllm`
wird `unsloth.toml` benötigt, `sglang` benötigt leider aktuell eine
eigene Umgebung, weil das Gemma-Modell in der neuesten Version von `sglang`
nicht funktioniert.
Wenn sich nicht alles installieren lässt, klären wir das direkt im
Workshop. 

Es läuft auch unter Windows, allerdings ist die Installation etwas
*hakelig*. Gleiches gilt für AMD-Grafikkarten, das kann ich ohne
entsprechende Karte leider nicht testen.

Bei Macs bitte das `.cuda()` entfernen.

Wir arbeiten mit unterschiedlichen Sprachmodellen. Je nach Internet-Verbindung
kann es sinnvoll sein, diese vorher herunterzuladen:

## Modelle
Für die Einleitung verwenden wir:
* google-bert/bert-base-multilingual-cased
* nlptown/bert-base-multilingual-uncased-sentiment
* MoritzLaurer/mDeBERTa-v3-base-mnli-xnli

Für Embeddings nutzen wir diese Modelle:
* multi-qa-MiniLM-L6-cos-v1
* google/embeddinggemma-2
* microsoft/harrier-oss-v1-0.6b

Wir benutzen folgende Cross-Encoder:
* cross-encoder/ms-marco-MiniLM-L-6-v2
* mixedbread-ai/mxbai-rerank-large-v1

Bei der generativen Inferenz arbeiten wir mit diesen Modellen:
* Qwen/Qwen3.5-9B
* google/gemma-4-12B-it
* google/gemma-4-12B-it-qat-w4a16-ct
* google/gemma-4-12B-it-assistant
* turboderp/Qwen3.8-27B-exl3 
* GestaltLabs/Qwen3.8-27B-DFlash-EXL3-4bit
* ISTA-DASLab/Qwen3.8-27B-GSQ-RCO-GGUF
* neroued/Qwen3.8-27B-NInfer
