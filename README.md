# EXERCICE 1 : Mini-jeu de devinette de nombre

## Objectif
Créer un jeu où l'utilisateur doit deviner un nombre aléatoire entre 0 et 99.  
À chaque essai, un message s'affiche pour indiquer si le nombre recherché est plus grand, plus petit ou si l'utilisateur a trouvé la bonne réponse.

---

### Consignes pour le code HTML

1. Ajoutez un titre (`<h1>`) pour expliquer le but du jeu.
2. Créez un champ de saisie (`<input>`) avec `type="number"` pour que l'utilisateur puisse entrer un nombre.
3. Ajoutez un bouton (`<button>`) pour vérifier la devinette.
4. Préparez un espace de texte (`<p>`) pour afficher les messages (correct, plus grand, plus petit).

---

### Consignes pour le code JavaScript

1. **Nombre à deviner** : Utilisez le code suivant pour générer le nombre aléatoire entre 0 et 99 :
 
   ```javascript
   const randomNumber = Math.floor(Math.random() * 100);
   ```

2. **Bouton de vérification** : Sélectionnez le bouton en utilisant `document.getElementById`.

3. **Ajouter l’événement `click`** :

 - Ajoutez un `click` sur le bouton pour lancer la vérification.
 - Dans cet événement :
   - Récupérez la valeur du champ de saisie et convertissez-la en nombre avec `parseInt`.
   - Comparez ce nombre avec `randomNumber`.
   - Affichez un message différent selon le résultat :
     - "Bravo, vous avez trouvé !" si le nombre est correct.
     - "C'est plus grand !" si la devinette est trop petite.
     - "C'est plus petit !" si la devinette est trop grande.
