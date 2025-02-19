---
title: 'Iniziare a utilizzare la soluzione Email Pro'
excerpt: 'Come eseguire le prime operazioni sul servizio Email Pro'
updated: 2024-01-29
---

> [!primary]
> Questa traduzione è stata generata automaticamente dal nostro partner SYSTRAN. I contenuti potrebbero presentare imprecisioni, ad esempio la nomenclatura dei pulsanti o alcuni dettagli tecnici. In caso di dubbi consigliamo di fare riferimento alla versione inglese o francese della guida. Per aiutarci a migliorare questa traduzione, utilizza il pulsante "Contribuisci" di questa pagina.
>

## Obiettivo

La soluzione Email Pro permette di usufruire di un servizio di posta elettronica professionale a un prezzo competitivo, per supportare o avviare la tua attività.

**Questa guida ti mostra le operazioni di base da effettuare sul tuo servizio di posta elettronica Email Pro.**

## Prerequisiti

- Disporre di una soluzione [Email Pro](https://www.ovhcloud.com/it/emails/email-pro/){.external}
- Aver ricevuto l’email di conferma dell’installazione di Email Pro
- Disporre di un dominio OVH
- Avere accesso allo [Spazio Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.it/&ovhSubsidiary=it){.external}

## Procedura

### Step 1: accedi alla gestione del servizio

Per gestire la soluzione Email Pro accedi allo [Spazio Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.it/&ovhSubsidiary=it){.external} e seleziona il tuo servizio nella sezione `Email Pro`{.action}.

> [!primary]
>
> Nello Spazio Cliente OVHcloud il nome di questo servizio inizia per *emailpro-*, contiene una parte dell’identificativo cliente e termina con una cifra (1 per la prima soluzione Email Pro installata, 2 per la seconda, ecc...).
>

### Step 2: aggiungi il dominio

Se il servizio Email Pro è stato appena ordinato, si apre automaticamente la finestra `Aggiungi un dominio`{.action}. Se non compare, clicca sulla scheda `Domini associati`{.action} e poi sul pulsante `Aggiungi un dominio`{.action}.

A questo punto scegli una delle opzioni proposte:

- **Seleziona un dominio dalla lista** : nell’elenco vengono mostrati soltanto i domini che utilizzano una configurazione OVHcloud e associati al tuo identificativo cliente come contatto. Se il dominio è registrato in OVHcloud ma non compare nello Spazio Cliente, è necessario aggiungerlo con l’opzione "Inserisci un dominio non gestito dal tuo account OVHcloud"
- **inserire un dominio non gestito dal proprio account OVHcloud** : questa opzione è disponibile se il dominio è registrato in OVHcloud ma configurabile da un altro Spazio Cliente OVHcloud **o** se il dominio è registrato presso un altro Registrar. Per il corretto funzionamento del servizio Email Pro è necessario essere in grado di modificare la configurazione del nome di dominio (zona DNS).

Una volta effettuata la scelta, clicca su `Continua`{.action}. 

![emailpro](images/emailpro-01.png){.thumbnail}

Compare un messaggio con le informazioni relative alla configurazione della modalità del dominio.

![emailpro](images/emailpro-02.png){.thumbnail}

- **Se il dominio inserito non è gestito da OVHcloud**, la modalità non autoritativa verrà configurata di default.

- **Se il dominio inserito è gestito da OVHcloud**, è possibile scegliere tra due modalità.
    - **Autoritativa**: È utile nel caso in cui Email Pro sia l’unica soluzione di posta elettronica utilizzata con il dominio. e non consente l’utilizzo simultaneo della tua soluzione di posta elettronica.
    - **Non autoritativa**: È utile nel caso in cui Email Pro **e un altro servizio di posta elettronica vengano utilizzati insieme al dominio**.

> **Informazioni sulle modalità Autoritativa e Non autoritativa**
>
> - Quando un’email viene trasmessa verso la piattaforma Email Pro (*Inbound mail server Email Pro*) in modalità **autoritativa**, significa che tutti gli indirizzi email del tuo dominio sono ospitati esclusivamente su questa piattaforma. <br> <br> Ad esempio, se si invia un’email all’indirizzo "*mary.johnson@mydomain.ovh*", il server Email Pro "*Inbound mail server Email Pro*" restituirà un messaggio di errore al mittente, in quanto questo indirizzo non esiste sul server Email Pro "*Inbound mail server Email Pro*".
> - Quando un’email viene trasmessa verso la piattaforma Email Pro (*Inbound mail server Email Pro*) in modalità **non autoritativa**, significa che gli indirizzi email del dominio sono ripartiti tra la piattaforma email principale (*Inbound mail server Email Pro*) e un altro servizio di posta (*Inbound mail server MXplan*). <br> <br> Ad esempio, se si invia un’email all’indirizzo "*mary.johnson@mydomain.ovh*", il server Email Pro *Inbound mail server Email Pro* inoltrerà l’email al server MXplan "*Inbound mail server MXplan*" perché quest’ultimo possa consegnarla.
>
> ![Add Domain](images/authoritative-mode.png){.thumbnail}
>

> [!warning]
>
> Se durante l’aggiunta del dominio alla piattaforma di posta viene visualizzato il messaggio "**authoritative domain detected**", significa che il dominio è dichiarato in modalità **autoritativa** su un’altra piattaforma di posta elettronica. Sarà quindi necessario attivarlo in modalità **non autoritativa** per entrambe le piattaforme, in modo che possano convivere.

Se si sceglie la modalità **non autoritativa** e si utilizza un servizio:

- **E-mail OVHcloud (Exchange o MXplan)**, inserisci direttamente come server email di destinazione "*mx1.mail.ovh.net*" ( funziona allo stesso modo con *mx0.mail.ovh.net*, *mx2.mail.ovh.net*, *mx3.mail.ovh.net*, *mx4.mail.ovh.net* ).
- **Email esterna a OVHcloud (offerta email concorrente, server email privato)**, inserisci nella casella server di posta di destinazione il nome host del server in entrata di questo servizio esterno assicurandoti che autorizzi le richieste email provenienti dal tuo servizio Email Pro

La scelta della modalità non è definitiva e può essere modificata dallo Spazio Cliente OVHcloud.

Una volta effettuata la scelta, clicca su `Continua`{.action}.

**Se il dominio selezionato dalla lista è gestito da OVHcloud**, è disponibile la configurazione automatica e per aggiungere il dominio sarà sufficiente spuntare le caselle e cliccare su `Continua`{.action}.

![emailpro](images/emailpro-03.png){.thumbnail}

- **SRV**: record DNS che consente di configurare automaticamente il tuo servizio di posta elettronica nel momento in cui aggiungi un indirizzo email.
- **MX**: record DNS dei server di posta elettronica necessario per la ricezione delle email sul dominio interessato.
- **DKIM** : Applicazione di una firma digitale cifrata per proteggere gli scambi di email. Per maggiori informazioni, consulta la nostra guida "[Configurare un record DKIM ](/pages/web_cloud/domains/dns_zone_dkim)".

**Se il dominio inserito non è gestito da OVHcloud**, segui lo Step 3 .

Alla fine del processo di configurazione, ti consigliamo di verificare il riepilogo. Se tutte le informazioni risultano corrette, clicca su `Conferma`{.action} per avviare l’operazione di aggiunta del dominio.

### Step 3: configura il dominio

A operazioni ultimata, il dominio aggiunto dovrebbe risultare come dominio associato: per verificarne i parametri, consulta la tabella presente nell’interfaccia.

Nella colonna `Diagnostica`{.action} è possibile assicurarsi della corretta configurazione del dominio. Se è presente una casellina rossa, significa che è necessario modificare alcuni parametri. Quindi hai due possibilità:

- ** In caso di configurazione automatica**, l’aggiornamento nello [Spazio Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.it/&ovhSubsidiary=it){.external} potrebbe richiedere qualche ora.

- **Se il dominio inserito non è gestito da OVHcloud** : clicca sulla casellina rossa per visualizzare le modifiche da apportare.
    - *Per creare un record CNAME*, consulta la nostra guida "[Creare un record CNAME per aggiungere un dominio associato](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/exchange_dns_cname)".
    - *Per un record MX*, consulta la nostra guida "[Aggiungere un record MX alla configurazione di un dominio](/pages/web_cloud/domains/dns_zone_mx)".
    - *Per un record SRV*, completa la zona DNS con le informazioni fornite quando clicchi sulla casellina rossa. Per aggiungere questo record, consulta la guida "[Modificare una zona DNS OVHcloud](/pages/web_cloud/domains/dns_zone_edit)".
    - *Per un record SPF*, completa la zona DNS con le informazioni fornite quando clicchi sulla casellina. Per aggiungere questo record, consulta la guida "[Configurare un record SPF](/pages/web_cloud/domains/dns_zone_spf)".
    *Per un record DKIM*, completa la zona DNS con le informazioni fornite quando clicchi sulla casellina. Per aggiungere questo record, consulta la guida "[Configurare un record DKIM ](/pages/web_cloud/domains/dns_zone_dkim)".

![emailpro](images/emailpro-04.png){.thumbnail}

### Step 4: configura gli account Email Pro 

Per procedere con la configurazione degli indirizzi email, seleziona la scheda `Account email`{.action}.  Visualizzi una tabella con tutti gli account ordinati, nel formato “*@configureme.me*”.

Per configurarli, clicca sul pulsante `...`{.action} e poi su `Modifica`{.action}.

![emailpro](images/emailpro-05.png){.thumbnail}

Completa con le informazioni richieste.

|Campo|Descrizione|
|---|---|
|Account email|Inserisci il nome che vuoi assegnare al tuo account email (ad esempio nome.cognome) e seleziona il dominio dalla lista.|
|Nome|Inserisci un nome.|
|Cognome|Inserisci un cognome.|
|Nome da visualizzare|Indica il nome che comparirà come mittente delle email inviate da questo indirizzo.|
|Password e Conferma|Crea una password complessa di almeno 8 caratteri e contenente almeno una maiuscola, una minuscola e un numero.| 

Dopo aver completato tutti i campi clicca su `Continua`{.action}, verifica la correttezza delle informazioni inserite e poi clicca su `Conferma`{.action}.

> [!primary]
>
> Ripeti questa operazione per tutti gli account che vuoi creare, in base al numero a tua disposizione. Per ordinare account aggiuntivi, clicca sul pulsante `Ordina account`{.action}.
>

### Step 5: utilizza gli indirizzi email

Una volta creati gli account non ti resta che utilizzarli. Per accedervi OVHcloud mette a disposizione un’applicazione online (*webapp*), accessibile all’indirizzo <https://www.ovhcloud.com/it/mail/> usando le credenziali associate al tuo indirizzo di posta elettronica.

Per configurare l’account su un altro client di posta o dispositivi come _smartphone_ e tablet, [è possibile trovare alcune informazioni utili nelle nostre guide disponibili online](/products/web-cloud-email-collaborative-solutions-email-pro). Se non conosci i parametri necessari alla configurazione dell’account email, ecco i valori da utilizzare:

|Tipo di server|Nome del server|Tipo di sicurezza|Porta|
|---|---|---|---|
|In entrata|pro**?**.mail.ovh.net|SSL/TLS|993|
|In uscita|pro**?**.mail.ovh.net|STARTTLS|587|

> [!primary]
>
> Nel nostro esempio, usiamo il nome del server, ad esempio: pro**?**.mail.ovh.net, dove “?” dovrà essere sostituito con il numero che indica il server del servizio Email Pro.
> 
> Questa informazione è disponibile nello [Spazio Cliente OVHcloud](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.it/&ovhSubsidiary=it){.external}, sezione `Web Cloud`{.action}, selezionando `Email Pro`{.action}. Il nome del server è visibile nel riquadro **Connessione** della `scheda Informazioni generali`{.action}.
> 

## Per saperne di più

[Guida all’utilizzo di Outlook Web App con un account email](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/email_owa)

[Creare regole di posta in arrivo in Outlook Web App (OWA)](/pages/web_cloud/email_and_collaborative_solutions/using_the_outlook_web_app_webmail/creating-inbox-rules-in-owa-mx-plan)

[Aggiungi un alias al tuo account email](/pages/web_cloud/email_and_collaborative_solutions/common_email_features/feature_redirections)

[Creare firme automatiche](/pages/web_cloud/email_and_collaborative_solutions/microsoft_exchange/feature_footers)

[Gestire la fatturazione dei tuoi account Email Pro](/pages/web_cloud/email_and_collaborative_solutions/email_pro/manage_billing_emailpro)

[Gestire la politica di sicurezza di un servizio di posta elettronica](/pages/web_cloud/email_and_collaborative_solutions/common_email_features/security-policy)

Contatta la nostra Community di utenti all’indirizzo <https://community.ovh.com/en/>.