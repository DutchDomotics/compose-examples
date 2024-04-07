# Titel

## Introduction
Watchtower is een applicatie / container die je kan gebruiken om je containers up to date te houden dit automatisch
(al is het aangeraden dat zoveelmogelijk met de hand te doen als het een belangrijk iets is)


## uitleg componenten
 TODO

### toevoegen aan de te updaten containers 

De te updaten container kan je makkelijk voorzien van een zogenoemd label.
Op het moment dat een container onderstaand label bevat dan zal deze worden meegenomen in de update cyclus.

    ```yaml
        labels:
            # Watchtower add to auto update
            - com.centurylinklabs.watchtower.enable=true
    ```

Volledig voorbeeld:

    ```yaml
    version: "3"
    services:
        someimage:
            container_name: someimage
            labels:
              - "com.centurylinklabs.watchtower.enable=true"
    ```

### alleen monitoren (en melden)

Als je een container alleen wil monitoren (met het doel dat Watchtower meld dat er een update is).  
Dan gaat dat op een vergelijkbaare manier als het updaten, namelijk met een label:

    ```yaml
        labels:
            # Watchtower add to auto update
            - com.centurylinklabs.watchtower.monitor-only="true"
    ```

TODO Telegram voorbeeld:
## Referenties

Officiele site: [https://containrrr.dev/watchtower/]



[Dutchdomotics Discord](https://discord.gg/7ZVGJQwD)