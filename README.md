# ChessFPS

Konsep game yang menggabungkan permainan catur dengan duel orang pertama. Pemain tetap bermain catur di papan; ketika sebuah bidak akan memakan bidak lawan dalam mode FPS, permainan berpindah ke arena duel. Pemenang duel mengambil petak dan bidak yang kalah dihilangkan dari papan.

## Mode permainan

### Catur Klasik

- Mengikuti aturan catur standar: gerakan bidak, giliran, skak, skakmat, rokade, en passant, promosi pion, dan remis.
- Tidak ada duel. Bidak yang dimakan langsung dikeluarkan dari papan.

### Catur FPS

- Pemain memilih langkah catur yang sah.
- Jika langkah tersebut memakan bidak, permainan masuk ke duel 1 lawan 1 antara kedua bidak.
- Duel dapat memakai tangan kosong atau perlengkapan/senjata sesuai aturan pertandingan.
- Bidak pemenang tetap hidup dan menempati petak tujuan; bidak yang kalah dihilangkan.
- Jika penyerang kalah, langkah makan dibatalkan dan bidak tetap di petak asal.
- Jika raja kalah dalam duel, pemain tersebut kalah. Aturan kemenangan akhir dapat disetel agar tetap memakai skakmat atau memakai eliminasi raja.

## Multiplayer

- Sasaran awal adalah dua pemain pada satu perangkat (hot-seat), agar aturan catur dan duel dapat dimainkan tanpa layanan jaringan.
- Multiplayer online dapat ditambahkan setelah versi dasar stabil. Permainan online memerlukan sinkronisasi giliran, pencocokan pemain atau kode ruang, validasi langkah di sisi server, serta penanganan koneksi terputus.
- Opsi pertandingan yang direncanakan: catur klasik/FPS, durasi giliran, jenis duel, dan arena.

## Alur satu giliran di mode FPS

1. Pemain memilih bidak dan petak tujuan yang sah.
2. Untuk langkah biasa, bidak berpindah dan giliran berganti.
3. Untuk langkah makan, kedua bidak dipindahkan ke arena duel.
4. Hasil duel menentukan bidak yang bertahan.
5. Papan diperbarui, kondisi menang/remis diperiksa, lalu giliran berganti.

## Kebutuhan pengembangan

### Perangkat dan alat

- Komputer pengembangan yang mampu menjalankan game engine dan editor 3D.
- Game engine. **Unity dengan C# direkomendasikan untuk prototipe awal** karena mendukung pembuatan papan, kontrol FPS, animasi, UI, serta multiplayer melalui ekosistem yang luas. Unreal Engine dengan Blueprint/C++ juga bisa dipakai jika proyek mengutamakan visual 3D yang lebih berat.
- Git untuk version control dan pencadangan perubahan.
- Blender atau alat sejenis untuk membuat/mengubah model bidak dan arena jika aset siap pakai tidak digunakan.

### Sistem game

- Logika aturan catur yang dapat memvalidasi semua langkah dan kondisi permainan.
- Tampilan papan dan bidak, pemilihan bidak, penanda langkah sah, serta informasi giliran.
- Arena duel FPS, kamera orang pertama, kontrol gerak, serangan, pertahanan, dan kondisi menang/kalah duel.
- Penghubung antara hasil duel dan keadaan papan agar bidak serta giliran selalu diperbarui dengan benar.
- Menu utama, pilihan mode, pengaturan pertandingan, jeda, dan layar hasil.
- Aset visual dan audio: model bidak, arena, tangan/senjata, animasi, efek, musik, dan suara. Aset placeholder cukup untuk prototipe.
- Untuk online: backend atau layanan jaringan, identitas/lobby, sinkronisasi state, dan pengujian latensi.

## Rencana pengerjaan

1. Tetapkan platform target dan engine.
2. Buat prototipe papan 2D/3D dengan aturan catur dan mode klasik.
3. Tambahkan arena duel FPS sederhana dengan placeholder.
4. Hubungkan duel ke aksi makan dan pastikan aturan papan tetap konsisten.
5. Tambahkan jenis duel, senjata/perlengkapan, animasi, UI, dan audio.
6. Poles keseimbangan, aksesibilitas, performa, dan pengalaman bermain.
7. Tambahkan multiplayer online sebagai tahap lanjutan jika dibutuhkan.

## Status

Dokumen ini adalah rancangan awal. Engine, platform rilis (PC, web, atau lainnya), gaya visual, skema kontrol, dan aturan duel masih perlu ditetapkan sebelum implementasi. Untuk versi pertama, rekomendasi engine di atas menjadi asumsi awal sampai kebutuhan platform dipastikan.

## Kontribusi

Sebelum mengubah kode atau aset, buat branch Git. Sertakan ringkasan perubahan dan cara memeriksa hasilnya pada pull request.
