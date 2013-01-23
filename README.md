Delve into the stack
====================
Anderhalf jaar geleden begon mijn stage bij OSP; mijn eerste aanraking met open-source. Zowel OSP als open-source heeft me niet meer losgelaten. Ik werk op Linux en gebruik vrije-software. Daarnaast probeer ik grafisch ontwerp en programmeren met elkaar te verbinden, iets wat niet direct voortkomt vanuit open-source maar binnen open-source wel goed gedijt.
De meest bekende eigenschap van open-source-programma's is dat de broncode te lezen en te wijzigen is. Maar het is naar mijn mening ook een omgeving die bewust structuren maakt om leren aan te moedigen. Bijvoorbeeld door documentatie, fora, maillijsten of F/LOSS-manuals. Dat is natuurlijk niet zo gek, een open-source-project bestaat bij de gratie van breed gebruik én bijdragen aan de code. En heeft er dus zo belang bij om zo toegangelijk mogelijk te zijn als programma maar zeker ook als code. Die 'emancipatie' ontwikkelt mijn inziens ook een kritsche gebruiker. De transparantie van het ontwikkelproces, door commentaar in de code of discussies op de maillijst, toont de keuzes die gemaakt zijn binnen de code. Het wordt zo zichtbaar waarom software is zoals het is maar laat tegelijkertijd de betrekkelijkheid van diezelfde keuzes en software zien.
In de afgelopen zomer heb ik geëxperimenteerd met een penplotter. Ik wilde een apparaat dat eigenlijk bedoeld is om vectoren te tekenen gebruiken om bitmap-afbeeldingen te 'printen'. Gebasseerd op offsetdruk ontwikkelde ik programma's die verschillende soorten rasters konden tekenen met de plotter. Het leverde herkenbare beelden op met een eigen visuele taal, maar uiteindelijk blijft dit onderzoek beperkt tot een 'tour de force' van mijn programmeurskunsten: Hoe 'dwing' ik het apparaat tot iets waar het eigenlijk niet hoort te zijn?
Deze experimenten bevestigde voor mij dat 'printen' niet eenvoudig is, dat er een hoop wetenschap verborgen gaat achter het simpele 'Druk af'-venster. Maar meer nog dan respect voor de machine en techniek gaf het me een idee van de enorme laag aan software en processen die niets anders doen dan beslissingen nemen waarvan ik niet eens doorheb dat ze genomen worden - laat staan dat ik ze zou kunnen beïnvloeden.
Maar als ik op papier krijg wat ik globaal op mijn scherm zie, wat is er dan aan de hand? Eigenlijk juist die misvatting: Wat ik op mijn scherm zie kan nooit zo gedrukt worden, al is het maar door het verschil in materiaal, kleur en resolutie. Eigenlijk zijn beide (het scherm en de afdruk) benaderingen van het bedoelde beeld, een ideaal, de waarheid(?) dat in het bronbestand wordt beschreven. Hoe een document op de juiste manier wordt getoond/vertaald ligt uiteindelijk beschreven in standaarden en protocollen, maar de daadwerkelijke implementaties - de software die wij dagelijks gebruiken - zijn altijd intrepetaties van programmeurs van die protocollen.
In reguliere software is deze laag verborgen en ontoegankelijk maar binnen een open-source omgeving kan ik er gewoon bij. Juist omdat ik me bewust ben van die laag, juist omdat ik deze laag aan kan raken én begrijpen vind ik dat ik hem als ontwerper niet mag negeren. Ik wil hem verkennen, openbreken, manipuleren. Door het verkennen en bevragen van die hele laag aan software en protocollen onderzoek ik niet alleen de rol en invloed van de computer maar ook mijn houding ten opzichte van grafisch ontwerp. Een standaard is in zekere zin ook een beschrijving van zichzelf, de werking, de mogelijkheden, de keuzes binnen de standaarden tonen ook de intenties en ideeën van dezelfde standaard. De laag aan grafische software toont zo -in zekere zin- de gedachten over ontwerp binnen de open-source-gemeenschap. Mijn kritiek daarop, of onderzoek daarnaar verraad het mijne.

Plotteronderzoek
----------------
Al langer probeer ik programmeren in te zetten voor mijn grafisch ontwerp. Vaak werden het generatieve ontwerpen die soms werden gevoed door informatie die ik (automatisch) op het internet verzamelde. Ook schreef ik 'filters' voor afbeeldingen, geintrigeerd door puntrasters probeerde ik met behulp van PHP-scripts afbeeldingen opnieuw op te bouwen, bijvoorbeeld met cirkels die groter en kleiner werden, lijnen die draaide of punten die dichter en verder van elkaar af stonden.

In Juni 2012 kocht ik een penplotter het leek me fantastisch om deze printers te kunnen 'controleren' veel spannender dan de vlakke eenduidige beweging van een laser- of inktjetprinter, apparaten die bovendien zo complex en gesloten zijn dat je het wel uit je hoofd laat ze te 'hacken'. Heel simpel gezegd is de penplotter een automatische pen die je met je computer kunt besturen. Elke punt, lijn of cirkel op de pagina wordt getekend met een beweging en kost dus ook tijd. Elk element heeft zo dus gevolgen voor de duur van het proces, maar ook de beweging in zijn geheel. Moderne printers verwerken eerst de pagina in zijn geheel en bepalen vervolgens de meest optimale weg om de afbeelding te printen. De plotter begint simpelweg aan het element dat als eerste wordt beschreven in het bestand - wat natuurlijk niet aan de bovenkant van de pagina hoeft te staan.
Wanneer je de plotter langzaam laat tekenen wordt het inzichtelijk hoe een afbeelding beschreven was in het bestand en wordt opgebouwd door de printer. Die inzichtelijkheid gecombineerd met de beweging en het geluid die de plotter maakt geeft het voor mij een zekere theatraliteit.
Als eerste project wilde ik de plotter gebruiken om bitmap afbeeldingen te 'printen'. De scripts die ik eerder als filters had geschreven herschreef ik in Python. Uiteindelijk nam dit 'kleine onderzoek' mijn hele zomer in beslag. De filters die ik had geschreven waren vaak gebasseerd op cirkels, en juist die cirkels nemen heel veel tijd in beslag op de plotter. Vandaar dat ik lijnen en punten ben gaan gebruiken, iets wat veel meer in de aard van de plotter ligt. Toch kostte de schetsen veel tijd om te printen, een schets op A0-formaat die was opgebouwd uit honderdduizenden punten kostte een weekend om te plotten en liet ik s'nachts op de gang draaien zodat ik ondanks de herrie kon slapen.
Daarnaast bleek het een hele tour om de juiste pennen te vinden. De originele stiften werken fantastisch maar zijn alleen verkrijgbaar in de Verenigde Staten en erg duur. Goedkope viltstiften leken een goede oplossing, maar gingen erg snel leeg en ik had niet alle 32 kleuren in de verpakking nodig. Uiteindelijk bleken de Stabilo 68 fineliners en viltstiften ideaal. Ze pasten perfect in het adaptertje dat ik had, ze gingen lang mee, waren per stuk verkrijgbaar en gingen lang mee.
Uiteindelijk leverde het me een hele stapel 'esthetische' schetsen op, waar ik heel blij mee ben, maar het beperkt zich tot een heel formeel onderzoek naar een verouderd apparaat. Buiten zichzelf raakt het weinig aan en ik zie ook geen uiteinden om het ergens heen te trekken zonder dat het geforceerd lijkt. Tot nu toe blijft het een vingeroefening.

Onderzoeksplan
--------------
De laag aan software die ik eerder besprak wordt ook wel de 'renderstack' genoemd: De stapel aan soft- en firmware die stap voor stap een afbeelding toont op een beeldscherm of papier. Hieronder toon ik een aantal van die stacks voor verschillende soorten 'output', het geeft een idee van de stappen en transformaties in het proces.

Een renderstack voor fonts
	Programma
	^v
	Pango
	^v
	Harfbuzz
	^v
	Fribidi
	^v
	Freetype
	^v
	Fontconfig
	^v
	Font

Renderstack beeldscherm
	Programma of bestand
	^v
	Cairo - GTK+ - QT - Pango
	^v
	Xlib
	^v
	2D Driver
	^v
	Graphics card
	
Renderstack print
	Programma
	^v
	Cairo - GTK+ - QT - Pango
	^v
	PostScript
	^v
	CUPS
	^v
	Printer Driver | Printer PS interpreter | Ghostscript
	^v
	Printer

Het toont dat wat je op het scherm ziet net zo goed een vertaling is als dat de print dat is. Het bronbestand wordt zo goed mogelijk volgens een standaard geïntrepeteerd.

	      A                     •                     B
	     [x] < ~ < ~ < ~ < ~ < (x) > ~ > ~ > ~ > ~ > {x}
	beeld op scherm            bron              beeld geprint

Uiteindelijk wil ik de gevolgen en de potenties van dit proces onderzoeken. Kan ik lagen verwisselen, aanpassen of misschien wel helemaal weglaten? Kan ik het proces inzichtelijk maken voor andere ontwerpers of misschien zelfs toegankelijk zodat de computer wat minder aanvoelt als een black box maar meer als een te behrijpen stuk gereedschap.
Veel keuzes voor dat onderzoek moeten nog gemaakt worden, focus ik alleen op typografie of beeld, kleur, resolutie? Of houdt ik me alleen bezig met de tussenliggende protocollen, hoe ze tot stand komen en het werk beïnvloeden?
