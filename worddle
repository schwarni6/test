import random

def wordle():
    # Liste der möglichen Wörter (alle müssen 5 Buchstaben haben)
    woerter = ["APFEL", "BIRNE", "STERN", "RADIO", "STADT", "GLUCK", "REGEN"]
    geheimnis = random.choice(woerter).upper()
    versuche = 6
    
    print("--- Willkommen bei Python Wordle! ---")
    print(f"Errate das Wort mit 5 Buchstaben. Du hast {versuche} Versuche.\n")

    for versuch in range(1, versuche + 1):
        tipp = input(f"Versuch {versuch}: ").upper()

        # Validierung der Eingabe
        while len(tipp) != 5:
            tipp = input("Das Wort muss genau 5 Buchstaben haben: ").upper()

        # Ergebnis berechnen
        ergebnis = ""
        for i in range(5):
            if tipp[i] == geheimnis[i]:
                # Buchstabe korrekt und an der richtigen Stelle (Grün)
                ergebnis += f"\033[92m {tipp[i]} \033[0m"
            elif tipp[i] in geheimnis:
                # Buchstabe im Wort enthalten, aber falsche Stelle (Gelb)
                ergebnis += f"\033[93m {tipp[i]} \033[0m"
            else:
                # Buchstabe nicht im Wort (Grau/Standard)
                ergebnis += f" {tipp[i]} "

        print(ergebnis)

        if tipp == geheimnis:
            print(f"\nGlückwunsch! Du hast das Wort in {versuch} Versuchen erraten.")
            break
    else:
        print(f"\nSchade! Das Wort war: {geheimnis}")

if __name__ == "__main__":
    wordle()
