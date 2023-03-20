# Tugas-pertemuan-3

ayah(john, peter).
ayah(john, mary).
ayah(david, liza).
ayah(david, john).
ayah(jack, susan).
ayah(jack, ray).
bunda(susan, peter).
bunda(susan, mary).
bunda(amy, liza).
bunda(amy, john).
bunda(karen, susan).
bunda(karen, ray).

ortu(X,Y):-ayah(X,Y);bunda(X,Y).
saudaraKandung(Z,Y):- ayah(Z,X),ayah(Z,Y),X\=Y; bunda(Z,X),bunda(Z,Y), X\=Y.
sepupu(X,Y):-ortu(Z,X),ortu(W,Y),saudaraKandung(Z,W),X\=Y.
ponakan(X,Y):- saudaraKandung(Z,Y),ortu(Z,X).
suami(X,Y):- menikah(X,Y),ayah(X,Z),ortu(Z,Y).
