# Esercizio - Spring Boot - CRUD
* scrivere un'applicazione Spring Boot con le dipendenze necessarie che:
  * ha un'entità chiamata "Car" con le seguenti colonne:
    * un `id`
    * un `nomemodello`
    * un `tipo`
  * ha un repository dedicato per `Car`
  * ha un controller dedicato per `Car` che:
    * è mappato su `cars`
    * esegue le seguenti operazioni CRUD:
      * crea una nuova `Car`
      * restituisce un elenco di tutte le `Car`
      * restituisce un singolo `Car` - se `id` non è nel db (usa `existsById()`), restituisce un `Car` vuoto
      * aggiorna il `type` di una specifica `Car`, identificata da `id` e passando un parametro di query - se non presente nel db, restituisce una `Car` vuota
      * elimina una specifica `Car` - se assente, la risposta avrà uno stato HTTP `Conflict`
      * cancella tutte le `Car` nel db
* testare gli endpoint utilizzando `Postman` per:
  * creando 2 auto diverse
  * recuperare tutte le auto
  * recupero di un'auto tramite `id`
  * cercando di recuperare un'auto assente
  * aggiorna il `tipo` di una specifica `Auto`
  * cercando di aggiornare un'auto assente
  * eliminazione di una specifica `Car`
  * cercando di eliminare una `Car` assente
  * cancellando tutti i db
* **nota per i revisori**: visualizza "CarCRUD.postman_collection.json" nella cartella principale per tutte le chiamate "Postman"

# Exercise - Spring Boot - CRUD
* write a Spring Boot application with the necessary dependencies that:
  * has an entity called `Car` with the following columns:
    * an `id`
    * a `modelName`
    * a `type`
  * has a dedicated repository for the `Car`
  * has a dedicated controller for the `Car` that:
    * is mapped on `cars`
    * executes the following CRUD operations:
      * create a new `Car`
      * return a list of all the `Car`s
      * return a single `Car` - if the `id` is not in the db (use `existsById()`), returns an empty `Car`
      * updates the `type` of a specific `Car`, identified by `id` and passing a query param - if not present in the db, returns an empty `Car`
      * deletes a specific `Car` - if absent, the response will have a `Conflict` HTTP status
      * deletes all the `Car`s in the db
* test the endpoints using `Postman` for:
  * creating 2 different cars
  * retrieving all the cars
  * retrieving a car by the `id`
  * trying to retrieve an absent car
  * updates the `type` of a specific `Car`
  * trying to update an absent car
  * deleting a specific `Car`
  * trying to delete an absent `Car`
  * deleting all the db 
* **note for reviewers**: view `CarCRUD.postman_collection.json` in the root folder for all the `Postman` calls
