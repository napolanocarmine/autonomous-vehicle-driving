# autonomous-vehicle-driving

Linee guida per il progetto di Autonomous Vehicle Driving a.a. 2020-2021

Informazioni generali e consegna

L'elaborato progettuale sostituisce lo scritto per un anno accademico a
partire dalla fine del corso (ovvero dal primo appello della sessione
estiva a.a. 2020-2021, fino al secondo appello della sessione fuoricorso
II semestre dell'a.a. 2021-2022, indicativamente maggio 2022).

Il progetto dovrà essere consegnato dal rappresentante del Gruppo:

> ● Entro e non oltre il **XXX** per i gruppi in cui almeno un
> componente intende partecipare al primo appello della sessione estiva;
>
> ● Entro e non oltre **XXX** per tutti i gruppi che non hanno già
> consegnato nella prima data, qualunque sia l'appello a cui intendono
> partecipare. Pertanto, questa data è da considerarsi la data finale di
> consegna dell'elaborato progettuale.

Il progetto può essere consegnato una sola volta. Se si consegna il
progetto per il primo appello, non sarà possibile modificarlo e
consegnarlo nuovamente entro la seconda data. Ciò implica che, anche se
non tutti i componenti partecipano al primo appello, essi non potranno
inviare una nuova versione del progetto. È importanteindicareilnumero
delGruppointutte le comunicazioni ed inserireglialtri
partecipantidelgruppo in tutte le comunicazioni con il docente, in
particolare in quella di consegna dell'elaborato.

La consegna del progetto consiste in:

> ● Relazione di progetto (maggiori dettagli sono forniti nel seguito) ●
> Software realizzato per il progetto
>
> ● Video demo (maggiori dettagli sono forniti nel seguito)

Il software deve essere consegnato tramite piattaforma e-learning come
un archivio .zip che ha come nome "gruppoXX" dove XX indica il numero
del gruppo su due cifre. Tutti gli elementi del progetto devono essere
presenti all'interno della cartella.

Obiettivo del progetto

I gruppi dovranno integrare all'interno del software fornito come
baseline del progetto un detector di semafori (anch'esso fornito come
materiale del progetto, ma non integrato nella baseline) e progettare un
hierarchical planner che permetta al veicolo di navigare in maniera
autonoma all'interno della mappa **Town01**. Pertanto, behavioral
planner e local planner dovranno essere progettati e realizzati in modo
da gestire il comportamento del veicolo in caso di semaforo rosso,
giallo o verde, oltre che per evitare collisioni con altri veicoli e
pedoni presenti all'interno della scena.

Dettagli sul progetto

La baseline fornita include già un behavioral planner simile a quello
fornito a lezione e l'inizializzazione di un mission planner, con punto
di partenza e punto di arrivo parametrici. Si consiglia di effettuare
diversi test al variare di tali punti e del numero di veicoli e pedoni
presenti all'interno della scena, poichè tali valori saranno scelti
dinamicamente dai docenti in seduta d'esame.

I gruppi dovranno estendere la baseline con i seguenti obiettivi:

> 1\. Evitare le collisioni con tutti i pedoni e i veicoli, utilizzando
> i dati "perfetti" dei sensori di Carla. Nella baseline viene già
> fornita una funzione che effettua la proiezione del bounding box 3D
> degli oggetti (veicoli e pedoni) nel mondo. I gruppi dovranno quindi
> integrare nel progetto la gestione delle collisioni con tali oggetti.
>
> 2\. Considerare la presenza disemafori all'interno della scena,
> fermandosi al semaforo rosso e passando o ripartendo solo quando il
> semaforo è verde. La presenza del semaforo dovrà essere rilevata
> mediante un detector, che fornisce anche lo stato del semaforo (stop,
> go). Il codice del detector è disponibile al seguente link:
> [[https://github.com/affinis-lab/traffic-light-detection-module]{.underline}.](https://github.com/affinis-lab/traffic-light-detection-module)
> I gruppi dovranno integrare il detector nel progetto, interpretare lo
> stato del semaforo e implementare la logica di gestione dei semafori
> nel behavioral planner.

Dettagli sulla relazione

La relazione del progetto deve essere sintetica e focalizzata sugli
elementi fondamentali del progetto. Essa deve contenere i seguenti
elementi:

> ● **Frontespizio**
>
> Deve contenere **almeno** le seguenti informazioni: o Corso e Anno
> Accademico
>
> o Numero del Gruppo
>
> o Componenti del gruppo con le relative matricole ● **Executive**
> **Summary** **(max** **2** **pagine)**
>
> Deve contenere **almeno** le seguenti informazioni:
>
> o Descrizione preliminare sinteticadel progetto, delle eventuali
> assunzioni fatte e dei problemi affrontati
>
> ● **Progettazione** **ed** **implementazione**
>
> Deve contenere **almeno** le seguenti informazioni:
>
> o Descrizione dell'architettura del hierarchical planner (con
> particolare riferimento al behavioral planner), con rappresentazione
> di alto livello di tutti i moduli e delle loro interazioni.
>
> o Descrizione di dettaglio di ogni modulo. ● **Analisi**
> **sperimentale** **del** **sistema**
>
> Deve contenere **almeno** le seguenti informazioni:
>
> o Analisi quantitative dei risultati (numero di test completati con
> successo rispetto al numero di test effettuati). Si riporti un
> dettaglio dei test effettuati.
>
> o Analisi qualitative dei risultati, con screenshot di casi d'uso che
> dimostrano il funzionamento del sistema in alcuni scenari critici.
>
> o Link a tre video, eventualmente commentati a voce, in cui si mostra
> il funzionamento in tempo reale del sistema proposto in Carla nelle
> seguenti tre situazioni: stop al semaforo rosso e passaggio con
> semaforo verde, gestione collisioni con altri veicoli, gestione
> collisioni con pedoni.

Elementi di valutazione

Nel seguito, vengono indicati gli elementi che saranno oggetto di
valutazione e a cui è opportuno prestare particolare attenzione:

> ● La valutazione tiene conto sia della relazione che del progetto. Non
> trascurare nessuno di questi due elementi. Inoltre, è fondamentale la
> coerenza tra ciò che viene dichiarato nella relazione e ciò che è
> presente nell'implementazione.
>
> ● Il codice consegnato deve essere opportunamente commentato, e deve
> essere evidente il collegamento con le specifiche sezioni della
> relazione in cui le scelte progettuali relative vengono spiegate.
>
> ● Durante l'esame orale, al gruppo sarà richiesto di lanciare un test
> in tempo reale, con valori di alcuni parametri (punto di partenza,
> punto di arrivo, numero di pedoni, numero di veicoli) a discrezione
> della commissione. La valutazione tiene conto dell'esito del test e
> delle risposte ad eventuali domande della commissione ai singoli
> componenti del gruppo.
>
> ● Agli studenti può essere chiesto di spiegare, commentare e discutere
> di ogni modulo software presentato nell'ambito del progetto. Più in
> generale, ogni argomento trattato durante il corso è oggetto di
> valutazione durante il colloquio orale.
>
> ● La valutazione individuale dello studente prende in considerazione
> quattro aspetti: la valutazione globale del progetto; la conoscenza
> individuale di tutti gli elementi del progetto e la consapevolezza
> delle scelte; il contributo nell'ambito del progetto, dichiarato dai
> vari componenti; l'esame orale, che verterà su tutti gli argomenti
> trattati durante il corso.

Gestione dei conflitti

Si precisa, sin d'ora che eventuali e non auspicabili minori contributi
da parte di qualche singolo componente del gruppo, anche per cause di
forza maggiore, andranno immediatamente segnalati al docente da parte
del Responsabile del Gruppo a tutela del singolo e dell'intero Gruppo.

Tali circostanze, qualora si verificassero, saranno approfondite e
valutate dal docente che fornirà al Gruppo le necessarie direttive
eliminando ogni motivo di tensione, salvaguardando il lavoro e la
valutazione dei singoli Studenti.

Si precisa infine che in tali casi, a seguito degli eventuali
approfondimenti che il docente riterrà di effettuare, tutti
indistintamente e indipendentemente dalle motivazioni che inducono
eventuali problemi, dovranno adeguarsi alle direttive impartite.

Incasodi anomalie riscontrate, i docenti possonochiedere ai
singolicomponenti del gruppodelleintegrazioni sul progetto, o in casi
limite, anche la necessità di dover fare un nuovo progetto.

Per ogni chiarimento sulla traccia e sul tema assegnato, si invitano gli
studenti a contattare i docenti per mezzo email:
[[asaggese@unisa.it]{.underline}](mailto:asaggese@unisa.it) e
[[agreco@unisa.it]{.underline}](mailto:agreco@unisa.it)

