
# Score F1

## 1. Définition
Le score F1 représente la moyenne harmonique de la précision (proportion de 
prédictions positives correctes) et du rappel (proportion de cas positifs réels 
correctement identifiés).

On le calcule avec la formule suivante :

$$ F1 = 2 \times \frac{ \text{Précision} \times \text{Rappel}}{ \text{Précision} + \text{Rappel}} $$

## 2. Asymétrie
Le score F1 peut varier lorsqu'on inverse les labels positifs et négatifs dans les 
données. Cette asymétrie est due à la dépendance de la précision et du rappel 
vis-à-vis de la classe définie comme positive.

### Exemple 
Supposons un ensemble de 10 instances avec 8 de la classe A et 2 de la classe B. 
Considérons que les résultats de prédiction sont les suivants :

- True Positives : 5
- False Negatives : 8 - 5 = 3
- True Negatives : 1
- False Positives : 2 - 1 = 1

Calcul du score F1 si l'on considère la classe A comme positive :
- Précision = 5 / 6 ≈ 0.83
- Rappel = 5 / 8 = 0.625
- Score F1 ≈ 0.71

Calcul du score F1 si l'on considère la classe B comme positive :
- Précision = 0.25
- Rappel = 0.5
- Score F1 ≈ 0.33


## 3. Conclusion
Se méfier des métriques qui paraissent intuitives mais qui ne le sont pas. 
Pour les modèles de classification, utiliser la **matrice de confusion** !!