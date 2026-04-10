# StrukturData-Q1-2501010076-Budiarta-C

## 1. Kenapa Array Cepat 
Bayangkan Array itu seperti perumahan townhouse. Rumah-rumahnya berurutan (kontinu) dan punya nomor yang pasti. Kalau kamu mau ke rumah nomor 5, kamu bisa langsung lari ke sana karena tahu persis lokasinya. Komputer tinggal hitung jaraknya, makanya instan (O(1)).Sedangkan Linked List itu seperti permainan mencari jejak (scavenger hunt). Rumah-rumahnya mencar (non-kontinu). Untuk sampai ke rumah ke-5, kamu harus ke rumah ke-1 dulu buat nanya alamat rumah ke-2, lalu ke rumah ke-2 buat nanya alamat rumah ke-3, dan seterusnya. Karena harus mampir satu-satu, jadinya lama (O(n)).

## 2. Kapan Linked List Menang lawan Array?
Linked List jago banget kalau kita sering tambah atau hapus data di tengah atau di depan.
  -Teorinya: Kalau di Array, pas kamu hapus data di tengah, data di belakangnya harus "geser" semua biar nggak ada lubang. Capek, kan?
  -Solusi: Di Linked List, nggak ada geser-geseran. Kamu tinggal "putus tali" dari satu data dan "sambungin" ke data lainnya. Beres! Nggak perlu peduli seberapa banyak data di belakangnya.

## 3. Apa itu Doubly Linked List?
Anggap saja ini Linked List yang lebih canggih.
  -Anatomi: Kalau Linked List biasa cuma punya satu tangan (nunjuk ke depan), Doubly Linked List punya dua tangan (satu nunjuk ke depan/next, satu lagi nunjuk ke belakang/prev).

  -Efeknya: Memori jadi sedikit lebih boros (karena harus simpan satu alamat tambahan). Tapi, untungnya kita jadi fleksibel. Kita bisa jalan maju, bisa juga jalan mundur. Kalau di Linked List biasa, kalau sudah kelewat satu data, kamu nggak bisa balik lagi kecuali mulai dari awal.

## 4. Circular Linked List itu Apa?
Bedanya cuma satu: nggak ada ujungnya. Kalau di Linked List biasa data terakhir bakal nunjuk ke "kosong" (NULL), di Circular, data terakhir bakal nunjuk balik lagi ke data pertama. Jadi muter terus kayak lingkaran.
  -Skenario nyata: Sistem ganti-gantian (Round Robin). Contohnya, kalau kamu lagi dengerin lagu di playlist terus kamu nyalain fitur repeat all. Pas lagu terakhir habis, dia otomatis balik lagi ke lagu pertama.

## 5. Apa yang Terjadi di Balik Layar list.append Python?
Python itu pintar. Dia pakai Dynamic Array.

1.Awalnya dia kasih kamu "kamar" kosong yang jumlahnya terbatas (misal 4 slot).

2.Pas kamu isi terus sampai penuh dan mau nambah lagi (misal data ke-5), Python bakal panik dikit, terus dia sewa gedung baru yang ukurannya jauh lebih besar (biasanya hampir 2x lipat).

3.Dia pindahin (copy) semua data lama ke gedung baru, baru deh data baru kamu dimasukkan.

4.Gedung lama yang kekecilan tadi dibuang.
