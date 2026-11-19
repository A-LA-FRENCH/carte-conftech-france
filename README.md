# Carte des conférences tech en France

Carte interactive, en français et en anglais, des conférences et meetups tech en France métropolitaine et en outre-mer, jusqu'au 31 décembre 2027 : développeurs, IA, API, GreenTech, cloud native, cybersécurité, data, open source, agile et produit, salons.

*English version below.*

## Ce que fait la page

- Une carte de France avec une pastille par ville, un encart pour les lieux parisiens et une rangée de tuiles pour l'outre-mer.
- Une liste datée, filtrable par thème, mois, lieu, mot-clé et par signataires de la [lettre ouverte de l'AFUP](https://lettreouverte.afup.org/#signataires).
- Les événements terminés passent d'eux-mêmes dans la section « Événements passés », d'après la date du jour.
- Les conférences co-localisées de la FOST (CNIT Forest, 1er–3 décembre 2026) sont comptées comme des événements indépendants.

Tout tient dans un seul fichier, `index.html`, sans dépendance ni serveur. Il suffit de l'ouvrir dans un navigateur, ou d'activer GitHub Pages sur la branche `main`.

## Ajouter ou corriger un événement

Les données sont dans le `<script>` de `index.html`, entre les commentaires `// EVENTS-START` et `// EVENTS-END`. Un événement est un objet :

```js
{n:"Nom", s:"2027-03-11", e:"2027-03-12", p:"nantes",
 c:["dev","cloud"], u:"https://exemple.org/",
 d:{fr:"Une phrase en français.", en:"One sentence in English."}}
```

| Champ | Rôle |
| --- | --- |
| `n` | Nom de l'événement |
| `s`, `e` | Dates de début et de fin, au format AAAA-MM-JJ |
| `p` | Clé de `PLACES` (ville de métropole) ou de `OM` (territoire d'outre-mer : `gp`, `mq`, `gf`, `re`, `yt`, `nc`, `pf`) |
| `vk` | Clé de `VENUES`, pour les événements d'Île-de-France |
| `v` | Lieu précis, facultatif : `{fr, en}` |
| `c` | Thèmes parmi `dev`, `ai`, `api`, `cloud`, `green`, `cyber`, `data`, `oss`, `lead`, `eco` |
| `sig` | Nom du signataire de la lettre ouverte AFUP, si l'organisateur en fait partie |
| `u` | Lien vers l'événement |
| `d` | Description d'une phrase : `{fr, en}` |
| `note` | Précision facultative, par exemple des dates contradictoires : `{fr, en}` |

Pour une nouvelle ville, ajoutez une entrée dans `PLACES` avec sa latitude et sa longitude. Les contributions sont bienvenues par pull request.

## Sources

[dev.events](https://dev.events/EU/FR), [developers-conferences-agenda](https://github.com/scraly/developers-conferences-agenda), [Agenda Tech](https://www.agenda-tech.com/agenda), la [lettre ouverte de l'AFUP](https://lettreouverte.afup.org/#signataires), [FOST Paris](https://apidays.global/fost-events/paris), meetup.com et les sites des organisateurs. Les contours des régions viennent de [france-geojson](https://github.com/gregoiredavid/france-geojson).

Vérifiez toujours dates et lieux auprès des organisateurs avant de réserver : certaines dates diffèrent d'une source à l'autre et sont signalées sur la fiche de l'événement.

---

# Tech conference map of France

An interactive map, in French and English, of tech conferences and meetups in mainland France and its overseas territories until 31 December 2027: developers, AI, API, GreenTech, cloud native, cybersecurity, data, open source, agile and product, trade shows.

## What the page does

- A map of France with one pin per city, an inset for Paris-area venues and a row of tiles for the overseas territories.
- A dated list you can filter by topic, month, place, keyword and by signatories of the [AFUP open letter](https://lettreouverte.afup.org/#signataires).
- Finished events move to the "Past events" section by themselves, based on today's date.
- The conferences co-located at FOST (CNIT Forest, 1–3 December 2026) are counted as separate events.

Everything lives in a single file, `index.html`, with no dependency and no server. Open it in a browser, or turn on GitHub Pages for the `main` branch.

## Adding or fixing an event

The data sits in the `<script>` of `index.html`, between the `// EVENTS-START` and `// EVENTS-END` comments. The fields are described in the table above: name, ISO start and end dates, place key, topics, link, and a one-sentence description in both languages. Pull requests are welcome.

## Sources

[dev.events](https://dev.events/EU/FR), [developers-conferences-agenda](https://github.com/scraly/developers-conferences-agenda), [Agenda Tech](https://www.agenda-tech.com/agenda), the [AFUP open letter](https://lettreouverte.afup.org/#signataires), [FOST Paris](https://apidays.global/fost-events/paris), meetup.com and organisers' own sites. Region outlines come from [france-geojson](https://github.com/gregoiredavid/france-geojson).

Always check dates and venues with the organisers before booking: some dates differ between sources and are flagged on the event card.
