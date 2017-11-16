Calibr8 Media
----------
Versie 4.1.x van calibr8 media module integreert Drupal 8 met media entity, entity browser, en image widget crop.

Versies 3.x en lager gebruikten de file entity module. Aangezien media entity naar core verhuist, wordt file entity deprecated.
Voor de media entity module wordt een upgrade path voorzien, daarom baseer je een nieuwe drupal install best daarop.

Hieronder staat beschreven hoe je best een nieuw veld toevoegt aan een entity, om van alle magic gebruik te maken.
Zie ook https://www.calibr8.gcecc.be/nl/calibr8-media

Een nieuw veld toevoegen
------------------------
We werken met een reference naar een media entity ipv een image/file field.
Kies bij het aanmaken van een nieuw media veld voor 'reference > other' de media entity staat namelijk niet in de lijst.

Op de volgende pagina kan je dan kiezen om het entity type 'Media' te gebruiken. Dit maakt nu een entity reference veld aan dat media entities gebruikt.

Selecteer op de volgende pagina de 'image' media entity bundle, en kies de default selectie methode.
Gebruik entity_browser als form widget
Door entity browser te gebruiken als form widget, is het mogelijk om zowel afbeeldingen op te laden als bestaande afbeeldingen te hergebruiken.

Formulier configureren
------------------------
Configureer het formulier om entity browser te gebruiken als form widget. Kies voor 'rendered entity' als preview image. Er is een thumbnail view mode voorzien die gebruikt kan worden voor deze preview.

Gebruik Field formatter
------------------------
Om niet voor elke image style een media view mode te moeten voorzien, kunnen we rechtstreeks op de node display de image style instellen. Daarvoor maken we gebruik van de field_formatter module.

Kies de formatter 'Field formatter with inline settings'. Kies bij 'Field name' voor 'Image', en kies de correcte formatter instellingen voor de afbeelding. 