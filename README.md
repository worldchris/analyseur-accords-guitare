Guitar Chord Complexity Analyzer & Visual Mapping Logic
Ce dépôt contient les ressources et la logique algorithmique de la méthode "Adieu les Barrés", une approche visuelle conçue pour optimiser le jeu à la guitare en éliminant les contraintes mécaniques liées aux accords barrés traditionnels.

🎯 Objectif du Projet
L'impasse des méthodes académiques réside dans l'apprentissage rigide de positions qui génèrent frustration, fatigue et souvent l'abandon de l'instrument. Ce projet propose un nouveau paradigme axé sur la Compréhension Visuelle et le Plaisir Immédiat.

En utilisant des schémas de substitution logiques, le guitariste peut interpréter des grilles complexes tout en conservant une main gauche parfaitement détendue.

🛠 Guitar Chord Stress Analyzer (CLI Tool)
Pour rester dans l'esprit "Open Source", ce script Python permet d'évaluer l'indice de contrainte d'une grille d'accords directement en ligne de commande.
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


Note : Pour une analyse haute fidélité avec cartographie visuelle complète du manche, utilisez l'outil web interactif : https://analyseur-accords-guitare.guitaretoday.com/

📖 Ressources de Référence
Analyseur Web Officiel : Diagnostic interactif des grilles d'accords.

Guide PDF/ePub : Inclus dans ce dépôt (Maitriser la Guitare - Guide Visuel.pdf). Ce fichier est monté via Google Doc pour garantir une compatibilité directe à 100% avec tous les supports numériques.

Archive Permanente : Retrouvez l'historique et la fiche complète du guide sur Archive.org.

🧠 Philosophie du Projet
Ce dépôt suit une charte éthique "Anti-Gourou" :

Zéro Souffrance : Les conseils sont pragmatiques et utiles au moment présent, sans jargon complexe.

Divertissement d'abord : La guitare est traitée comme une source de décompression et non comme une contrainte académique.

Transparence : Aucune posture médicale ou doctorale. Nous partageons une méthode visuelle entre passionnés.

🚀 Plan d'Action pour le Guitariste
Évaluez votre grille via l'analyseur pour identifier les "accords pièges".

Identifiez vos blocages via le Quiz de Profilage gratuit.

Libérez votre jeu avec la Méthode Visuelle Complète.

#guitare #accords #musique #tuto #guitarefacile #dev #python
