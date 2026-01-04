# Projet — États quantiques à trois qubits avec Qiskit

## Description

Ce dépôt contient une implémentation de circuits quantiques à **trois qubits** (GHZ et W) réalisée avec Qiskit.

---

## Script du projet

Le code complet du projet est disponible dans le notebook Jupyter suivant :
[ghz_w.ipynb](https://github.com/SaadHadadia/GHZ_and_W_quantic_states/blob/main/ghz_w.ipynb)

---

## Objectifs

* Créer et manipuler des circuits quantiques à 3 qubits.
* Préparer les états intriqués GHZ et W.
* Exécuter les circuits sur le simulateur (`qasm_simulator` / Aer) et sur un backend IBM Quantum via Qiskit Runtime.
* Récupérer les distributions de mesures (counts/distributions) et afficher des histogrammes.

---

## Concepts (résumé)

* **Qubit** : état quantique de base, superposition de |0⟩ et |1⟩.
* **État intriqué (entangled)** : état quantique non séparable entre plusieurs qubits (par ex. états du bell à 2: `(|00⟩ + |11⟩)/√2` ).
* **Espace 3-qubits** : dimension 2³ = 8 (états |000⟩…|111⟩).
* **GHZ** : état multipartite (par ex. `(|000⟩ + |111⟩)/√2` ).
* **W** : état multipartite (par ex. `(|001⟩ + |010⟩ + |100⟩)/√3` ).
* **Transpilation** : adapter un circuit au jeu d'instructions et à la topologie d'un backend.
* **Mesures** : projections sur la base computationnelle; les counts représentent les fréquences observées.

---

## Dépendances

Les bibliothèques Python nécessaires sont listées ci-dessous.

```
qiskit
qiskit_aer
qiskit_ibm_runtime
matplotlib

```

---

## Notes sur le code fourni

* Le script montrent la préparation des états (GHZ et W), la transpilation pour le simulateur Aer, l'exécution via `Aer.get_backend('qasm_simulator')`, la récupération des `counts` et l'affichage d'un histogramme.
* Pour l'exécution sur un backend IBM Quantum, le script utilise `QiskitRuntimeService` pour se connecter et exécuter les circuits.
* Pour les notebooks Jupyter, le fichier peut contenir la directive `%matplotlib inline` afin d'afficher les figures directement.

---


## Sorties affichées

Le script imprime les dictionnaires `counts` (par ex. `{'000': 512, '111': 512}`) et affichent des histogrammes ou des distributions.
Les histogrammes montrent la répartition des résultats de mesure pour les états GHZ et W.

---

## Auteurs

* HADADIA Saad
* MAKTOUB Wiam
