# Guitar Chord Complexity Analyzer & Visual Mapping Logic

Ce dépôt contient les ressources et la logique algorithmique de la méthode **"Adieu les Barrés"**, une approche visuelle conçue pour optimiser le jeu à la guitare en éliminant les contraintes mécaniques liées aux accords barrés traditionnels.

## 🎯 Objectif du Projet
L'impasse des méthodes académiques réside dans l'apprentissage rigide de positions qui génèrent frustration, fatigue et souvent l'abandon de l'instrument. Ce projet propose un nouveau paradigme axé sur la **Compréhension Visuelle** et le **Plaisir Immédiat**. 

En utilisant des schémas de substitution logiques, le guitariste peut interpréter des grilles complexes tout en conservant une main gauche parfaitement détendue.

## 🛠 Guitar Chord Stress Analyzer (CLI Tool)
Pour rester dans l'esprit "Open Source", ce script Python permet d'évaluer l'indice de contrainte d'une grille d'accords directement en ligne de commande.

```python
def calculate_chord_stress(chord_sequence):
    """
    Calcule l'indice de complexité (C) basé sur la charge de pression (barrés).
    Formule : C = (accords_pièges / total_accords) * 100
    """
    # Liste des accords exigeant une pression ou une extension importante
    stress_indicators = ['F', 'Fa', 'Bm', 'Sim', 'B', 'Si', 'F#m', 'Fa#m', 'C#m', 'Do#m']
    
    total = len(chord_sequence)
    if total == 0: return 0
    
    stress_count = sum(1 for c in chord_sequence if c in stress_indicators)
    return (stress_count / total) * 100

# Exemple de test :
song_chords = ["G", "C", "D", "F", "Am", "Bm"]
score = calculate_chord_stress(song_chords)

print(f"Indice de fatigue détecté : {score:.2f}%")
