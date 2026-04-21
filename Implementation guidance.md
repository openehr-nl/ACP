Notities sessie 29-01-2026

Vervolgstappen
Feedback verwerken in template.
Toestemming en informeren naasten: lokale archetypes maken die de ZIB en FHIR-resource mimicken.
Euthanasiestandpunt toevoegen.
Implementatieadvies opstellen voor bepaalde mappings.
FHIR Connect aanpassen conform wijzigingen.
Nieuwe reviewronde organiseren.
Governance-sessie inplannen: onder andere bespreken het gebruik van niet-internationale CKM-archetypes.
Default values in een aparte sessie doornemen.


Bespreekpunten:
Wat is het doel van de template? Data set vs formulier 🡪 vorige keer al teruggekoppeld dat we de dataset zib2020 aanhouden. De template is bedoel voor het vastleggen (met openehr) en beschikbaar stellen (met fhir) en niet bedoeld voor raadplegen. De template wordt een gestandaardiseerde dataset waaruit organisatie dan zelf kunnen kiezen wat ze wel/niet gebruiken.
Beleidsvraag: algemene of niet algemene CKM vragen? Gebruik van archetypes die niet in de internationale CKM staan? Hoe gaan we hiermee om? 🡪 bespreken in een governance sessie; internationaal waar mogelijk, lokale archetypes alleen wanneer dat echt nodig is.
Opmerking: We willen in principe geen informatie toevoegen die niet in informatiestandaard zit 🡪 wel de volgorde van de informatiestandaard aanhouden
Willen we contactpersoon wel of niet meenemen want dit komt ook uit andere informatie – implementatie advies voor gebruik van contactpersoon: patiënt gegevens, datum invullen zit standaard in openehr, naampatiënt wordt buiten openehr gedaan met referentie naar openehr waar waardes staan, geboortedatum geldt hetzelfde voor
Bespreken (regel 8 relationship van de excel) relevant om vast te leggen of iemand op dit moment wilsonbekwaam is, wie is dan de gesprekspartner - …
Regel 10 role – lijst uitbreiden. Wel liever ophalen van de Terminologie server of van artdecor. Voor lokale implementaties kunnen dan andere values wel worden toegevoegd.
Bespreken (regel 21 gesprek gevoerd in het bijzijn van van de excel) is dit relevant? 🡪 verwijderen
Regel 26 gesprek gevoerd door - practitionor role eruit en gesprek gevoerd door mappen op composer (referentie met ID en evt naam. Functie zit er niet expliciet in maar kan wel uit ander model komen.), uitdrukken in fhirconnect.
regel 36 reason bespreken wat is reden contact? – verwijderen
regel 37 name organisatie vastleggen? – verwijderen
regel 38 probleem - verwijderen, goal ook verwijderen. Value set vervangen bij intent of care. Bij advance intervention decisions CPR verwijderen. In zib afspraakpartij wordt gevuld o.b.v composer en participations en participations expliciet de wettelijke vertegenwoordiger
regel 44 wilsverklaring wel opnemen – behouden
regel 46 status – aanpassen
regel 49/50 keuze orgaandonatie vastgelegd, bespreken - verwijderen, lokaal archetype maken. Lokaal hangen er snomed codes aan, Harmke kan dit delen
regel 52 behandelbesluit, aanpassen vertaling verkeerd – hernoemen
regel 53 behandelbesluit occurence - aanpassen
regel 59 CPR decision – verwijderen
regel 63 personal request or preference, nog aanpassen en vertalen – aanpassen
regel 65 toestemming – koppelen aan plek waar je toestemmingen uitwisselt, bv via lsp met een automatisch vinkje?
regel 66 specific third party included – communication request met fhir resource voor vertellen aan familie?

Overige
Wat verder nog belangrijk is – toevoegen


https://docs.google.com/document/d/1_OhoxNjkIO5hmmL5ngrPL4JLqXzusDg9
