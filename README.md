Topic : Pediatrik Acute Myeloid Leukemia
Tools: GEO, GEO2R, R (R/Rstudio), GO (g:profiler), KEGG
Ini adalah pembelajaran berbasis proyek (PBL) di OmicsLite tentang eksplorasi penjelasan dari satu jurnal tentang kasus pedaitrik leukemia mieloid akut

Langkah-Langkah Analisis GEO / GEO2R
Periksa jurnal yang akan kita eksplorasi
Periksa akses untuk GEO2R 
Setelah itu, periksa dataset (GSE2191), buka situs web analisis GEO2R
Di situs web analisis GEO2R, ​​kita dapat memfilter baris dan kemudian memberi nama, Pediatric AML "Sakit" dan Normal bone marrow sebagai "Sehat"
Periksa opsi analisis di taskbar (di bawah)
Pilih "Opsi", Biasanya secara default opsi sudah dipilih. Tetapi, terapkan "Disediakan oleh Pengirim" di kategori platform (Karena NCBI mungkin menghasilkan beberapa perubahan pada dataset) dan pilih "ya" untuk menerapkan limma.
image
Menjalankan data ("Reanalyze")
The Result
image
Kemudian, Anda dapat memilih visualisasi yang lebih baik, seperti plot heatmap dan diagram Venn, untuk DEG (Gen Ekspresi Diferensial)
Pilih "Unduh tabel", output akan menjadi "tsv"
Sebagai tantangan, Anda dapat mengkonversi data ekstensi .tsv menjadi .csv, kemudian mengkonversi dari data di Ms.Excel atau Anda dapat menggunakan basis data SQL. Tetapi dengan cara yang lebih mudah, Anda dapat menggunakan ChatGPT, untuk memfilter 20 gen sampel yang mengalami peningkatan dan penurunan ekspresi dalam dataset (dengan petunjuk)
Setelah mendapatkan 20 DEG yang mengalami penurunan ekspresi dan 20 DEG yang mengalami peningkatan ekspresi, Anda dapat menyalin "Gen Simbol". Biasanya, gen simbol memiliki dua atau lebih gen simbol dengan pembatas "//", Anda dapat menggunakan ChatGPT dengan perintah "Silakan, saring simbol "//" dalam data 20 DEG yang mengalami penurunan dan peningkatan ekspresi, setelah itu, buat data menjadi vertikal"
Langkah-Langkah Analisis GO (Gene Ontology)
Kunjungi GO (situs web g:Profiler atau DAVID) Tautan g:Profiler
Masukkan daftar gen setelah penyaringan dan buat data vertikal (formulir ChatGPT)
Jalankan analisis
Kunjungi GO-BP, GO-MP, GO-CC. Temukan "Respons imun bawaan", "Respons inflamasi", "Respons terhadap virus", "Proses apoptosis", dll.
Jelajahi analisis lain untuk membuat kesimpulan.Concept Workflow
Langkah-Langkah KEGG Pathway
Identifikasi jalur hasil dari pengayaan.
Kunjungi KEGG Mapper Link KEGG Mapper (Cari organisme Homo sapiens)
Masukkan DEG (satu per satu), misalnya pertama masukkan DEG yang mengalami penurunan ekspresi kemudian analisis, setelah itu masukkan DEG yang mengalami peningkatan ekspresi
Analisis output (“Jalur pensinyalan reseptor Toll-like – 5 gen ditemukan”, “Interaksi sitokin-reseptor sitokin – 7 gen ditemukan”, “Apoptosis – 3 gen ditemukan”), gabungkan dengan hasil dari GO.
Langkah-Langkah Interpretasi
Masukkan data visualisasi dari GEO2R (R/Rstudio)
Masukkan data daftar, seperti GO-BP, GO-MP, GO-CC.
Masukkan visualisasi data gen jalur.
Buat kesimpulan dengan visualisasi data tersebut.
