# Hangman

---

### Objectif du projet : Hangman

L'objectif de ce projet est de créer un jeu de Hangman en ligne de commande en Go, avec des fonctionnalités et une structure spécifiées dans les deux parties suivantes.

### **Partie 1 : Règles du jeu**

1. **Chargement des mots** :  
   Le jeu commence en prenant un fichier en paramètre (par exemple, `words.txt`), contenant une liste de mots (un mot par ligne, séparés par des retours à la ligne). Le programme sélectionnera un mot au hasard dans ce fichier pour démarrer la partie.

2. **Révélation des lettres** :  
   Une fois qu'un mot est choisi, le programme révélera un certain nombre de lettres aléatoires de ce mot. Le nombre de lettres à révéler sera égal à `n = (len(word) / 2) - 1` (la moitié de la longueur du mot, moins un).

3. **Tentatives** :  
   Le joueur aura 10 tentatives pour deviner le mot. À chaque tentative, le programme attendra une lettre de l'utilisateur via l'entrée standard.
   
   - **Si la lettre n'est pas présente dans le mot** :  
     Le programme affiche un message d'erreur et réduit le nombre de tentatives restantes.
   
   - **Si la lettre est présente dans le mot** :  
     Le programme révèlera toutes les lettres correspondantes à cette lettre dans le mot.
   
   Le jeu continue jusqu'à ce que le joueur trouve le mot ou que le nombre de tentatives atteigne 0.

4. **Fin du jeu** :  
   Si le joueur devine correctement toutes les lettres du mot avant que les tentatives ne soient épuisées, il gagne. Sinon, il perd et devra affronter la malheureuse destinée de José, le personnage pendu.

---

### **Partie 2 : L'Histoire de José**

Si le joueur perd, sera affichée en fonction du nombre de tentatives restantes.

1. **Fichier `hangman.txt`** :  
   Vous recevrez un fichier nommé `hangman.txt` contenant les positions de José à afficher à chaque tentative échouée. Ce fichier comportera 10 positions (une pour chaque tentative).

2. **Format du fichier `hangman.txt`** :  
   Chaque position du pendu est représentée par un dessin ASCII de hauteur 7 lignes et longueur 9 caractères. Chaque position est séparée par une nouvelle ligne.

   Exemple d'une position (la septième position) :
   
   ```
     +---+  
     |   |  
     O   |  
    /|   |  
         |  
         |  
   =========
   ```

   - **Premier essai** : Le dessin du pendu sera vide.
   - **Dernier essai (10ème)** : Le dessin du pendu sera complet, symbolisant la fin tragique de la partie.

3. **Affichage dynamique** :  
   Le programme doit parser ce fichier et afficher le dessin approprié de José en fonction du nombre de tentatives restantes. À chaque erreur de lettre, le dessin sera mis à jour pour montrer José dans une position de plus en plus désespérée.

---

### **Structure et fonctionnement** :

- Le jeu utilise un fichier `words.txt` pour charger les mots, et un fichier `hangman.txt` pour afficher l'illustration du pendu à chaque tentative.
- Le programme doit gérer l'affichage dynamique du mot à deviner, des lettres révélées, des lettres incorrectes et des tentatives restantes.
- Un mécanisme de contrôle du jeu doit être mis en place pour gérer l'entrée de l'utilisateur et la progression du jeu.
- Les fichiers d'illustration (positions de José) doivent être correctement analysés et utilisés pour afficher l'image en fonction de l'état du jeu.

---

### Exigences techniques :
- Le programme doit être écrit en Go.
- Le jeu se joue en ligne de commande, et l'interaction se fait via des entrées utilisateur pour deviner des lettres.
- La gestion des fichiers (lecture des mots et des positions de José) doit être efficace et correcte.
- Le programme doit afficher des messages appropriés et des illustrations ASCII selon l'état du jeu.

Ce projet est un excellent moyen de démontrer votre capacité à gérer la logique d'un jeu, à manipuler des fichiers et à afficher du texte formaté en Go.
