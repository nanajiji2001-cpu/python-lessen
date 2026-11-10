def bereken_edelsteen_kracht(aantal_edelstenen):
    """Geeft krachtpunten op basis van het aantal edelstenen."""
    # Edelstenen worden krachtiger als je er meer hebt.
    if aantal_edelstenen == 1:
        return 5
    elif aantal_edelstenen == 2:
        return 15
    elif aantal_edelstenen >= 3:
        return 50
    else:
        return 0
def spreuk_kracht(oude_spreuk_stukken):
    return (oude_spreuk_stukken // 3) * 20


def bereken_gevecht_kracht(edelstenen, potions, is_vervloekt, oude_spreuk_stukken):
    edelsteen_kracht = bereken_edelsteen_kracht(edelstenen)
    potion_kracht = bereken_potion_kracht(potions, is_vervloekt)
    spreuk = spreuk_kracht(oude_spreuk_stukken)

    return edelsteen_kracht + potion_kracht + spreuk


tovenaars_kracht = bereken_gevecht_kracht(3, 2, True, 3)
print("Kracht van je personage is " + str(tovenaars_kracht))