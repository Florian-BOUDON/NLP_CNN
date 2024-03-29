# NLP : Analyse de données textuelles 
# CNN : Réseau de neurones convolutif (TensorFlow) 

### Etude de faisabilité d'un moteur de classification, basé sur une description et sur une image

Cette étude vise à comparer deux approches, le notebook 1 classe les images selon leur description et le notebook 2 classe les images en utilisant une méthode de transfert Learning basée sur VGG16.

### Notebook 1 NLP: Analyse des descriptions textuelles 

Un prétraitement des données textuelles:
- Enlever la **ponctuation**
- Enlever les **chiffres**
- Transformer les phrases en **liste de tokens** (en liste de mots)
- Enlever les **stopwords** (mots n'apportant pas de sens)
- **Lemmatizer**
- Enlever les **majuscules**
- **Reformer les phrases** avec les mots restants

Comparaison de 4 méthodes afin d’extraire les features texte : 
- Deux approches de type **bag-of-words**, comptage simple de mots et **Tf-idf** 
- Une approche de type word/sentence embedding classique avec **Word2Vec**
- Une approche de type word/sentence embedding avec **BERT** 
- Une approche de type word/sentence embedding avec **USE**(Universal Sentence Encoder)
  
Une réduction en 2 dimensions **T-SNE**, afin de projeter les produits sur un graphique 2D, sous la forme de points dont la couleur correspondra à la catégorie réelle.             
Réalisation d’une mesure pour confirmer l'analyse visuelle, en calculant la similarité entre les catégories réelles et les catégories issues d’une segmentation en clusters, basée sur **l'ARI**.     
Démonstration, par cette approche, de la faisabilité du regroupement automatique des produits de même catégorie.

### Notebook 2 CNN :  réseau de neurones convolutifs

Comparaison de deux méthodes:
- Extraction des features des images : algorithme de type **SIFT**
   Créations des descripteurs de chaque image         
      - Pour chaque image : passage en gris et equalisation      
      - Création d'une liste de descripteurs par image ("sift_keypoints_by_img") qui sera utilisée pour réaliser les histogrammes par image       
      - Création d'une liste de descripteurs pour l'ensemble des images ("sift_keypoints_all") qui sera utilisée pour créer les clusters de descripteurs     
- Un algorithme de type CNN transfer learning : **VGG16** (google)

Une réduction en 2 dimensions **T-SNE**, afin de projeter les produits sur un graphique 2D, sous la forme de points dont la couleur correspondra à la catégorie réelle.      
Réalisation d’une mesure pour confirmer l'analyse visuelle, en calculant la similarité entre les catégories réelles et les catégories issues d’une segmentation en clusters, basée sur **l'ARI**.        
Démonstration, par cette approche, de la faisabilité du regroupement automatique des produits de même catégorie.    

*********
Ce projet fait partie de la formation data-scientist par CentraleSupélec & Openclassrooms (certificat bac+5).





