# Bienvenue sur ce rappel des bases du Réseaux !

## Les adresss IP

192.168.100.*

Toutes les adresses commençant par “192.168.100.*” appartiennent au
même réseau, soit 192.168.100.1/24, 192.168.100.2/24, etc. jusque 192.168.100.255.

---

## Les bits

1 octet = 8 Bit

Pour les bits nous retrouveront majoritairement :
- /8  (1 octet)
- /16 (2 octets)
- /24 (3 octets)

et très rarement voir jamais :
- /0
- /32 
- /12 
- /14

---

## Les masques de sous réseaux (sous réseaux)
- 255.0.0.0 => /8
- 255.255.0.0 /24
- 255.255.255.0 /16
- 255.255.255.255 /24

___


## Les classes réseaux
Les classes réseaux concernent l'adressage IP

### Classe A
La classe A est définit en fonction de son nombre de bit
/8 Bits (1 octet = 8 bits 😏)

Adresse IP = 192 .* .* .*

Sous réseaux = 255.0.0.0

### Classe B
La classe B est définit en fonction de son nombre de bit
/16 Bits (2 octets = 16 bits 😏)

Adresse IP = 192 .52 .* .*

Sous réseaux = 255.255.0.0

### Classe C
La classe C est définit en fonction de son nombre de bit
/24 Bits (3 octets = 24 bits 😏)

Adresse IP = 192 .52 .87 .*

Sous réseaux = 255.255.255.0


### Classe D E F etc... (Vous ne les verez jamais)


## Les nombres d'hôtes

Il s'agit du nombre de personnes pouvant se connecter simultanement sur le réseau

>Pour la classe A (1 octet ou 8 bits), le nombre d'hôtes est de 16 777 214

>Pour la classe B (2 octets ou 16 bits), le nombre d'hôtes est de 65 534

>Pour la classe C (3 octet ou 24 bits), le nombre d'hôtes est de 254 


Si l'on souhaite calculer le nombre d'hôtes disponible pour 18 bits (/18)
alors nous devons calculer les sous-réseaux IP et les hôtes disponibles.


Nombre de sous-réseaux = 2^n, où n est le nombre de 1 dans l'ID du sous-réseau    // annexe

Nombre d'hôtes disponible 2^h, où h est le nombre de 0 dans l'ID d'hôte

On a une IP 192.182.21.103 avec comme masque de sous-réseau 255.255.255.0 (/24)

sa valeur Binaire est égale :
11000000 . 10110110 . 00010101 . 1100111  (Pour l'IP) // annexe
11111111 . 11111111 . 11111111 | 00000000 (Pour le Sous réseau)

2^8 = 256

256-2 = 254

Nous avons donc 254 hôtes disponibles


Pas eu le temps de finir mais il faut parler de :

- Différence entre adresse IP et adresse Public
- en gros tcp c'est du handshake donc tu attends que la personne confirme avoir recu ton message alors que udp tu balance tout et osef la réponse donc plus rapide mais posssibilté d'erreur ça dépend de la nature de ton flux
- infrastructures


- des bisous, Hakan du passé 😘

