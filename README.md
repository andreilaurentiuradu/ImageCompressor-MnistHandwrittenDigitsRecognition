Radu Andrei-Laurentiu 312CC

Task1
	Realizam compresia unei imagini primita ca parametru 
utilizand descompunerea in valori singulare. Functia intoarce 
aproximarea fotografiei initiale convertita la uint8.

Task2
	Calculam principalele componente folosind SVD si algoritmul 
prezentat:
	1)normalizam matricea initiala scazand din ea media 
fiecarui rand. Pentru asta facem o parcurgere pe randuri.
  	2)construim matricea Z pe baza formulei
	3)calculam matricile U, S si V din SVD aplicat matricii Z
	4)construim matricea W din primele pcs coloane ale lui V
	5)calculam matricea Y pe baza formulei
	6)aproximam matricea initiala pe baza formulei
	7)transforma matricea in uint8 pentru a fi o imagine valida

Task3
	Calculam componentele principale folosind un algoritm bazat 
pe matricea de covarianta:
	1)calculam media fiecarui rand al matricii.
  	2)normalizam matricea initiala scazand din ea media fiecarui 
rand. Pentru asta facem o parcurgere
	3)calculam matricea de covarianta pe baza formulei
	4)calculam vectorii si valorile proprii ale matricei de 
covarianta.
	5)ordonam descrescator valorile proprii si creaza o matrice 
V formata din vectorii proprii asezati pe coloane, astfel incat prima 
coloana sa fie vectorul propriu corespunzator celei mai mari valori 
proprii si asa mai departe.Luam dimensiunea matricii patratice ce contine 
valorile proprii pe diagonala principala
	6)sortam descrescator valorile proprii in matrice si interschimbam 
coloanele matricii cu vectorii proprii pe baza lor
	7)pastram doar primele pcs coloane
	8)construim matricea W din primele pcs coloane ale lui V
	9)cream matricea Y schimband baza matricii initiale.
	10)calculam matricea new_X care este o aproximatie a matricii 
initiale
	11)adunam media randurilor scazuta anterior.
	12)transformam matricea in uint8 pentru a fi o imagine valida.
	
Task4
	Realizam un algoritm pentru recunoasterea cifrelor scrise de mana, 
utilizand urmatoarele functii:
	1)Functia prepare_data importa datele necesare din fisierul „mnist.mat”.
	2)Functia visualise_image arata imaginea cu numarul
number din setul de date. Daca decomentati ultima comanda, atunci puteti 
vedea imaginea cu care lucrati.
	3)Functia magic_with_pca aplica PCA asupra matricii de antrenament, 
implementand pasii 2-9 din algoritmul de predictie.
	4)Functia prepare_photo primeste imaginea de test pe care o modifica 
si o transforma intr-un sir pentru a se putea face mai usor predictia. 	
Imaginile de antrenament au fundalul negru si cifra alba, pe cand cele de 
test au fundalul alb si cifra neagra, asa ca trebuie sa se inverseze culorile.
	5)Functia KNN aplica algoritmul de k-nearest neighbours.
	6)Functia classify_image pune cap la cap functiile anterioare pentru 
a returna predictia pe care o face.

	
	
	
	

