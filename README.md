# python_lab4
LAB4
seuil = 10
notes = []
print("--- Gestion des Notes ---")
print("Entrez vos notes une par une. Tapez 'stop' pour terminer.")
while True:
    entree = input("Entrez une note : ")
    if entree.lower() == "stop":
        break
    try:
        note = float(entree)
        if 0 <= note <= 20:
            notes.append(note)
        else:
            print("Erreur : La note doit être entre 0 et 20.")
    except ValueError:
        print("Valeur incorrecte, merci d'entrer un nombre.")
print("-" * 30)
for index, note in enumerate(notes, start=1):
    statut = "Admis" if note >= seuil else "Refusé"
    print(f"Étudiant {index} : note {note} -> statut : {statut}")