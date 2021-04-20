# Java2 - Lekce 3 Domaci ukol

Vašim domácím úkolem je implementovat následující příklady pomocí Stream API:

1. Napište program, který vezme pole Stringu A, b, C, De, fF, gHiJK, LmN 
1.1. Najde nejdelším retězec
1.2. V nejdelším řetězci spočítá počet kapitálek
2. Napište program, který přečte soubor (priklad2.txt) a spočítá počet znaků na každém řádku, který neobsahuje číslici.
3. Napište program, který přečte dva soubory (priklad3_1.txt, priklad3_2.txt), vezme všechna čísla a spočítá jejich průměr zaokrouhlený na 2 desetinná místa.
4. Napište program, který vezme 2 čísla (a,b) a spočítá druhou mocninu všech čísel mezi a a b včetně <a,b>.

## Hint

1. Převedení Stringu na Character[]
```
.flatMap(str -> Arrays.stream(str.chars().mapToObj(c -> (char) c).toArray(Character[]::new)))
```

2. Comparator - otočení pořadí
```
//Podle délky 
Comparator.comparingInt(String::lenght).reversed()

//Obecné otočení pořadí
Comparator.reverseOrder()
```
