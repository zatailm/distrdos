# DESKRIPSI

Kode ini adalah sebuah fungsi dalam bahasa pemrograman R yang bertujuan untuk mendistribusikan 
mahasiswa ke dosen pembimbing dan penguji untuk skripsi atau tugas akhir. Fungsi ini menggunakan 
data mahasiswa, dosen, pendamping, dan penguji yang diberikan sebagai input untuk melakukan 
distribusi. Distribusi dilakukan dengan mempertimbangkan kesesuaian antara topik skripsi mahasiswa
dan bidang doseb (khusus untuk dosen utama), ketersediaan dosen, dan batas maksimal mahasiswa yang 
dapat dibimbing oleh setiap dosen. Selain itu, fungsi ini juga berusaha memastikan bahwa setiap 
mahasiswa memiliki dosen pembimbing dan penguji yang berbeda, serta memenuhi batas maksimal 
mahasiswa yang dapat dibimbing oleh setiap dosen. Kode ini dapat digunakan untuk memudahkan 
proses distribusi mahasiswa dalam program studi.

Kode ini disediakan "sebagaimana adanya", tanpa jaminan jenis apapun.
Author: maz ilmam

Contoh hasil:

| NO  | NIM     | MAHASISWA         | TOPIK        | JUDUL              | DOSEN UTAMA            | BIDANG       | DOSEN PENDAMPING        | DOSEN PENGUJI           |
| --- | ------- | ----------------- | ------------ | ------------------ | ---------------------- | ------------ | ----------------------- | ----------------------- |
| 1   | 2021001 | Aditya Pratama    | Politik      | Cerita tersembunyi | Hapipi Jayadi, MAP     | Politik      | Elita Anggriani, M.Si    | Rohani Inta Dewi, MA    |
| 2   | 2021002 | Siti Nurhaliza    | Pemberdayaan | Matahari terbenam  | Rohani Inta Dewi, MA   | Pemberdayaan | H. Lalu Hidir, MH        | Lalu Moh. Nazar Fajri, MAP |
| 3   | 2021003 | Muhammad Firdaus  | Ketahanan    | Hujan lebat        | M. Adib Zata Ilmam, M.Sc.| Ketahanan  | Alwafi Ridho S, M.I.Pol  | Natila Rizka Safitri, M.Si |
| 4   | 2021004 | Angela Li         | Tata Kelola  | Laut biru          | Abdul Mukmin RY, M.Si  | Tata Kelola  | Reni Anggriani, MH       | Mufidah, M.Si           |
| 5   | 2021005 | Carlos Rodriguez  | Organisasi   | Bunga bersemi      | M. Nasuhi, MAP         | Organisasi   | Rohani Inta Dewi, MA     | Alwafi Ridho S, M.I.Pol |
| 6   | 2021006 | Priya Patel       | Pemerintahan | Langit berawan     | Pahrizal Iqrom, MAP    | Pemerintahan | Hamdi, MAP               | Elita Anggriani, M.Si   |
| 7   | 2021007 | Andrei Ivanov     | Kebijakan    | Angin bertiup      | Lalu Moh. Nazar Fajri, MAP | Kebijakan | M. Adib Zata Ilmam, M.Sc. | Mikyarul Ilmi, M.Si   |
| 8   | 2021008 | Mei Ling Wong     | Sosial       | Senyum terindah    | Mufidah, M.Si          | Sosial       | Hapipi Jayadi, MAP       | Alwafi Ridho S, M.I.Pol |
| 9   | 2021009 | Javier Garcia     | Hukum        | Gelap malam        | H. Lalu Hidir, MH      | Hukum        | Mufidah, M.Si            | M. Nasuhi, MAP          |
| 10  | 2021010 | Fatima Khan       | Tata Kelola  | Harapan menyala    | Abdul Mukmin RY, M.Si  | Tata Kelola  | Mikyarul Ilmi, M.Si      | Hamdi, MAP              |
| 11  | 2021011 | Hiroshi Tanaka    | Politik      | Waktu berlalu      | Hapipi Jayadi, MAP     | Politik      | Pahrizal Iqrom, MAP      | Elita Anggriani, M.Si   |
| 12  | 2021012 | Maria Santos      | Pemberdayaan | Cinta datang       | Rohani Inta Dewi, MA   | Pemberdayaan | Mufidah, M.Si            | Natila Rizka Safitri, M.Si |
| 13  | 2021013 | Ahmed Ibrahim     | Ketahanan    | Mimpi melayang     | M. Adib Zata Ilmam, M.Sc.| Ketahanan  | Reni Anggriani, MH       | Mufidah, M.Si           |
| 14  | 2021014 | Elena Petrova     | Pemerintahan | Petir menyambar    | Pahrizal Iqrom, MAP    | Pemerintahan | Hapipi Jayadi, MAP       | M. Nasuhi, MAP          |
| 15  | 2021015 | Juan Martinez     | Organisasi   | Daun jatuh         | M. Nasuhi, MAP         | Organisasi   | Mikyarul Ilmi, M.Si      | Hazazi Ridho S, M.I.Pol |
| 16  | 2021016 | Olivia Johnson    | Kebijakan    | Duka mendalam      | Lalu Moh. Nazar Fajri, MAP | Kebijakan | Muh. Sahli, MAP          | Mikyarul Ilmi, M.Si   |
| 17  | 2021017 | Stefan Popescu    | Sosial       | Pagi yang cerah    | Natila Rizka Safitri, M.Si | Sosial     | Hazazi Ridho S, M.I.Pol  | M. Adib Zata Ilmam, M.Sc. |
| 18  | 2021018 | Aisha Abdullah    | Tata Kelola  | Malam sunyi        | Abdul Mukmin RY, M.Si  | Tata Kelola  | Alwafi Ridho S, M.I.Pol  | Pahrizal Iqrom, MAP     |
| 19  | 2021019 | Luca Rossi        | Politik      | Rindu tak terucap  | Hapipi Jayadi, MAP     | Politik      | Natila Rizka Safitri, M.Si | Hazazi Ridho S, M.I.Pol |
| 20  | 2021020 | Emily Smith       | Pemberdayaan | Pelangi muncul     | Rohani Inta Dewi, MA   | Pemberdayaan | Lalu Moh. Nazar Fajri, MAP | Hamdi, MAP            |
| 21  | 2021021 | Abdul Rahman      | Hukum        | Suara gemuruh      | H. Lalu Hidir, MH      | Hukum        | Rohani Inta Dewi, MA     | M. Nasuhi, MAP          |
| 22  | 2021022 | Sophie Dupont     | Pemerintahan | Cahaya redup       | Pahrizal Iqrom, MAP    | Pemerintahan | Natila Rizka Safitri, M.Si | Reni Anggriani, MH    |
| 23  | 2021023 | Ji-hoon Kim       | Organisasi   | Terima kasih       | M. Nasuhi, MAP         | Organisasi   | Abdul Mukmin RY, M.Si    | H. Lalu Hidir, MH       |
| 24  | 2021024 | Gabriela Silva    | Ketahanan    | Api membakar       | M. Adib Zata Ilmam, M.Sc.| Ketahanan  | Pahrizal Iqrom, MAP      | Rohani Inta Dewi, MA    |
| 25  | 2021025 | Mikhail Ivanov    | Tata Kelola  | Bunga mekar        | Abdul Mukmin RY, M.Si  | Tata Kelola  | Hamdi, MAP               | M. Adib Zata Ilmam, M.Sc. |
| 26  | 2021026 | Sofia Hernandez   | Kebijakan    | Langkah terhenti   | Lalu Moh. Nazar Fajri, MAP | Kebijakan | Muh. Sahli, MAP          | M. Nasuhi, MAP          |
| 27  | 2021027 | David Wilson      | Politik      | Air mengalir       | Hapipi Jayadi, MAP     | Politik      | Elita Anggriani, M.Si    | Abdul Mukmin RY, M.Si   |
| 28  | 2021028 | Chihiro Yamamoto  | Sosial       | Cinta tumbuh       | Natila Rizka Safitri, M.Si | Sosial     | H. Lalu Hidir, MH        | Hamdi, MAP              |
| 29  | 2021029 | Ahmed Ali         | Pemberdayaan | Malam gelap        | Rohani Inta Dewi, MA   | Pemberdayaan | Hazazi Ridho S, M.I.Pol  | Hapipi Jayadi, MAP      |
| 30  | 2021030 | Emma Brown        | Hukum        | Senyum mengembang  | H. Lalu Hidir, MH      | Hukum        | Abdul Mukmin RY, M.Si    | Lalu Moh. Nazar Fajri, MAP |
| 31  | 2021031 | Matheus Oliveira  | Organisasi   | Angin sepoi-sepoi  | M. Nasuhi, MAP         | Organisasi   | Hamdi, MAP               | Abdul Mukmin RY, M.Si   |
| 32  | 2021032 | Isabella Rossi    | Ketahanan    | Rindu melanda      | M. Adib Zata Ilmam, M.Sc.| Ketahanan  | Lalu Moh. Nazar Fajri, MAP | Pahrizal Iqrom, MAP    |
| 33  | 2021033 | Khaled Mahmoud    | Tata Kelola  | Hujan deras        | Hamdi, MAP             | Politik      | Lalu Moh. Nazar Fajri, MAP | Muh. Sahli, MAP        |
| 34  | 2021034 | Leila Rahman      | Pemerintahan | Mata tertutup      | Pahrizal Iqrom, MAP    | Pemerintahan | M. Adib Zata Ilmam, M.Sc. | Hapipi Jayadi, MAP      |
| 35  | 2021035 | Marco Esposito    | Politik      | Jalan berliku      | Hamdi, MAP             | Politik      | M. Nasuhi, MAP           | Lalu Moh. Nazar Fajri, MAP |
| 36  | 2021036 | Natalia Rodriguez | Kebijakan    | Suara nyaring      | Lalu Moh. Nazar Fajri, MAP | Kebijakan | M. Nasuhi, MAP           | Reni Anggriani, MH      |
| 37  | 2021037 | Amir Khan         | Sosial       | Asa menyala        | Natila Rizka Safitri, M.Si | Sosial     | M. Nasuhi, MAP           | Lalu Moh. Nazar Fajri, MAP |
| 38  | 2021038 | Fiona Campbell    | Pemberdayaan | Pelangi tercipta   | Hamdi, MAP             | Politik      | M. Nasuhi, MAP           | H. Lalu Hidir, MH       |
| 39  | 2021039 | Chen Wei          | Hukum        | Bunga berkembang   | H. Lalu Hidir, MH      | Hukum        | Lalu Moh. Nazar Fajri, MAP | Muh. Sahli, MAP        |
