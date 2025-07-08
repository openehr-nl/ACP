PZP Hackathon

- teruggeven aan voorzittergroep --> geen leveranciers betrokken dus behorend bij het doel van de hackathon wat verwachten we dan in aanloop naar de connectathon van leveranciers. Gaan wij opleveren wat er nodig is in het veld. 

- Agenda:
	- Archetype bekijken
	- FHIR connect
		- specifiek even de onderverdeling in de consent en servicerequest
	- De vraag waarom zou je OpenEHR doen 
	- Wat is de rol van van OpenEHR in de informatiestandaard 

Waarom doen we dit eigenlijk? 

---------------------------

Wat zijn de knelpunten bij het archetype: 
de focus van het archetype gaat meer om het beleid vanuit de zorgverlener waar de zib meer gaat over de afspraak tussen zorgverlener en patient. 

- Afspraakpartijen -- additional details met als cluster afspraakpartijen en daar personen in stoppen 
voor de patient een party self instoppen 
in plaats van patient awareness zou je een hermodellering waarmee je hem constraint op een specifieke manier van awareness zodat je hier dingen als instemming in kan verwerken. 

De openstaande vraag: Hoe modelleer je als de patient het er niet mee eens is 

patient awareness zou wellicht in de toekomst ook voor wilsbekwaamheid gebruikt kunnen worden. 

--- opmerking vanuit openEHR  - het laat zien dat zelfs al heb je twee uitgedachte modellen er snel semanthiek verloren gaat in theorie kan dat ook vanuit de zib 

maar de modellering van de zib is gebasseerd op uitwisseling en niet voor vastlegging


zibbehandelaanwijzing2 gaat uit van 1 besluit en het archetype is 1 niveau hoger en daar kunnen meerder beslissingen in zitten. 

meerdere behandelaanwijzings zib kunnen mappen naar 1 archetype 

zijn de behandelaanwijzingen losse dingen of is het 1 cluster 
in openEHR zit een harde versie historie waar 
valid period start en valid period end zou je per behandelbesluit vast willen leggen en niet alleen voor het geheel. 

Voorstel: Moet er aan OpenEHR gevraagd worden om een valid period start en einddatum

terug mappen vanuit losse zibs naar 1 advance intervention decissions wordt lastig
ideeeen: identifier, history
de vraag is wil je dat en waarom? 
wat is dan de betekenis van het samenvoegen daarvan 

Hoe identificeer je dan wat bij elkaar hoort en hoe zie je de historie hiervan 
wordt de identifier gebruikt en wordt hij netjes gebruikt. als iets wijzigt krijg je dan dezelfde identifier of krijg je dan een andere. 

CPR decision is los gemodelleerd op basis van snomed zou dit van fhir naar het archetype geen probleem moeten zijn  

commentveld in openEHR wordt vrij vaak gebruikt in de mapping. Hier zit mogelijk een probleem bij heen en weer mappen dat als een zib ontvangen wordt en weer aangevuld. 

last updated is niet het beste veld voor de mapping van openEHR naar de zib andersom wel 
patient awareness zou hier nog als datum veld voor gebruikt kunnen worden. Maar dit gaat weer over alle interventies en niet de losse. 

bespreekmoment is een specifiek type update bijvoorbeeld niks veranderd maar wel besproken 
dat moet worden vastgelegd in een specifiek template

conclusie:
archetype heeft een template nodig dat past op het profiel bij de informatiestandaard 

scenarios: 
- je maakt een template dat een op een mapt met de zib met wat uitdagingen 
- Voor de lastige velden maak je extensies die je internationaal inbrengt om de converging verder te brengen


------------------
Leveranciers:
Vraag heeft het waarde wat we doen als er geen leveranciers komen. Fundamenteel verschil: Je kan een template maken en de OpenEHR tooling maakt er een formulier van. 
Dat is logisch want de leverancier pakt het archteype op. 

Verwachten we in het proces van ontvangen een consolidatie stap waar mogelijk interesse in is. 
Eventueel Nedap vragen hoe ze hier naar kijken --> waarschijnlijk consolidatie UI 

Vraag aan leveranciers --> de vastlegging ook standaardiseren helpt je dat om beter te voldoen aan de informatiestandaard. 

archetype naar zib viewer de ellende zit in het openEHR model. Als terugbrengen niet hoeft scheelt heel veel werk. 

Rol OpenEHR in informatiestandaard:
- Door de specificatie in archteype en de FHIR connect specificatie hoef je geen datamodel mapping vanuit vastlegging naar uitwisseling te maken als leverancier. 
	- Scheelt leverancier kosten 
	- Opschaling is makkelijker 
	- als zorginstelling kan je onafhankelijker worden van je leverancier 
	- Doordat er al veel is nagedacht over de modellen zijn deze zorgvuldiger en vaker gereviewd dan het zelf bedenken
	- zib zijn specifiek geen vastleggingsmodel dus bieden niet voldoende houvast voor een  datamodel voor vastlegging
	- Het is makkelijker om sneller aan te sluiten bij veranderingen in informatiestandaarden

FHIR: Consent en servicerequest resources -- dubbele stuk 
ondersteunt fhir connect dupliceren

Als je de andere kant op gaat wordt het lastiger, hoe zit dit in FHIR. 
Zit er een hierarchie in de mapping voor welk gegeven pak ik de service request en voor welke pak ik de consent bij binnenkomende berichten. 

WAt is er gedupliceerd? Wat zijn de risico's. 

WAt zijn de stappen die we in de techniek verwachten:
datamodel epd
--> via zib 
--> naar FHIR resource 

Of kan de zib mapping eruit

uiteindelijke doel is nergens data opslaan in de vorm van de zib 
