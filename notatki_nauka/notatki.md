NOTATKI HTML

<!-- Tak wygląda komentarz HTML -->


    można te strzałki se przenieść na dół

UWAGA!!! Wszystkie stylizacje, jak tagi <i></i> oraz <b></b> powinny być robione w CSS, nie w HTML!

Tagi:

```html
<!DOCTYPE html>     deklaracja typu dokumentu
<html>      typ dokumentu dla przeglądarki
    <head>          główne ustawienia strony
        <meta charset="UTF-8">      używany na stronie system znaków
        <meta name="description" content="co zawiera strona"        opis zawartości strony dla indeksacji
    </head>      
    <body>      główna zarartość strony
        <h1>TEKST</h1>        nagłówek (heading) największy
        <h2>TEKST</h2>       nagłówek (heading) mniejszy
        ...
        <h6>TEKST</h6>      nagłówek (heading) najmniejszy
        <br/> lub <br>      pojedynczy odstęp
        <hr/> lub <hr/>     pojedyncza linia oddzielająca od jednej, do drugiej strony dokumentu
        <p>NOWY PARAGRAF</p>
        <b>POGRUBIENIE</b>
        <i>POCHYLENIE</i>
        <big>POWIĘKSZENIE TEKSTU</big>
        <small>POMNIEJSZENIE TEKSTU</small>
		<em></em>			emphasis (nacisk). Przeglądarka wyświetla ten element jako tekst pochylony, ale NIE jest rozumiany jako tekst pochylony, a właśnie ten, na który kładziemy nacisk. Bardzo ważny dla Search Engine! Styl w jaki wyświetla się ten element, można zmienić w CSS.
        <strong></strong>	element podobny do <em></em>. Ten z kolei domyślnie pogrubia tekst, natomiast również jest to odpowiednio indeksowane przez search engine. Również tu można zmienić styl taga w CSS.
		<p>10<sup>2</sup></p>       tekst u góry (potęgowanie na przykład)
        <p>H<sub>2</sub>O</p>       tekst na dole (znaki chemiczne na przykład)
        <p style="color: red;">CZERWONA CZCIONKA</p>
        <p style="background-color: blue">KOLOR TŁA CZCIONKI</p>
        <p style="color: red; background-color: blue;">OBYDWA STYLE W JEDNEJ LINII</p>
        <h2 style="color: red; background-color: blue;">TO SAMO DLA INNYCH ELEMENTÓW</h2>
        <body style="background-color: lightblue">       można nadać styl całej części dokumentu
    </body>
</html>
```


--------------------------------------------------------------------------------------------------


POPRAWNY LAYOUT:

!!! NA STRONIE MOŻE BYĆ TYLKO JEDEN HEADER 1 <h1></h1>, który jest głównym tytułem strony
poniżej headery 2 <h2></h> definiujące sekcje strony
header 3 używamy aby zrobić podsekcje w headerze nr 2
hierarchiczne używanie headerów:
h1
    h2
        h3

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="description" content="montaż drzwi i okien">
        <title>ANG montaż drzwi i okien</title>
    </head>
    <body>
       <header>     górna część strony (przeważnie z paskiem nawigacji)
            <nav>
                miejsce, w którym będzie kod dla linków nawigacyjnych
            </nav>
       </header>
       <main>
            <article>       sekcja strony z artykułami
                <section>       zawsze należy podzielić je na sekcje
                    <h1></h1>   oraz używać w nich odpowiednich headerów
                </section>
                <section>       sekcji może być kilka
                    <h2></h2>
                </section>
                <section>
                    <aside>
                                kontent, który nie jest bezpośrednio związany z treścią strony (np. reklamy adsense)
                    </aside>     
                </section>
            </article>
       </main>
       <footer>

       </footer>



    </body>
</html>
```


--------------------------------------------------------------------------------------------------


LINKI

```html
<a href="https://www.google.com" target="_blank"><h1>Google's Homepage</h1></a>
```

W linkach można używać innych tagów HTML, jak np. headerów.
target="_blank"     otwiera link w nowym oknie, nie w oknie z naszą stroną

```html
<a href="page2.html" >O MNIE</a>     link łączący z drugim plikiem w tym samym folderze
<a href="dir2/page3.html"></a>      link łączący z drugim plikiem w folderze podrzędnym
<a href="pics/index_image.jpg" >COŚ TAM</a>     link do pliku ze zdjęciem (nie wyświetla samego zdjęcia!)
```

OBRAZY

```html
<img src="https://duzekubki.pl/wp-content/uploads/2018/07/JK165_04.jpg.jpg">
<img src="https://duzekubki.pl/wp-content/uploads/2018/07/JK165_04.jpg" alt="MIAŁ BYĆ DINOŻARŁ" />      można użyć obrazów z internetu za pomocą linka.
alt="OPIS"      dzięki tej funcji dodajemy alternatywny tekst, w razie gdyby nie można było załadować zdjęcia
<img src="pics/index_image.jpg" alt="pikczer1" />       linkowanie obrazów z dysku
<img width="720" height="480" src="pics/index_image.jpg" alt="pikczer1" />      resizing (uwaga na aspect ratio!)
<img width="720" src="pics/index_image.jpg" alt="pikczer1" />       resizing tylko jednego parametru spowoduje, że HTML sam dostosuje odpowiednio drugi parametr

PONIŻEJ TWORZENIE ZDJĘCIA BĘDĄCEGO LINKIEM DO NASTĘPNEGO ZDJĘCIA / STRONY:
<a href="https://roadmap.sh/full-stack">
    <img width="720" src="pics/index_image.jpg" alt="pikczer1" />
</a>
```

--------------------------------------------------------------------------------------------------



VIDEO ORAZ YOUTUBE iFRAMES

```html
<video src="C1014.mp4" poster="pics/uslugi_image.jpg" loop autoplay controls width="760">TU POWINNO BYĆ WIDEO</video>
```

Film znajdujący się w tym samym folderze.
Atrybut poster="" dodaje miniaturkę do filmu (w innym przypadku jest to pierwsza klatka filmu).
Atrybut loop powtarza film w pętli.
Atrybut autoplay odtwarza film od razu po załadowaniu strony.
Atrybut controls dodaje do filmu możliwość odtwarzania go i kontrolowania, np. głośności.
Tekst między tagami pełni taką samą rolę jak w przypadku zdjęć (gdyby coś się spieprzywszy).

OPCJA "EMBED" W YOUTUBE (skopiować, wkleić)

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/Ode1O-ISwdI?si=bmwJJ5-7USoNH26u" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
```

iframe umożliwa załadowanie innej strony w naszej stronie



--------------------------------------------------------------------------------------------------



LISTY

Unordered list:

```html
<ul>
    <li>ITEM1/li>
    <li><a href="#"></li>       można tu wrzucać linki
</ul>
```

Ordered list:

```html
<ol type="1">           artybut type="" daje możliwość zmiany numeracji
    <li>ITEM1/li>
    <li><a href="#"></li>       można tu wrzucać linki
</ol>
```

type="1"        lista numerowana 
type="A"        lista A-Z wielkie litery
type="a"        lista a-z małe litery
type="I"        lista z numeracją rzymską wielką
type="i"        lista z numeracją rzymską małą

Embeded list (lista w liście):

```html
 <ol type"I">
    <li>Słodycze</li>
        <ol type="a">
            <li>Żelki</li>
            <li>Cukierki</li>
        </ol>
    <li>Owoce</li>
    <li>Warzywa</li>
</ol>
```

Description list:

```html
<dl>
    <dt>Apple</dt>              description term
    <dd>- They are red</dd>     description of the term
</dl>
```



--------------------------------------------------------------------------------------------------



TABELE
Tabele same zmieniają swój rozmiar i przenoszą tekst. Można dodawać dodatkowe rzędy / kolumny bez dodawania innych atrybutów.

```html
<table>
    <thead>                         Górna część tabeli (header tabeli)
        <caption><h2>List of numbers<h2></caption>  Tytuł tabeli (ustawia się po środku). Można używać innych tagów.
        <tr>
            <th>num1</th>           Table Header (nagłówki tabeli)
            <th>num2</th>
            <th>num3</th>
        </tr>
    </thead>
    <tbody>                         Body tabeli
        <tr>                        table row - rzędy kolumny
            <td>one</td>            table data - kolumny tabeli
            <td colspan="2">two</td>ten wpis zajmuje teraz dwie kolumny
            <td>three</td>
        </tr>
        <tr>
            <td>four</td>
            <td>five</td>
            <td>six</td>
        </tr>
    </tbody>
</table>
```


--------------------------------------------------------------------------------------------------



DIVS & SPANS (kontenery)
Używane, aby "owinąć" inne elementy kodu html.
Jest dobrze, aby stosować te "wrapper-tagi" przy działaniach np. z CSS, ponieważ wtedy CSS stosuje się do wrapper-taga, który nada wszystkim podrzędnym elementom odpowiedni styl.

HTML wyświetla wszystko na dwa podstawowe sposoby:
- block - zajmują całą szerokość strony
- inline - zajmuje tylko taka część strony, jaką potrzebuje (mogą być obok siebie w przeciwieństwie do bloków, ponieważ blok może być tylko jeden ze względu na jego szerokość)

Z tego powodu różne tagi będą się wyświetlały w różny sposób, w zależności od ich typu.
Np. linki to inline, ponieważ zajmują tylko tyle miejsca, ile zajmuje tekst linkujący.
Np. paragraf <p>Paragraf1</p> to block, ponieważ dwa paragrafy nie są w stanie wyświetlić się obok siebie.

```html
<span>PRZYKLAD</span> - kontener dla inline
<div>PRZYKLAD2</div> - kontener dla block
```

Generalnie, najczęściej wszystko owija się kontenerami <div></div>, natomiast kontenery <span></span> służą sytuacjom bardziej specyficznym.




--------------------------------------------------------------------------------------------------



Input & Forms (wprowadzanie i formularze)

Definiowanie i tworzenie tych elementów w HTMLu nie oznacza, że będą działały. Aby można było zebrać i użyć to, co użytkownik wprowadził, trzeba użyć JavaScript.

UWAGA!

```html
<form>                                                  jest to wrapper dla wszelkich pól typu "input" dla użytkownika. Jest to bardzo ważne przy współpracy z serwerem, JSem itd.
    <input type="text"
</form>
```

Same elementy HTML wyglądają tak:

```html
<input type="text" />                                   wpisywanie zwykłego tekstu, np. username
<input type="password" />                               wpisywanie hasła, znaki będą wykropkowane
<input type="text" value="Enter your username"/>        w ten sposób można zdefiniować domyślną zawartość pola tekstowego
<input type="date" />                                   specjalne pole do wpisania daty
<input type="email" />                                  pole do wpisania maila, podobne do zwykłego textboxa
<input type="range" />                                  slider wyboru zakresu
<input type="file" />                                   przycisk "upload" ("wybierz plik") dla użytkownika, aby mógł przesłać jakieś pliki
```

```html
<input type="checkbox" />                               przycisk "checkbox" do zaznaczania wielokrotnego wyboru. W przeciwieństwie do przycisków typu "radio" mogą być zaznaczone więcej, niż jeden na raz.
<input type="checkbox" />
```

```html
<input name="button" type="radio" />                    przycisk typu "radio" (kółeczko) jednokrotnego wyboru. Jeśli mają te same imię, może być zaznaczony tylko jeden na raz.
```

```html
<input name="button" type="radio" />
<input type="submit" />                                 przycisk "submit" (prześlij) do przesyłania np. odpowiedzi w formularzu.
```

```html
<textarea rows="10" cols="30">                          duże pole do wpisywania tekstu i można zmieniać mu rozmiar. Można od razu zdefiniować ilość kolumn i rzędów, co wpłynie na rozmiar.
    Enter a text                                        w ten sposób tworzy się domyślną zawartość pola.
</textarea>
```

WIĘCEJ TAGÓW NA STRONIE:
https://www.w3schools.com/tags/tag_input.asp



--------------------------------------------------------------------------------------------------



iFRAMES

Element służący do wyświetlania innych stron na mojej stronie internetowej.

```html
<iframe src="https://www.w-multimedia.pl" frameborder="0" width="1000" height="800">TO ZOSTANIE WYŚWIETLONE, JEŚLI NIE DA SIĘ WYŚWIETLIĆ STRONY</iframe>
src="" - źródło. Duże strony, jak np. amazon, youtube mają często zablokowaną tą opcję.
frameborder="0" - to ustawienie usuwa ramkę i strona jest jeszcze bardziej "embedded" w mojej stronie.
width="1000" height="800" - aby strona nie wyświetlała się jako okrutnie mała, można zastosować dodatkowe parametry wymiarowe.
```


--------------------------------------------------------------------------------------------------



META TAGI

Self explanatory... Te tagi zawsze żyją w "headzie" dokumentu html.

```html
<html lang="pl-PL">
    <head>
        <meta charset="UTF-8">
        <meta name="description" content="montaż drzwi i okien" >
        <meta name="author" content="Łukasz Waleszczyński" >
        <meta name="keywords" content="montaż drzwi, montaż okien, Adam Gasperowicz" >
        <meta name="viewport" content="width=device-width, initial-scale=1.0" >
        <title>ANG montaż drzwi i okien</title>
    </head>
```




--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------




ARTYKUŁY I FIGCAPTION

```html
<!DOCTYPE html>
<html lang="pl">
	<head>
		<meta charset="UTF-8">
		<meta name="description" content="chatgpt's exercise 7">
		<meta name="author" content="Łukasz Waleszczyński">
		<meta name="keywords" content="enhance, article, aside, figure, section, html">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>exercise7</title>
	</head>
	<body>
		<header>
			<nav>
				# placeholder
			</nav>
			<h1>WEBSITE TITLE</h1>
		</header>
	</body>
		<main>
			<article>
				<h2>ARTICLE 1 TITLE</h2>
				<figure>
				<img src="/website_pics/article1.jpg" width="800" alt="Article 1 picture">
				<figcaption>Article 1 picture</figcaption>
				</figure>
				<section>
					<h3>This is section 1 of Article 1</h3>
					<p>And this is content for section 1</p>
				</section>
				<br/>
				<section>
					<h3>This is section 2 of Article 1</h3>
					<p>And this is content for section 2</p>
				</section>
			</article>
			<aside>
				<h3>Check also:</h3>
				<p><a href="https://www.some-relevant-link.com">Relevant source</a></p>
			</aside>
			<hr/>
			<hr/>
			<article>
				<figure>
				<img scr="https://www.some-relevant-pic-link.com/image.jpg" width="800">
				<figcaption>This is another nice and relevant image for article 2</figcaption>
				</figure>
				<section>
					<h3>This is section 1 of article 2</h3>
					<p>This is content for section 1 article 2</p>
				</section>
				<br/>
				<section>
					<h3>This is section 2 of article 2</h3>
					<p>This is content for section 2 article 2</p>
				</section>
			</article>
			<aside>
				<h3>Check also:</h3>
				<p><a href="a href="https://www.some-relevant-link.com">Relevant source"</a></p>
			</aside>
		</main>
		<footer>
			<p>&copy 2023 Łukasz Waleszczyński</p>
		</footer>
	</main>
</html>
```



--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------




SPRAWDZANIE:

```html
<form>
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="password">Password (8-16 characters):</label>
  <input type="password" id="password" name="password" minlength="8" maxlength="16" required>

  <label for="age">Age (between 18 and 99):</label>
  <input type="number" id="age" name="age" min="18" max="99" required>

  <button type="submit">Submit</button>
</form>
```

PRZYKŁAD:

```html
<!DOCTYPE html>
<html lang="pl">
	<head>
		<meta charset="UTF-8">
		<meta name="description" content="chatgpt's exercise 10">
		<meta name="author" content="Łukasz Waleszczyński">
		<meta name="keywords" content="validation, html, exercise10">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<title>Page title</title>
	</head>
	<body>
		<header>
			<nav>
				# placeholder
			</nav>
		</header>
		<main>
			<form>
				<label for="username">Username:</label>
				<input type="text" id="username" name="username" required>
				<br/>
				<label for="email">Email:</label>
				<input type="email" id="email" name="email" required>
				<br/>
				<label for="password">Password:</label>
				<input type="password" id="password" name="password" minlength="8" maxlength="16" required>
				<br/>
				<label for="age">Age (between 18 and 99):</label>
				<input type="number" id="age" name="age" min="18" max="99" required>
				<br/>
				<button type="submit">SUBMIT</button>
			</form>
		</main>
		<footer>
			<p>&copy 2023 Łukasz Waleszczyński</p>
		</footer>
	</body>
</html>
```



--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------



TABELE - FULL

```html
<!DOCTYPE html>
<html lang="pl'>
	<head>
		<meta charset="UTF-8">
		<meta name="description" content="chatgpt's exercise 6">
		<meta name="author" content="Łukasz Waleszczyński">
		<meta name="keywords" content="html, table, learning">
		<meta name="viewport" content="width=devicewidth, initial-scale=1.0">
		<title>exercise6</title>
	</head>
	<body>
		<header>
			<nav>
				# placeholder
			</nav>
		</header>
		<main>
			<table>
				<thead>
					<caption><b>This is the exercise table</b></caption>
					<tr>
						<th>Name</th>
						<th>Age</th>
						<th>Occupation</th>
					</tr>
				</thead>
				<tbody>
					<tr>
						<td>Kristofer</td>
						<td>26</td>
						<td>Berlin</td>
					</tr>
					<tr>
						<td>Lisa</td>
						<td>19</td>
						<td>Paris</td>
					</tr>
					<tr>
						<td>Pablo</td>
						<td>48</td>
						<td>Mexico</td>
					</tr>
				</tbody>
			</table>
		</main>
		<footer>
			# placeholder
		</footer>
	<body>
</html>
```



--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------




DRUGI TUTORIAL
PROGRAMMING WITH MOSH -- HTML TUTORIAL for Beginners: HTML Crash Course (https://www.youtube.com/watch?v=qz0aGYrrlhU)

ENTITIES (wyświetlanie znaków specjalnych HTML jako tekstu)

```html
< - &lt; (lesser than...)
> - &gt; (greater than...)
Przykład: <h1>&lt;HTML!&gt;</h1>
```

```html
&copy; - copyright symbol
&nbsp; - non breakable single space (poczas, gdy w długim tekście, w wyrazie tworzy się automatyczna spacja dzieląca wyraz na dwoje i przenosząca jego treść linijkę niżej)
```

LINK W POSTACI ZDJĘCIA:

```html
<body>
	<a href="page2.html">
		<img src="pics/obraz.jpg" alt="jakis_tam_obrazek">
	</a>
</body>
```

DLA ELEMENTU ZNAJDUJĄCEGO SIĘ W FOLDERZE WYŻEJ:

```html
<a href=../index.html>HOME</a>		dla plików znajdujących się o jeden poziom wyżej
../../../../index.html				dla plików znajdujących się kilka poziomów wyżej
```

POBIERANIE ZDJĘCIA:

```html
<a href="pics/zdjecie.jpg" download>My Photo</a>
```

TWORZENIE ELEMENTU NA STRONIE, DO KTÓREGO MOŻNA SIĘ ODNIEŚĆ I LINKOWAĆ:

```html
<h2 id="section-css">CSS</h2>
```

```html
<a href="#section-css">CSS</a>		link do tego elementu

<a href="#">TOP</a>					przeniesienie się na samą górę strony

<a href="mailto:l.waleszczynski@gmail.com">NAPISZ DO MNIE!</a>		link kierujący do domyślnego programu pocztowego
```
