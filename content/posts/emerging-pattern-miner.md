---
title: Emerging Pattern Miner
date: 2021-11-18
description: "Java - Un applicazione Client-Server che implementa l'algoritmo Apriori, partendo da un dataset in un database MySQL
ci permette di trovare pattern frequenti ed emergenti. "
image: images/EPMiner1.png
---

## EPMiner


EPMiner è un applicativo che ci permette di scoprire Pattern Frequenti e Pattern Emergenti, partendo da
una collezione di transazioni.
EPMiner implementa l'algoritmo di Data Mining Apriori.
Per la scoperta di Pattern Frequenti dovremo inserire la frequenza minima, anche detta supporto.
Una volta trovati i Pattern Emergenti possiamo andare alla scoperta di Pattern Emergenti, qui dovremo invece
inserire il tasso di crescita minimo, anche detto growrate.

L'applicativo si suddivide in due moduli, che sono rispettivamente la parte Server e la parte Client del
programma. 
Il Client si occupa prevalentemente di ricevere i dati in input dall'utente, inviarli al Server,
rimanere in attesa dei risultati per poi stamparli a video una volta ricevuti. 
Il Server invece contiene gli algoritmi di scoperta di Pattern Frequenti ed Emergenti, e si limita a ricevere i dati in input, processarli per poi rispedirli al Client.
L'architettura Client-Server è realizzata attraverso l'utilizzo dei Socket in Java.
La collezione di transazioni si ritrova su un Database MySQL, il Server affinchè possa lavorare deve interrogare la
base dati, questo è permesso dal Driver MySQL Connector.
