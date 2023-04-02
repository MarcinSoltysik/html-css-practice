#

# notebook

Notes from the tour-web project

## Building a project from scratch

1. import fontów
<link href="https://fonts.googleapis.com/css?family=Lato:100,300,400,700,900">

2. icona, favicon
<link rel="shortcut icon" type="image/jpg" href="img/favicon.png" />

3. global reset - css

- Każda przeglądarak, ma jakieś domyślne swoje ustawienia jak dany tag wyświetlać, dlatego na początku robisz tzw. reste globalny. Dajesz selektor \* ,

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

- możesz też na początku projektu zrobić font dla całego projektu, już jest zaimportowany w html, a teraz w css, dajesz jego właściciwosci
- dalczego w body - dlatego, aby w ramach dziedziczenia każdy nastepny elelemnt miał już to ustawione

body {
font-family: 'Lato', sans-serif;
font-weight: 400;
font-size: 16px;
}

### How it's working

1. Wyjasnij co to

   - box-sizing: border-box;
   - line-height: 1.7;
   - height: 95vh;
     // obrazek nie zajmuje całego ekranu, zobacz masz odcięcie na dole

2. ustawienie obrazka jako tła,
   Tu masz kilka rzeczy do zrobienia, i wyjaśnienia

- height: 95vh; - zajmuje 95 wysokosci okna przegladarki

- background-image: url(./img/hero.jpg);
  // miejsce gdzie masz polozony obrazek

- background-size: cover;
  // pokrycie obrazkiem,

- background-position: top; // bottom, center
  // tu musisz sobie zobaczyc co sie dzieje jak zmniejszasz okno przegldaraki, w zaleznosci co masz ustawione to w taki sposb ten obraze zawsze bedzie "przypiety" a inne elementy beda obcinane

3. stylowanie obrazu - 'kolorowanie'
   background-image: linear-gradient(
   to right bottom,
   rgba(126, 213, 111, 0.8),
   rgba(40, 180, 131, 0.8)
   ),
   url(img/hero.jpg);

4. robienie kształtów - https://bennettfeely.com/clippy/

   - clip-path: polygon(0 0, 100% 0, 100% 550px, 0 100%);

   - clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);

   - zamiast sztywnego px, zrób vh, dzieki temu bedzie "responsywne'

5. pos
   position: relative;
   position: absolute;
   stylowanie top, left, względem rodzica, dlatego tag ktory chdesz stylowac musi byc absolute ale kjego rodzic musi byc relative
