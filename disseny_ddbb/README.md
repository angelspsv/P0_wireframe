## Aquesta és la meva proposta de base de dades per l'exercici del festival de música

# Breu explicació del diagrama de taules

Són 9 taules que formen dos grups connectats per la novena taula Acceso.

# Les relacions entre les taules són aquestes:

+ Recinto i Concierto mitjançant el camp id_recinto en una relació de PK-FK
+ Grupo i Concierto mitjançant el camp id_grup en una relació de FK-PK
+ Grupo i Sustituto mitjançant el camp id_grup en una relació de PK-FK
+ Calle i Parcela mitjançant el camp id_calle en una relació de PK-FK
+ Parcela i Alquiler mitjançant el camp id_parcela en una relació de PK-FK
+ Usuario i Alquiler mitjançant el camp id_usuario en una relació de PK-FK
+ Recinto i Usuario amb Acceso amb els camps id_recinto (PK-FK) i id_usuari (PK-FK)


+ La relació de Recinto amb Concierto és de 1:N, ja que un recinte pot tenir molts concerts.
+ La relació Grupo amb Concierto és de 1:N, ja que un grup pot fer molts concerts, però en un concert pot haber només un grup.
+ La relació entre Grupo i Sustituto és de N:N, ja que un grup pot tenir més d’un substitut i un grup pot substituir molts grups.
+ La relació entre Usuario i Acceso és de 1:N, perquè tot assistent pot realitzar múltiples entrades.
+ La relació entre Recinto i Acceso és de 1:N, perquè a un recinte poden accedir molts usuaris. Un assistent només pot estar a un recinte al mateix temps.
+ La relació entre Usuario i Alquiler és de 1:1 perquè un usuari només pot tenir un lloguer i un lloguer/parcel•la pot estar llogada a un assistent al mateix temps.
+ La relació entre Parcela i Alquiler és de 1:1 perquè una parcel•la només pot estar llogada un cop al mateix temps. La parcel•la només pot tenir un llogater durant el festival.
+ La relació entre Calle i Parcela és de 1:N, perquè un carrer pot tenir moltes parcel•les, però una parcel•la només pot estar a un carrer en concret.

__Imatge del diagrama de les taules__
![Imatge del diagrama de les taules]()