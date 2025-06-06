<h1><code>Module 323</code> - Programmer de manière fonctionnelle</h1>

# 😅 Exercice XX - Entraînement à map().filter().reduce()

## Objectifs

- S'entraîner à l'utilisation de ces méthodes incontournables de programmation fonctionnelle que sont `map()`, `filter()` et `reduce()`.

## Rapports à produire

Dans le fichier [ex04-data.js](/src/ex04-data.js) vous disposez, directement au format JSON, d'une extraction d'**un grand nombre de notes d'une base de données des notes d'un établissement scolaire**.

Vous allez devoir filtrer, réduire et ne prendre que la partie nécessaire de ces données qui correspondent à une liste de demandes spécifiques.

>[!TIP]
>**N.B.** : Observez les noms des rapports à produire (libellés sur les boutons). Ils vous indiquent clairement si vous devez retourner un tableau [] ou un objet {}.

Les rapports à produire :

- [A1 - \[Branches\], trié](#a1---branches-trié)
- [A2 - \[Prénom NOM\], trié](#a2---prénom-nom-trié)
- [B - {Branches : nbre de notes}](#b---branches--nbre-de-notes)
- [C - \[{Branche, nbre notes}\], trié](#c---branche-nbre-notes-trié)
- [T1 - Apprentis contenant      Partie connue](#t1---apprentis-contenant------partie-connue)
- [T2 - Total évaluations de cette branche](#t2---total-évaluations-de-cette-branche)
- [D - \[{Branche, moyenne}\], trié](#d---branche-moyenne-trié)
- [E - \[{Branche, nbre, moyenne}\], trié](#e---branche-nbre-moyenne-trié)
- [F - \[{Elève, \[branches, \[notes\]\]}\], trié](#f---elève-branches-notes-trié)
- [G - \[{Elève, \[branches, nbre, min, max, moyenne, \[notes\]\]}\], trié](#g---elève-branches-nbre-min-max-moyenne-notes-trié)
- [H -\[{Elève, \[branches, nbre, min, max, moyenne, \[{date, note}\]\]}\], trié](#h--elève-branches-nbre-min-max-moyenne-date-note-trié)

### A1 - [Branches], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   "Allemand",
   "Anglais",
   "Chimie",
   "Français",
   "Géographie",
   "Histoire",
   "Maths",
   "Physique"
]
```

### A2 - [Prénom NOM], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   "Alain TERNET",
   "Alain TERRIEUR",
   "Alex TERRIEUR",
   "Claire VOYANTE",
   "Eddy FICE",
   "Guy TARISTE",
   "John D'ŒUF",
   "Mac HARONI",
   "Remy NISSENS",
   "Théo RIQUE"
]
```

### B - {Branches : nbre de notes}

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
{
   "Allemand": 78,
   "Anglais": 83,
   "Chimie": 84,
   "Français": 86,
   "Géographie": 85,
   "Histoire": 82,
   "Maths": 84,
   "Physique": 84
}
```

### C - [{Branche, nbre notes}], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   {
      "branche": "Allemand",
      "count": 78
   },
   {
      "branche": "Anglais",
      "count": 83
   },
   {
      "branche": "Chimie",
      "count": 84
   },
   {
      "branche": "Français",
      "count": 86
   },
   {
      "branche": "Géographie",
      "count": 85
   },
   {
      "branche": "Histoire",
      "count": 82
   },
   {
      "branche": "Maths",
      "count": 84
   },
   {
      "branche": "Physique",
      "count": 84
   }
]
```

### T1 - Apprentis contenant      Partie connue

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

Si aucun texte n'est fourni :

```json
[
   "Alain TERNET",
   "Alain TERRIEUR",
   "Alex TERRIEUR",
   "Claire VOYANTE",
   "Eddy FICE",
   "Guy TARISTE",
   "John D'ŒUF",
   "Mac HARONI",
   "Remy NISSENS",
   "Théo RIQUE"
]
```

Si le texte 'eR' est fourni :

```json
[
   "Alain TERNET",
   "Alain TERRIEUR",
   "Alex TERRIEUR"
]
```

### T2 - Total évaluations de cette branche

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

Si aucune branche n'est fournie :

```json
666
```

Si la branche 'MaTHs' est fournie :

```json
84
```

### D - [{Branche, moyenne}], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   {
      "branche": "Allemand",
      "moyenne": 4.28
   },
   {
      "branche": "Anglais",
      "moyenne": 4.39
   },
   {
      "branche": "Chimie",
      "moyenne": 4.26
   },
   {
      "branche": "Français",
      "moyenne": 4.22
   },
   {
      "branche": "Géographie",
      "moyenne": 4.33
   },
   {
      "branche": "Histoire",
      "moyenne": 4.33
   },
   {
      "branche": "Maths",
      "moyenne": 4.5
   },
   {
      "branche": "Physique",
      "moyenne": 4.31
   }
]
```

### E - [{Branche, nbre, moyenne}], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   {
      "branche": "Allemand",
      "count": 78,
      "moyenne": 4.28
   },
   {
      "branche": "Anglais",
      "count": 83,
      "moyenne": 4.39
   },
   {
      "branche": "Chimie",
      "count": 84,
      "moyenne": 4.26
   },
   {
      "branche": "Français",
      "count": 86,
      "moyenne": 4.22
   },
   {
      "branche": "Géographie",
      "count": 85,
      "moyenne": 4.33
   },
   {
      "branche": "Histoire",
      "count": 82,
      "moyenne": 4.33
   },
   {
      "branche": "Maths",
      "count": 84,
      "moyenne": 4.5
   },
   {
      "branche": "Physique",
      "count": 84,
      "moyenne": 4.31
   }
]
```

### F - [{Elève, [branches, [notes]]}], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   {
      "eleve": "Alain TERNET",
      "branches": [
         {
            "branche": "Français",
            "notes": [
               4,
               4.3,
               4.7,
               5.5,
               4.8,
               2.8,
               4.1,
               3.5,
               4.6,
               4,
               4,
               4.2,
               4,
               4.2,
               3.9,
               4,
               4.8
            ]
         },
         {
            "branche": "Allemand",
            "notes": [
               3.9,
               3.7,
               4.1,
               2.9,
               3.8,
               4.8,
               4.8,
               6,
               5.7,
               5.2,
               5.7,
               3,
               4.5
            ]
         },
         {
            "branche": "Histoire",
            "notes": [
               4.9,
               5.7,
               4.7,
               4.9,
               3.2,
               4.9,
               3.8,
               4.9,
               3.4,
               5.5,
               5.7,
               5,
               5.6
            ]
         },
         {
            "branche": "Chimie",
            "notes": [
               3.1,
               4.5,
               5.6,
               5.1,
               4.3,
               4.8,
               3.3,
               4.1,
               2.7,
               2.8,
               5,
               4.3,
               3.8,
               4.2,
               6,
               4.4,
               3.2,
               4.1,
               3.1,
               3.5
            ]
         },
         {
            "branche": "Géographie",
            "notes": [
               4.6,
               4.8,
               3.3,
               3.7,
               2.9,
               4.9,
               4.5,
               5.5,
               3.1,
               4.4,
               3.8,
               3.2,
               5.7,
               4.7,
               5.6,
               5.8
            ]
         },
         {
            "branche": "Anglais",
            "notes": [
               3.8,
               2.9,
               3.2,
               4.1,
               5.8,
               4.9,
               3.4,
               5.6,
               3.7,
               4.1,
               3.3,
               2.7,
               3.1
            ]
         },
         {
            "branche": "Physique",
            "notes": [
               3.1,
               3.5,
               3.4,
               4.7,
               2.8,
               5.3,
               3.5,
               2.9,
               3.3,
               3.5,
               5.5
            ]
         },
         {
            "branche": "Maths",
            "notes": [
               5.8,
               5,
               4.7,
               3,
               3.9,
               5.2,
               4.1,
               5.2,
               4.9,
               5,
               5.5
            ]
         }
      ]
   },
   {
      "eleve": "Alain TERRIEUR",
      "branches": [
         {
            "branche": "Physique",
            "notes": [
               3.3,
               5,
               3.7,
               4.7,
               2.7,
               5,
               5.1,
               4.2,
               4.3,
               3.4,
               5.3
            ]
         },
         {
            "branche": "Histoire",
            "notes": [
               2.7,
               5.9,
               4.2,
               4.5,
               3.3,
               3.6,
               3.8
            ]
         },
         {
            "branche": "Chimie",
            "notes": [
               3.1,
               6,
               4.1,
               5.2,
               4.2,
               5.4,
               4.7
            ]
         },
         {
            "branche": "Géographie",
            "notes": [
               5.9,
               6,
               5,
               3,
               3.9,
               4.6,
               4.5
            ]
         },
         {
            "branche": "Français",
            "notes": [
               3.8,
               3.4,
               5.3,
               4.5,
               4.3,
               5.4,
               4.1,
               3.4,
               3.5,
               4.5,
               3.7
            ]
         },
         {
            "branche": "Anglais",
            "notes": [
               5.8,
               5.7,
               3.7,
               3.2,
               4.2,
               3.5,
               2.9,
               5.1
            ]
         },
         {
            "branche": "Allemand",
            "notes": [
               3.9,
               4.1,
               3.3,
               3.5,
               5.4,
               3.8,
               3
            ]
         },
         {
            "branche": "Maths",
            "notes": [
               2.8,
               3,
               5.5,
               4.2
            ]
         }
      ]
   },

...

   {
      "eleve": "Remy NISSENS",
      "branches": [
         {
            "branche": "Histoire",
            "notes": [
               3.5,
               5.8,
               3.2,
               4.6,
               2.7,
               5.6,
               5.1,
               5.9
            ]
         },
         {
            "branche": "Français",
            "notes": [
               5.9,
               5.3,
               5.7,
               3.7,
               5.1,
               4.5,
               3,
               5,
               2.8
            ]
         },
         {
            "branche": "Chimie",
            "notes": [
               4.5,
               3,
               4.2,
               5,
               2.8,
               5
            ]
         },
         {
            "branche": "Géographie",
            "notes": [
               5.5,
               3.9,
               6,
               5.2,
               4.6,
               4.3
            ]
         },
         {
            "branche": "Maths",
            "notes": [
               2.7,
               2.7,
               6,
               4.8,
               5.8,
               5,
               5,
               3.9
            ]
         },
         {
            "branche": "Allemand",
            "notes": [
               3.1,
               2.9,
               2.9,
               5.8
            ]
         },
         {
            "branche": "Physique",
            "notes": [
               5.3
            ]
         },
         {
            "branche": "Anglais",
            "notes": [
               4.6,
               4.2,
               5.1,
               3,
               4.5,
               5,
               5.9
            ]
         }
      ]
   },
   {
      "eleve": "Théo RIQUE",
      "branches": [
         {
            "branche": "Physique",
            "notes": [
               5.3,
               3.1,
               5.8,
               3.3,
               4.1,
               5.8,
               2.9,
               5.7,
               3.8,
               3.1,
               4.7,
               3.9
            ]
         },
         {
            "branche": "Anglais",
            "notes": [
               3.6,
               3.1,
               3.6,
               4.3,
               5.3,
               5.6,
               3.6,
               3.6,
               3.9
            ]
         },
         {
            "branche": "Chimie",
            "notes": [
               5.2,
               4.3,
               4,
               4.2,
               5.9,
               5.6,
               3.3
            ]
         },
         {
            "branche": "Histoire",
            "notes": [
               3.5,
               3.8,
               5.7,
               3,
               3.8,
               3.8,
               3.4,
               4.5,
               3.8
            ]
         },
         {
            "branche": "Allemand",
            "notes": [
               3,
               2.8,
               5.2,
               6,
               3.8,
               4.7,
               4.1,
               4
            ]
         },
         {
            "branche": "Français",
            "notes": [
               5.8,
               3.7,
               5.9,
               3.6,
               3
            ]
         },
         {
            "branche": "Maths",
            "notes": [
               5.7,
               3,
               4.2,
               4,
               5.4,
               3.4,
               3.5
            ]
         },
         {
            "branche": "Géographie",
            "notes": [
               3.8,
               5,
               5.1,
               2.7,
               5.5,
               4.3,
               4.1
            ]
         }
      ]
   }
]
```

### G - [{Elève, [branches, nbre, min, max, moyenne, [notes]]}], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   {
      "eleve": "Alain TERNET",
      "branches": [
         {
            "branche": "Français",
            "nbre": 17,
            "min": 2.8,
            "max": 5.5,
            "moyenne": 4.2,
            "notes": [
               4,
               4.3,
               4.7,
               5.5,
               4.8,
               2.8,
               4.1,
               3.5,
               4.6,
               4,
               4,
               4.2,
               4,
               4.2,
               3.9,
               4,
               4.8
            ]
         },
         {
            "branche": "Allemand",
            "nbre": 13,
            "min": 2.9,
            "max": 6,
            "moyenne": 4.47,
            "notes": [
               3.9,
               3.7,
               4.1,
               2.9,
               3.8,
               4.8,
               4.8,
               6,
               5.7,
               5.2,
               5.7,
               3,
               4.5
            ]
         },
         {
            "branche": "Histoire",
            "nbre": 13,
            "min": 3.2,
            "max": 5.7,
            "moyenne": 4.78,
            "notes": [
               4.9,
               5.7,
               4.7,
               4.9,
               3.2,
               4.9,
               3.8,
               4.9,
               3.4,
               5.5,
               5.7,
               5,
               5.6
            ]
         },
         {
            "branche": "Chimie",
            "nbre": 20,
            "min": 2.7,
            "max": 6,
            "moyenne": 4.09,
            "notes": [
               3.1,
               4.5,
               5.6,
               5.1,
               4.3,
               4.8,
               3.3,
               4.1,
               2.7,
               2.8,
               5,
               4.3,
               3.8,
               4.2,
               6,
               4.4,
               3.2,
               4.1,
               3.1,
               3.5
            ]
         },
         {
            "branche": "Géographie",
            "nbre": 16,
            "min": 2.9,
            "max": 5.8,
            "moyenne": 4.41,
            "notes": [
               4.6,
               4.8,
               3.3,
               3.7,
               2.9,
               4.9,
               4.5,
               5.5,
               3.1,
               4.4,
               3.8,
               3.2,
               5.7,
               4.7,
               5.6,
               5.8
            ]
         },
         {
            "branche": "Anglais",
            "nbre": 13,
            "min": 2.7,
            "max": 5.8,
            "moyenne": 3.89,
            "notes": [
               3.8,
               2.9,
               3.2,
               4.1,
               5.8,
               4.9,
               3.4,
               5.6,
               3.7,
               4.1,
               3.3,
               2.7,
               3.1
            ]
         },
         {
            "branche": "Physique",
            "nbre": 11,
            "min": 2.8,
            "max": 5.5,
            "moyenne": 3.77,
            "notes": [
               3.1,
               3.5,
               3.4,
               4.7,
               2.8,
               5.3,
               3.5,
               2.9,
               3.3,
               3.5,
               5.5
            ]
         },
         {
            "branche": "Maths",
            "nbre": 11,
            "min": 3,
            "max": 5.8,
            "moyenne": 4.75,
            "notes": [
               5.8,
               5,
               4.7,
               3,
               3.9,
               5.2,
               4.1,
               5.2,
               4.9,
               5,
               5.5
            ]
         }
      ]
   },
   {
      "eleve": "Alain TERRIEUR",
      "branches": [
         {
            "branche": "Physique",
            "nbre": 11,
            "min": 2.7,
            "max": 5.3,
            "moyenne": 4.25,
            "notes": [
               3.3,
               5,
               3.7,
               4.7,
   
   ...
]
```

### H -[{Elève, [branches, nbre, min, max, moyenne, [{date, note}]]}], trié

À partir des données déjà chargées dans `jsonData`, vous devez obtenir ceci :

```json
[
   {
      "eleve": "Alain TERNET",
      "branches": [
         {
            "branche": "Français",
            "min": 2.8,
            "max": 5.5,
            "nbre": 17,
            "moyenne": 4.2,
            "notes": [
               {
                  "date": "02.08.2024",
                  "note": 4.2
               },
               {
                  "date": "04.10.2024",
                  "note": 4
               },
               {
                  "date": "12.10.2024",
                  "note": 4.2
               },
               {
                  "date": "01.11.2024",
                  "note": 4.3
               },
               {
                  "date": "03.11.2024",
                  "note": 4
               },
               {
                  "date": "22.12.2024",
                  "note": 4.6
               },
               {
                  "date": "13.01.2025",
                  "note": 4.7
               },
               {
                  "date": "14.01.2025",
                  "note": 4
               },
               {
                  "date": "07.02.2025",
                  "note": 5.5
               },
               {
                  "date": "25.02.2025",
                  "note": 2.8
               },
               {
                  "date": "06.03.2025",
                  "note": 4
               },
               {
                  "date": "08.03.2025",
                  "note": 3.9
               },
               {
                  "date": "29.03.2025",
                  "note": 4.1
               },
               {
                  "date": "04.04.2025",
                  "note": 4.8
               },
               {
                  "date": "23.04.2025",
                  "note": 4.8
               },
               {
                  "date": "11.05.2025",
                  "note": 4
               },
               {
                  "date": "20.06.2025",
                  "note": 3.5
               }
            ]
         },
         {
            "branche": "Allemand",
            "min": 2.9,
            "max": 6,
            "nbre": 13,
            "moyenne": 4.47,
            "notes": [
               {
                  "date": "11.08.2024",
                  "note": 4.8
               },
               {
                  "date": "01.09.2024",
                  "note": 5.2
               },
               {
                  "date": "19.09.2024",
                  "note": 4.8
               },
               {
                  "date": "24.09.2024",
                  "note": 4.5
               },
               {
                  "date": "01.10.2024",
                  "note": 3
               },
               {
                  "date": "23.10.2024",
                  "note": 3.7
               },
               {
                  "date": "26.11.2024",
                  "note": 3.8
               },
               {
                  "date": "25.02.2025",
                  "note": 5.7
               },
               {
                  "date": "22.04.2025",
                  "note": 4.1
               },
               {
                  "date": "03.06.2025",
                  "note": 3.9
               },
               {
                  "date": "16.06.2025",
                  "note": 2.9
               },
               {
                  "date": "17.06.2025",
                  "note": 6
               },
               {
                  "date": "30.06.2025",
                  "note": 5.7
               }
            ]
         },
...         
```

---

<img src="res/EMF_logo_RVB_Info_long.png" width="25%" style="margin-left:-20px;">
