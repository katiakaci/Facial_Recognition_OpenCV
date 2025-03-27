# reconnaissance-faciale

Voici l'enoncé et le tutoriel à suivre: [Énoncé](https://cours.etsmtl.ca/mti805/private/labos/laboratoire1.pdf) & [Tutoriel](https://pyimagesearch.com/2018/09/24/opencv-face-recognition/).

Voici les étapes importantes à connaitre pour démarrer le code.

### Pip Install

Pour commencer faire une pip install dans la console (PowerShell ou CMD). Donc faire la commande suivante: `pip install imutils numpy argparse opencv-contrib-python scikit-learn`

### Sortir les Embeddings des images de training (dataset)

Faire la commande suivante dans la console pour starter le code: `python extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7`

### Entrainer le model

Faire la commande suivante dans la console pour starter le code: `python train_model.py --embeddings output/embeddings.pickle --recognizer output/recognizer.pickle --le output/le.pickle`

### Tester le model

Faire la commande suivante dans la console pour starter le code: `python recognize.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle --image images/[nom de l'image]`

Simplement remplacer [nom de l'image] par l'image qu'on souhaite tester.

Faire la commande suivante pour reconnaitre un visage dans une vidéo: `python recognize_video.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle`
