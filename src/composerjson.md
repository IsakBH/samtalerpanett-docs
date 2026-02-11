# Composer.json
Composer.json er en fil som forteller både [Composer](https://getcomposer.org/) og mennesker som leser den litt informasjon om [Samtaler På Nett](https://isak.brunhenriksen.no/samtalerpanett). Den inneholder dependencies, navn, beskrivelse, forfattere og mer. Det er viktig at det ikke er noe feil om den, og at den er som den skal. Dette vil si: ikke fuck med den pls. Prøv å la Composer deale med alle insertions inn i den, og hvis det er noe du vil legge til så vennligst sjekk [dokumentasjonen til Composer](https://getcomposer.org/doc/04-schema.md).

Slik ser vår `composer.json` ut:
```json
{
    "require": {
        "phpmailer/phpmailer": "^7.0",
        "vlucas/phpdotenv": "^5.6",
        "cboden/ratchet": "^0.4.4"
    },

    "license": "MIT",
    "name": "isaveg/samtalerpanett",
    "description": "Et fint chatteprogram laget av Brun og Weiss",
    "type": "project",
    "authors": [
        {
            "name": "Isak Brun Henriksen",
            "email": "isak@brunhenriksen.net",
            "homepage": "https://isak.brunhenriksen.no",
            "role": "Developer"
        },
        {
            "name": "Viggo Weissmuller",
            "email": "veggene.v@gmail.com",
            "homepage": "https://veggenss.github.io/MinSide2025/",
            "role": "Developer"
        }
    ]
}

```