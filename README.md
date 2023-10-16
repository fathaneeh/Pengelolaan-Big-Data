# Pengelolaan-Big-Data
Matakuliah Pengelolaan Big Data

<h2>#Cara Install MongoDB ke Docker</h2>
<li> Pull image mongodb </li>
  <p>docker pull mongo </p> 
<li> Jalankan container mongodb dan menamai container dengan "mongoData" (nama container kalian)</li>
  <p>docker run --name mongoData -p 27017:27017 mongo</p>
<li> Cek container apakah sudah ada (bisa di cek lewat docker desktop) </li>
  <p>docker images </p> 
<li> Membuat user</li>
  <p>docker exec -it mongoData bash</p>
<li> Masuk ke mongodb dengan mongosh (yang sudah terupdate) </li>
  <p>mongosh</p> 
<li> Melihat data base yang aktif</li>
  <p>show dbs </p>
<li> menghubungkan ke mongoDB compass (optional)) </li>
  <p><img width="954" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/e088e408-ff4a-4d63-8973-fd74cbc13452"></p> 
<li> menghubungkan dengan extention mongoDB di vscode (optional)</li>
  <p><img width="960" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/1a2a58d6-f9f2-45ef-8912-771b6eacd188"> </p> 
   


<h2>#Crawling Data</h2>
<p>Terdapat 2 file di bagian crawling data</p>
<p>file 1 : crawling data dengan menggunakan python via Jupiter Notebook</p>
<p>file 2 : Scraping data dengan menggunakan web scraping Phanthom Buster</p>

<h3>#Crawling data instagram menggunakan Python (Jupiter Notebook)</h3>
<p>pada bagian ini hanya menjelaskan sampai tahap crawling dan tidak melanjutkan ke tahap memasukan ke database mongoDB</p>
<p>Pastikan sudah terinstall ke dalam library : </p>
<li>Instaloader : Untuk Crawling data Instagram </li>
<li>Jsonpickle : Untuk Konversi data Python ke Json </li>
<br>
<p> Import instaloader </p>
<p>>Bikin code sederhana</p>
<p><img width="562" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/641b4b0d-3b42-47f0-9040-d33eed4d4f44"></p>
<p>tujuan code sederhana yang saya buat adalah untuk mendapatkan informasi dari postingan akun tersebut yang berupa : Gambar postingan (png), Caption (txt), video (mp4)</p>
<p>untuk fungsi query instaloader dapat dilihat di : https://instaloader.github.io/</p>
<li>Masukan Akun instagram yang ingin di crawling. Case saya menggunakan brand Kahf (brand perawatan untuk pria)</li>
<p><img width="677" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/d709d706-cc5d-4fa7-b057-197364d210ac"></p>
<p>setelah crawling selesai file hasil crawling akan langsung muncul ditempat membuat file codenya</p>
<p><img width="569" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/04b97bc7-6cd6-4085-9d34-92ed72aa82e3"></p>

<h3>#Scraping data dengan menggunakan web scraping Phanthom Buster</h3>
<br>
<p>Phanthom buster adalah web scraper yang berfungsi scraping data tertentu dari media sosial</p>
<p><img width="953" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/8122f725-31c3-4b3f-aee7-d7b15cf56ef6"> </p>
<p> disana juga tersedia cara penggunaannya yang bisa dipahami dan juga ada video tutorialnya </p>
<br>
<p>Pastikan sudah connect ke mongodb lewat vscode/mongoDB Compass </p>
<p>Pastikan sudah membuat collection di mongoDB</p>
<br>
<li>Akses ke pnathom boster : https://phantombuster.com/?deal=jong94 </li>
<li>Pilih fitur Instagram profile Extractor untuk melakukan scraping ke instagram</li>
<p><img width="958" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/07dfd5b5-1df3-4099-9159-be4c9408b194"></p>
<li>Tentukan akun yang ingin di scraper</li>
<p><img width="941" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/4afc54ed-f1a2-4310-b3de-3c421f06814a"></p>
<li>Tentukan jumlah data yang ingin diambil</li>
<p><img width="960" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/e0360953-99b7-4e0f-ab6b-f3135927f7c3"></p>
<li>Tentukan frequensi pengambilan data</li>
<p><img width="955" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/b93629c4-5fe8-4ba1-bc57-7932886722c9"></p>
<li>lakukan scraping</li>
<p><img width="950" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/a2c880e3-3b58-498d-95de-ce86dab3f23e"></p>
<li>download result</li>
<p><img width="960" alt="image" src="https://github.com/fathaneeh/Pengelolaan-Big-Data/assets/115605304/65b8062c-6e11-4b36-996e-d68c3043c451"></p>
<li>Import file csv/json ke mongogb</li>
<br>
<p>Sumber :</p>
<li>https://phumipatc.medium.com/how-to-install-mongodb-to-docker-f17cec2b1f8f</li>
<li>https://www.youtube.com/watch?v=tzVk6aV66so&t=744s</li>
<li>https://www.youtube.com/@phantombuster4587/search</li>
