GALERIE DE MARIAGE - CLOUDFLARE PAGES + R2

Ce ZIP ajoute les fonctions Pages sous /functions. Il conserve les fichiers visuels d'origine.

1. Dans Workers et Pages > votre site > Paramètres > Variables et secrets :
   - Secret INVITE_CODE = code commun choisi (ne pas mettre le code dans le HTML/JS)
   - Secret ADMIN_SECRET = une autre valeur longue et aléatoire, distincte du code invité
   Vérifier les NOMS EXACTS des variables. Les secrets sont lus côté serveur uniquement.
2. Dans Liaisons : compartiment R2 avec nom de variable MARIAGE_PHOTOS
   vers mariage-laetitia-frederic-2027.
3. Déployer le contenu de ce ZIP sur le projet Pages EXISTANT, en conservant
   l'arborescence /functions. Le tableau de bord doit indiquer les fonctions.
4. Tester avec un mauvais code (refus), puis le bon code, puis une petite photo.
5. Laisser l'accès public R2 désactivé. Ne pas créer de clé API R2.

IMPORTANT : Ne pas déployer tant que INVITE_CODE et ADMIN_SECRET ne sont pas
configurés. Cette version est une base fonctionnelle pour petits volumes ;
les gros volumes, les vidéos longues et la modération nécessiteront des améliorations.
La limite est de 30 Mo par fichier. Les coûts R2 ne sont pas plafonnés automatiquement.
Les opérations d'upload via formulaire consomment de la mémoire et du quota Workers.
Le listing est limité à 1000 objets par page et devra être amélioré pour >1000 souvenirs.
La modération masque un objet mais ne le supprime pas du stockage facturable.
