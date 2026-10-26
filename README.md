# UTS Graf Sains Data: Rekomendasi RetailRocket dengan Neo4j

Nama / NIM: Hana Maftuha / 24031554066 | Matakuliah: Graf Sains Data 

Proyek ini membangun graf interaksi e-commerce dari dataset RetailRocket di Neo4j, lalu menghitung similarity antar-visitor dan membuat rekomendasi item dengan KNN berbasis user. Data dibagi menjadi dua periode, yaitu P1 (16-30 Juni 2015) sebagai data training dan P2 (01-18 September 2015) sebagai data testing. Hanya P1 yang diimpor ke Neo4j, sedangkan P2 dipakai untuk evaluasi.

Graf terdiri dari simpul Visitor dan Item yang dihubungkan oleh relasi VIEWED, ADDED_TO_CART, dan BOUGHT. Interaksi diubah menjadi matriks User x Item dengan bobot 1, 3, dan 5, lalu dihitung cosine similarity pada proyeksi User-User. Rekomendasi dibuat dengan KNN (k = 5) untuk satu user acak (seed 42), dan hasilnya dievaluasi dengan Hit@5 dan NDCG@5. Hasil similarity dan rekomendasi juga disimpan kembali ke graf sebagai relasi SIMILAR_TO, KNN_NEIGHBOR, dan RECOMMENDED.
