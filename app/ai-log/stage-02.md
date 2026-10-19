
# Laboratorul 2: AI log

## Tools
- Gemini
- https://share.gemini.google/S30eykGvalgg 

## Key requests
### 1. Implementarea funcțiilor utilitare pentru destinații
- **Asked**: Am cerut ajutorul pentru crearea fișierului `src/utils/destinatii.js` și implementarea a șase funcții (`getOrase`, `getNevizitate`, `totalZile`, `formatDestinatie`, `numarPeTara`, `sortDupaZile`) folosind metode specifice de array (`map`, `filter`, `reduce`), destructuring și template literals, conform unui tabel cu cerințe.
- **Got**: Codul JavaScript complet și explicat pentru fiecare funcție în parte, folosind sintaxa modernă ES6+ (arrow functions) și asigurându-se că lista originală nu este mutată (de exemplu, folosind `[...list].sort()`).
- **Changed or rejected**: Am preluat codul generat, fiind exact ceea ce se cerea în laborator pentru a putea fi importat ulterior în componentele React.

### 2. Validarea rezultatelor din consolă și clarificarea logicii de calcul
- **Asked**: Am atașat o captură de ecran cu output-ul din consolă pentru a verifica dacă funcțiile sunt corecte. Eram nelămurit de ce log-ul pentru "zile de vizitat" afișa rezultatul `18` în loc de `22` (cât era în exemplul inițial din tabel).
- **Got**: AI-ul a analizat imaginea și output-ul, ajutându-mă să deduc că funcțiile sunt scrise perfect. Mi-a explicat că în fișierul de test (`main.jsx`), funcția `totalZile` a fost apelată pe rezultatul funcției `getNevizitate` (doar pentru destinațiile cu `vizitat: false`), ceea ce înseamnă că 18 (4+3+6+5) este de fapt suma corectă pentru destinațiile rămase de vizitat. 
- **Changed or rejected**: Nu a fost nevoie să modific nicio funcție din `destinatii.js`, deoarece logica din spate era funcțională, iar output-ul diferit se datora strict modului specific în care s-a făcut apelul combinat în fișierul principal.

## What I learned / what did not work
Inițial m-am blocat crezând că funcția `reduce` este implementată greșit pentru că rezultatul total al zilelor nu se potrivea cu exemplul brut din foaia de laborator (18 vs 22). Am învățat cum se pot înlănțui și combina logic funcțiile (ex: calcularea sumei pe o listă deja filtrată). De asemenea, mi-am consolidat lucrul cu array-uri în JavaScript (`map`, `filter`, `reduce`), modul în care `reduce` poate construi un obiect folosind chei calculate (pentru gruparea pe țări) și importanța destructurării parametrilor pentru a scrie un cod mai curat.