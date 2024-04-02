import random

def zahlenraten():
    print("Willkommen beim Zahlenraten-Spiel!")
    print("Ich denke an eine Zahl zwischen 1 und 100.")
    zielzahl = random.randint(1, 100)
    versuche = 0

    while True:
        eingabe = input("Rate die Zahl: ")
        versuche += 1

        try:
            rate = int(eingabe)
        except ValueError:
            print("Bitte gib eine gültige Zahl ein.")
            continue

        if rate < zielzahl:
            print("Die gesuchte Zahl ist größer.")
        elif rate > zielzahl:
            print("Die gesuchte Zahl ist kleiner.")
        else:
            print(f"Herzlichen Glückwunsch! Du hast die Zahl {zielzahl} erraten!")
            print(f"Du hast {versuche} Versuche gebraucht.")
            break

if __name__ == "__main__":
    zahlenraten()
