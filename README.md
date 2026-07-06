# Odev

> Web Programming coursework — Izmir University of Economics

Homework submissions for **Emre Özel** (20252425263, Şube 2). Each assignment is archived as a standalone `.zip`, exactly as submitted, containing small PHP/HTML exercises that build from static forms to session auth to database-backed logic.

## Tech Stack

| Layer      | Tools                              |
| ---------- | ----------------------------------- |
| Language   | PHP, HTML, CSS, JavaScript         |
| Data       | JSON, MySQL (`mysqli`)             |
| Auth       | PHP sessions                       |

## Assignments

| Archive | Topic | Description |
| --- | --- | --- |
| [`Odev2`](20252425263_EmreOzel_Sube2_Odev2.zip) | Written theory + templated page | **Soru 1:** Word doc answering the assignment's theory questions. **Soru 2:** a PHP-rendered art-portfolio page (`index.php`) built on a "Sanat Sitesi" template, with PHP variables for contact info (city, phone, email, hours). |
| [`Odev3`](20252425263_EmreOzel_Sube2_Odev3.zip) | Form handling & sanitization | **Soru 1:** login form → `kullanici_kontrol.php` validates a hardcoded username/password, sanitized with `htmlspecialchars`. **Soru 2:** shopping-cart form → `sepet_toplam.php` computes subtotal, VAT, discount, and grand total. |
| [`Odev4`](20252425263_EmreÖzel_Sube2_MBP192-102_Odev4.zip) | Session-based auth | `login.php` authenticates (`admin`/`123`) and starts a session, `panel.php` shows a welcome message to logged-in users (redirects otherwise), `logout.php` destroys the session. |
| [`Odev5`](20252425263_EmreOzel_Sube2_MBP192-102_Odev5.zip) | Grade calculation (JSON) | `index.php` reads student records from `ogrenciler.json`, computes a weighted grade (25% midterm, 25% homework, 5% project, 45% final), derives letter grade / GPA coefficient / pass-fail status, and writes results to `sonuclar.json`. |
| [`Odev6`](20252425263_EmreOzel_Sube2_MBP192-102_Odev6.zip) | Grade calculation (MySQL) | Same grading logic as Odev5, backed by a database: `db.php` holds the connection config (`okul_db`), `index.php` queries the `ogrenciler` table and computes grades from the returned rows. |

## Running an Assignment

Each archive is self-contained. To run one locally:

1. Unzip the archive into your PHP server's document root (e.g. `htdocs/`, or serve with `php -S localhost:8000`).
2. For **Odev6**, create a MySQL database named `okul_db` with an `ogrenciler` table (columns: `okul_no`, `ad_soyad`, `ders_adi`, `vize`, `odev`, `proje`, `final`) and update the credentials in `db.php` if needed.
3. Open `index.html` or `index.php` in a browser through the running server.

## Author

Emre Özel — Associate Degree student, Izmir University of Economics
