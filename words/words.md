<div class="section">
    <div>
    	<iframe id="splash" width="960" height="480" src="banners/splash.html"></iframe>
        <div style="top: 70px;font-size: 75px;font-weight: bold;">
        	Co będzie dalej?
       	</div>
		<div style="font-weight: 500;top: 140px;left: 10px;font-size: 29px;">
			Możliwe ścieżki rozwoju sytuacji COVID-19, objaśnione przy pomocy symulacji
		</div>
		<div style="font-weight: 100;top: 189px;left: 10px;font-size: 19px;line-height: 21px;">
			<b>
				🕐 30 minut zabawy i czytania
				&nbsp;&middot;&nbsp;
			</b>
			autorzy:
			<a href="https://scholar.google.com/citations?user=_wHMGkUAAAAJ&amp;hl=en">Marcel Salathé</a>
			(epidemiolog)
			oraz
			<a href="https://ncase.me/">Nicky Case</a>
			(kod i oprawa graficzna)
		</div>
	</div>
</div>

„Tylko strachu należy się bać” to głupia porada.

Pewnie, nie wykupujcie papieru toaletowego – jednak jeśli prawodawcy boją się strachu, będą udawać, że prawdziwe zagrożenia są niewielkie, aby uniknąć „masowej paniki”. To nie w strachu leży problem, tylko w tym, *jak go kierujemy*. Strach daje nam siłę, żeby stawić czoło zagrożeniom w tej chwili, i żeby przygotować się na niebezpieczeństwo w przyszłości.

Szczerze, my (Marcel, epidemiolog i Nicky, grafika/kod) jesteśmy zaniepokojeni. Pewnie wy także! Z tego powodu użyliśmy siłę naszego strachu do zrobienia tych **grywalnych symulacji**, abyście *wy* mogli użyć siły waszego strachu, żeby zrozumieć:

* **kilka ostatnich miesięcy** (podstawy epidemiologii, model SEIR, R i R<sub>0</sub>)
* **kilka kolejnych miesięcy** (zakaz wychodzenia, śledzenie kontaktów, maski)
* **kilka kolejnych lat** (utrata odporności? brak szczepionki?)

Niniejszy przewodnik (w angielskim oryginale opublikowany 1go maja 2020. kliknij przypis!→[!data]) ma za zadanie wskrzesić *zarówno* nadzieję, *jak i* strach. Aby pokonać COVID-19 **jednocześnie chroniąc nasze zdrowie psychiczne i możliwości finansowe**, potrzebujemy optymizmu do tworzenia planów i pesymizmu do tworzenia planów zapasowych. Jak kiedyś powiedziała Gladys Bronwyn Stern, *„Optymista wymyśli samolot, a pesymista spadochron”*.

[^data]: Przypisy będą zawierać żródła, odnośniki, albo dodatkowe komentarze. Tak, jak ten komentarz!
    
    **Ten przewodnik został opublikowany w oryginalnej wersji angielskiej 1go maja 2020.** Wiele szczegółów kiedyś przestanie być aktualnych, ale jesteśmy pewni, że ten przewodnik obejmie 95% możliwych ścieżek w przyszłość, a podstawy epidemiologii zawsze będą przydatne.

Zapnijcie więc pasy i przygotujcie się na turbulencje.

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>Kilka ostatnich miesięcy</div>
    </div>
</div>

Piloci uczą się na symulatorach lotu, jak nie rozbijać samolotów.

**Epidemiolodzy uczą się na symulatorach epidemii, jak nie rozbić ludzkości.**

Stwórzmy więc bardzo, *bardzo* prosty „symulator lotu epidemii”! W tej symulacji <icon i></icon> Zaraźliwi ludzie przekształcają <icon s></icon> Podatnych ludzi w kolejnych <icon i></icon> Zaraźliwych:

![](pics/spread.png)

Szacuje się, że *przy wybuchu* zarazy COVID-19, wirus przeskakuje z <icon i></icon> na <icon s></icon> *przeciętnie* co 4 dni[^serial_interval]. (Nie zapominajcie, że wahania są spore.)

[^serial_interval]: „Przeciętny [szeregowy] okres wynosił 3,96 dni (przedział ufności 95% 3,53–4,39 dni).” [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L (ang.)](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article) (Uwaga: wczesne wydania artykułów nie są ich ostatecznymi wersjami.)

Co stanie się, jeśli na populacji, gdzie jest tylko 0.001% <icon i></icon>, zasymulujemy „podwojenie co 4 dni” *i nic poza tym*? 

**Kliknij „Start”, żeby rozpocząć symulację! Później można ją rozegrać ponownie z innymi ustawieniami:** (Uwagi techniczne: [^caveats])

[^caveats]: **Nie zapomnijcie, że wszystkie przedstawione symulacje są super uproszczone w celu dydaktycznym.**

    
    Uproszczenie: gdy zadacie symulacji, żeby „zainfekować jedną nową osobę co X dni”, rzeczywiście zwiększa ona liczbę zainfekowanych o 1/X każdego dnia. Podobnie działają przyszłe ustawienia przedstawionych symulacji – „ozdrowienie co X dni” to zmniejszenie liczby zainfekowanych o 1/X co dnia.
    
    To *nie jest* dokładnie to samo, ale jest wystarczająco dokładne i bardziej zrozumiałe, niż bezpośrednie ustawianie szybkości zakażeń i ozdrowień.

<div class="sim">
		<iframe src="sim?stage=epi-1" width="800" height="540"></iframe>
</div>

Oto **wykres wzrostu wykładniczego**. Zaczyna się powoli, potem wybucha. Od „przecież to tylko grypa” do „przecież grypa nie tworzy *masowych grobów w bogatych miastach*”. 

![](pics/exponential.png)

Ale ta symulacja jest błędna. Wzrost wykładniczy, na szczęście, nie może iść w nieskończoność. Coś, co przeszkadza wirusowi się rozprzestrzeniać to ludzie, którzy *już go mają*:

![](pics/susceptibles.png)

Im więcej jest <icon i></icon>, tym szybciej <icon s></icon> stają się <icon i></icon>, **ale im mniej jest <icon s></icon>, tym *wolniej* <icon s></icon> stają się <icon i></icon>.**

Jak wpływa to na postęp epidemii? Sprawdźmy:

<div class="sim">
		<iframe src="sim?stage=epi-2" width="800" height="540"></iframe>
</div>

Oto S-kształtny wykres **wzrostu logistycznego**. Zaczyna się powoli, potem wybucha, a w końcu zwalnia.

Ale ta symulacja wciąż jest błędna. Nie wzięliśmy pod uwagę, że <icon i></icon> Zaraźliwi w końcu przestają być zaraźliwi, poprzez 1) ozdrowienie, 2) „ozdrowienie” z uszkodzeniami płuc, albo 3) śmierć.

Dla ułatwienia, załóżmy, że <icon i></icon> Zainfekowany przechodzą w <icon r></icon> Ozdrowiałych. (Pamiętaj, że w rzeczywistości część z nich będzie martwa.) <icon r></icon> nie dadzą się już więcej zarazić. Przyjmijmy też, – *póki co!* – że są odporni do końca życia.

W przypadku COVID-19, szacuje się, że *przeciętnie*, osoba <icon i></icon> Zaraźliwa zaraża przez 10 dni[^infectiousness]. To oznacza, że niektórzy ozdrowieją przed upływem 10 dni, a niektórzy po. **Zaczynając od 100% <icon i></icon>, wygląda to tak:**

[^infectiousness]: “Mediana okresu zaraźliwego \[...\] wynosiła 9,5 dnia.” [Hu, Z., Song, C., Xu, C. et al (ang.)](https://link.springer.com/article/10.1007/s11427-020-1661-4) Tak, wiemy, że „mediana” to nie to samo, co „przeciętna”. Ale w celu uproszczenia i edukacji jest wystarczająco podobna.

<div class="sim">
		<iframe src="sim?stage=epi-3" width="800" height="540"></iframe>
</div>

To natomiast przeciwieństwo wzrostu wykładniczego: **tłumienie (gaśnięcie) wykładnicze**.

Co więc stanie się, jeśli zrobimy symulację wzrostu w kształcie S i *dodamy ozdrowienia*?

![](pics/graphs_q.png)

Sprawdźmy.

<b style='color:#ff4040'>Czerwony obszar</b> to chorzy *w tej chwili* <icon i></icon>,    
<b style='color:#999999'>Szary obszar</b> to ozdrowiali <icon r></icon>. Jego górna krawędź to *suma wszystkich zachorowań* (chorzy + ozdrowiali <icon r></icon>).
Zaczynamy od tylko 0.001% <icon i></icon>:

<div class="sim">
		<iframe src="sim?stage=epi-4" width="800" height="540"></iframe>
</div>

To właśnie stąd pochodzi ten słynny kształt! Nie jest to rozkład normalny, nawet nie logarytmicznie normalny. Nie ma własnej nazwy. Ale na pewno widzieliście go miliard y razy, i byliście błagani, żeby go spłaszczyć.

**Model SIR**[^sir]    
(<icon s></icon>**S**usceptible - podatny, <icon i></icon>**I**nfectious - zarażający, <icon r></icon>**R**ecovered - ozdrowiały)      
to *druga* co do ważności podstawa epidemiologii:
101:

[^sir]: Aby zasięgnąć więcej informacji na temat modelu SIR, odwołaj sie do [the Institute for Disease Modeling (ang.)](https://www.idmod.org/docs/hiv/model-sir.html#) oraz [Wikipedii (ang.)](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SIR_model)

![](pics/sir.png)

**UWAGA: Symulacje, na których polegają ustawodawcy, są *o wiele* bardziej zaawansowane, niż te!** Pomimo to, model SIR jest w stanie pokazać nam ogólne zasady, nawet jeśli pomija niuanse.

Dodajmy jednak jeden szczegół: zanim <icon s></icon> zmieni się w <icon i></icon>, niech najpierw stanie się <icon e></icon> Zaatakowanym. Jest zarażony wirusem, ale jeszcze go nie przekazuje – zara*żony*, ale nie zara*źliwy*.

![](pics/seir.png)

(Ten wariant to **model SEIR**[^seir], gdzie „E” pochodzi od „Exposed” i oznacza <icon e></icon> „zaatakowany”. Zwróćmy uwagę, że, inaczej niż mogłoby się wydawać, Zaatakowany nie może się bronić. Zgodnie z tą definicją, Zaatakowany wirusa już ma. Tłumaczenie terminologii jest trudne.)

[^seir]: Więcej informacji na temat modelu SEIR można znaleźć w [the Institute for Disease Modeling (ang.)](https://www.idmod.org/docs/hiv/model-seir.html) oraz [na Wikipedii](https://en.wikipedia.org/wiki/Compartmental_models_in_epidemiology#The_SEIR_model)

Osoby dotknięte COVID-19 pozostają <icon e></icon> *zarażone, ale jeszcze nie zaraźliwe* przeciętnie przez 3 dni.[^latent] Co się stanie, jeśli włączymy to do symulacji?

[^latent]: „Zakładając rozkład czasu inkubacji ze średnią 5,2 dni wynikającą z odrębnego badania wczesnych przypadków COVID-19, wydedukowaliśmy, że zaraźliwość rozpoczyna się 2,3 dnia (przedział ufności 95%, 0,8–3,0 dni) zanim pojawią się pierwsze oznaki choroby” (w skrócie: jeśli oznaki pojawiają się po 5 dniach, zarażanie rozpoczyna się 2 dni wcześniej = zarażanie zaczyna się po 3 dniach) [He, X., Lau, E.H.Y., Wu, P. et al. (ang.)](https://www.nature.com/articles/s41591-020-0869-5)

<b style='color:#ff4040'>Obszary Czerwony</b> <b style='color:#FF9393'>i Różowy</b> to razem chorzy w tej chwili (zaraźliwi <icon i></icon> + zaatakowani<icon e></icon>),    
górna krawędź <b style='color:#888'>Szarego obszaru</b> to *suma wszystkich zachorowań* (chorzy + ozdrowiali <icon r></icon>):

<div class="sim">
		<iframe src="sim?stage=epi-5" width="800" height="540"></iframe>
</div>

Niewiele się zmieniło! To, jak długo pozostajemy <icon e></icon> Zaatakowani wpływa na proporcje <icon e></icon> do <icon i></icon>, i na to, *kiedy* mamy największą liczbę chorych... ale *szczytowa liczba* chorych, tak, jak i całkowita liczba zachorowań, nie zmieniają się.

Dlaczego tak się dzieje? To dzięki *najważniejszej* podstawie epidemiologii:

![](pics/r.png)

Stopa (współczynnik) Reprodukcji. Odzwierciedla ona *średnią* liczbę ludzi, których <icon i></icon> zarazi *przed* własnym ozdrowieniem (albo śmiercią).

![](pics/r2.png)

**R** zmienia się w miarę rozwoju epidemii, w miarę, jak uzyskujemy odporność i przeprowadzamy działania przeciwko epidemii.

**R<sub>0</sub>** to wartość, którą R przyjmuje *w chwili rozpoczęcia zarazy, zanim zaczniemy jej przeciwdziałać*. R<sub>0</sub> odzwierciedla dokładniej siłę wirusa samego w sobie, ale też zmienia się w zależności od obszaru. Przykładowo, R<sub>0</sub> jest wyższe w gęściej zasiedlonych miastach, niż w luźniejszych terenach wiejskich.

(Większość artykułów prasowych – a nawet niektóre publikacje naukowe! – mylą ze sobą R i R<sub>0</sub>. Ponownie, terminologia to ciężki orzech do zgryzienia.)

R<sub>0</sub> corocznej grypy wynosi około 1.28[^r0_flu]. To oznacza, że *w momencie wybuchu* epidemii grypy, każdy z <icon i></icon> zarazi *średnio* po 1,28 osoby (O ile to może wyglądać dziwnie, że mamy ułamek osoby, to zwróćmy uwagę na to, że „średnio” matki, mają po 2,4 dziecka, a jednak nie widujemy pół-dzieci na ulicach.)

[^r0_flu]: „Mediana R w przypadku grypy sezonowej wyniosła 1,28 (rozstęp ćwiartkowy: 1,19–1,37)” [Biggerstaff, M., Cauchemez, S., Reed, C. et al. (ang:)](https://bmcinfectdis.biomedcentral.com/articles/10.1186/1471-2334-14-480)

Szacuje się, że R<sub>0</sub> dla COVID-19 to około 2,2,[^r0_covid] chociaż pewne jeszcze *niezakończone* badanie wskazuje na 5,7(!) w Wuhan.[^r0_wuhan]

[^r0_covid]: „Szacujemy, że podstawowy współczynnik reprodukcji R0 wynosi około 2,2 (przedział 95% prawdopodobieństwa: 1,4–3,8)” [Riou J, Althaus CL. (ang.)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7001239/)

[^r0_wuhan]: „obliczyliśmy, że mediana wartość R0 wynosi 5,7 (przedział ufności 95% 3,8–8,9)” [Sanche S, Lin YT, Xu C, Romero-Severson E, Hengartner N, Ke R. (ang.)](https://wwwnc.cdc.gov/eid/article/26/7/20-0282_article)

W naszych symulacjach – *zarówno przy rozpoczęciu, jak i przeciętnie* – każdy <icon i></icon> zaraża kogoś nowego przez 10 dni, co 4 dni. „10 dni” zawiera dwie i pół porcji „czterech dni”, więc – *zarówno przy rozpoczęciu, jak i przeciętnie* – każdy z naszych <icon i></icon> zaraża po 2,5 osoby. Zatem R<sub>0</sub> = 2,5 (uwagi:[^r0_caveats_sim]).

[^r0_caveats_sim]: Przy założeniu, że przez cały „okres zaraźliwości” jesteśmy zaraźliwi zawsze w tym samym stopniu. Jest to kolejne uproszczenie w imię zrozumiałości.

**Sprawdź, jak R<sub>0</sub> zależy od czasu do ozdrowienia i czasu do zarażenia majstrując wartościami w tym kalkulatorze:**

<div class="sim">
		<iframe src="sim?stage=epi-6a&format=calc" width="285" height="255"></iframe>
</div>

Pamiętaj jednak, że im mniej <icon s></icon>, tym *wolniej* <icon s></icon> zmieniają się w <icon i></icon>. Stopa reprodukcji (R) *w tej chwili* zależy nie tylko od *podstawowej* stopy reprodukcji (R<sub>0</sub>), ale *również* od tego, ile ludzi już nie jest <icon s></icon> Podatnych. (Na przykład dlatego, że wyzdrowieli i mają naturalną odporność.)

<div class="sim">
		<iframe src="sim?stage=epi-6b&format=calc" width="285" height="390"></iframe>
</div>

Gdy ludzi odpornych jest wystarczająco wiele, R < 1, a wtedy wirus jest opanowany!Nazywa się to **odpornością stadną**. Odporność stadną od grypy dają nam *szczepionki*. Dawanie się zarazić, żeby osiągnąć „naturalną odporność stadną”, to *okropny* pomysł. (Ale nie z powodu, o którym myślicie! Czytajcie dalej.)

Spójrzmy znów na model modelu SEIR, ale tym razem z widoczną wartością R<sub>0</sub>, chwilową R, oraz progiem odporności stadnej:

<div class="sim">
		<iframe src="sim?stage=epi-7" width="800" height="540"></iframe>
</div>

**UWAGA: Całkowita ilość zachorowań *nie zatrzymuje się* przy odporności stadnej, ale przekracza ją!** Próg jest przekroczony dokładnie w momencie, gdy mamy maksymalną liczbę obecnie chorych. (Będzie tak nieważne, jak zmienimy ustawienia – spróbujcie!)

Jest tak dlatego, że gdy mamy więcej nie-<icon s></icon>, niż wynosi próg odporności stadnej, to otrzymujemy R < 1. A gdy R < 1, to liczba nowych przypadków przestaje rosnąć: maksimum.

**Najważniejsza lekcja, którą powinniście wynieść z tego przewodnika, to ten diagram** – jest bardzo skomplikowany, więc poświęćcie trochę czasu na przyswojenie go:

![](pics/r3.png)

**Oznacza to: NIE TRZEBA całkowicie, ani nawet prawie całkowicie, zatrzymać przechodzenie wirusa z osoby na osobę, żeby powstrzymać COVID-19!**

To paradoks. COVID-19 jest chorobą niezwykle zaraźliwą, a mimo to, aby ją opanować, musimy zatrzymać "tylko" ponad 60% zarażeń. 60%?! Na studiach mogłoby to odpowiadać ocenie dostateczny plus. Ale gdy R<sub>0</sub> = 2,5, to zmniejszenie go o 61% daje nam R = 0.975, czyli R < 1, czyli opanowanego wirusa (dokładny wzór:[^exact_formula])!

[^exact_formula]: Zwróćmy uwagę na to, że R = R<sub>0</sub> · część niewstrzymanych zarażeń ze wszystkich. Pamiętajmy też, że część niewstrzymanych zarażeń = 1 - część *zatrzymanych*.
    
    Zatem, aby uzyskać R < 1, należy najpierw doprowadzić do R<sub>0</sub> · ZarażeniaNiewstrzymane < 1. 
    
    Zatem ZarażeniaNiewstrzymane < 1/R<sub>0</sub>
    
    Zatem 1 - ZarażeniaZatrzymane < 1/R<sub>0</sub>
    
    Zatem, ZarażeniaZatrzymane > 1 - 1/R<sub>0</sub>
    
    Zatem należy zatrzymać więcej, niż **1 - 1/R<sub>0</sub>** zarażeń, aby uzyskać R < 1 i zatrzymać wirusa!

![](pics/r4.png)

(Jeśli uważacie, że wartości R<sub>0</sub> albo jakiekolwiek inne są w naszych symulacjach zbyt niskie albo wysokie, cieszy nas, że podważacie nasze założenia! Pod koniec przewodnika będzie „tryb piaskownicy”, gdzie można będzie podstawić *własne* liczby i sprawdzić, co z tego wyniknie.)

*Każdy* sposób przeciwdziałania COVID-19, o którym słyszeliście – mycie rąk, dystansowanie fizyczne, samoizolacja, śledzenie kontaktów i kwarantanny, maski, nawet „odporność stadna” – *wszystko* to sprowadza się do jednego:

do obniżenia R poniżej 1.

Użyjmy zatem naszego „symulatora lotu epidemii”, żeby zdobyć odpowiedź na pytanie: jak otrzymać R < 1 na sposób, który **jednocześnie chroni nasze zdrowie psychiczne i możliwości finansowe**?

Przygotujcie się na lądowanie awaryjne...

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Months</div>
    </div>
</div>

...mogło być gorzej. Udało nam się uniknąć równoległego świata, w którym rozwinął się:

###Scenariusz 0: Nie róbmy zupełnie nic

Około 1 na 20 osób zarażonych COVID-19 potrzebują pomocy z OIOMu (Ośrodka Intensywnej Opieki Medycznej)[^icu_covid]. W Stanach Zjednoczonych Ameryki, które są krajem bogatym, jedno łóżko na ICU [OIOMie] przypada na 3400 ludzi.[^icu_us] Zatem USA jest w stanie poradzić sobie z 20 zarażonymi osobami *naraz* z każdych 3400 – w przeliczeniu, 0,6% ludności.

[^icu_covid]: [„Proporcja przypadków COVID-19, które wymagały przyjęcia na ICU [OIOM] w USA od 12 lutego do 16 marca 2020, podział na grupy wiekowe.” (ang.)](https://www.statista.com/statistics/1105420/covid-icu-admission-rates-us-by-age-group/). Między 4,9% a 11,5% *wszystkich* przypadków COVID-19 wymagało intensywnej opieki. Wybierając dolną granicę przedziału (co ułatwia zadanie), to 5%, czyli 1 z 20. Należy zwrócić uwagę na to, że ta liczba odpowiada konkretnie rozkładzie wiekowemu USA, oraz będzie większa w krajach o starszej ludności, a mniejsza w krajach o młodszej.

[^icu_us]: „Liczba łóżek na ICU [OIOM] = 96596”. Za [the Society of Critical Care Medicine (ang.)](https://sccm.org/Blog/March-2020/United-States-Resource-Availability-for-COVID-19) liczba ludności USA wyniosła 328 200 000 w roku 2019. 96 596 spośród 328 200 000 = około 1 na 3400. 

Nawet, gdyby *ponadpotroić* tą ilość do 2%, to oto, co stałoby się, *jeśli nie zrobilibyśmy zupełnie nic*:

<div class="sim">
		<iframe src="sim?stage=int-1&format=lines" width="800" height="540"></iframe>
</div>

Niedobrze.

To właśnie opisał [raport Imperial College z 16 marca (ang.)](http://www.imperial.ac.uk/mrc-global-infectious-disease-analysis/covid-19/report-9-impact-of-npis-on-covid-19/): jeśli nie zrobimy nic [w kontekście USA i Wielkiej Brytanii], to przekroczymy możliwości OIOMów, a ponad 80% ludności zostanie zarażona (pamiętajcie, że całkowita ilość zarażeń *przekracza* próg odporności stadnej).

Nawet jeśli tylko 0,5% zarażonych umiera – wspaniałomyślne założenie, w przypadku, gdy OIOMy są pełne – w większym kraju, jak USA, przy 300 milionach ludzi, 0,5% z 80% z 300 milionów daje 1,2 miliona martwych... *JEŚLI nie zrobilibyśmy nic*.

(W prasie i mediach społecznościowych często mówi się, że „80% będzie zarażonych”, *nie wspominając* o „JEŚLI NIE ZROBIMY NIC”. Strach został wykorzystany, żeby nabić kliknięcia, a nie zrozumieć sprawę. *Ech.*)

###Scenariusz 1: Spowalnianie epidemii / odporność stadna

Spowalnianie epidemii było strategią wszelkich organizacji zajmujących się opieką zdrowotną, natomiast plan „odporności stadnej” Wielkiej Brytanii spotkał się powszechnie złym odbiorem. Tylko, że to *ta sama strategia*. Wielka Brytania nie potrafiła jednak dobrze przekazać, co robią.[^yong]

[^yong]: „Mówi, że cel jest taki sam, jak w innych krajach: spowolnić epidemię przez rozłożenie zarażeń w czasie. W rezultacie, naród mógłby uzyskać odporność stadną; to efekt uboczny, a nie cel. [...] Strategia działań rządu, która jest dostępna w internecie, w ogóle nie wspomina o odporności stadnej.”
    
    Zaczerpnięte z [artykułu Eda Younga w magazynie The Atlantic (ang.)](https://www.theatlantic.com/health/archive/2020/03/coronavirus-pandemic-herd-immunity-uk-boris-johnson/608065/)

Niestety, obie strategie miały pewną, dosłownie tragiczną, wadę.

Spójrzmy najpierw na dwa główne sposoby na spowolnienie epidemii: mycie rąk oraz zachowanie odstępów.

Częstsze mycie rąk zmniejsza występowanie gryp oraz przeziębień o ok. 25% w krajach o wysokich dochodach[^handwashing], a zakaz wychodzenia z domów w Londynie zmniejsza bliskie kontakty o ok. 70%[^london]. Załóżmy więc, że mycie rąk zmniejsza R o *najwyżej* 25%, a zachowanie odstępów o *najwyżej* 70%:

[^handwashing]: „Wszystkie osiem z kwalifikujących się badań stwierdziły, że mycie rąk zmniejszyło ryzyko infekcji dróg oddechowych, przy zmniejszeniu ryzyka od 6% do 44% [wartość ogółem 24% (przedział ufności 95% 6–40%)].” W symulacjach zaokrągliliśmy wartość do 25% w imię prostoty. [Rabie, T. and Curtis, V. (and.)](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1365-3156.2006.01568.x) Uwaga: jak zauważa ta meta-analiza, jakość badań na temat mycia rąk (przynajmniej w krajach o wysokim dochodzie) pozostawia wiele do życzenia.

[^london]: „Zaobserwowaliśmy zmniejszenie średniej liczby dziennych kontaktów każdego uczestnika badania o 73%. Byłoby to wystarczające, aby zmniejszyć R0 z wartości 2,6 przed do 0,62 (0,37 - 0,89) po wprowadzeniem zasad pozostawania w domach.”. W imię prostoty, zaokrągliliśmy to do 70% w tych symulacjach. [Jarvis and Zandvoort et al (ang.)](https://cmmid.github.io/topics/covid19/comix-impact-of-physical-distance-measures-on-transmission-in-the-UK.html)

**Sprawdź za pomocą kalkulatora, jak % nie-<icon s></icon>, mycie rąk oraz pozostawanie w domach wpływa na R:** (ich efekty są przedstawione *względnie*, dzięki czemu zwiększanie jednego parametru wydaje się zmniejszać efekt pozostałych[^log_caveat].)

[^log_caveat]: Zniekształcenia tego nie byłoby, gdyby R było nakreślone na skali logarytmicznej... ale wtedy musielibyśmy wytłumaczyć, czym jest *skala logarytmiczna*.

<div class="sim">
		<iframe src="sim?stage=int-2a&format=calc" width="285" height="260"></iframe>
</div>

Przeprowadźmy teraz symulację epidemii COVID-19 od marca 2020, zakładając, że zaczęliśmy już częściej myć ręce, ale tylko *trochę* unikamy ludzi – tak, że R spadło, ale wciąż jest powyżej 1:

<div class="sim">
		<iframe src="sim?stage=int-2&format=lines" width="800" height="540"></iframe>
</div>

Trzy obserwacje:

1. Całkowita liczba zarażeń *spadła*! **Nawet, jeśli nie osiągniemy R < 1, to zmniejszenie R wciąż może ocalić życie wielu ludziom, poprzez zmniejszenie tego, jak bardzo epidemia przekroczy próg odporności stadnej.** Wielu ludziom wydaje się, że spowolnienie epidemii tylko rozkłada w czasie zarażenia bez zmniejszania ich całkowitej liczby. To byłoby niemożliwe w *żadnym* prostym modelu epidemiologicznym. Ale gdy media mówiły, że „zarażonych będzie ponad 80%”, jakby to było pewne, to było to rozumiane w ten sposób, że całkowita liczba zarażeń jest już niezmienna i wykuta w kamieniu. *Ech*.

2. Ze względu na dodatkowe przeciwdziałania, liczba obecnie zarażonych osiąga maksimum *przed* odpornością stadną. W tej symulacji całkowita liczba zarażeń przekracza próg odporności stadnej *tylko trochę* – plan Wielkiej Brytanii! W tym momencie mamy R < 1, możemy dać sobie spokój z przeciwdziałaniem, a COVID-19 pozostaje opanowany! Oprócz jednego drobnego problemu...

3. Nadal nie starcza nam miejsc na OIOMach. Przez wiele miesięcy (nie zapominajmy, że w symulacji już je potroiliśmy).

To było drugie odkrycie raportu Imperial College z 16 marca, dzięki któremu Wielka Brytania porzuciła swój pierwotny plan. Żadne próby **złagodzenia** (zmniejszyć R, ale wciąż R > 1) nie opanują sytuacji. Jedyne wyjście to **stłumienie** (zmniejszyć R poniżej 1).

![](pics/mitigation_vs_suppression.png)

Czyli, nie jedynie „spowolnienie”, ale *zduszenie* epidemii. Na przykład za pomocą...

###Scenariusz 2: Zakaz wychodzenia przez wiele miesięcy

Zobaczmy, co się stanie, jeśli *zdusimy* epidemię poprzez pięciomiesięczny zakaz, który prawie zlikwiduje <icon i></icon>, a następnie – *w końcu* – powrócimy do normalności:

<div class="sim">
		<iframe src="sim?stage=int-3&format=lines" width="800" height="540"></iframe>
</div>

Oj.

Widzimy tu „drugą falę”,  o której tyle się mówi. Gdy tylko zniesiemy ograniczenia wychodzenia, wracamy do R > 1. Niedobitki <icon i></icon> (albo importowane <icon i></icon>) mogą spowodować kolejny szczyt epidemii, który ma prawie takie same skutki, jak w scenariuszu 0: nie róbmy zupełnie nic.

**Zakaz wychodzenia nie jest wybawieniem, a jedynie rozpoczęciem od nowa.**

Czyli co, będziemy wprowadzać zakaz co jakiś czas?

###Scenariusz 3: Przerywany zakaz

Jako pierwszy, rozwiązanie te zaproponował raport Imperial College z 16 marca, a później również publikacja Harvardu.[^lockdown_harvard]

[^lockdown_harvard]: „Przy braku innych działań, kluczową miarą powodzenia ograniczenia kontaktów jest to, czy możliwości opieki zdrowotnej nie zostaną przekroczone. Aby tego uniknąć, może powstać potrzeba przedłużonego albo przerywanego ograniczenia kontaktów do roku 2022.”[Kissler and Tedijanto et al (ang.)](https://science.sciencemag.org/content/early/2020/04/14/science.abb5793)

**Oto symulacja:** (Gdy rozegracie „nagrany scenariusz”, możecie spróbować *własnego* planu zakazu wychodzenia, przesuwając suwaki *podczas* działania symulacji! Pamiętajcie, że symulację można wstrzymać i kontynuować, a także zmienić jej tempo.)

<div class="sim">
		<iframe src="sim?stage=int-4&format=lines" width="800" height="540"></iframe>
</div>

To *powstrzymałoby* liczbę zachorowań, zanim przekroczyłaby możliwości OIOMów! Do tego jest to *o wiele* lepsze, niż utrzymywanie zakazu przez 18 miesięcy do pojawienia się szczepionki. Musimy jedynie... utrzymać zakaz przez kilka miesięcy, dać luz na kolejne kilka, a potem powtarzać, aż do pojawienia się szczepionki. (A jeśli nie będzie szczepionki, powtarzać, aż wykształci się odporność stadna... w roku 2022.)

Dobra, łatwo jest narysować linię oznaczającą „możliwości OIOMów”, ale jest kilka spraw, których tutaj *nie możemy* zasymulować. Takich, jak:

**Zdrowie psychiczne**: samotność jest jednym z największych czynników ryzyka dla depresji, zaburzeń lękowych oraz samobójstwa. Do tego, powiązana jest z wcześniejszą śmiercią do tego samego stopnia, co palenie 15 papierosów dziennie.[^loneliness]

[^loneliness]: Zobacz [Ryc. 6 z Holt-Lunstad & Smith 2010 (ang.)](https://journals.sagepub.com/doi/abs/10.1177/1745691614568352). Oczywiście, wielka uwaga, badanie wykazało *korelację*. Jednakże, o ile nie zaczniemy losowo wybierać ludzi, żeby przez całe życie byli samotni, wiedzę możemy czerpać jedynie z obserwacji.

**Zdolności finansowe**: pytanie „a co z gospodarką?” brzmi, jakby pytającemu zależało bardziej na pieniądzach, niż na życiu, ale „gospodarka” to nie tylko inwestycje: to zdolność społeczeństwa do zapewnienia jedzenia i domu dla swoich bliskich, do wykształcenia swoich dzieci, to możliwość korzystania ze sztuki, dobrego jedzenia, gier komputerowych – tych rzeczy, dla których warto żyć. A poza tym, bieda *sama w sobie* ma okropny wpływ na zdrowie zarówno psychiczne, jak i fizyczne.

Nie mówimy też, że *nie powinniśmy* wprowadzić zakazów ponownie! W dalszej części przyjrzymy się zakazom w roli „bezpiecznika”. W każdym razie, nie jest to rozwiązanie idealne.

Chwila... przecież Tajwanowi i Korei Południowej *już udało się* opanować COVID-19, prawda? Całe 4 miesiące, *bez* długotrwałych zakazów?

Jak?

###Scenariusz 4: Badania, śledzenie, izolacja

*„Pewnie, że \*mogliśmy\* zrobić to, co Tajwan i Korea zrobiły od razu, ale już jest za późno. Przegapiliśmy odpowiedni moment.”*

Ale właśnie o to chodzi! „Zakaz to nie wybawienie, a rozpoczęcie od nowa”... **a nowy początek to dokładnie to, czego nam trzeba.**

Aby zrozumieć, jak Tajwan i Korea Południowa opanowały COVID-19, należy zapoznać się z rozwojem typowego zarażenia COVID-19[^timeline]:

[^timeline]: **Przeciętnie 3 dni do zaraźliwości**: „Zakładając rozkład czasu inkubacji ze średnią 5,2 dni wynikającą z odrębnego badania wczesnych przypadków COVID-19, wydedukowaliśmy, że zaraźliwość rozpoczyna się 2,3 dnia (przedział ufności 95%, 0,8–3,0 dni) zanim pojawią się pierwsze oznaki choroby” (w skrócie: jeśli oznaki pojawiają się po 5 dniach, zarażanie rozpoczyna się 2 dni wcześniej = zarażanie zaczyna się po 3 dniach) [He, X., Lau, E.H.Y., Wu, P. et al. (ang.)](https://www.nature.com/articles/s41591-020-0869-5)  
    
    **przeciętnie 4 dni do zarażenia kolejnej osoby**: „Przeciętny [szeregowy] okres wynosił 3,96 dni (przedział ufności 95% 3,53–4,39 dni).” [Du Z, Xu X, Wu Y, Wang L, Cowling BJ, Ancel Meyers L (ang.)](https://wwwnc.cdc.gov/eid/article/26/6/20-0357_article)
    
    **średnio 5 dni do wystąpienia objawów**: „przeciętny czas inkubacji szacuje się na 5,1 dnia (przedział ufności 95% od 4,5 do 5,8 dnia)” [Lauer SA, Grantz KH, Bi Q, et al (ang.)](https://annals.org/AIM/FULLARTICLE/2762808/INCUBATION-PERIOD-CORONAVIRUS-DISEASE-2019-COVID-19-FROM-PUBLICLY-REPORTED)

![](pics/timeline1.png)

Jeśli chorzy schowają się w domach dopiero, gdy poczują się źle (czyli gdy odczują objawy), to wirus wciąż może się rozprzestrzeniać:

![](pics/timeline2.png)

W rzeczy samej, 44% zarażeń dzieje się *zanim* zarażający poczuje objawy! [^pre_symp]

[^pre_symp]: „Szacujemy, że 44% (przedział ufności 95% 25%–69%) nosicieli wtórnych zostało zarażonych w czasie, gdy nosiciel pierwotny był w stadium przedobjawowym” [He, X., Lau, E.H.Y., Wu, P. et al (ang.)](https://www.nature.com/articles/s41591-020-0869-5)

Ale jeśli odnajdziemy osoby, które miały niedawno styczność z osobą mającą objawy, oraz zastosujemy wobec nich kwarantannę... zatrzymamy rozprzestrzenianie się wirusa, będąc jeden krok przed nim!

![](pics/timeline3.png)

Nazywa się to **śledzeniem kontaktów**. Pomysł nie jest nowy, był już użyty na niespotykaną skalę, aby opanować Ebolę[^ebola], a teraz jest jednym z podstawowych sposobów Tajwanu i Korei Południowej na opanowanie COVID-19!

[^ebola]: „Śledzenie kontaktów było kluczowy działaniem podjętym w Liberii i jednym z najszerzej zakrojonych projektów śledzenia kontaktów podczas epidemii w dziejach.” [Swanson KC, Altare C, Wesseh CS, et al. (ang.)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6152989/)

(Pozwala nam również lepiej wykorzystać ograniczoną liczbę zestawów testowych, bo można wtedy znaleźć przedobjawowych <icon i></icon> bez potrzeby sprawdzania prawie wszystkich.)

Osoby mające styczność z chorym są zwyczajowo znajdowane poprzez wypytywanie, ale jako jedyny sposób byłoby to zbyt powolne, gdy COVID-19 pozostawia nam tylko ok. 48 godzin. Dlatego osoby przeprowadzające takie wywiady potrzebują pomocy ze strony aplikacji do śledzenia kontaktów – chociaż *nie powinny* ich zastąpić.

(Pomysł ten nie wyszedł z głów „komputerowców”: pomysł aplikacji do walki z COVID-19 był pierwszy raz zaproponowany przez [zespół epidemiologów z Oksfordu (ang.)](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936).)

Zaraz, aplikacje, które śledzą, z kim mamy styczność?… Czy to nie naruszenie mojej sfery prywatności, wpuszczenie Wielkiego Brata?

Raczej, że nie! **[DP-3T (ang.)](https://github.com/DP-3T/documents#decentralized-privacy-preserving-proximity-tracing)**, czyli zespół epidemiologów i kryptologów (w tym jeden z nas, Marcel Salathé), *już zajmuje się* tworzeniem aplikacji do śledzenia kontaktów – z kodem dostępnym publicznie – która nie ujawnia **żadnych informacji o waszej tożsamości, waszym położeniu, o osobach, z którymi mieliście styczność, a nawet *ile to było osób***.

Działa to w ten sposób:

![](pics/dp3t.png)

([a to pełna wersja komiksu](https://ncase.me/contact-tracing/))

Wraz z podobnymi zespołami, jak TCN Protocol[^tcn] i MIT PACT[^pact], przekonali Apple do tego, żeby wbudować śledzenie kontaktów szanujące prywatność bezpośrednio w Androida i iOS.[^gapple] (Nie ufasz Google czy Apple? To w porządku! Piękno tego systemu polega na tym, że *nie wymaga* on zaufania!) Wasze instytucje opieki zdrowotnej mogą wkrótce prosić o ściągnięcie aplikacji. Jeśli szanuje ona prywatność oraz ma upubliczniony kod, wtedy prosimy: zróbcie to!

[^tcn]: [Temporary Contact Numbers [Tymczasowe Numery Kontaktowe], zdecentralizowany protokół śledzenia kontaktów, który chroni prywatność (ang.)](https://github.com/TCNCoalition/TCN#tcn-protocol)

[^pact]: [Private Automated Contact Tracing [Automatyczne Prywatne Śledzenie Kontaktów] (ang.)](https://pact.mit.edu/)

[^gapple]: [Apple oraz Google podejmują współdziałanie w kwestii technologii śledzenia kontaktów COVID-19 (ang.)](https://www.apple.com/ca/newsroom/2020/04/apple-and-google-partner-on-covid-19-contact-tracing-technology/). Należy zwrócić uwagę, że nie budują *samych aplikacji*, tylko systemy, które je *wesprą*.

A co z ludźmi bez smartfonów? Z zarażeniami poprzez klamki? Z „rzeczywistymi” przypadkami bezobjawowymi? Aplikacje nie mogą wskazać wszystkich przypadków, kiedy doszło do zarażenia... *ale to nic!* Nie musimy złapać ich *wszystkich*, a tylko ponad 60%, aby otrzymać R < 1.

(Mieszanie przypadków przedobjawowych i „rzeczywiście” bezobjawowych jest męczące. „Prawdziwie” bezobjawowe przypadki zachorowań są rzadkie: [^rant])

[^rant]: Wiele artykułów dziennikarskich – a nawet naukowych – nie odróżnia chorych którzy „mieli objawy, kiedy ich badano” (przedobjawowych) od tych, którzy „*w ogóle* nigdy nie mieli objawów” (rzeczywiście bezobjawowych). Jedyny sposób, w który można ich odróżnić to wrócić kiedyś do przebadanych.
   
    Dlatego też zrobiono to w [tym badaniu (ang.)](https://wwwnc.cdc.gov/eid/article/26/8/20-1274_article). (Uwaga: wczesne wydania artykułów nie są ich ostatecznymi wersjami.) W telefonicznym centrum obsługi w Korei Południowej, w którym zaobserwowano wybuch COVID-19 „jedynie 4 (1,9%) osób nie miało objawów podczas trwania 14-dniowej kwarantanny, oraz żadna z osób mieszkających z nimi nie została wtórnie zarażona."
    
    Oznacza to, że osoby przechodzące chorobę „rzeczywiście bezobjawowo” są rzadko spotykane, a zarażenie się od nich może być jeszcze bardziej niezwykłe!

Odizolowanie chorych *z objawami* zmniejszyłoby R o nie więcej, niż 40%, a kwarantanna dla osób, z którymi się zetknęli, a które same *nie mają objawów* zmniejszyłoby R o nie więcej, niż 50%[^oxford]:

[^oxford]: Za badaniem, które wskazało na aplikacje jako sposób walki z COVID-19: [Luca Ferretti & Chris Wymant et al (ang.)](https://science.sciencemag.org/content/early/2020/04/09/science.abb6936/tab-figures-data) Zob. Ryc. 2. Zakładając, że R<sub>0</sub> = 2,0, stwierdzono tam, że:    
    
    * Chorzy z objawami mają udział R = 0,8 (40%)
    * Chorzy przed objawami mają udział R = 0,9 (45%)
    * Chorzy bezobjawowi mają udział R = 0,1 (5%, chociaż w modelu badaczy jest duża dawka niepewności, więc wartość może być mniejsza)
    * Warunki środowiskowe jak klamki odpowiadają za R = 0,2 (10%)

    Suma chorych przedobjawowych oraz bezobjawowych (45% + 5%) daje razem 50% udziału w R!

<div class="sim">
		<iframe src="sim?stage=int-4a&format=calc" width="285" height="340"></iframe>
</div>

Zatem nawet bez idealnej kwarantanny kontaktów można otrzymać R < 1 *bez zakazów wychodzenia!* To dużo lepsze dla naszego zdrowia psychicznego i finansów. (Jeśli mowa o kosztach, które ponoszą osoby, które się izolują, *rządy powinny ich wesprzeć* – płacić za badania, chronić ich pracę, dopłacać do urlopów chorobowych itd. Będzie to i tak tańsze, niż zakaz przerywany.)

Potem utrzymujemy R poniżej i aż do chwili, gdy mamy szczepionkę, która przemienia podatnych <icon s></icon> w odpornych <icon r></icon>. Odporność stadna *tak, jak należy*:

<div class="sim">
		<iframe src="sim?stage=int-4b&format=calc" width="285" height="230"></iframe>
</div>

(Uwaga: ten kalkulator zakłada, że szczepionki są stuprocentowo skuteczne. Musimy pamiętać, że w rzeczywistości trzeba zaszczepić *więcej osób*, niż wynosi próg „odporności stadnej”, żeby ją rzeczywiście osiągnąć.)

Starczy tego gadania. Oto symulacja, w której mamy:

1. Kilka miesięcy ograniczeń, po których...
2. Wprowadzamy badania, śledzenie i izolację, aby móc...
3. Zaszczepić wystarczająco wiele osób, bo wtedy...
4. Zwyciężymy.

<div class="sim">
		<iframe src="sim?stage=int-5&format=lines" width="800" height="540"></iframe>
</div>

I tyle! Tak ląduje się awaryjnie tym samolotem.

Tak pokonamy COVID-19.

...

A co, jeśli *mimo wszystko*, coś pójdzie nie tak? Już nieraz zdarzało się, że coś poszło tragicznie. To przemawia strach, ale to dobrze! Strach daje nam siły na zrobienie planów awaryjnych.

Pesymista wymyśli spadochron.

###Scenariusz 4+: Maski dla każdego, lato, bezpieczniki

Co, jeśli R<sub>0</sub> jest o wiele wyższe, niż oczekiwaliśmy, a powyższe przeciwdziałania, nawet wraz z zachowaniem odstępów, *wciąż* nie daje nam R < 1?

Przypomnijmy sobie, że nawet, jeśli nie osiągniemy R < 1, obniżenie R wciąż zmniejsza „nadwyżkę” chorych po przekroczeniu progu odporności stadnej, więc przekłada się na ocalone życie. Ale R < 1 to wciąż nasz cel, więc mamy jeszcze kilka sposobów na obniżenie R:

**Maski dla każdego:**

*„Zaraz“*, zapytacie, *„przecież maski nie chronią przed zachorowaniem?”*

Zgadza się. Maski nie chronią noszących przed zachorowaniem[^incoming]... za to chronią *innych* przed zarażającym noszącym maskę.

[^incoming]: „Żadna z masek chirurgicznych nie wykazała wystarczającej skuteczności filtrowania ani dopasowania do twarzy, aby można było ją uznać za urządzenie chroniące drogi oddechowe” [Tara Oberg & Lisa M. Brosseau (ang.)](https://www.sciencedirect.com/science/article/pii/S0196655307007742)

[^outgoing]: „3,4-krotny spadek [o 70%] cząstek aerozoli, oraz niemal całkowity zanik większych kropli zaobserwowany przez by Johnson et al. może oznaczać, że maski chirurgiczne noszone przez zarażonych mają znaczący wpływ na zarażanie.” [Milton DK, Fabian MP, Cowling BJ, Grantham ML, McDevitt JJ (ang.)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3591312/)

[^homemade]: [Davies, A., Thompson, K., Giri, K., Kafatos, G., Walker, J., & Bennett, A](https://www.cambridge.org/core/journals/disaster-medicine-and-public-health-preparedness/article/testing-the-efficacy-of-homemade-masks-would-they-protect-in-an-influenza-pandemic/0921A05A69A9419C862FA2F35F819D55) See Table 1: a 100% cotton T-shirt has around 2/3 the filtration efficiency as a surgical mask, for the two bacterial aerosols they tested.

![](pics/masks.png)

Przekładając to na liczby, maski chirurgiczne *noszone przez chorych* zmniejszają liczbę wirusów grypy i przeziębienia w powietrzu o 70%.[^outgoing] Obniżka zarażeń o 70% byłaby tak samo skuteczna, jak zakazy!

Nie znamy jednak wpływu masek *konkretnie* na COVID-19. Wyniki naukowe powinny być publikowane dopiero, gdy pewność osiąga 95% (...powinny[^replication]). Pierwszego maja 2020 roku maski są „pewne” na mniej niż 95%.

[^replication]: Każdy szanujący się naukowiec, który przeczytał ostatnie zdanie pewnie śmieje się teraz przez łzy. Zobacz: [tzw. p-hacking](https://pl.wikipedia.org/wiki/P-hacking), [kryzys replikacji](https://pl.wikipedia.org/wiki/Replikacja_(metoda_naukowa)#Kryzys_replikacji)).

Ale pandemie są jak poker. **Stawiajcie tylko gdy masz 95% pewności, a przegracie całą stawkę.** Jak zauważa British Medical Journal[^precautionary] w świeżym artykule o maskach, w warunkach niepewności *musimy* stosować analizę kosztów i korzyści. Na przykład tak:

[^precautionary]: „Czas zastosować zasadę ostrożności” [Trisha Greenhalgh et al \[PDF\] (ang.)](https://www.bmj.com/content/bmj/369/bmj.m1435.full.pdf)

Koszty: W przypadku domowych masek z materiału (skutecznych w ok. 2/3 w porównaniu do chirurgicznych[^homemade]), bardzo niewielkie. Przy maskach chirurgicznych, większe, ale wciąż małe.

Korzyści: Nawet jeśli mamy 50% szans zarówno na to, że maski chirurgiczne zmniejszają zarażenia o 0%, jak i o 70%, to średnia „wartość oczekiwana” wynosi 35%, czyli połowa tego, co wprowadzenie zakazów! Załóżmy, że maski chirurgiczne – na oko i po uwzględnieniu niepewności – zmniejszają R o nie więcej niż 35%. (Inne założenia można tu również wypróbować przez przesuwanie suwaków w górę i w dół.)

<div class="sim">
		<iframe src="sim?stage=int-6a&format=calc" width="285" height="380"></iframe>
</div>

(Więcej argumentów za oraz przeciwko maskom:[^mask_args].)

[^mask_args]: **„Musimy oszczędzać wyposażenie, aby wystarczyło szpitalom** *Pełna zgoda.* Ale to argument bardziej za wzmożeniem produkcji masek, a nie za reglamentacją. W międzyczasie możemy robić je z materiału.
   
   **„Trudno używać ich we właściwy sposób.”** Trudno jest też umyć ręce zgodnie z wytycznymi Światowej Organizacji Zdrowia, a mimo to zalecamy mycie rąk, bo zrobienie czegoś średnio daje lepsze efekty, niż nierobienie w ogóle niczego.
   
   **„Przez maski ludzie zaczną lekceważyć mycie rąk i zachowanie odstępów.”** Tak samo, jak przez pasy bezpieczeństwa lekceważone są znaki STOP, a ci, co myją zęby, częściej żują kamienie. Na poważnie, stawiamy na coś przeciwnego: maski *stale przypominają* o byciu ostrożnym – a na wschodzie Azji są symbolem solidarności!
    
    

Same tylko maski nie dadzą R < 1. Ale gdy mycie rąk oraz badania, śledzenie i izolacja dają razem R = 1,1, to noszenie masek przez 1/3 wszystkich osób zmniejszyłoby to do R < 1, wirus opanowany!

**Lato:**

Dobra, nie jest to „działanie”, które można przeprowadzić, ale też pomoże! Media mówią czasem, że lato nie zmieni nic w sprawie COVID-19. Mają trochę racji: Lato nie da R < 1, ale *i tak* zmniejszy R.

W przypadku COVID-19, każdy 1°C obniża R o 1,2%[^heat]. Różnica między latem a zimą w Warszawie wynosi ok. 16.8°C,[^nyc_heat], czyli latem R spadnie o ok. 20%.

[^heat]: „Wzrost temperatury o jeden stopień Celsjusza [...] obniża R o 0,0225”, oraz „średnia wartość R pośród tych 100 miast to 1,83”. 0,0225 ÷ 1,83 ≈ 1,2%. [Wang, Jingyuan and Tang, Ke and Feng, Kai and Lv, Weifeng (ang.)](https://papers.ssrn.com/sol3/Papers.cfm?abstract_id=3551767)

[^nyc_heat]: Miesiące zimowe (grudzień, styczeń, luty) mają średnią temperaturę -1,2°C, a letnie (czerwiec, lipiec, sierpień) ok. 18°C. Dane z lat 1982-2010 z [IMGW](http://pogodynka.pl/polska/daneklimatyczne/).

<div class="sim">
		<iframe src="sim?stage=int-6b&format=calc" width="285" height="220"></iframe>
</div>

Lato samo w sobie nie spowoduje, że R < 1, ale jeśli mamy ograniczone możliwości, możemy osłabić pewne przeciwdziałania na lato, *żeby wzmóc je* zimą.

**A "Circuit Breaker" Lockdown:**

And if all that *still* isn't enough to get R < 1... we can do another lockdown.

But we wouldn't have to be 2-months-closed / 1-month-open over & over! Because R is reduced, we'd only need one or two more "circuit breaker" lockdowns before a vaccine is available. (Singapore had to do this recently, "despite" having controlled COVID-19 for 4 months. That's not failure: this *is* what success takes.)

Here's a simulation a "lazy case" scenario:

1. Lockdown, then
2. A moderate amount of hygiene & "Test, Trace, Isolate", with a mild amount of "Masks For All", then...
3. One more "circuit breaker" lockdown before a vaccine's found.

<div class="sim">
		<iframe src="sim?stage=int-7&format=lines&height=620" width="800" height="620"></iframe>
</div>

Not to mention all the *other* interventions we could do, to further push R down:

* Travel restrictions/quarantines
* Temperature checks at malls & schools
* Deep-cleaning public spaces
* [Replacing hand-shaking with foot-bumping](https://twitter.com/V_actually/status/1233785527788285953)
* And all else human ingenuity shall bring

. . .

We hope these plans give you hope. 

**Even under a pessimistic scenario, it *is* possible to beat COVID-19, while protecting our mental and financial health.** Use the lockdown as a "reset button", keep R < 1 with case isolation + privacy-protecting contract tracing + at *least* cloth masks for all... and life can get back to a normal-ish!

Sure, you may have dried-out hands. But you'll get to invite a date out to a comics bookstore! You'll get to go out with friends to watch the latest Hollywood cash-grab. You'll get to people-watch at a library, taking joy in people going about the simple business of *being alive.*

Even under the worst-case scenario... life perseveres.

So now, let's plan for some *worse* worst-case scenarios. Water landing, get your life jacket, and please follow the lights to the emergency exits:

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Next Few Years</div>
    </div>
</div>

You get COVID-19, and recover. Or you get the COVID-19 vaccine. Either way, you're now immune...

...*for how long?*

* COVID-19 is most closely related to SARS, which gave its survivors 2 years of immunity.[^SARS immunity]
* The coronaviruses that cause "the" common cold give you 8 months of immunity.[^cold immunity]
* There's reports of folks recovering from COVID-19, then testing positive again, but it's unclear if these are false positives.[^unclear]
* One *not-yet-peer-reviewed* study on monkeys showed immunity to the COVID-19 coronavirus for at least 28 days.[^monkeys]

But for COVID-19 *in humans*, as of May 1st 2020, "how long" is the big unknown.

[^SARS immunity]: “SARS-specific antibodies were maintained for an average of 2 years [...] Thus, SARS patients might be susceptible to reinfection ≥3 years after initial exposure.” [Wu LP, Wang NC, Chang YH, et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2851497/) "Sadly" we'll never know how long SARS immunity would have really lasted, since we eradicated it so quickly.

[^cold immunity]: “We found no significant difference between the probability of testing positive at least once and the probability of a recurrence for the beta-coronaviruses HKU1 and OC43 at 34 weeks after enrollment/first infection.” [Marta Galanti & Jeffrey Shaman (PDF)](http://www.columbia.edu/~jls106/galanti_shaman_ms_supp.pdf)

[^unclear]: “Once a person fights off a virus, viral particles tend to linger for some time. These cannot cause infections, but they can trigger a positive test.” [from STAT News by Andrew Joseph](https://www.statnews.com/2020/04/20/everything-we-know-about-coronavirus-immunity-and-antibodies-and-plenty-we-still-dont/)

[^monkeys]: From [Bao et al.](https://www.biorxiv.org/content/10.1101/2020.03.13.990226v1.abstract) *Disclaimer: This article is a preprint and has not been certified by peer review (yet).* Also, to emphasize: they only tested re-infection 28 days later. 

For these simulations, let's say it's 1 year.
**Here's a simulation starting with 100% <icon r></icon>**, exponentially decaying into susceptible, no-immunity <icon s></icon>s after 1 year, on *average*, with variation:

<div class="sim">
		<iframe src="sim?stage=yrs-1&format=lines&height=600" width="800" height="600"></iframe>
</div>

Return of the exponential decay!

This is the **SEIRS Model**. The final "S" stands for <icon s></icon> Susceptible, again.

![](pics/seirs.png)

Now, let's simulate a COVID-19 outbreak, over 10 years, with no interventions... *if immunity only lasts a year:*

<div class="sim">
		<iframe src="sim?stage=yrs-2&format=lines&height=600" width="800" height="600"></iframe>
</div>

In previous simulations, we only had *one* ICU-overwhelming spike. Now, we have several, *and* <icon i></icon> cases come to a rest *permanently at* ICU capacity. (Which, remember, we *tripled* for these simulations)

R = 1, it's **endemic.**

Thankfully, because summer reduces R, it'll make the situation better:

<div class="sim">
		<iframe src="sim?stage=yrs-3&format=lines&height=640" width="800" height="640"></iframe>
</div>

Oh.

Counterintuitively, summer makes the spikes worse *and* regular! This is because summer reduces new <icon i></icon>s, but that in turn reduces new immune <icon r></icon>s. Which means immunity plummets in the summer, *creating* large regular spikes in the winter.

Thankfully, the solution to this is pretty straightforward – just vaccinate people every fall/winter, like we do with flu shots:

**(After playing the recording, try simulating your own vaccination campaigns! Remember you can pause/continue the sim at any time)**

<div class="sim">
		<iframe src="sim?stage=yrs-4&format=lines" width="800" height="540"></iframe>
</div>

But here's the scarier question:

What if there's no vaccine for *years*? Or *ever?*

**To be clear: this is unlikely.** Most epidemiologists expect a vaccine in 1 to 2 years. Sure, there's never been a vaccine for any of the other coronaviruses before, but that's because SARS was eradicated quickly, and "the" common cold wasn't worth the investment. 

Still, infectious disease researchers have expressed worries: What if we can't make enough?[^vax_enough] What if we rush it, and it's not safe?[^vax_safe]

[^vax_enough]: “If a coronavirus vaccine arrives, can the world make enough?” [by Roxanne Khamsi, on Nature](https://www.nature.com/articles/d41586-020-01063-8)

[^vax_safe]: “Don’t rush to deploy COVID-19 vaccines and drugs without sufficient safety guarantees” [by Shibo Jiang, on Nature](https://www.nature.com/articles/d41586-020-00751-9)

Even in the nightmare "no-vaccine" scenario, we still have 3 ways out. From most to least terrible:

1) Do intermittent or loose R < 1 interventions, to reach "natural herd immunity". (Warning: this will result in many deaths & damaged lungs. *And* won't work if immunity doesn't last.)

2) Do the R < 1 interventions forever. Contact tracing & wearing masks just becomes a new norm in the post-COVID-19 world, like how STI tests & wearing condoms became a new norm in the post-HIV world.

3) Do the R < 1 interventions until we develop treatments that make COVID-19 way, way less likely to need critical care. (Which we should be doing *anyway!*) Reducing ICU use by 10x is the same as increasing our ICU capacity by 10x:

**Here's a simulation of *no* lasting immunity, *no* vaccine, and not even any interventions – just slowly increasing capacity to survive the long-term spikes:**

<div class="sim">
		<iframe src="sim?stage=yrs-5&format=lines" width="800" height="540"></iframe>
</div>

Even under the *worst* worst-case scenario... life perseveres.

. . .

Maybe you'd like to challenge our assumptions, and try different R<sub>0</sub>'s or numbers. Or try simulating your *own* combination of intervention plans!

**Here's an (optional) Sandbox Mode, with *everything* available. (scroll to see all controls) Simulate & play around to your heart's content:**

<div class="sim">
		<iframe src="sim?stage=SB&format=sb" width="800" height="540"></iframe>
</div>

This basic "epidemic flight simulator" has taught us so much. It's let us answer questions about the past few months, next few months, and next few years.

So finally, let's return to...

<div class="section chapter">
    <div>
		<img src="banners/curve.png" height=480 style="position: absolute;"/>
        <div>The Now</div>
    </div>
</div>

Plane's sunk. We've scrambled onto the life rafts. It's time to find dry land.[^dry_land]

[^dry_land]: Dry land metaphor [from Marc Lipsitch & Yonatan Grad, on STAT News](https://www.statnews.com/2020/04/01/navigating-covid-19-pandemic/)

Teams of epidemiologists and policymakers ([left](https://www.americanprogress.org/issues/healthcare/news/2020/04/03/482613/national-state-plan-end-coronavirus-crisis/), [right](https://www.aei.org/research-products/report/national-coronavirus-response-a-road-map-to-reopening/ ), and [multi-partisan](https://ethics.harvard.edu/covid-roadmap)) have come to a consensus on how to beat COVID-19, while protecting our lives *and* liberties.

Here's the rough idea, with some (less-consensus) backup plans:

![](pics/plan.png)

So what does this mean for YOU, right now?

**For everyone:** Respect the lockdown so we can get out of Phase I asap. Keep washing those hands. Make your own masks. Download a *privacy-protecting* contact tracing app when those are available next month. Stay healthy, physically & mentally! And write your local policymaker to get off their butt and...

**For policymakers:** Make laws to support folks who have to self-isolate/quarantine. Hire more manual contact tracers, *supported* by privacy-protecting contact tracing apps. Direct more funds into the stuff we should be building, like...

**For builders:** Build tests. Build ventilators. Build personal protective equipment for hospitals. Build tests. Build masks. Build apps. Build antivirals, prophylactics, and other treatments that aren't vaccines. Build vaccines. Build tests. Build tests. Build tests. Build hope. 

Don't downplay fear to build up hope. Our fear should *team up* with our hope, like the inventors of airplanes & parachutes. Preparing for horrible futures is how we *create* a hopeful future.

The only thing to fear is the idea that the only thing to fear is fear itself.
