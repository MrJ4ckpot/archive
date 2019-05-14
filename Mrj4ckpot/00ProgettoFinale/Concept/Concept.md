# Beholder #

### Realmente reale ###

La prospettiva è il punto da cui e verso cui vediamo il mondo e gli oggetti; la fotografia insegna che la prospettiva, ma anche la luce, quello che appare nell'inquadratura e la lunghezza del fuoco determinano valori e significati aggiunti a ciò che vediamo. Tuttavia, possiamo dire di essere in grado di "vedere" e capire un oggetto nella sua interezza se le prospettive dei singoli hanno questa eccezionale capacità di alterare la percezione?

Possiamo realizzare uno strumento capace di unire i punti di vista dei singoli per riprodurre quella che sarebbe la percezione del collettivo? Possiamo arricchire ulteriormente la percezione visiva attraverso il risultato di questo esperimento?

<img align="left" width="150" height="150" src="https://i.imgur.com/FVv1M4Z.jpg?1"> La **teoria delle lenti colorate** spiega come la nostra percezione del mondo sia alterata e distorta rispetto alla realtà in sè; un pò come se cercassimo di immaginarci tutti i colori, avendo indossato per tutta la vita lenti blu.

<br/><br/><br/><br/>

<img align="left" width="150" height="150" src="https://i.imgur.com/eyy5Bt6.jpg?1"> L'album "Non al denaro, non all'amore nè al cielo" di Fabrizio de Andrè contiene il brano **"Un ottico"** , che racconta i pazienti di un oculista, che provando lenti sbagliate sono in grado di vedere distorsioni della realtà, che rivelano verità sul loro passato.


### Prototipo ###

![Imgur](https://i.imgur.com/ajectdI.jpg?1)

Due o più webcam, collegate a uno schermo o un visore, che osservano, ricostruiscono e reinterpretano (anche in maniera assurda) ciò che vedono come collettivo e non come singoli.

1. Le catture di due o più immagini riprese da webcam vengono inizialmente divise in tasselli e mescolate tra loro (mantenendo le posizioni originali nell'inquadratura), seguendo un pattern che può essere selezionato dall'utente. Il risultato viene salvato a parte come **TEXTURE**.

2. **TEXTURE** viene analizzata tramite una rete neurale di image classification, che sceglie un'immagine in scala di grigi da un database, basandosi su ciò che pensa di vedere in **TEXTURE**. 

3. Questa immagine, in scala di grigi, viene utilizzata per produrre una **HEIGHTMAP**, ovvero un modello 3D di un piano, dove in corrispondenza dei nodi, l'altezza Z viene scelta in base alla quantità di bianco in quel punto dell'immagine: 100% sul bianco e 0% sul nero.

4. **TEXTURE** viene applicata su **HEIGHTMAP**, producendo come risultato un oggetto 3D distorto ma che presenta vaghe somiglianze con qualcos'altro. 