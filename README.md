## Perbaikan Kode HTML dan CSS
Pada kode HTML dan CSS di program, beberapa perbaikan yang dilakukan meliputi:

1. *Struktur HTML*:
   - Ditambahkan tag <html>, <head>, dan <body> yang sesuai untuk membuat dokumen HTML menjadi valid dan terstruktur dengan baik.
   - Ditambahkan <meta charset="UTF-8"> dan <meta name="viewport" content="width=device-width, initial-scale=1.0"> untuk mendukung karakter UTF-8 dan tampilan responsif di perangkat mobile.
   - Tag <title> disertakan untuk memberikan judul pada halaman.
   - File CSS eksternal ditautkan melalui <link rel="stylesheet" href="./assets/styles/styles.css"> untuk memisahkan styling dari struktur HTML.
  
2. *Perbaikan Struktur CSS*:
   - CSS dipindahkan ke file terpisah (styles.css) untuk meningkatkan keterbacaan dan pemeliharaan kode.
   - Penggunaan *grid layout* ditambahkan pada elemen body untuk mengatur tata letak halaman.
   - Setiap elemen (header, nav, section, footer) diberi *warna latar belakang, **grid-area, dan **padding* agar terlihat lebih rapi.

---

## Penjelasan Penggunaan CSS vs Tanpa CSS pada HTML

Menggunakan CSS (Cascading Style Sheets) dalam sebuah halaman HTML memberikan tampilan dan tata letak yang lebih baik daripada hanya menggunakan HTML tanpa CSS. Berikut adalah penjelasan perbedaan yang signifikan.

### 1. *Tampilan Visual*
- *Tanpa CSS*: 
  - HTML tanpa CSS hanya menampilkan elemen-elemen secara default, tanpa penyesuaian warna, ukuran, atau posisi.
  - Semua elemen ditampilkan dalam tata letak linier dari atas ke bawah, dengan tampilan warna standar hitam-putih.
- *Dengan CSS*: 
  - Elemen-elemen halaman dapat disesuaikan dengan berbagai atribut visual seperti warna latar belakang, margin, padding, dan tata letak grid.
  - Pada contoh ini, CSS memberikan warna latar yang berbeda untuk header, nav, section, dan footer, serta membuat tata letak grid yang memposisikan nav di sebelah kiri dan section di tengah.

### 2. *Tata Letak Halaman*
- *Tanpa CSS*: 
  - Semua elemen ditampilkan secara vertikal dalam satu kolom, yang seringkali terlihat monoton dan kurang menarik.
- *Dengan CSS*: 
  - Penggunaan *grid layout* pada CSS memungkinkan penataan elemen secara responsif. Contohnya:
    css
    body {
        display: grid;
        grid-template-areas:
            "header header header"
            "nav section section"
            "footer footer footer";
        grid-template-rows: 80px 1fr 50px;
        grid-template-columns: 20% 1fr 18%;
    }
    
    Hal ini membuat header berada di bagian atas, nav di sebelah kiri, section di tengah, dan footer di bawah.

### 3. *Warna dan Gaya Visual*
- *Tanpa CSS*: 
  - Elemen-elemen ditampilkan dengan warna standar browser (umumnya hitam dan putih).
- *Dengan CSS*: 
  - Setiap elemen dapat memiliki warna khusus, contohnya header dan footer memiliki warna abu-abu gelap, nav berwarna abu-abu muda, dan section berwarna abu-abu netral:
    css
    header {
        background: #707070;
    }
    nav {
        background: #C9BFBF;
    }
    section {
        background: #ABABAB;
    }
    footer {
        background: #707070;
    }
    

### 4. *Ukuran dan Spasi Antar Elemen*
- *Tanpa CSS*:
  - Setiap elemen ditampilkan dengan margin dan padding default yang kurang rapi.
- *Dengan CSS*:
  - CSS memungkinkan kita menambahkan margin, padding, dan jarak antar elemen untuk memberikan ruang yang lebih rapi dan estetis:
    css
    header, nav, section, footer {
        padding: 5px;
    }
    

### 5. *Responsivitas*
- *Tanpa CSS*:
  - Halaman tidak dapat menyesuaikan diri dengan berbagai ukuran layar.
- *Dengan CSS*:
  - Penggunaan CSS memungkinkan tata letak yang responsif, seperti pengaturan grid yang lebih fleksibel untuk berbagai ukuran layar.

### *Kesimpulan*
CSS sangat penting dalam menciptakan halaman web yang menarik dan user-friendly. Dengan CSS, elemen-elemen dapat diatur secara lebih profesional dan estetis.

---

## Source Code

### HTML Sebelum Diperbaiki

html
<!DOCTYPE html>
<header> 
 <h1>HTML5 Semantic</h1> 
</header> 
<nav> 
 <ul> 
 <li><a href="#home">Home</a></li> 
 <li><a href="#pengertian">Pengertian</a></li> 
 <li><a href="#kesimpulan">Kesimpulan</a></li> 
 </ul> 
</nav> 
<section> 
 Konten 
</section> 
<footer> 
 Copyright 
</footer>


### HTML Setelah Diperbaiki

html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML5 Semantic</title>
    <link rel="stylesheet" href="./assets/styles/styles.css">
</head>
<body>
    <header>
        <h1>HTML5 Semantic</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#pengertian">Pengertian</a></li>
            <li><a href="#kesimpulan">Kesimpulan</a></li>
        </ul>
    </nav>
    <section>
        Konten
    </section>
    <footer>
        Copyright
    </footer>
</body>
</html>


### CSS File (styles.css)

css
nav {
    background: #C9BFBF;
    grid-area: nav;
}

header {
    background: #707070;
    grid-area: header;
    text-align: center;
}

section {
    background: #ABABAB;
    grid-area: section;
}

footer {
    background: #707070;
    grid-area: footer;
    font-size: small;
    text-align: center;
}

body {
    display: grid;
    grid-template-areas:
        "header header header"
        "nav section section"
        "footer footer footer";
    grid-template-rows: 80px 1fr 50px;
    grid-template-columns: 20% 1fr 18%;
    grid-gap: 5px;
    height: 100vh;
    margin: 10px;
}

header, nav, section, footer {
    padding: 5px;
}


---
