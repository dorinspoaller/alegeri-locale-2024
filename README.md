# Alegerile locale din România, 9 iunie 2024, localitate cu localitate

Rezultatele oficiale ale alegerilor locale din 2024 pentru fiecare comună, oraș, municipiu și sector din România (3.186 de unități): primari, consilii locale, consilii județene și președinți ai consiliilor județene. Sunt incluse toate candidaturile, nu doar câștigătorii.

Datele au fost descărcate manual, județ cu județ, de pe platforma Autorității Electorale Permanente. Aici sunt păstrate și fișierele originale, neschimbate, și tabele curățate, gata de folosit.

Harta făcută pe baza lor: [romaniainteractiva.ro/locale](https://romaniainteractiva.ro/locale/)

## Ce conține

### `date/`: tabele curățate

Toate fișierele sunt CSV, cu codare UTF-8 și diacritice corecte (ș, ț). Fiecare rând are codul **SIRUTA** al unității administrative, ca să poată fi legat de alte seturi de date, de exemplu de recensăminte.

| Fișier | Un rând pentru | Rânduri |
|---|---|---|
| `uat_sumar.csv` | fiecare comună, oraș, municipiu și sector: cine a câștigat fiecare alegere | 3.186 |
| `primari_candidati.csv` | fiecare candidat la primărie, cu voturile și procentul lui | 11.385 |
| `consilii_locale.csv` | fiecare partid sau independent din fiecare consiliu local, cu voturi și mandate | 14.958 |
| `consilii_judetene_pe_uat.csv` | votul pentru consiliul județean, pe partide, în fiecare localitate | 25.200 |
| `presedinti_cj_pe_uat.csv` | votul pentru președintele CJ, pe candidați, în fiecare localitate | 21.034 |
| `presedinti_cj_alesi.csv` | președintele de consiliu județean ales în fiecare județ și primarul general al Bucureștiului | 42 |

Coloane comune:
- `siruta`: codul SIRUTA al unității administrativ-teritoriale (pentru București, codul sectorului);
- `uat`, `judet`, `tip_uat` (municipiu, oraș, comună, sector);
- `partid`: denumirea completă, ca în procesele-verbale; `partid_scurt`: denumirea uzuală (PSD, PNL, Alianța PSD–PNL etc.);
- `voturi` și `procent`: procentul e calculat din voturile valabil exprimate pentru acea alegere, în acea localitate.

### `originale/`: fișierele AEP, neschimbate

- `primari-pe-judete.zip`, `consilii-locale-pe-judete.zip`, `consilii-judetene-pe-judete.zip`, `presedinti-cj-pe-judete.zip`: câte 42 de fișiere, unul pe județ, exact cum au fost descărcate de la AEP. Primarii și consiliile locale sunt pe unități administrative; consiliile județene și președinții CJ sunt pe secții de votare.
- `pv_final_cntry_*.csv`: totalurile pe județe, folosite pentru verificare.

## Verificări

- Numărul de primari pe partide coincide cu totalurile oficiale AEP: PSD 1.674, PNL 1.133, UDMR 200, independenți 43.
- În două comune primii doi candidați la primărie au avut exact același număr de voturi, iar alegerile s-au repetat: **Poșaga** (Alba) și **Chețani** (Mureș). În `uat_sumar.csv` au `egalitate_primar = 1` și nu au primar ales trecut.
- Rezultatele turului repetat din aceste două comune nu sunt incluse.

## Note

- **București**: fiecare sector are primarul și consiliul local propriu. Pentru consiliul județean este folosit Consiliul General al Municipiului București, iar pentru președintele CJ, primarul general.
- **Consiliul local**: `partid_cl_cele_mai_multe_mandate` e partidul cu cele mai multe mandate (la egalitate de mandate, cel cu mai multe voturi). `partid_cl_cele_mai_multe_voturi` e partidul cu cele mai multe voturi. De obicei coincid, dar nu întotdeauna.
- **Candidații independenți** apar cu partidul „Independent”.
- Numele candidaților sunt scrise cu literă mare doar la inițiale; forma oficială, cu majuscule, e în fișierele originale.

## Sursa

**Autoritatea Electorală Permanentă (AEP)**, procesele-verbale finale ale alegerilor locale din 9 iunie 2024, publicate pe platforma [prezenta.roaep.ro](https://prezenta.roaep.ro). Numele județelor și ale localităților sunt cele din nomenclatorul SIRUTA al Institutului Național de Statistică.

## Licență și citare

Rezultatele electorale aparțin **Autorității Electorale Permanente**. Dacă le folosești, citează AEP ca sursă.

Curățarea, unificarea și legarea datelor sunt publicate sub licența [Creative Commons Atribuire 4.0 Internațional (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.ro). Le poți folosi, modifica și republica liber, inclusiv în scop comercial, dacă menționezi sursa.

Sugestie de citare:

> Spoaller, D. (2026). *Alegerile locale din România, 9 iunie 2024, localitate cu localitate* [set de date]. România Interactivă. https://github.com/dorinspoaller/alegeri-locale-2024

Contact: dorin.spoaller@ubbcluj.ro
