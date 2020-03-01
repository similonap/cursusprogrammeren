# Labo-oefeningen

## Pokémons deel 2

### Constructors

Pas de kennis van constructors toe op je Pokémon-project uit het vorige hoofdstuk. Zorg ervoor dat je Pokémons op 3 manieren kunt aanmaken als volgt:

* Via een default constructor: alle base stats worden daarbij op 10 standaard ingesteld via de constructor
* Via een overloaded constructor die de gebruiker toelaat om de 6 base stats als parameters mee te geven \(bv `new Pokemon(45,42,50,65,34,67)`\)
* Via object initializer syntax waarbij je eender welke stat kunt instellen.

### Static methoden

* Verhuis de methoden \(`GeneratorPokemon` en `Battle`\) die je maakte in deel 3 van de Pokémon-opdracht in vorige hoofdstuk naar de klasse `Pokemon` zelf en test of deze nog steeds werkt. \(Is dit een logischere plek?\)
* Voeg enkele static properties met private set toe om bij te houden:
  * Hoe vaak een Pokémon z'n level werd verhoogd \(dus telkens bij aanroep van `VerhoogLevel`\)
  * Hoe veel Battles er al zijn geweest \(verhoogt telkens `Battle` wordt uitgevoerd\)
  * Hoe vaak een battle resulteerde in gelijkstand \(verhoogd bij gelijkstand in  `Battle`\)
  * Hoe veel random Pokémons werden aangemaakt \(verhoogt telkens `GeneratorPokemon` wordt aangeroepen\)
* Maak een static methode `Info` die deze properties als een soort samenvatting naar het scherm stuurt
* Maak een static property `NoLevelingAllowed` aan van het type bool. Deze kan van buiten de klasse aangepast worden. Indien deze bool op `true` staat kunnen Pokémons hun level niet verhoogd worden. Wanneer in dit geval `VerhoogLevel` wordt aangeroepen zal er een foutboodschap op het scherm komen.

Toon in je hoofdprogramma aan dat je kunt werken met deze static methoden en properties.

## Digitale kluis

Maak een klasse `DigitaleKluis` die we gaan gebruiken om een kluis voor te stellen.

De klasse heeft volgende elementen:

* Een private variabele die de toegangscode van de kluis bewaard als geheel getal \(naam: `code`\) 
* Een overloaded constructor die als parameter een geheel getal toelaat. Dit getal zal worden toegewezen aan de private variabele code.
* Een full property `CanShowCode` die kan ingesteld worden op true or false, om aan te geven of de code van buitenuit kan gezien worden.
* Een read-only property `CodeLevel` van type int. Deze property zal het level van de code teruggeven. Het level is eenvoudigweg de code gedeeld door 1000 als geheel getal \(dus indien de code 500 is zal 0 worden teruggegeven, indien de code 2000 is wordt 2 teruggegeven, etc.\) 
* Een fullproperty `Code` met private set. De get van deze property zal -666 teruggeven, tenzij CanShowcode op true staat, in dit geval zal de effectieve code worden terug gegeven. 
* Een methode `TryCode` die een geheel getal als parameter aanvaardt. De methode geeft een true terug indien de code correct was, anders false. Deze methode kan gebruikt worden om extern een code te testen , indien deze overeenkomt met de bewaarde code dan zal gemeld worden dat de code geldig is en wordt ook getoond hoeveel keer de gebruiker geprobeerd heeft. Indien de gebruiker -666 meegaf dan meldt de methode dat de gebruiker een cheater is . Indien de gebruiker een foute code meegaf dan meldt de methode dat dit een foute code was en wordt het aantal pogingen met 1 verhoogd.  
* Een private variabele `aantalpogingen` om bij te houden hoe vaak de gebruiker geprobeerd heeft de code te vinden.

Maak enkele Digitale Kluis objecten aan in je main en test of je bovenstaande klasse correct is geïmplementeerd.

## Werken met string en csv

Opgelet! Er is geen aparte oefening waar wordt gewerkt rond string en het verwerken van csv-bestanden. Zorg dat je dit beheerst door bijvoorbeeld zelf een oefening uit te werken waarin je een csv-bestand verwerkt!

