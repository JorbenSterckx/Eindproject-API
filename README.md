# Eindproject-API
*Jorben Sterckx 2CCS02*
## Thema API
Voor mijn project heb ik het thema **films** gekozen. 
Ik heb dit gekozen omdat ik graag films kijk en er al veel heb gegeken.

In mijn database staan 3 tabellen:
- users
- movies
- ratings

Door middel van POST requests kan ik films aanmaken. als ik inlog als een gebruikers kan ik een een rating aan een bepaalde film geven.

## Werking API
In deze sectie ga ik laten zien hoe mijn API werkt en welke endpoints ik heb gebruikt.

### POST
Ik heb 4 POST endpoints gemaakt.
1. De eerste dient voor het aanmaken van een token.
2. De tweede dient voor het aanmaken van een gebruiker.
3. De derde dient voor het aanmaken van een film.
4. De vierde dient voor het aanmaken van een rating voor een film.
#### Aanmaken van een user
![Screen van postman voor het aanmaken van een gebruiker](/screens/Aanmaken_gebruiker.png)

#### Aanmaken van een film
![Screen van postman voor het aanmaken van een film](screens/Aanmaken_film.png)

#### Aanmaken van een rating
![Screen van postman voor het rating](screens/Aanmaken_rating.png)

### GET
Ik heb 5 GET endpoints gemaakt:
1. De eerste dient voor het weergeven van alle gebruiker.
2. De tweede dient voor het weergeven van de huidige gebruiker.
3. De derde dient voor het weergeven van alle films.
4. De vierde dient voor het weergeven van alle ratings voor een bepaalde films.
5. De vijfde dient voor het weergeven van een bepaalde films.

#### Alle gebruikers weergeven
![Screen van postman voor het weergeven van alle gebruikers](screens/Alle_gebruikers.png)

#### Alle films weergeven
![Screen van postman voor het weergeven van alle films](screens/Alle_films.png)

#### Een bepaalde films weergeven
![Screen van postman voor het weergeven van een bepaalde film](screens/Film.png)

#### Alle ratings van een bepaalde films weergeven
![Screen van postman voor het weergeven van een rating](screens/Ratings_van_film.png)

### DELETE
Ik heb 1 DELETE endpoint gemaakt:
1. Deze dient voor het verwijderen van een rating voor een bepaalde films

#### Een bepaalde rating van een film verwijderen
![Screen van postman voor het verwijderen van een film](screens/Verwijderen_rating.png)
![Screen van postman voor validatie dat de film verwijderd is](screens/Delete_validation.png)

### PUT
Ik heb 1 PUT endpoint gemaakt:
1. Deze dient voor het aanpassen van een rating.

#### Een rating van een film aanpassen
![Screen van postman voor de update van een rating](screens/Pre-update.png)
![Screen van postman voor het updaten van een rating](screens/Update_rating.png)
![Screen van postman voor validatie dat de rating geüpdate is](screens/Update_validation.png)

### Hashing & OAuth
#### Hashing
Ik heb hasing geïmplementeerd zodat het wachwoord dat ik
ingeef gehashed wordt. Hierdoor is het wachwoord niet
zichtbaar en moeilijk te achterhalen is.

#### OAouth
Ik heb ook Aouth geïmplementeerd zodat ik bij het inloggen
een token krijg zodat mijn gegevens op de server bewaard worder
en daardoor veiliger kan werken.
![Screen van FastAPI docs voor het inloggen](screens/Aouth1.png)
![Screen van FastAPI docs na het inloggen](screens/Aouth2.png)
![Screen van FastAPI docs van de token](screens/Aouth3.png)
Via de post request van /users/ kan ik een gebruiker aanmaken
en hierna kan ik zoals op de foto's hierboven inloggen.

#### Postmanscreen
Op postman kan ik op 2 manieren authorizeren
1. Basic Auth:
Hier kan ik mijn username an password van de gebruiker die ik heb aangemaakt invullen.
![Screen 1 voor inloggen van postman](screens/1.png)
   
3. Bearer Token:
Hier kan ik de token in die ik heb gekregen bij het aanmaken van een gebruiker invullen.
![Screen 2 voor inloggen van postman](screens/2.png)


### Testing
In de root van mijn project heb ik een test file aangemaakt
die alle get-endpoint test.
![Testen van alle get-endpoints](screens/Testing.png)

### OpenAPI docs
Dit is mijn OpenAPI documentatie die ik terug vind wanneer ik naar mijn localhoste op poort 8000 /docs ga http://127.0.0.1:8000/docs.
![](screens/Doc1.png)
![Screen van FastAPI docs voor token](screens/Doc_post_token.png)
![Screen van FastAPI docs voor aanmaken users](screens/Doc_post_users.png)
![Screen van FastAPI docs voor weergeven gebruiker](screens/Doc_get_users.png)
![Screen van FastAPI docs voor weergeven huidige gebruiker](screens/Doc_get_current_user.png)
![Screen van FastAPI docs voor aanmaken van films](screens/Doc_post_movies.png)
![Screen van FastAPI docs voor weergeven films](screens/Doc_get_movies.png)
![Screen van FastAPI docs voor aanmaken ratings](screens/Doc_post_ratings.png)
![Screen van FastAPI docs voor weergeven ratings](screens/Doc_get_ratings.png)
![Screen van FastAPI docs voor verwijderen ratings](screens/Doc_delete_ratings.png)
![Screen van FastAPI docs voor weergeven film](screens/Doc_get_movie.png)
![Screen van FastAPI docs voor updaten ratings](screens/Doc_put_rating.png)


### Hosted API
Dit is de link waar mijn API wordt gehost op Okteto: [Hosted API](https://api-service-jorbensterckx.cloud.okteto.net/)
