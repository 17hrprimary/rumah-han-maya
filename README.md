# Rumah Han & Maya

Rumah 3D (three.js) dengan teras, ruang tamu, dapur, tiga kamar (Han, Maya, Nayla & Alya), taman, pantai di belakang rumah, dan kucing Mochi.

- **PC**: klik lantai = Han jalan ke situ, klik kursi/sofa = Han duduk, klik nama = kamera ikutin, drag = putar, scroll = zoom.
- **HP**: tap lantai/kursi/nama, geser satu jari = putar, cubit = zoom, dua jari = geser.
- Tombol bawah: lompat ke tiap ruangan, 🌤️ Langit (kamera rendah buat lihat langit & awan), 🕐 Jam asli (langit ikut jam WITA), siang/malam manual, mode dinding (potong / penuh / + atap), kredit.
- Langit realtime: warna langit, matahari, bulan, bintang, cahaya, dan lampu rumah ikut jam WITA (UTC+8, Maros) dengan transisi halus. Pagi/siang/sore/malam. Ada awan yang pelan-pelan bergerak.
- Animasi: Idle/Walk/Sit/Wave tambahan dari Rocketbox (`models/anim-*.glb`), crossfade halus; Maya pakai animasi napas, jalan, dan duduk kursi asli.

- **Furnitur solid + A\***: semua benda (dinding, kusen, furnitur, pagar, pohon, semak) otomatis jadi rintangan di grid 10 cm dengan peta jarak bebas. Karakter dan Mochi cari jalan pakai A* (8 arah, lebih suka lewat tengah lorong), lalu jalurnya dirapikan (tarik tali) selama garisnya tetap aman. Tikungan cuma dipotong kalau nggak nyerempet apa pun.
- **Antar karakter nggak saling tembus**: tiap orang punya radius badan. Yang lagi diam/duduk dianggap rintangan dan dijalani memutar; kalau papasan di pintu, yang prioritasnya lebih rendah (Han > Maya > Nayla > Alya > Mochi) nunggu dulu. Mochi minggir kalau ngalangin jalan. Orang dewasa yang duduk telapak kakinya napak lantai.
- **🏖️ Pantai**: lewat dua gapura "Ke Pantai" di pagar belakang (kiri & kanan rumah). Pasir, pasir basah, laut dengan ombak bergerak ke arah pantai (shader gelombang + buih di puncak ombak pecah), air naik-turun di bibir pantai, pohon kelapa, dua payung, empat kursi pantai (tinggi dudukan sama kayak kursi teras, jadi duduk proper & kaki napak), istana pasir, kerang, bintang laut, batu karang, tali pembatas, dan lampu pantai yang nyala pas malam. Karakter & Mochi jalan ke sana pakai A* (siang aja; malam mereka di dalam). Laut = rintangan, jadi Han di mode POV berhenti di bibir air. Tombol 🏖️ Pantai di bar bawah buat lihat pantainya.
- **🎮 POV Han**: tombol pertama di bar bawah. Jalan sendiri jadi Han, dilihat dari mata Han (atau 🧍 dari belakang). PC: WASD jalan, ←→ / Q E / drag mouse lihat sekeliling, Shift lari, V ganti mata/belakang, Esc keluar. HP: stick kiri jalan, geser layar lihat sekeliling, tombol 👁️ / 🏃 / ✕ di kanan bawah. Tabrakan pakai peta jarak bebas yang sama dengan A* plus radius badan orang lain & Mochi (geser per 3 cm, meluncur di sepanjang dinding), jadi nggak nembus apa pun. Kalau Han lagi duduk, dia berdiri dulu. Tap nama orang lain waktu POV = dia nyapa.

Karakter (Maya, Han, Nayla, Alya) memakai label nama CSS2D. Maya memakai perbaikan emissive yang sama dengan web kantor (emissiveMap = tekstur warna, intensitas 0.12 siang, naik 0.48 waktu malam).

## Kredit

- **Maya**: avatar "Female_Adult_03", warna dan tekstur dimodifikasi (model yang sama dengan web kantor).
- **Han**: avatar "Sports_Male_04"; lengan, bahu, dada, leher, dan kaki dibikin lebih kekar.
- **Nayla**: "Female_Child_01" · **Alya**: "Female_Child_02".
- Animasi diam, jalan, dan duduk di-retarget ke tiap karakter.

Semua karakter dan animasi dari [Microsoft Rocketbox Avatar Library](https://github.com/microsoft/Microsoft-Rocketbox), © 2020 Microsoft, lisensi MIT (salinan: `models/LICENSE-Microsoft-Rocketbox.md`).

Kucing Mochi: berdasarkan ["animated bengal cat"](https://sketchfab.com/3d-models/animated-bengal-cat-30444a1c97e9411693023c75403b38d8) karya [dinomaster](https://sketchfab.com/dinomaster), lisensi [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/). Bulu diwarnai ulang jadi oranye dan animasinya dirapikan (`models/mochi.glb`).

Rumah, perabot, langit, dan awan dibikin langsung pakai kode. Mesin 3D: [three.js](https://threejs.org) (MIT).
