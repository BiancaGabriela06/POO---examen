# POO---examen
Teorie, exercitii, subiecte rezolvate pentru examen

***CURS 1 extract***

Supraîncărcarea funcțiilot (Polimorfism la compilare) se face prin folosirea aceluiasi nume pentru functii diferite, dar cu inteles apropiat, ele difera pron numarul si tipul parametrilor. Daca diferenta e doar la tipul de date intors, atunci va fi EROARE DE COMPILARE

Tipul referinta - o referinta trebuie sa fie initializată când este definita, daca nu este membră a unei clase, un parametru de functie sau o valoare returnata.
                - nu se poate obtine adresa unei referinte
                - nu se poate face referinta la un camp de biti
              
 #Principalele concepte utilizate in POO sunt:
* Obiecte
* Clase
* Mostenire
* Ascunderea informatiei
* Polimorfism

**CLASA** defineste atribute si metode; folositoare la ascunderea informatiilor si la reutilizare de cod(mostenire).                                                           
**OBIECTUL** este o instanta a unei clase care are o anumita stare (repr. prin valoare) si are un comportament (repr. prin functii).   
**INCAPSULAREA** contopirea datelor cu codul.              
**MOSTENIREA** este posibilitarea de a extinde o clasa prin adaugarea de noi functionalitati; reutilizare de cod.         
**ASCUNDEREA INFORMATIEI**

![image](https://user-images.githubusercontent.com/92989083/159280198-e5a61990-1be6-4f3f-86a7-01c1422d37e8.png)

**POLIMORFISMUL** intr-o ierarhie de clase obtinuta prin mostenire, o metoda poate avea implementari diferite la nivele diferite in acea ierarhie.

***CURS 2 extract***                                          
**AGREGAREA** ( ierarhia de obiecte ) compunerea unui obiect din mai multe obiecte mai simple. ( "has a" )                    
**MOSTENIREA** (ierarhia de clase ) relatie intre clase in care o clasa mosteneste stuctura si comportarea definita in una sau mai multe clase. ( "is a ", "is like a") 
      *terminologie* : clasa de baza -  clasa derivata , superclasa - subclasa , parinte - fiu 
      
**POLIMORFISM** la compilare sau la executie

***CURS 3 extract***

*Struct si class* : singura diferenta este ca struct are default **membrii publici**, iar class **membrii privati**                                          
*Union si class* : membrii sunt publici (by default)                                                                   
                 Union ca o clasa                                                                    
                 * nu poate mosteni si nu se poate mosteni din el                                                                         
                 * nu avem obiecte care fac overoad pe =                                                                                              
                 * obiecte cu constructor sau destructor definiti nu pot fi membri in union                                                              
                 Union anonime                                                                                                      
                 * nu au nume pentru tip                                                                                                      
                 * nu se pot declara obiecte de tipul respectriv                                                                                               
                 * sunt folosite pentru a spune compilatorului cum se aloc/procesez variabilele respective in memorie                                                 
                 * variabilele din union sunt accesibile ca si cum ar fi declarate in blocul respectiv                                                                
   
 *Functii **prieten***                                                                                                                                          
         * pentru a accesa campurile **protected**, **private** din alta clasa                                                                               
         * folositoare la **overload**-area operatorilor pentru unele functii de I/O    
         * pot fi *clase prieten* si *clase prietene cu functii*                                                                  
         * in rest nu prea conteaza 😂                                                 

*Constructori si destructori*
          * initializare automata, nu se specifica tipul returnat                                                                      
          * obiectele nu sunt statice                                                                                     
          * **constructorul** are numele clasei; **destructorul** are ~numele clasei                                                       
          * **constructorul** poate avea parametri ( impliciti ) si se pot supradefini; **destructorul** este unic si fara parametri                                
          * este **necesar** si constructorul **de copiere** : creeaza un obiect preluand valorile corespunzatoare altui obiect, folosit doar la initializari                           
          * constructorii parametrizati pot fi definiti cu mai multe variante de numere si tipuri de parametri --> overload de constructori  
          * constructorii se apeleaza in ordinea declararii obiectelor, iar destructorii in sens invers
          * daca o functie are ca parametru un obiect, care nu e transmis cu referinta, atunci se activaza constructorul de copiere si implicit, la iesirea din
          functie, obiectul se distruge, deci se apeleaza destructorul    
          * **Polimorfism pe constructori** - foarte comun sa fie supraincarcati, pentru a putea defini obiecte initializate si neinitializate; **NU SE POT INITIALIZA 
          OBIECTE DINTR-O LISTA ALOCATA DINAMIC**                                                         
          * **overload pe constructori** -> flexibilitate; definim constructori pentru toate modurile de initializare                                   
          Constructor de copiele:                                                                                                              
  ![image](https://user-images.githubusercontent.com/92989083/159311416-28616fb9-e452-4690-901f-577d8816d9c1.png)

          
          
  ![image](https://user-images.githubusercontent.com/92989083/159305061-866ffe7e-2b29-4e78-a1cc-5d38f180ad79.png)


**CURS 4+5 extract**
  *Membrii statici ai unei clase*
          * date membre : **nestatice** ( distincte pentru fiecare obiect) si **statice** ( unicce pentru toate obiectele clasei, exista o singura copie pt. toate 
          obiectele                                               
          * cuvantul cheie este **static**
          * sunt create, initializate si accesate independent de obiecte clasei **+** alocarea si initializarea se face in afara clasei
          * **functii statice** -> efectueaza operatii asupra intregii clase, nu au cuvantul cheie *this* 
          * ** referirea mebrilor statici** -> clasa :: membru;   obiect.membru (identic cu nestatic).
      "::" se numeste **operator de rezolutie de scop** ( exemplul din curs este cu o variabila declarata global. in clasa i se atribuie 10 astfel -> ::i = 10)
   
   *Clase locale*                                                                                           
          * putem defini clase in clase sau functii, iar operatorul de rezolutie de scop ajuta in aceste cazuri; totusi sunt rar utilizate       
     
   *Functii care intorc obiecte*                                                         
          * o functie poate intoarce obiecte ; un obiect temporar este creat **automat** pentru a tine informatiile din obiectul de intors. acesta este obiectul de
          intors. dupa ce valoarea a fost intoarsa, acest obiect este distrus;                                                         
                             ** in cazul de mai sus mentionat, sunt probleme cu memoria dinamica. solutia este polimorfism pe = si pe constructorul de copiere**
                         
   *Supraincarcarea operatorilor in c++*
   
   
   
   **CURS 6 extract**                                                                                              
         *Mostenirea    ----- >    class Y: public/protected/private X  { /*declaratii*}                                                       
                   
      
          

