# Rilevamento Anomalie Industriali
## Un approccio basato su Intelligenza Artificiale

---

## Il Problema
**Come troviamo i difetti?**

Nelle linee di produzione industriale, i difetti possono essere rari e molto vari.
È difficile programmare un computer per riconoscere *ogni possibile* difetto (graffi, macchie, rotture, ecc.).

**L'idea:** Invece di insegnare al computer cosa è "sbagliato", gli insegniamo cosa è **"giusto"**.
Tutto ciò che non è "giusto", è un'anomalia.

---

## La Soluzione: PatchCore

L'algoritmo utilizzato si chiama **PatchCore**.
Funziona come un operaio esperto che ha visto migliaia di pezzi perfetti.

1. **Osserva**: Guarda l'immagine pezzetto per pezzetto ("patch").
2. **Ricorda**: Ha una "memoria" di come appaiono i pezzetti dei prodotti perfetti.
3. **Confronta**: Se un pezzetto del nuovo prodotto non assomiglia a nulla che ha visto prima...
4. **Segnala**: ...allora quel pezzetto è un'anomalia!

---

## Come Funziona: 1. Visione

L'immagine viene analizzata da una **Rete Neurale**.
Questa rete scompone l'immagine in tante piccole caratteristiche (features).

![Analisi Features](images/4/analysis.png)
*Qui vediamo come l'immagine viene "smontata" in diversi livelli di dettaglio.*

---

## Come Funziona: 2. La Mappa di Calore

L'algoritmo crea una **Heatmap** (mappa di calore).
- **Blu/Viola**: Tutto normale.
- **Giallo/Rosso**: Alta probabilità di difetto.

![Heatmap](images/4/hm.png)
*Le aree più luminose indicano dove l'algoritmo è "sorpreso" di vedere qualcosa di nuovo.*

---

## Risultati: Esempio 1

Ecco un esempio di rilevamento su un componente.

| Input | Output (Sovrapposizione) |
|:---:|:---:|
| ![Input](images/4/input.png) | ![Output](images/4/output.png) |

L'algoritmo evidenzia con precisione l'area anomala.

---

## Risultati: Esempio 2

Un altro test con un difetto diverso.

| Input | Output (Sovrapposizione) |
|:---:|:---:|
| ![Input](images/5/input.png) | ![Output](images/5/output.png) |

Anche qui, l'anomalia viene localizzata correttamente.

---

## Risultati: Esempio 3

Terzo esempio di applicazione.

| Input | Output (Sovrapposizione) |
|:---:|:---:|
| ![Input](images/6/input.png) | ![Output](images/6/output.png) |

Il sistema è robusto e funziona su diverse tipologie di difetti senza bisogno di essere ri-addestrato per ognuno.

---

## Conclusione

- **Veloce**: Analizza le immagini in tempo reale.
- **Flessibile**: Basta mostrargli esempi di prodotti "buoni".
- **Preciso**: Localizza il difetto a livello di pixel.

Questo sistema permette un controllo qualità automatico e affidabile.
