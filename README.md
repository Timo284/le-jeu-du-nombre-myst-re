import random

def jeu_nombre():
    nombre_secret = random.randint(1, 100)
    essais = 0
    
    print("Bienvenue ! J'ai choisi un nombre entre 1 et 100.")
    
    while True:
        choix = int(input("Entrez un nombre : "))
        essais += 1
        
        if choix < nombre_secret:
            print("Trop petit !")
        elif choix > nombre_secret:
            print("Trop grand !")
        else:
            print(f"Bravo ! Vous avez trouvé en {essais} essai(s) !")
            break

jeu_nombre()
