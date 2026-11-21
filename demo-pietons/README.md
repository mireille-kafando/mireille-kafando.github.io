# Démo : détection de piétons (YOLOv8n) dans le navigateur

Page : https://mireille-kafando.github.io/demo-pietons/

- `model/v2.onnx` et `model/v1.onnx` : poids de la v2 (`v2/best_v2.pt`) et de la v1 (`models/best.pt`) du projet [pedestrian-detection-adas](https://github.com/mireille-kafando/pedestrian-detection-adas), exportés par `demo/export_onnx.py`. Licence AGPL-3.0, comme Ultralytics. La page charge la v2 ; la v1 n'est téléchargée que si on la choisit.
- `ort/` : ONNX Runtime Web 1.31.1 (licence MIT), version WebAssembly.
- `exemples/bus.jpg` : image d'exemple fournie avec la bibliothèque Ultralytics.

Le prétraitement (redimensionnement rectangulaire au multiple de 32) et la suppression des doublons (NMS, IoU 0,7) reproduisent ceux d'Ultralytics ; sur l'image d'exemple, la page retrouve les mêmes détections.
