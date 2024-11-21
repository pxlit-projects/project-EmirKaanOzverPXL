# Architecture

Hier in dit document kunt u de gekozen architectuur vinden van dit project. Onderaan vind zich de architectuur schema.

# Client App

Voor de client applicatie wordt er gebruik gemaakt van een Angular app in TypeScript.

# Microservices

## Config Server

Centrale plaats waar alle configuratie en application details in worden opgeslagen. Elke microservice spreek dit aan om zijn configuratie op te laden bij startup.

## Eureka

De Eureka Discovery Service zorgt ervoor dat alle microservices elkaar kunnen weten te vinden in de backend.

## Services

- **Post Service**:
  - Behandeld --> US1, US2, US3, US4, US5
- **Review Service**:
  - Behandeld --> US7, US8, US9
- **Comment Service**:
  - Behandeld --> US10, US11, US12

## Andere Info

De communicatie tussen de microservices gebeurt synchroon (open-feign) of asynchroon (rabbitmq messagebus). Elke microservice heeft ook zijn eigen databank om aan te spreken.

## Syncrhone Communicatie
- Post opslaan als concept
- Inhoud post bewerken
- Posts bekijken
- Posts goedkeuren / afwijzen
- Opmerkingen toevoegen
- Andere comments lezen
- Eigen comments bewerken / verwijderen

## Asynchrone Communicatie
- Posts plaatsen
- Comments plaatsen

![Architecture Diagram](https://github.com/pxlit-projects/project-EmirKaanOzverPXL/blob/main/architecture/architecture.png)
