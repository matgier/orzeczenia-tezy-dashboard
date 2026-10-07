# Graf tez i orzeczeń – dashboard ewaluacji

Interaktywny dashboard ewaluacji ekstrakcji tez prawnych z 10 orzeczeń arkusza
referencyjnego: model językowy wydobywa tezy z uzasadnienia prawnego, walidator
9 kryteriów je potwierdza, a arkusz dobrych i złych tez służy wyłącznie do oceny.

Zakładki: Gemma 4 31B, Qwen3 32B i Bielik 11B v3 (vLLM), po 3 przebiegi.

Dashboard: `index.html` (jeden plik; dane wbudowane, biblioteka grafu z CDN).
Generowany przez `3_run_evaluation.py --przebiegi` w repozytorium projektu.

## Wyszukiwarka orzeczeń z tezami

`przegladarka/index.html` – narzędzie dla prawników (262 orzeczenia, 1196 potwierdzonych tez): tryby zapytanie,
artykuł, temat, klaster i opis sytuacji; orzeczenia w kolejności trafności i znaczenia (tezy powtórzone w innych
orzeczeniach, powołania); pełna metryka SAOS i tekst orzeczenia jak w oryginale z podświetlonymi tezami; ocena tez
i oznaczanie nowych tez do zbioru walidacyjnego (zapis w przeglądarce, eksport JSON/CSV). Na tej stronie działa
podobieństwo słów (BM25); podobieństwo znaczeniowe (BGE-M3, MMLW, hybrydowe) – po uruchomieniu
`./uruchom_wyszukiwarke.sh` na własnym komputerze. Dane: tezy wydobyte i potwierdzone przez Gemmę 4 31B (vLLM).
Generowana przez `aplikacja/zbuduj_dane.py`.
