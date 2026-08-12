# Estrazione automatica del contenuto degli scontrini della Lidl

Tramite l'app Lidl Plus, nella sezione Account -> Scontrini digitali, è possibile scaricare gli scontrini in formato .png\
Con questo progetto si possono elaborare i dati contenuti negli scontrini digitali.

## Descrizione

Bisogna avere e utilizzare l'app Lidl Plus. Scaricando gli scontrini, si può estrarne il contenuto nel file "Database.csv".\
In una prima fase di monitoraggio, è opportuno controllare eventuali errori di lettura nel file "Corretti manualmente.csv".\
Correggendo manualmente gli errori nel file "Database.csv", si creano/aggiornano di conseguenza i file "Articoli unici.xlsx" (elenco di articoli, categorie e sottocategorie).\
Nel file "Elenco scontrini letti.csv" c'è l'elenco degli scontrini letti con le relative informazioni principali.

*Maggiori dettagli nel file "Istruzioni e miglioramenti futuri.txt"*

Note:
- stimando un volume di scontrini contenuto, non ritengo problematico scaricare manualmente gli scontrini dall'app (anche perchè la mia tessera viene usata anche da altri membri della famiglia)
- c'è una componente manuale nell'assegnazione di categorie e sottocategorie, fino a quando non si acquistano più prodotti mai acquistati prima
- avendo inizialmente pensato di creare un database testuale, nella tabella dei fatti ("Database.csv") ci sono le stringhe degli articoli. Grazie a "Fact table.ipynb" si può ricreare a posteriori l'architettura con gli indici al posto delle stringhe

## Requisiti e librerie

- Python 3.x (io ho usato 3.12.13)
- easyocr
- os
- pandas
- cv2
- numpy
- csv
- openpyxl
