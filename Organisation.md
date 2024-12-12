## Pourquoi le deep learning est important en cryo-tomographie electronique dans l'identification et la comprehension des complexes proteiques 

Les protéines dans notre corps jouent un rôle crucial pour nous maintenir en bonne santé. Par exemple, l’hémoglobine transporte l’oxygène dans notre sang, et la kératine est essentielle pour nos cheveux. Ces protéines travaillent souvent ensemble en formant des "complexes protéiques" – comme une équipe qui collabore pour accomplir une tâche.

Pour comprendre comment ces complexes fonctionnent, les scientifiques utilisent une technologie spéciale appelée cryo-tomographie électronique (cryoET). Elle crée des images 3D très détaillées des cellules et des protéines, directement dans leur environnement naturel. C’est un peu comme explorer une forêt et observer les animaux dans leur habitat, mais ici, on regarde à l'intérieur des cellules.

Le problème, c’est que ces images sont très complexes et difficiles à analyser. Les protéines y apparaissent dans tous les sens, et c’est un vrai défi de dire où se trouve chaque type de protéine. Actuellement, même avec ces super images, les scientifiques ont du mal à identifier les protéines, même celles qui sont faciles à reconnaître à l’œil nu.

## Defi du concour Kaggle

 Créer un programme d’intelligence artificielle capable d’identifier automatiquement cinq types de complexes protéiques sur des images 3D (encore appelees tomogrammes). Si on y arrive, cela aidera les chercheurs à mieux comprendre les cellules, à découvrir de nouvelles protéines "cachées" (comme des trésors encore non explorés), et à avancer dans la recherche pour la santé humaine.

En résumé, il s’agit d’entraîner des ordinateurs à "voir" et reconnaître des protéines dans des images compliquées, un peu comme un détective qui identifierait des objets dans une pièce très encombrée.

## Metriques d'evaluation 

#### Type d'apprentissage: **Apprentissage supervisee**
#### Sous categorie correspondante: **Classification**
#### Metrique d'evaluation: F_4. 

Cette métrique combine à la fois la précision et le rappel dans son évaluation. La F_4 accorde quatre fois plus d'importance au rappel qu'à la précision.Mais pourquoi??? 
La précision fait référence à la quantité  des particules correctement identifiées par le modèle, tandis que le rappel met l'accent sur le nombre de particules détectées. Ici la proportion de particules détectées a plus d'importance car les scientifiques ne veulent pas passer à côté de phénomènes clés s'opérant au cours du fonctionnement de la cellule.

### Particule Vraie:

Une particule détectée par le modèle est considérée comme correcte si elle est suffisamment proche de la position d’une vraie particule dans l’image, c’est-à-dire dans un rayon 0,5 fois la taille d'une particule réelle.

### Poids associes aux  particules dans la metrique d'evaluation:

**Particules  Faciles**: Ribosome, particules de type viral, apo-ferritine (poids = 1).

**Particules Difficiles**: Thyroglobuline, β-galactosidase (poids = 2).

Ces poids influencent la façon dont les erreurs sont comptées :
Les erreurs sur les particules « difficiles » sont plus graves, car elles comptent deux fois plus dans le calcul de la métrique que les erreurs sur les particules « faciles ».

### Comment s'evalue la metrique?

La métrique évalue les performances globales sur toutes les images, en s’assurant que les résultats soient équilibrés. Les particules de bêta-amylase sont là uniquement pour enrichir l’entraînement, mais elles n’affectent pas les scores.


### Deroulement du concour:

- 6 novembre 2024 – Date de début.
- 29 janvier 2025 – Date limite d’inscription.
- 29 janvier 2025 – Date limite de fusion des équipes.
- 5 février 2025 – Date limite de soumission finale.

### Prix

- 1ère place – 15 000 $
- 2e place – 12 000 $
- 3e place – 10 000 $
- 4e place – 7 000 $
- 5e place – 6 000 $
- 6e place – 5 000 $
- 7e place – 5 000 $
- 8e place – 5 000 $
- 9e place – 5 000 $
- 10e place – 5 000 $


### Rapport du concour 

Au cas ou on obtenait une place parmi les prix on devrait fournir un rapport d'environ 4 pages,  rediger  en anglais incluant les details techniques. Rapport a fournir au plus grand tard 02 semaines apres la soumission. 

### Dossier de soumission

- Nom du fichier de soumission: `submission.csv`
- Code dans un notebook jupyter

- Apercu du fichier de soumission:

```id,experiment,particle_type,x,y,z
0,TS_5_4,beta-amylase,2983.596,3154.13,764.124
1,TS_5_4,beta-amylase,2983.596,3154.13,764.124
2,TS_5_4,beta-galactosidase,2983.596,3154.13,764.124
etc.
```






### Qui sont les commanditaires du concour?
Chan Zuckerberg Imaging Institute.




