# Personal-name replacement log

This file records the deterministic replacement of occupational/common-noun NPs with German personal names in `sentences_mvb_8_versions.csv`.

## Reproducibility and scope

- Assignment seed: `spr-norming-strong-gender-names-v2-2026-07-27`
- Source SHA-256: `0ad83476c1b8b4f4d4550978fa57557886360ee5f62a4847cc6fbdca6aa4780e`
- Superseded previous personal-name CSV SHA-256: `8a5cbb7ec58856239ba24061f93cfbee0471d0c154bec52e2f1661b5baffede9`
- Modified SHA-256: `d65e63a83344637724108d78c33e108545a934edfee64a917ed62a6c74b7005b`
- Shape preserved: 936 data rows × 45 columns; 117 `list_item` values × 8 rows each.
- Encoding and line endings preserved: UTF-8 with BOM, CRLF.
- Each `list_item` uses one fixed four-name set: NP1 male, NP1 female, NP2 male, NP2 female.
- Within a `list_item`, the two male names differ and the two female names differ.
- Each personal name is assigned to at most 10 item roles across the 234 roles of its gender.
- The pools intentionally exclude names that can plausibly be read as gender-neutral or cross-gender in German/international contexts (for example Finn, Kim, Robin, Sascha, Andrea, Jan, and Kai).
- `original`, `both_male`, `both_female`, and `swapped` select names according to their existing gender design.
- Prepositions (`mit`, `bei`), separable-verb particles, punctuation, verbs, pronouns, adjectives, and all non-NP sentence material were preserved.

## Name-selection sources

- Cross-generational frequency list for Germany (separate female/male rankings): https://www.beliebte-vornamen.de/28071-derzeit-lebende-bevoelkerung.htm
- GfdS 2016 list of common girls' and boys' names: https://gfds.de/nur-dieses-jahr-die-beliebtesten-35-maedchen-und-jungennamen/
- Linda: explicitly classified as a female first name, with German frequency history: https://www.beliebte-vornamen.de/7792-linda.htm
- David: explicitly classified as a male first name, with German frequency history: https://www.beliebte-vornamen.de/4914-david.htm

Selection policy: names were drawn primarily from the most common names across Germany's living population, then manually restricted to conventional spellings with a strong and familiar female/male reading. Linda and David were retained as requested exemplars. The source notes that Germany has no central official first-name register, so the frequency ranking is a research-based estimate rather than an official census.

## Changed columns

| Column | Changed cells | Rule |
|---|---:|---|
| `NP1` | 936 | Replaced the original NP1 expression with its assigned personal name. |
| `NP2` | 936 | Replaced the original NP2 expression with its assigned personal name while retaining prepositions/verb particles/punctuation. |
| `NP1 - male` | 936 | Assigned NP1 male name for the item. |
| `NP1 - female` | 936 | Assigned NP1 female name for the item. |
| `NP2 - male` | 936 | Assigned NP2 male name for the item. |
| `NP2 - female` | 936 | Assigned NP2 female name for the item. |
| `Generated-Sentence` | 936 | Replaced only the initial NP1 and NP2 expressions; the remaining sentence substring is byte-for-byte unchanged. |

Total changed cells: 6552. All other 38 columns are unchanged in every row.

## Names used

Male (24 unique; each assigned to 9–10 item roles): Alexander, Andreas, Christian, Daniel, David, Florian, Frank, Hans, Johannes, Jürgen, Karl, Klaus, Martin, Matthias, Michael, Paul, Peter, Philipp, Sebastian, Stefan, Thomas, Tobias, Uwe, Wolfgang.

Female (24 unique; each assigned to 9–10 item roles): Anna, Barbara, Birgit, Claudia, Daniela, Eva, Jana, Johanna, Julia, Katharina, Laura, Lena, Linda, Lisa, Maria, Martina, Monika, Nicole, Nina, Petra, Renate, Sabine, Sarah, Susanne.

## Per-item assignment and original expressions

| list_item | Original NP1 male | NP1 male name | Original NP1 female | NP1 female name | Original NP2 male | NP2 male name | Original NP2 female | NP2 female name |
|---:|---|---|---|---|---|---|---|---|
| 1 | Der Schüler | David | Die Schülerin | Sabine | den Lehrer | Frank | die Lehrerin | Linda |
| 2 | Der Bär | Peter | Die Bärin | Eva | den Löwen | Sebastian | die Löwin | Katharina |
| 3 | Der Schäferhund | Michael | Die Schäferhündin | Nina | der Besitzer | Stefan | die Besitzerin | Barbara |
| 4 | Der Schaffner | Martin | Die Schaffnerin | Renate | den Reisenden | Tobias | die Reisende | Birgit |
| 5 | Der Liebhaber | Paul | Die Liebhaberin | Maria | den Komponisten | Florian | die Komponistin | Petra |
| 6 | Der Zuschauer | Daniel | Die Zuschauerin | Martina | den Puppenspieler | Karl | die Puppenspielerin | Jana |
| 7 | Der Schamane | Johannes | Die Schamanin | Claudia | den Gott | Jürgen | die Göttin | Julia |
| 8 | Der Krankenpfleger | Philipp | Die Krankenpflegerin | Daniela | den Patienten | Alexander | die Patientin | Susanne |
| 9 | Der Richter | Andreas | Die Richterin | Lisa | den Mann | Thomas | die Frau | Johanna |
| 10 | Der Kellner | Christian | Die Kellnerin | Laura | den Besucher | Matthias | die Besucherin | Anna |
| 11 | Der Verkäufer | Uwe | Die Verkäuferin | Sarah | den Kunden | Klaus | die Kundin | Nicole |
| 12 | Der Freund  | Hans | Die Freundin | Monika | dem Mann | Wolfgang | der Frau | Lena |
| 13 | Der Redner | Karl | Die Rednerin | Nina | den Zuhörer | Christian | die Zuhörerin | Jana |
| 14 | Der Sohn | Alexander | Die Tochter | Katharina | den Vater | Tobias | die Mutter | Laura |
| 15 | Der Stiefsohn | David | Die Stieftochter | Renate | den Urgroßvater | Wolfgang | die Urgroßmutter | Sabine |
| 16 | Der Magier | Michael | Die Magierin | Barbara | den Prinzen | Paul | die Prinzessin | Claudia |
| 17 | Der Therapeut | Martin | Die Therapeutin | Monika | den Soldaten | Thomas | die Soldatin | Martina |
| 18 | Der Senior | Frank | Die Seniorin | Eva | den Herrn | Uwe | die Dame | Julia |
| 19 | Der Lehrer | Daniel | Die Lehrerin | Lisa | den Schüler | Johannes | die Schülerin | Lena |
| 20 | Der Soldat | Hans | Die Soldatin | Daniela | den Feind | Peter | die Feindin | Maria |
| 21 | Der Chef | Sebastian | Die Chefin | Sarah | den Mitarbeiter | Stefan | die Mitarbeiterin | Anna |
| 22 | Der Assistent | Florian | Die Assistentin | Linda | den Wissenschaftler | Matthias | die Wissenschaftlerin | Susanne |
| 23 | Der Unteroffizier | Andreas | Die Unteroffizierin | Nicole | den Oberleutnant | Klaus | die Oberleutnantin | Birgit |
| 24 | Der Trainer | Jürgen | Die Trainerin | Johanna | den Spieler | Philipp | die Spielerin | Petra |
| 25 | Der Junge | Peter | Das Mädchen | Claudia | den Freund | Stefan | die Freundin | Daniela |
| 26 | Der Studienrat | Klaus | Die Studienrätin | Sabine | den Schüler | Hans | die Schülerin | Renate |
| 27 | Der Schöne | Andreas | Die Schöne | Lisa | den Verehrer | Jürgen | die Verehrerin | Sarah |
| 28 | Der Erzieher | Martin | Die Erzieherin | Martina | den Jugendlichen | Karl | die Jugendliche | Linda |
| 29 | Der Leistungssportler | Florian | Die Leistungssportlerin | Laura | den Freizeitsportler | Johannes | die Freizeitsportlerin | Barbara |
| 30 | Der Trainer | Paul | Die Trainerin | Johanna | den Spieler | Sebastian | die Spielerin | Lena |
| 31 | Der Mann | Michael | Die Frau | Eva | den Rivalen | Tobias | die Rivalin | Maria |
| 32 | Der Landwirt | Christian | Die Landwirtin | Susanne | den Politiker | David | die Politikerin | Nicole |
| 33 | Der Vater | Thomas | Die Mutter | Jana | dem Dieb | Wolfgang | der Diebin | Birgit |
| 34 | Der Dörfler | Frank | Die Dörflerin | Petra | den Bürgermeister | Uwe | die Bürgermeisterin | Anna |
| 35 | Der Dieb | Daniel | Die Diebin | Nina | den Rivalen | Philipp | die Rivalin | Julia |
| 36 | Der Mieter | Matthias | Die Mieterin | Monika | den Einbrecher | Alexander | die Einbrecherin | Katharina |
| 37 | Der Wächter | Philipp | Die Wächterin | Maria | den Autodieb | Daniel | die Autodiebin | Daniela |
| 38 | Der Eremit | Matthias | Die Eremitin | Jana | den Anführer | Jürgen | die Anführerin | Julia |
| 39 | Der Schüler | Frank | Die Schülerin | Anna | den Zauberer | Hans | die Zauberin | Eva |
| 40 | Der Fürsprecher | Paul | Die Führsprecherin | Birgit | den Lehrer | Martin | die Lehrerin | Claudia |
| 41 | Der Kaiser | Sebastian | Die Kaiserin | Linda | den Gladiator | Andreas | die Gladiatorin | Susanne |
| 42 | Der Opa | Uwe | Die Oma | Martina | den Esel | Tobias | die Eselin | Barbara |
| 44 | Der Mann | Johannes | Die Frau | Sarah | den Kollegen | Klaus | die Kollegin | Laura |
| 45 | Der Mann | David | Die Frau | Renate | den Fremden | Alexander | die Fremde | Sabine |
| 46 | Der Verantwortliche | Wolfgang | Die Verantwortliche | Monika | den Schüler | Peter | die Schülerin | Nicole |
| 47 | Der Bewohner | Karl | Die Bewohnerin | Lena | den Kater | Thomas | die Katze | Lisa |
| 48 | Der Firmenleiter | Christian | Die Firmenleiterin | Petra | den Naturschützer | Michael | die Naturschützerin | Katharina |
| 49 | Der Botaniker | Florian | Die Botanikerin | Johanna | den Zoologen | Stefan | die Zoologin | Nina |
| 50 | Der Polizist | Hans | Die Polizistin | Birgit | den Randalierer | Thomas | die Randaliererin | Daniela |
| 51 | Der Hilfsarbeiter | Martin | Die Hilfsarbeiterin | Barbara | den Chef | David | die Chefin | Sabine |
| 52 | Der Mönch | Karl | Die Nonne | Claudia | den Teenager | Daniel | die Teenagerin | Martina |
| 53 | Der Anführer | Paul | Die Anführerin | Laura | den Krieger | Christian | die Kriegerin | Julia |
| 54 | Der Unternehmer | Peter | Die Unternehmerin | Maria | dem Bewerber | Stefan | der Bewerberin | Lisa |
| 55 | Der Gutsherr | Matthias | Die Gutsherrin | Nicole | den Knecht | Andreas | die Magd | Lena |
| 57 | Der Politiker | Tobias | Die Politikerin | Linda | den Parteigenossen | Jürgen | die Parteigenossin | Susanne |
| 58 | Der Leiter | Philipp | Die Leiterin | Monika | den Jugendlichen | Alexander | die Jugendliche | Katharina |
| 59 | Der Teilnehmer | Uwe | Die Teilnehmerin | Johanna | den Partner | Florian | die Partnerin | Petra |
| 60 | Der Nachrichtensprecher | Klaus | Die Nachrichtensprecherin | Renate | den Naturschützer | Michael | die Naturschützerin | Jana |
| 61 | Der Bruder | Frank | Die Schwester | Eva | den Kollegen | Johannes | die Kollegin | Nina |
| 62 | Der Neffe | Wolfgang | Die Nichte | Anna | dem Onkel | Sebastian | der Tante | Sarah |
| 63 | Der Mieter | Matthias | Die Mieterin | Claudia | den Vermieter | Jürgen | die Vermieterin | Sarah |
| 64 | Der Spieler | Daniel | Die Spielerin | Linda | den Trainer | Peter | die Trainerin | Barbara |
| 65 | Der Onkel | Andreas | Die Tante | Maria | den Neffen | Sebastian | die Nichte | Birgit |
| 66 | Der Verkäufer | Martin | Die Verkäuferin | Laura | den Kunden | Uwe | die Kundin | Monika |
| 67 | Der Darsteller | Frank | Die Darstellerin | Lena | den Zuschauer | Stefan | die Zuschauerin | Martina |
| 68 | Der Heimleiter | Karl | Die Heimleiterin | Anna | den Senioren | David | die Seniorin | Renate |
| 69 | Der Komiker | Wolfgang | Die Komikerin | Sabine | den Zuschauer | Alexander | die Zuschauerin | Petra |
| 70 | Der Chef | Tobias | Die Chefin | Julia | den Mitarbeiter | Michael | die Mitarbeiterin | Katharina |
| 71 | Der Arzt | Paul | Die Ärztin | Susanne | den Patienten | Hans | die Patientin | Lisa |
| 72 | Der Herr | Christian | Die Herrin | Jana | den Pagen | Klaus | die Zofe | Eva |
| 73 | Der Musiker | Philipp | Die Musikerin | Daniela | den Zuhörer | Thomas | die Zuhörerin | Nicole |
| 74 | Der Vater | Johannes | Die Mutter | Johanna | den Sohn | Florian | die Tochter | Nina |
| 75 | Der Schüler | Thomas | Die Schülerin | Susanne | den Lehrer | Andreas | die Lehrerin | Johanna |
| 76 | Der Akrobat | Tobias | Die Aktrobatin | Sabine | den Mann | Stefan | die Frau | Claudia |
| 77 | Der Anwohner | Karl | Die Anwohnerin | Barbara | den Obdachlosen | Philipp | die Obdachlose | Birgit |
| 78 | Der Onkel | Johannes | Die Tante | Monika | den Sohn | Klaus | die Tochter | Lisa |
| 79 | Der Priester | Michael | Die Priesterin | Petra | den Ministranten | Florian | die Ministrantin | Maria |
| 80 | Der Enkel | Matthias | Die Enkelin | Eva | dem Großvater | Frank | der Großmutter | Katharina |
| 81 | Der Judokämpfer | Sebastian | Die Judokämpferin | Sarah | den Gegner | Martin | die Gegnerin | Jana |
| 82 | Der Makler | Jürgen | Die Maklerin | Linda | den Interessenten | Christian | die Interessentin | Nina |
| 83 | Der Jugendliche | Wolfgang | Die Jugendliche | Laura | den Lehrer | Peter | die Lehrerin | Daniela |
| 84 | Der Zuhörer | Hans | Die Zuhörerin | Renate | den Referenten | David | die Referentin | Julia |
| 85 | Der Lehrer | Daniel | Die Lehrerin | Lena | den Schüler | Uwe | die Schülerin | Martina |
| 86 | Der Taxifahrer | Alexander | Die Taxifahrerin | Nicole | den Passagier | Paul | die Passagierin | Anna |
| 87 | Der Landwirt | Andreas | Die Landwirtin | Johanna | den Erntehelfer | Florian | die Erntehelferin | Linda |
| 88 | Der Sohn | Alexander | Die Tochter | Eva | den Vater | Karl | die Mutter | Petra |
| 89 | Der Angehörige | David | Die Angehörige | Renate | dem Mönch | Uwe | der Nonne | Sabine |
| 90 | Der Liebhaber | Christian | Die Liebhaberin | Lisa | den Liebsten | Peter | die Liebste | Nina |
| 91 | Der Spaziergänger | Frank | Die Spaziergängerin | Birgit | den Anwohner | Matthias | die Anwohnerin | Sarah |
| 92 | Der Wettkämpfer | Hans | Die Wettkämpferin | Monika | dem Trainer | Michael | der Trainerin | Anna |
| 93 | Der Witwer | Stefan | Die Witwe | Martina | den Kater | Daniel | die Katze | Jana |
| 94 | Der Sünder | Sebastian | Die Sünderin | Laura | dem Priester | Wolfgang | der Priesterin | Claudia |
| 95 | Der Hund | Johannes | Die Hündin | Katharina | dem Sohn | Tobias | der Tochter | Susanne |
| 96 | Der Ehemann | Paul | Die Ehefrau | Julia | den Nachbarn | Martin | die Nachbarin | Maria |
| 97 | Der Sohn | Jürgen | Die Tochter | Nicole | den Vater | Klaus | die Mutter | Barbara |
| 98 | Der Kunsthistoriker | Thomas | Die Kunsthistorikerin | Daniela | den Touristen | Philipp | die Touristin | Lena |
| 99 | Der Politiker | Uwe | Die Politikerin | Linda | den Parteigenossen | Martin | die Parteigenossin | Johanna |
| 100 | Der Student | Tobias | Die Studentin | Sabine | den Professor | Peter | die Professorin | Jana |
| 101 | Der Abt | Klaus | Die Abtissin | Lisa | den Mönch | Johannes | die Nonne | Laura |
| 102 | Der Schachspieler | Michael | Die Schachspielerin | Maria | dem Gegner | Wolfgang | der Gegnerin | Daniela |
| 103 | Der Aufseher | Jürgen | Die Aufseherin | Petra | den Gefangenen | Hans | die Gefangene | Birgit |
| 104 | Der Jugendbetreuer | David | Die Jugendbetreuerin | Nicole | den Sohn | Thomas | die Tochter | Katharina |
| 105 | Der Rugbyspieler | Alexander | Die Rugbyspielerin | Renate | den Schiedsrichter | Philipp | die Schiedsrichterin | Anna |
| 106 | Der Chef | Andreas | Die Chefin | Barbara | den Mitarbeiter | Florian | die Mitarbeiterin | Eva |
| 107 | Der Vater | Sebastian | Die Mutter | Susanne | den Sohn | Christian | die Tochter | Lena |
| 108 | Der Student | Daniel | Die Studentin | Julia | den Tutor | Karl | die Tutorin | Nina |
| 109 | Der Verwandte | Paul | Die Verwandte | Monika | den Bestatter | Stefan | die Bestatterin | Claudia |
| 111 | Der Flugbegleiter | Matthias | Die Flugbegleiterin | Sarah | den Passagier | Frank | die Passagierin | Martina |
| 112 | Der Tänzer | David | Die Tänzerin | Eva | den Zuschauer | Daniel | die Zuschauerin | Nicole |
| 113 | Der Bauer | Paul | Die Bäuerin | Nina | den Bullen | Matthias | die Kuh | Julia |
| 114 | Der Vater | Andreas | Die Mutter | Daniela | den Sohn | Wolfgang | die Tochter | Susanne |
| 115 | Der Polizist | Peter | Die Polizistin | Martina | den Dieb | Alexander | die Diebin | Sarah |
| 116 | Der Passant | Karl | Die Passantin | Monika | den Fremden | Florian | die Fremde | Birgit |
| 117 | Der Fahrradfahrer | Johannes | Die Fahrradfahrerin | Johanna | den Autofahrer | Tobias | die Autofahrerin | Sabine |
| 118 | Der Kommissar | Michael | Die Kommissarin | Barbara | den Zeugen | Christian | die Zeugin | Jana |
| 119 | Der Versuchsleiter | Hans | Die Versuchsleiterin | Anna | den Probanden | Klaus | die Probandin | Lena |
| 120 | Der Kater | Frank | Die Katze | Claudia | den Mäuserich | Philipp | die Maus | Renate |

## Special NP2 constructions retained

- `list_item=102`: retained `mit` (for example, `mit <Name>`).
- `list_item=106`: retained `bei` (for example, `bei <Name>`).
