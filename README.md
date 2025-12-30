# Detection-Maladie-Pulmonaire
Classification de radiographies pulmonaires (pneumonie, COVID-19, sain) via ResNet pré-entraîné (fine-tuning) et interface Tkinter pour afficher le diagnostic

## Arborescence des fichiers
├── interface.ipynb # Interface principale pour tester avec une image

├── evaluation.ipynb # Métriques d’évaluation

├── code.ipynb # Traitement de données + entraînement du modèle

├── best_model.pth # Contient le modèle entraîné 

├── data/ # Quelques données de test

├── Rapport.pdf # Rapport sur le projet

└── README.pdf # Ce fichier
## Utilisation
### Tester le modèle avec une image
Pour tester le modèle sur une image, ouvrez et exécutez interface.ipynb.
Ce notebook permet de charger une image et d’obtenir une prédiction du modèle.
#### Fonctionnement de l’interface :
L’utilisateur clique sur le bouton « Choisir une radiographie » afin de sélectionner 
une radiographie provenant de l’un des trois répertoires suivants :
- Covid
- Pneumonia
- Normal
#### Affichage du diagnostic :
- Si le modèle prédit un cas de COVID-19 ou de Pneumonie, le diagnostic est 
affiché en rouge.
- Si le modèle prédit un cas Normal, le diagnostic est affiché en vert.
Le résultat inclut également un pourcentage de confiance, reflétant la probabilité 
estimée de la prédiction selon l’entraînement du modèle.

### Validation et évaluation
Si vous souhaitez consulter les performances du modèle (matrice de confusion,
cross-validation, classification report, accuracy sur les tests), ouvrez le notebook 
evaluation.ipynb.

###  Ne pas relancer l’entrainement
Le fichier code.ipynb continent : 
- Le code de traitement des données
- L’entrainement du modèle

!!! Ce notebook n'est pas conçu pour être relancé systématiquement. Il est long et 
nécessite beaucoup de ressources.
Servez-vous-en uniquement comme référence pour comprendre l’implémentation
