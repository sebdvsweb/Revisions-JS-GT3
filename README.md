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

 Remarques :
   **Math.random()** génère un nombre décimal aléatoire entre 0 (inclus) et 1 (exclus). En multipliant le nombre aléatoire par 100, on obtient un nombre décimal compris entre 0 et    99.9999.... Cela permet d'atteindre n'importe quelle valeur décimale dans cette plage, comme 45.67 ou 82.91. 
   
   **Math.floor()** "arrondit vers le bas" le nombre aléatoire obtenu. Par exemple, 45.67 deviendra 45, et 82.91 deviendra 82. Cela nous permet d'obtenir un nombre entier entre 0 et 99. 


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


# Exercice 2 : Contrôler une animation CSS avec JavaScript

### Objectif
Créer une page où l'utilisateur peut activer, désactiver, et ajuster la vitesse d'une animation en cliquant sur des boutons.

![Animation JS](https://sebastien-devos.fr/img/codegt/animation-js.png "Animation JS").

---

### Consignes pour le code HTML

1. Créez un conteneur (`<div>`) pour occuper tout l’écran.
2. Dans ce conteneur :
   - Ajoutez une `div` ronde avec une bordure blanche en pointillés, qui sera l’élément animé.
   - Ajoutez une section de contrôle avec trois boutons :
     - Un bouton pour activer/désactiver l'animation ("ON"/"OFF").
     - Deux boutons pour ajuster la vitesse (`-` et `+`).

---

### Consignes pour le CSS

1. **Structure et style de base** :
   - Centrez le contenu de la page avec flexbox.
   - Appliquez un fond noir à la page et une bordure blanche en pointillés à la `div` ronde.
   
2. **Animation** :
   - Définissez une animation de rotation qui tourne à 360° (utilisez des `keyframes` pour lacréer).
   - Masquez la `div` ronde par défaut (elle n'apparaîtra que quand l’animation sera activée).

---

### Consignes pour le JavaScript

1. **Bouton ON/OFF** :
   - Ajoutez un événement `click` sur le bouton ON/OFF :
     - Si l'animation est OFF, activez-la en affichant la `div` et en lançant l’animation.
     - Si l'animation est ON, désactivez-la en cachant la `div`.
   
2. **Contrôle de la vitesse** :
   - Ajoutez des événements `click` aux boutons `+` et `-` :
     - Le bouton `+` augmente la vitesse de rotation.
     - Le bouton `-` ralentit la vitesse de rotation.

---

### Résultat attendu
L'utilisateur peut activer et désactiver l'animation de la `div` ronde avec le bouton ON/OFF, et ajuster la vitesse avec les boutons `+` et `-`.
