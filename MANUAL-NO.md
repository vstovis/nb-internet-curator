# Brukersteg :open_book:
- Start et virtuelt miljø slik at programmet har alt det trenger for å kjøre. Slik gjør du dette i Windows: skriv "cmd.exe" i søkefeltet i startmenyen, og åpne  "Ledetekst". Skriv inn ``*filstien til mappen programmet er installert i\venv\bin\activate.bat``. Eksempel: ``C:\programfiler\nb-internet-curator\venv\bin\activate.bat``
- Deretter skriver du følgende i ledetekst for å starte programmet: ``python3 \*filstien til mappen programmet er installert i\main.py``. Eksempel: ``python3 C:\Programfiler\nb-internet-curator\main.py``
- Åpne nettleseren og skriv ``localhost:8080`` i adressefeltet. Husk å deaktivere alle “adblockers” i nettleseren din, eller hvitelist ``localhost:8080`` slik at siden vises korrekt. 
- Første gangen vil siden sannsynligvis være tom for innhold. Klikk på "Choose archive folder" knappen for å legge til innhold.
![Velg knapp steg](use-steps-images/choose_archive_btn.png)
- Gå til arkivmappen du ønsker å jobbe med, og velg "Last opp". Det er viktig at arkivmappen du laster opp befinner seg i samme sti som er definert i “arc_source_directory” i config-filen din. Hvis disse to ikke matcher, vil operasjonen mislykkes. 
<div>
   <img src="use-steps-images/upload_archive.png" alt="upload step" style="width: 49%">
   <img src="use-steps-images/arc_source_dir.png" alt="upload step" style="width: 49%">
</div>
 
- Etter at du har valgt et arkiv burde du se en blå melding som informerer om at arkiv lastes inn. Når meldingen forsvinner skal det kommer opp en ny samling i listen under “Collections:”. Hvis det ikke gjør det kan du prøve å laste siden på nytt (f5).
- Du burde nå se et nytt arkiv i samlingslisten. Trykk på denne. 
- På toppen av samlingens side skal det være en knapp hvor det “Start curating”
 
![Start curating step](use-steps-images/start_curating.png)
- Når du kommer inn på en side vil du få et panel i toppen av siden med noen alternativer.  
![curator actions](use-steps-images/curate_actions.png)
- Trykker du “Accept” blir siden markert som "godkjent", og du sendes til neste nettside.
- Trykker du “Reject” blir siden markert som "ikke godkjent", og du sendes til neste nettside.
- Alle sider kan ha en kommentar. Trykk på "Comment" for å legge til, lese eller endre en kommentar. 
- Øverst i høyre hjørne ser du statusen til nettsiden. “Undecided” betyr at du ikke har blitt behandlet enda. ”Accepted” betyr at siden har blitt godkjent. “Rejected” betyr at siden ikke er godkjent. Status kan også være “Error” og “Irrelevant”. Error betyr at det har oppstått en intern feil. Prøv å laste side på nytt, eller restart python applikasjonen. Irrelevant betyr at siden er en ressurs eller et sidespor fra en hovedside. 
- Når alle sidene i en samling er ferdig behandlet (når du blir sendt tilbake til samme side når du trykker Accept eller Reject), lagrer programmet en "verdicts"-fil. Den kan åpnes i Excel, og viser hvilke nettsider som er behandlet og hvilken status/kommentar de har fått. Den finner du i ``*filstien til programmet\res\verdicts\*navnet til samlingen.tsv``. Eksempel: ``C:\Programfiler\nb-internet-curator\res\verdicts\2009-04-02.tsv``
