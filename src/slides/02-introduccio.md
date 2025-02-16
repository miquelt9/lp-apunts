
class: center, middle


Llenguatges de Programació

# Conceptes bàsics

Albert Rubio, Jordi Petit, Fernando Orejas

<br/>

![:height 10em](img/periodic-table-pls.png)

<br/>

Universitat Politècnica de Catalunya, 2022

---

# Introducció

Un **llenguatge de programació** (LP) és un llenguatge formal utilitzat per
controlar el comportament d'un computador tot implementant un algorisme.

<br>
.center[![:height 10em](img/programming-languages-cloud.png)]
<br>



---

# Introducció

Tradicionalment, els LPs es consideren des de tres angles
(anàlegs a la lingüística):

- **Sintaxi:** la forma dels programes correctes.

- **Semàntica:** el significat de les construccions dels programes.

- **Pragmàtica:** com s'usa el LP.

<br>

La majoria d'LPs venen definits per

- una especificació estàndard, o

- una implementació de referència.



---

# Perquè estudiar els LPs?

- **Visió enginyeril:** Necessitem LPs per programar
computadors per fer coses xules.

- **Visió científica:** Necessitem LPs per descriure i raonar sobre aquestes computacions.


---

# Perquè estudiar els LPs?

Els LPs, en tant que llenguatges, ens permeten representar conceptes
<br> i són una eina de pensament.

**Exemples:**

.center[![:height 20em](img/llenguatges.png)]


---

# Perquè estudiar els LPs?


Els llenguatges que usem:

- influencien les nostres percepcions,
- guien i donen suport al nostre raonament,
- permeten i faciliten la nostra comunicació.

<br>

**Exemple:** Representacions dels nombres:

.center[
𒐖 𒌋𒐚 𒌍𒐖  &nbsp; / &nbsp;  𒌋𒐛 𒐘  &nbsp; = &nbsp; 𒐜

<span style="text-decoration:overline">Ⅷ</span>ⅭⅩⅭⅡ ÷ ⅯⅩⅩⅣ = Ⅷ

8192 / 1024 = 8

2<sup>13</sup> / 2<sup>10</sup> = 2<sup>13 - 10</sup> = 2<sup>3</sup>
]

---

# Perquè estudiar els LPs?

Els llenguatges que usem:

- influencien les nostres percepcions,
- guien i donen suport al nostre raonament,
- permeten i faciliten la nostra comunicació.

<br>

**Exemple:** Codi màquina *vs* codi alt nivell:

.center[![:height 12em](img/low-high-level.png)]


---

# Perquè estudiar els LPs?

Els llenguatges que usem:

- influencien les nostres percepcions,
- guien i donen suport al nostre raonament,
- permeten i faciliten la nostra comunicació.

<br>

**Exemple:** Programació imperativa *vs* declarativa:

.cols5050[
.col1[
```javascript
let xs = [1, 2, 3, 4, 5]

let ys = []
for (var i = 0; i < xs.length; i++) {
    ys.push(xs[i] * 2);
}
```
]
.col2[
```javascript
let xs = [1, 2, 3, 4, 5]

let ys = xs.map(function (x,i) {
    return 2*x
})

```
]]




---

# Com estudiar els LPs?

<br>

.cols5050[

.col1[
<br>

.center[Estudiar-los tots.]

.center[❌]


<br><br>

Estudiar les seves característiques, els seus usos, avaluar les seves qualitats, classificar-los
en famílies, conèixer la seva història, estudiar els seus fonaments...

.center[✅]

]
.col2[
![:width 16em](img/llibres-lps.png)
]
]

---

# Característiques bàsiques d'un LP

- Tipus de dades: amb quins dades i objectes treballem.

- Sistema de tipus.

- Control de seqüència: en quin ordre s'executen les operacions.

- Control de dades. Com s'accedeix a les dades i als objectes.

- Entrada / Sortida.

---

# Qualitats dels llenguatges de programació

- Llegibilitat

- Eficiència

- Fiabilitat

- Expressivitat

- Simplicitat

- Nivell d'abstracció

- Adequació als problemes a tractar

- Facilitat d'ús

- Ortogonalitat



---

# Història

📖 [*History of Programming Languages*](https://www.cs.toronto.edu/~gpenn/csc324/PLhistory.pdf), O'Reilly

.center[![:width 40em](img/programming-history.png)]





---

class: split-6040

# Història: Orígens

## Tauletes babilòniques (2000ac)

.cols6040[
.col1[
.xs[
A [rectangular] cistern.

The height is 3, 20, and a volume of 27, 46, 40 has been excavated.
The length exceeds the width by 50.
You should take the reciprocal of the height, 3, 20, obtaining 18.
Multiply this by the volume, 27, 46, 40, obtaining 8, 20.
Take half of 50 and square it, obtaining 10, 25.
Add 8, 20, and you get 8, 30, 25
The square root is 2, 55.
Make two copies of this, adding [25] to the one and subtracting from the other.
You find that 3, 20 [i.e., 3 1/3] is the length and 2, 30 [i.e., 2 1/2] is the width.

This is the procedure.


]]
.col2[
![:height 18em](img/babilonic-tablet.png)
]
]



<br>

.xxs[
📖 *[Ancient Babylonian Algorithms](http://steiner.math.nthu.edu.tw/disk5/js/computer/1.pdf)*. D.E. Knuth, Communications ACM 1972.

🎬 *[Math whizzes of ancient Babylon figured out forerunner of calculus](https://www.youtube.com/watch?v=Rx-5dCXx1SI)*, YouTube.
]

---

# Història: Orígens

## Teler de Jacquard (1804)


![:height 15em](img/jacquard1.png)
.sepimg[]
![:height 15em](img/jacquard2.png)

.xxs[Fotos: http://www.revolutionfabrics.com/blog/2018/9/26/the-jacquard-loom-and-the-binary-code]

🎬 .xxs[[How an 1803 Jacquard Loom Lead to Computer Technology](https://www.youtube.com/watch?v=MQzpLLhN0fY)]




---

# Història: Orígens

## Màquina analítica de Charles Babbage (1842)

Es considera que Ada Lovelace és la primera programadora.

![:height 10em](img/differential-engine.png)
.sepimg[]
![:height 10em](img/charles-babbage.png)
.sepimg[]
![:height 10em](img/ada-lovelace.png)

.xxs[Fotos: Domini públic]

<br>

.xxs[🎬 [Ada Lovelace, The World’s First Computer Nerd?](https://www.youtube.com/watch?v=lLOAuYv87uU)]


---

# Història: Ensambladors

Kathleen Booth va escriure el
primer llenguatge ensamblador (per un ordinador ARC al 1947).

![:height 10em](img/kathleen-booth.png)
.sepimg[]
![:height 10em](img/assembly-code.png)

.xxs[Fotos: Domini públic]

<br>
.xxs[
📖 [Kathleen Booth, Assembling Early Computers While Inventing Assembly](https://hackaday.com/2018/08/21/kathleen-booth-assembling-early-computers-while-inventing-assembly/)
]

---

# Història: Plankalkül

Primer LP d'alt nivell dissenyat per Konrad Zuse (1942-1945) pel seu
ordinador a relés Z4. Implementat al 1990.

![:height 10em](img/konrad-suze.png)
.sepimg[]
![:height 10em](img/computer-z4.png)
.sepimg[]
![:height 10em](img/plankalkul.png)

.xxs[Fotos: Domini públic]

---

# Història: Fortran

**FORmula TRANslator (1954-1957)**.
Desenvolupat per John Bakus a IBM per a computació científica.

Es volia generar codi comparable al programat en ensamblador.

Idees principals:

- Variables amb noms (6 caràcters)
- Bucles i condicionals aritmètics
- E/S amb format
- Subrutines
- Taules

![:height 8em](img/john-backus.jpg)
.sepimg[]
![:height 8em](img/punch-card.png)

.xxs[Fotos: Domini públic i Wikipedia]

---

# Història: Fortran

```fortran
C AREA OF A TRIANGLE WITH A STANDARD SQUARE ROOT FUNCTION
      READ INPUT TAPE 5, 501, IA, IB, IC
  501 FORMAT (3I5)
C IA, IB, AND IC MAY NOT BE NEGATIVE OR ZERO
C FURTHERMORE, THE SUM OF TWO SIDES OF A TRIANGLE
C MUST BE GREATER THAN THE THIRD SIDE, SO WE CHECK FOR THAT, TOO
      IF (IA) 777, 777, 701
  701 IF (IB) 777, 777, 702
  702 IF (IC) 777, 777, 703
  703 IF (IA+IB-IC) 777, 777, 704
  704 IF (IA+IC-IB) 777, 777, 705
  705 IF (IB+IC-IA) 777, 777, 799
  777 STOP 1
C USING HERON'S FORMULA WE CALCULATE THE
C AREA OF THE TRIANGLE
  799 S = FLOATF (IA + IB + IC) / 2.0
      AREA = SQRTF( S * (S - FLOATF(IA)) * (S - FLOATF(IB)) *
     +     (S - FLOATF(IC)))
      WRITE OUTPUT TAPE 6, 601, IA, IB, IC, AREA
  601 FORMAT (4H A= ,I5,5H  B= ,I5,5H  C= ,I5,8H  AREA= ,F10.2,
     +        13H SQUARE UNITS)
      STOP
      END
```

---

# Història: Fortran

.center[
![:height 25em](img/primer-programa-fortran.png)
]

.xxs[Font: [J.A.N. Lee, Twenty Five Years of Fortran](https://eprints.cs.vt.edu/archive/00000875/01/CS82010-R.pdf)]


---

# Història: COBOL

**COmmon Business Oriented Language  (1959).** Desenvolupat per Grace Hopper
pel DoD i fabricants per a aplicacions de gestió.

Idees principals:

- Vol semblar idioma anglès, sense símbols
- Macros
- Registres
- Fitxers
- Identificadors llargs (30 caràcters)

![:height 8em](img/grace-hopper.jpg)
.sepimg[]
![:height 8em](img/cobol-sheet.jpg)

.xxs[Foto: Domini públic]

---

# Història: COBOL

```cobol
IDENTIFICATION DIVISION.
PROGRAM-ID.  Multiplier.
AUTHOR.  Michael Coughlan.
* Example program using ACCEPT, DISPLAY and MULTIPLY to
* get two single digit numbers from the user and multiply them together

DATA DIVISION.

WORKING-STORAGE SECTION.
01  Num1                                PIC 9  VALUE ZEROS.
01  Num2                                PIC 9  VALUE ZEROS.
01  Result                              PIC 99 VALUE ZEROS.

PROCEDURE DIVISION.
    DISPLAY "Enter first number  (1 digit) : " WITH NO ADVANCING.
    ACCEPT Num1.
    DISPLAY "Enter second number (1 digit) : " WITH NO ADVANCING.
    ACCEPT Num2.
    MULTIPLY Num1 BY Num2 GIVING Result.
    DISPLAY "Result is = ", Result.
    STOP RUN.
```

---

# Història: LISP

**LISt Processing (1958)**.
Desenvolupat per John McCarthy al MIT per a recerca en IA.

Idees principals:

- Sintàxi uniforme
- Funcions (composició i recursivitat)
- Llistes
- Expressions simbòliques
- Recol·lector de brossa

![:height 8em](img/john-mccarthy.jpg)

.xxs[Foto: Wikipedia]

---

# Història: LISP

```lisp
(defun factorial (N)
    "Compute the factorial of N."
    (if (= N 1)
        1
        (* N (factorial (- N 1)))))
```


```lisp
(defun first-name (name)
    "Select the first name from a name represented as a list."
    (first name))

(setf names '((John Q Public) (Malcolm X)
              (Admiral Grace Murray Hopper) (Spot)
              (Aristotle) (A A Milne) (Z Z Top)
              (Sir Larry Olivier) (Miss Scarlet)))
```


---

# Història: Algol

**ALGOrithmic Language (1958)**.
Dissenyat com un llenguatge universal per computació científica.
No gaire popular, però dóna lloc a LPs com Pascal, C, C++, and Java.

Idees principals:

- Blocs amb àmbits de variables
- Pas per valor i pas per nom (≠ pas per referència)
- Recursivitat
- Gramàtica formal (Backus-Naur Form or BNF)



```algol
procedure Absmax(a) Size:(n, m) Result:(y) Subscripts:(i, k);
    value n, m; array a; integer n, m, i, k; real y;
begin
    integer p, q;
    y := 0; i := k := 1;
    for p := 1 step 1 until n do
        for q := 1 step 1 until m do
            if abs(a[p, q]) > y then
                begin y := abs(a[p, q]);
                    i := p; k := q
                end
end Absmax
```


---

# Història: Algol

Pas per nom:

```algol
begin
    integer i;
    integer array A[0:9];

    procedure ini (x); integer x;  (* pas per nom *)
    begin
        for i := 0 step 1 until 9 do x := 0
    end;

    ini(A[i]);
    ...
end
```

El paràmetre `x` es passa per nom (amb `value x;` es passaria per valor).

Dins de `ini()`, aparentment, s'assigna 10 cops 0 a `x`.

Però `x` és el "nom"
del paràmetre real, és a dir `A[i]`.

Per tant, `ini()` realment inicialitza a zero tot l'array.



---

# Exercici

Què fa aquest programa?

```algol
begin
    integer i, sum;
    integer array A[0:9];

    procedure suma (x, s); integer x, s;
    begin
        s := 0;
        for i := 0 step 1 until 9 do s := s + x
    end;

    suma(A[i], sum);
end
```

---

# Història: altres llenguatges



- Basic (Orientat a l'ensenyament de la programació) - 1964

- Pascal/Algol 68 (els hereus directes d'Algol 60) - 1970/1968

- C (Definit per programar Unix) - 1972

- Prolog (Primer llenguatge de programació lògica) - 1972

- Simula 67/Smalltalk  80 (primers llenguatges OO)

- Ada (LP creat per ser utilitzat pel Departament de Defensa Americà) - 1980

- ML/Miranda (primers llenguatges funcionals moderns) - 1983/1986

- C++ (llenguatge dinàmic i flexible compatible amb C) - 1983

- Java (llenguatge orientat a objectes per a torradores) - 1990

- Python (llenguatge llegible d'alt nivell de propòsit general) - 1991

- ...


---

# Ús dels LPs

Com mesurar la popularitat dels LPs?

- TIOBE Programming Community Index

  ![:height 15em](img/tiobe.png)

  .xxs[Font: https://www.tiobe.com/tiobe-index/ (2021)]


---

# Ús dels LPs

Com mesurar la popularitat dels LPs?

- IEEE Spectrum ranking: The Top Programming Languages 2018

  .center[![:height 15em](img/ieee-ranking.png)]

  .xxs[Font: https://spectrum.ieee.org/static/interactive-the-top-programming-languages-2018 (2018)]


---

# Ús dels LPs

Com mesurar la popularitat dels LPs?

- Estadístiques de GitHub

  ![:height 14em](img/github.png)
  ![:height 14em](img/github2.png)

  .xxs[Fonts: https://github.com i https://www.benfrederickson.com/ranking-programming-languages-by-github-users/]


---

# Ús dels LPs

Quins LPs estudiar/evitar?

  ![:height 12em](img/popularitat-1.png)
  ![:height 12em](img/popularitat-2.png)


.xxs[Font: https://www.benfrederickson.com/ranking-programming-languages-by-github-users/]


---

# Ús dels LPs

Quins LPs estudiar/evitar?

  .center[![:height 20em](img/popularitat-3.png)]


.xxs[Font: https://www.codeplatoon.org/the-best-paying-and-most-in-demand-programming-languages-in-2019/]



---

# Ús dels LPs 1965 - 2019

<br>

.center[
<iframe width="640" height="360" src="https://www.youtube.com/embed/Og847HVwRSI" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
]

---

# Paradigmes de LPs

Els **paradigmes de programació** classifiquen els LPs segons les
seves característiques.

<br>

.center[
![:height 15em](img/paradigms-floyd.png)
]

📖 [*The paradigms of programming.*](https://dl.acm.org/doi/pdf/10.1145/359138.359140) R. Floyd, Communications ACM 1979.




---

# Paradigmes de LPs


Paradigmes comuns:

- **Imperatiu**: Les instruccions precisen els canvis d'estat.

  ```c++
  f = 1;
  while (--n) f *= n;
  ```

- **Declaratiu**: Es caracteritza el resultat, però no com calcular-lo.

  ```sql
  select full_name, order_date, order_amount
  from customers inner join orders
  on customers.customer_id = orders.customer_id
  ```

- **Funcional**: El resultat és el valor d'una sèrie d'aplicacions de funcions.

  ```haskell
  cincMesGrans :: [a] -> [a]
  cincMesGrans = take 5 . reverse . sort
  ```



---

# Paradigma imperatiu

Caràcteristiques:

- Noció d'estat

- Instruccions per canviar l'estat

- Efectes laterals

Exemples:

- C/C++, Python, Java, Ensamblador, ...

Útils quan, per exemple, l'eficiència és clau.


---

# Paradigma imperatiu

Subclassificacions:

- **Procedural**: Les instruccions s'agrupen en procediments.

  ```pascal
  PROCEDURE swap (VAR a, b: INTEGER)
  VAR c: INTEGER;
  BEGIN
        c := a;  b := a;  a := c;
  END;
  ```

- **Orientat a objectes**: Les instruccions s'agrupen amb l'estat dels objectes
  sobre les quals operen.

  ```smalltalk
  Point»dist: aPoint
        dx := aPoint x - x.
        dy := aPoint y - y.
        ↑ ((dx * dx) + (dy * dy)) sqrt
  ```



---

# Paradigma declaratiu

Caràcteristiques:

- Llenguatges descriptius.

- El programa diu què s'ha de fer, però no necessariament com.


Utilitat:

- Prototipat d'aplicacions amb forta component simbòlica, problemes
combinatoris, etc.

- Consultes en bases de dades relacionals o lògiques.

- Per especificació i raonament automàtic.

Exemples:

- SQL (consultes relacionals) / GraphQL (consultes en grafs, amb tipus)
 / Prolog (lògica de primer ordre) / Matemàtiques



---

# Paradigma declaratiu

SQL: Trobar tots els emails dels usuaris del Jutge amb el Hello World acceptat.

```sql
EXPLAIN 
SELECT DISTINCT email 
FROM Users JOIN Submissions USING (user_id) 
WHERE problem_id='P68688_en' AND veredict='AC' 
ORDER BY email
```

Planificador (postgres):

```SQL
                                          QUERY PLAN
--------------------------------------------------------------------------------------------------------
 Unique  (cost=56242.20..56290.03 rows=9566 width=30)
   ->  Sort  (cost=56242.20..56266.11 rows=9566 width=30)
         Sort Key: users.email
         ->  Hash Join  (cost=2889.46..55609.71 rows=9566 width=30)
               Hash Cond: (submissions.user_id = users.user_id)
               ->  Bitmap Heap Scan on submissions  (cost=570.63..53265.77 rows=9566 width=7)
                     Recheck Cond: (problem_id = 'P68688_en'::text)
                     Filter: (veredict = 'AC'::text)
                     ->  Bitmap Index Scan on idx_submissions_problem_id  (cost=0.00..568.24 rows=21308 width=0)
                           Index Cond: (problem_id = 'P68688_en'::text)
               ->  Hash  (cost=1860.59..1860.59 rows=36659 width=37)
                     ->  Seq Scan on users  (cost=0.00..1860.59 rows=36659 width=37)
```

---

# Paradigma declaratiu

Subclasificacions:


- **Consultes**: Resposta a consultes a una base de dades.

  ```sql
  SELECT full_name, order_date, order_amount
  FROM customers INNER JOIN orders
  ON customers.customer_id = orders.customer_id
  ```

- **Matemàtic**: El resultat es declara com a la solució d'un problema d'optimització.

  ```bash
  Maximize
      x1 + 2 x2 + 3 x3 + x4
  Subject To
      - x1 + x2 + x3 + 10 x4 ≤ 20
      x1 - 3 x2 + x3 ≤ 30
      x2 - 3.5 x4 = 0
  ```

- **Lògic**: Resposta a una pregunta amb fets i regles.

  ```prolog
  human(socrates).
  mortal(X) :- human(X).
  ?- mortal(socrates).
  ```


---

# Paradigma funcional

Caràcteristiques:

- Procedural

- Sense noció d'estat i sense efectes laterals

- Més fàcil de raonar (sobre correctesa o sobre transformacions)

Utilitat:

- Útils per al prototipat, fases inicials de desenvolupament
(especificacions executables i transformables).

- Tractament simbòlic.

- Sistemes de tipus potents (incloent polimorfisme paramètric i
  inferència de tipus).

Exemples: Haskell, ML (Caml, OCaml), Erlang, XSLT (tractament XML),...

---

# Paradigma funcional

Conceptes clau:

- **Recursivitat:**

  ```scheme
  (define (fib n)
      (cond
        ((= n 0) 0)
        ((= n 1) 1)
        (else
          (+ (fib (- n 1))
             (fib (- n 2))))))
  ```

- **Funcions d'ordre superior**: funcions que reben o retornen funcions.

  ```python
  map(lambda x: 2*x, [1,2,3,4])
  ```

- **Aplicació parcial (currying)**:

  ```haskell
  doble = (*2)
  ```


---

# Paradigma funcional

Conceptes clau:

- **Funcions pures**: Amb els mateixos arguments, les funcions sempre retornen
  el mateix resultat. No hi ha efectes laterals.

- **Mecanismes d'avaluació**: Avaluació estricta *vs* avaluació mandrosa.

- Sistemes de tipus.


---

# Paradigma OO

Caràcteristiques:

- Es basa en *objectes* (atributs + mètodes) i potser *classes*.

- Inclou principalment *polimorfisme (subtipat)* i *herència*.

- Poden tenir sistemes de tipus complexos.


Exemples: Smalltalk, Simula, C++, Java...


---

# Llenguatges multiparadigma

Molts LPs combinen diferents paradigmes. Per exemple:

- Python, Perl: **imperatiu** + orientat a objectes + funcional

- OCaml: **funcional** + imperatiu + orientat a objectes


Alguns LPs incorporen caràcteristiques d'altres paradigmes:

- Prolog: **lògic** (+ imperatiu + funcional)


Altres combinacions:

- Erlang: **funcional** + concurrent + distribuït



---

# Llenguatges visuals

En un **llenguatges de programació visual** (VPL) els programes són creats manipulant
elements gràfics.

- **Visual Basic:** Dialecte de BASIC utilitzant
una interfície gràfica per facilitar la creació d'interfícies gràfiques (1991).

  .center[![:height 10em](img/visual-basic.png)]

- **Scratch:** Eina d'educació per a nens a partir de 8 anys (2003).

  .center[![:height 6em](img/scratch.png)]


---

# Llenguatges esotèrics

- **Brainfuck:** Basat en màquines de Turing, només té 8 instruccions. Hello world:

  ```bash
  ,>++++++[<-------->-],[<+>-],<.>.
  ```

- **Piet:** Usa imatges amb 20 colors com a codi font. Factorial:

  ![:height 6em](img/piet-factorial.png)


- **Whitespace**: Només té espais en blanc i tabuladors. BFS:

  ```bash

  ```

  (indenteu-lo bé quan el copieu 😛)


---

# Llenguatges esotèrics

- **Shakespeare**: Amaga un programa dins d'una obra de teatre.

<pre style='margin-left: 3em; padding: 10px; height: 32em; overflow-y: auto; background-color: #272822; border-radius: 5px; color: white; font-size: 12px;'>
The Infamous Hello World Program.

Romeo, a young man with a remarkable patience.
Juliet, a likewise young woman of remarkable grace.
Ophelia, a remarkable woman much in dispute with Hamlet.
Hamlet, the flatterer of Andersen Insulting A/S.


                    Act I: Hamlet's insults and flattery.

                    Scene I: The insulting of Romeo.

[Enter Hamlet and Romeo]

Hamlet:
 You lying stupid fatherless big smelly half-witted coward!
 You are as stupid as the difference between a handsome rich brave
 hero and thyself! Speak your mind!

 You are as brave as the sum of your fat little stuffed misused dusty
 old rotten codpiece and a beautiful fair warm peaceful sunny summer's
 day. You are as healthy as the difference between the sum of the
 sweetest reddest rose and my father and yourself! Speak your mind!

 You are as cowardly as the sum of yourself and the difference
 between a big mighty proud kingdom and a horse. Speak your mind.

 Speak your mind!

[Exit Romeo]

                    Scene II: The praising of Juliet.

[Enter Juliet]

Hamlet:
 Thou art as sweet as the sum of the sum of Romeo and his horse and his
 black cat! Speak thy mind!

[Exit Juliet]

                    Scene III: The praising of Ophelia.

[Enter Ophelia]

Hamlet:
 Thou art as lovely as the product of a large rural town and my amazing
 bottomless embroidered purse. Speak thy mind!

 Thou art as loving as the product of the bluest clearest sweetest sky
 and the sum of a squirrel and a white horse. Thou art as beautiful as
 the difference between Juliet and thyself. Speak thy mind!

[Exeunt Ophelia and Hamlet]


                    Act II: Behind Hamlet's back.

                    Scene I: Romeo and Juliet's conversation.

[Enter Romeo and Juliet]

Romeo:
 Speak your mind. You are as worried as the sum of yourself and the
 difference between my small smooth hamster and my nose. Speak your
 mind!

Juliet:
 Speak YOUR mind! You are as bad as Hamlet! You are as small as the
 difference between the square of the difference between my little pony
 and your big hairy hound and the cube of your sorry little
 codpiece. Speak your mind!

[Exit Romeo]

                    Scene II: Juliet and Ophelia's conversation.

[Enter Ophelia]

Juliet:
 Thou art as good as the quotient between Romeo and the sum of a small
 furry animal and a leech. Speak your mind!

Ophelia:
 Thou art as disgusting as the quotient between Romeo and twice the
 difference between a mistletoe and an oozing infected blister! Speak
 your mind!

[Exeunt]
</pre>

---

# Paradigmes de LPs: Més taxonomies

.center[![:height 25em](img/taxonomia.png)]

.right[.xxs[Font: [*Programming Paradigms for
Dummies*, P. Van Roy](https://www.info.ucl.ac.be/~pvr/VanRoyChapter.pdf)]]


---



# Turing completesa


.cols5050[
.col1[
**Màquina de Turing**: Model matemàtic de càlcul imperatiu molt simple<br/> (Alan Turing, 1936)

![:height 7em](img/alan-turing.jpg)
.sepimg[]
![:height 7em](img/turing-machine.png)

- Cinta infinita amb un capçal mòvil per llegir/escriure símbols
- Conjunt finit d'estats
- Funció de transició (estat, símbol ⟶ estat, símbol, moviment)
]
.col2[
**λ-càlcul**: Model matemàtic de càlcul funcional molt simple. <br/> (Alonzo Church, 1936).

![:height 7em](img/lambda2.png)
![:height 7em](img/alonzo-church.jpg)

- Sistema de reescriptura
- Basat en abstracció i aplicació de funcions
]
]

**Tesi de Church-Turing**: "Tot algorisme és
computable amb una Màquina de Turing o amb una funció en λ-càlcul".


.xxs[Fotos: Wikipedia, Fair Use, [Lambda Calculus for Absolute Dummies](http://palmstroem.blogspot.com/2012/05/lambda-calculus-for-absolute-dummies.html)]


---

# Turing completesa

Un LP és **Turing complet** si pot implementar qualsevol càlcul
que un computador digital pugui realitzar.





Alguns autors consideren només com a LPs els
llenguatges Turing complets.


- LPs Turing complets:

    - LPs de programació de propòsit general (C/C++, Python, Haskell...)
    - automàts cel·lulars (Joc de la vida, ...)
    - alguns jocs (Minecraft, Buscamines...)

  Per ser Turing complet només cal tenir salts condicionals (bàsicament,
  `if` i `goto`) i memòria arbitràriament gran.

- LPs no Turing complets:

    - Expressions regulars (a Perl o a AWK)
    - ANSI SQL




---

# Sistemes d'execució

- **Compilat**: el codi és transforma en codi objecte i després es monta en
  un executable. Sol ser eficient. Es distribueix l'executable.

  Exemples: C, C++, Ada, Haskell, ...

- **Interpretat**: el codi s'executa directament o el codi es transforma en
  codi d'una màquina virtual, que l'executa. Es distribueix el codi font.

  Aumenten la portabilitat i l'expressabilitat (es poden fer més coses
  en temps d'execució) però disminueix l'eficiència.

  Exemples: Python, JavaScript, Prolog (WAM), Java (JVM), ...


Sistemes mixtes:

- **Just in Time compilation**: Es compila (parcialment) en temps d'execució.

- Alguns interpretats, poden ser també compilats (per exemple, Prolog).
- I al revés (Haskell).

⇒ El sistema d'execució depèn més de la implementació que del LP.

---

# Sistemes de tipus

Un **sistema de tipus** és un conjunt de regles que assignen *tipus*  als
elements d'un programa (com ara variables, expressions, funcions...) per
evitar errors.

La comprovació de tipus verifica que les diferents parts d'un programa
es comuniquin adequadament en funció dels seus tipus.

Per exemple, amb:

```c++
class Persona;
class Forma;
class Rectangle :Forma;
class Triangle  :Forma;

double area (const Forma&);
```

- Cridar a `area` amb un `Rectangle` o un `Triangle` és correcte,
- Cridar a `area` amb una `Persona` o un enter és un error de tipus.



---

# Sistemes de tipus: Errors de tipus

Un **error de tipus** consisteix en aplicar a les dades una operació
que el seu tipus no suporta.

- Type Cast: usar un valor d'un tipus en un altre tipus.

  👉 En C, un enter pot ser usat com a funció (com a adreça), però pot
  saltar on no hi ha una funció i pot provocant un error.

  👉 En C, `printf("%s", 42);`.

- Aritmètica de punters.

  👉 En C++, si tenim `A p[10];` llavors `p[15]` té tipus `A`, però el que
  hi ha a `p[15]` pot ser qualsevol altra cosa i pot provocar un error de tipus.

- Alliberament explícit de memòria (deallocate/delete).

  Exemple: En Pascal usar un apuntador alliberat pot donar errors de
  tipus.

- En llenguatges OO (antics), no existència d'un mètode (degut a
  l'herència).



---

# Sistemes de tipus: Seguretat de tipus

La **seguretat de tipus** (*type safety*) és la mesura de com de fàcil/difícil és cometre errors
de tipus en un LP.

Exemples:

- C té reputació de ser un LP sense gaire seguretat de tipus (unions, enumerats, `void*`, ...).

- C++ hereta C però proporciona més seguretat de tipus:
    els enumerats no es poden convertr implícitament amb els enters o altres enumerats,
    el *dynamic casting* pot comprovar errors de tipus en temps execució, ...

- Java és dissenyat per a proporcionar seguretat de tipus. Però es pot abusar
del *classloader*.

- Python, igual que Java, està dissenyat per donar seguretat de tipus, malgrat que
el tipatge sigui dinàmic.

- Es creu que Haskell és *type safe* si no s'abusa d'algunes construccions com
`unsafePerformIO`.


---

# Sistemes de tipus: Tipat fort *vs* feble

**Tipat fort** (*strong typing*): L'LP imposa restriccions que
eviten barrejar valors de diferents tipus (conversions explícites).

**Tipat feble** (*weak typing*): L'LP té regles màgiques per convertir
tipus automàticament.

<br>

Javascript

```javascript
4 + '7';      // '47'
4 * '7';      // '28'
```


PHP

```php
4 + '7';      // '11'
4 * '7';      // '28'
```


Python

```python
4 + '7'       # ❌ TypeError: unsupported operand type(s) for +: 'int' and 'str'
4 * '7'       # '7777'
```

---

class: center, middle, inverse
![:width 30em](img/js-weird-1.png)

---

class: center, middle, inverse
![:width 40em](img/js-weird-3.png)

---

class: center, middle, inverse
![:width 30em](img/js-weird-4.png)

---

class: center, middle, inverse
![:width 30em](img/js-weird-2.png)

<br><br><br><br>
.center[https://javascriptwtf.com/]

.center[https://wtfjs.com/]


---

# Sistemes de tipus: Comprovació

La comprovació de tipus pot ser:

- **Estàtica**: en temps de compilació.

- **Dinàmica**: en temps d'execució.

- **Mixta**.



---

# Sistemes de tipus

.center[![:height 15em](img/tipatge.png)]

.right[.xxs[[Font](https://velog.io/@dhlee91/Static-vs.-Dynamic-Strong-vs.-Weak-typing)]]



---

# Exercicis

1. Digueu quin és el vostre LP favorit.

2. Expliqueu quines són les seves propietats fonamentals:

  - Propòsit del llenguatge.

  - Paradigma o paradigmes de programació que admet el llenguatge.

  - Sistema d'execució.

  - Sistema de tipus.

  - Principals aplicacions.

  - Història del LP i relació amb LPs similars.

  - Exemples de codi il·lustratius.

  - Altres característiques particulars.




---

# Exercicis


.center[

![:width 20em](img/guess-the-programming-language.png)

https://devawesome.io/guess-the-programming-language/
]



---

# Exercicis


.center[

![:width 20em](img/triviaplaza.png)

https://www.triviaplaza.com/programming-languages-quiz/
]


