---

# Web Scraping and Article Rewriting

This Python code is used to scrape data from the website aibusiness.com. It includes functions for text cleaning and manipulation, as well as using the OpenAI model to rewrite articles in Indonesian.

## Dependencies

Make sure you have installed all the required dependencies before running this code. The following dependencies are needed:

- numpy (version 1.21.2 or later)
- pandas (version 1.3.3 or later)
- beautifulsoup4 (version 4.9.3 or later)
- requests (version 2.26.0 or later)
- regex (version 2021.10.8 or later)
- json (version 2.0.9 or later)
- io (built-in with Python)
- base64 (built-in with Python)
- ast (built-in with Python)
- itertools (built-in with Python)
- urllib (built-in with Python)
- random (built-in with Python)
- schedule (version 1.1.0 or later)
- glob (built-in with Python)
- datetime (built-in with Python)
- tqdm (version 4.62.3 or later)
- selenium (version 4.0.0-alpha.7 or later)
- openai (version 0.29.0 or later)
- retry (version 0.9.2 or later)
- webdriver_manager (version 3.5.0 or later)
- Chrome WebDriver (compatible version with your Chrome browser)

## How to Use the Code

1. Make sure you have installed all the required dependencies.
2. Replace the `api_key` value with a valid OpenAI API key. You need to sign up with OpenAI to obtain an API key.
3. Run the code in a suitable Python environment.

## Main Functions

1. `clean_hashtag(text)`: This function removes hashtags (#) from the given text.
2. `clean_url_from_text(text)`: This function removes URLs from the given text.
3. `clean_multiple_spaces(text)`: This function removes excessive spaces from the given text.
4. `remove_non_ascii(text)`: This function removes non-ASCII characters from the given text.
5. `get_all_link(url)`: This function retrieves all article links from the given URL using Selenium and BeautifulSoup.
6. `get_link(soup)`: This function retrieves a list of article links from the BeautifulSoup object.
7. `get_artikel(url)`: This function retrieves the article content from the given URL using Selenium and BeautifulSoup.
8. `res_artikel(soup, url, scrapped_url)`: This function extracts article information from the BeautifulSoup object and returns it as a dictionary.
9. `get_list_links(results_urls)`: This function takes a list of search result URLs and returns a list of article links.
10. `find_artikel(urls, scrapped_url)`: This function takes a list of article links and a list of previously scraped URLs and returns a list of article links that have not been scraped before.
11. `rewrite(teks)`: This function rewrites the article in Indonesian using the OpenAI model.
12. `start_scrap()`: This function is the main entry point of the program. It runs the scraping and article rewriting process.

## Output

This code will generate a JSON file containing the rewritten articles in Indonesian. Each article will have information such as title, date, URL, source, and content. The JSON file can be used for further purposes, such as analysis or publication.

You can also customize this code to fit your needs. For example, by changing the value of the `keyword` to a topic of your interest, such as fashion, food, or other topics, you will get relevant articles based on your interest. Each time the code is run, one article will be generated in JSON format, which you can use for various purposes.

Furthermore, you can use automation to generate articles on a scheduled basis. For example, you can run this program automatically every day using cron jobs, schedulers, or similar tools. This way, you can upload new content automatically every day without having to do manual tasks.

With the flexibility and automation capability of this code, you can optimize your time and resources in producing quality articles according to your needs.

---




## Web Scraping dan Penulisan Ulang Artikel

Kode Python ini digunakan untuk melakukan scraping data dari situs web aibusiness.com. Kode ini mencakup fungsi-fungsi untuk membersihkan dan memanipulasi teks, serta menggunakan model OpenAI untuk menulis ulang artikel dalam bahasa Indonesia.

## Dependensi

Pastikan Anda telah menginstal semua dependensi yang diperlukan sebelum menjalankan kode ini. Berikut adalah dependensi yang diperlukan:

- numpy (versi 1.21.2 atau lebih baru)
- pandas (versi 1.3.3 atau lebih baru)
- beautifulsoup4 (versi 4.9.3 atau lebih baru)
- requests (versi 2.26.0 atau lebih baru)
- regex (versi 2021.10.8 atau lebih baru)
- json (versi 2.0.9 atau lebih baru)
- io (versi bawaan Python)
- base64 (versi bawaan Python)
- ast (versi bawaan Python)
- itertools (versi bawaan Python)
- urllib (versi bawaan Python)
- random (versi bawaan Python)
- schedule (versi 1.1.0 atau lebih baru)
- glob (versi bawaan Python)
- datetime (versi bawaan Python)
- tqdm (versi 4.62.3 atau lebih baru)
- selenium (versi 4.0.0-alpha.7 atau lebih baru)
- openai (versi 0.29.0 atau lebih baru)
- retry (versi 0.9.2 atau lebih baru)
- webdriver_manager (versi 3.5.0 atau lebih baru)
- Chrome WebDriver (versi yang sesuai dengan versi Chrome yang Anda gunakan)

## Cara Menggunakan Kode

1. Pastikan Anda telah menginstal semua dependensi yang diperlukan.
2. Ganti nilai `api_key` dengan kunci API OpenAI yang valid. Anda perlu mendaftar di OpenAI untuk mendapatkan kunci API.
3. Jalankan kode di lingkungan Python yang sesuai.

## Fungsi-fungsi Utama

1. `clean_hashtag(text)`: Fungsi ini menghapus hashtag (#) dari teks yang diberikan.
2. `clean_url_from_text(text)`: Fungsi ini menghapus URL dari teks yang diberikan.
3. `clean_multiple_spaces(text)`: Fungsi ini menghapus spasi berlebih dari teks yang diberikan.
4. `remove_non_ascii(text)`: Fungsi ini menghapus karakter non-ASCII dari teks yang diberikan.
5. `get_all_link(url)`: Fungsi ini mengambil semua link artikel dari URL yang diberikan menggunakan Selenium dan BeautifulSoup.
6. `get_link(soup)`: Fungsi ini mengambil daftar link artikel dari objek BeautifulSoup.
7. `get_artikel(url)`: Fungsi ini mengambil konten artikel dari URL yang diberikan menggunakan Selenium dan BeautifulSoup.
8. `res_artikel(soup, url, scrapped_url)`: Fungsi ini mengekstrak informasi artikel dari objek BeautifulSoup dan mengembalikannya dalam bentuk dictionary.
9. `get_list_links(results_urls)`: Fungsi ini menerima daftar URL hasil pencarian dan mengembalikan daftar link artikel.
10. `find_artikel(urls, scrapped_url)`: Fungsi ini menerima daftar link artikel dan daftar URL

 yang sudah diambil sebelumnya, dan mengembalikan daftar link artikel yang belum pernah diambil sebelumnya.
11. `rewrite(teks)`: Fungsi ini menulis ulang artikel dalam bahasa Indonesia menggunakan model OpenAI.
12. `start_scrap()`: Fungsi ini merupakan titik masuk utama program. Fungsi ini menjalankan proses scraping dan penulisan ulang artikel.

## Output

Kode ini akan menghasilkan file JSON yang berisi artikel yang telah ditulis ulang dalam bahasa Indonesia. Setiap artikel akan memiliki informasi seperti judul, tanggal, URL, sumber, dan konten. File JSON dapat digunakan untuk tujuan selanjutnya, seperti analisis atau publikasi.

Anda juga dapat mengkustomisasi kode ini untuk memenuhi kebutuhan Anda. Misalnya, dengan mengubah nilai `keyword` menjadi topik yang Anda minati, seperti fashion, makanan, atau topik lainnya, Anda akan mendapatkan artikel yang relevan dengan minat Anda. Setiap kali kode dijalankan, akan dihasilkan satu artikel dalam format JSON, yang dapat Anda gunakan untuk berbagai keperluan.

Selain itu, Anda dapat menggunakan otomatisasi untuk menghasilkan artikel secara terjadwal. Misalnya, Anda dapat menjalankan program ini secara otomatis setiap hari menggunakan cronjob, scheduler, atau alat serupa. Dengan demikian, Anda dapat mengunggah konten baru secara otomatis setiap hari tanpa harus melakukan tugas manual.

Dengan fleksibilitas dan kemampuan otomatisasi yang dimiliki oleh kode ini, Anda dapat mengoptimalkan penggunaan waktu dan sumber daya Anda dalam menghasilkan artikel berkualitas sesuai dengan kebutuhan Anda.

---
