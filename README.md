# Graf tez i orzeczeń – dashboard ewaluacji

Interaktywny dashboard ewaluacji ekstrakcji tez prawnych z 10 orzeczeń arkusza
referencyjnego: model językowy wydobywa tezy z uzasadnienia prawnego, walidator
9 kryteriów je potwierdza, a arkusz dobrych i złych tez służy wyłącznie do oceny.

Zakładki: Gemma 4 31B, Qwen3 32B i Bielik 11B v3 (vLLM), po 3 przebiegi.

Dashboard: `index.html` (jeden plik; dane wbudowane, biblioteka grafu z CDN).
Generowany przez `3_run_evaluation.py --przebiegi` w repozytorium projektu.

## Przeglądarka tez orzeczeń

`przegladarka/index.html` – aplikacja w trzech widokach: wyszukiwanie orzeczeń
i tez tematycznych, treść orzeczenia z podświetlonymi tezami i przepisami, graf
tych samych tez w różnych orzeczeniach. Dane: tezy wydobyte i potwierdzone przez
Gemmę 4 31B (vLLM). Generowana przez `aplikacja/zbuduj_dane.py`.
