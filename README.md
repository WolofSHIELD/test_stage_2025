**Objectif du Challenge**
 
Ce problème a pour but d'implémenter, en Rust ou en langage C, les principaux composants du cryptosystème TFHE (Fast Fully Homomorphic Encryption over the Torus), dans le cadre d'une démonstration simple de chiffrement homomorphe. Plus précisément, il s'agit de :

Chiffrer un message de 3 bits (valeur entière entre 0 et 7),

Évaluer de manière homomorphe des fonctions arithmétiques (addition, multiplication) sur ce message chiffré,

Déchiffrer à la fois le message initial et le résultat de l’évaluation,

Documenter le processus de manière reproductible et modulaire.

**Organisation du Challenge**

Une structure ce challenge claire est essentielle pour faciliter le développement, la lisibilité du code, et les tests. Le challenge sera organisé dans un dossier nommé RUST_tfhe/ ou C_tfhe/ selon le langage choisi.

Résumé des fichiers à nommer proprement

Dossier / Fichier	Rôle

main.rs ou main.c : lancement du programme

encryption.rs / .c : chiffrement du message

decryption.rs / .c	: déchiffrement du message

evaluation.rs / .c	: application des fonctions homomorphes

tests/test_vectors.txt	Exemples d’entrée/sortie attendus

doc/rapport.pdf ou .md	Détail du fonctionnement, schémas si besoin

CANDIDAT_Nom_Prenom.txt	Fiche d’identité technique à envoyer par mail : **wolofshield@gmail.com**

**Début Du Challenge**

**Fonctionnalités à implémenter, Encodage du message :**

Encodage sur 3 bits (valeurs 0 à 7),

Optionnel : affichage du message original pour vérification.

**Chiffrement homomorphe avec TFHE :**

1. Génération de la clé secrète, du masque, en utilisant le LWE/TLWE selon l'approche TFHE.
2. Chiffrer un message de 3 bits selon l’approche TFHE.

**Implémentation d'évaluation d’un chiffrement bit-à-bit du message.**

3. Soit la fonction affine : 𝑓(𝑥)=3𝑥+2. Évaluatrer bit-à-bit en exploitant les opérations logiques et arithmétiques supportées par TFHE

**Déchiffrement**:

4. Déchiffrement du message initial,
5. Déchiffrement du résultat de l’évaluation,
6. Comparaison des résultats avec les valeurs attendues en clair (pour vérification).

**Quelques Métriques**

7. Mesurer le temps de chiffrement et de déchiffrement, ainsi que la capacité mémoire utilisée lors de l'exécution du chiffrement et du déchiffrement.
8. Dire si ces algorithmes implémentées sont en temps constants ou pas. Sinon quel impact pourrait-on s'attendre quant à l'implémentation matérielle ?
9. Expliquer rapdiement le bootstrapping et dire son lien avec notre fonction d'évaluation : f(x)=3x+2


**Fin Du Challenge**


**Contraintes et remarques**

On pourra travailler sur ℤ/16ℤ dans tout le challenge. La fonction 𝑓(𝑥)=3𝑥+2 est considérée comme fonction de référence pour la vérification du bon fonctionnement du chiffrement et de l’évaluation. Les fonctions homomorphes doivent être implémentées en respectant les limitations de TFHE (opérations logiques / arithmétiques bit-à-bit). La sécurité cryptographique n’est pas l’objectif principal ici : l’accent est mis sur la compréhension et la démonstration du fonctionnement de TFHE. 
L’ensemble du **Challenge** doit être suffisamment documenté pour permettre à un tiers (correcteur, lecteur) de reproduire et comprendre les étapes de bout en bout.

