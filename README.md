# Rumah Han & Maya

Rumah 3D (three.js) dengan teras, ruang tamu, dapur, tiga kamar (Han, Maya, Nayla & Alya), taman, dan kucing Mochi.

- **PC**: klik lantai = Han jalan ke situ, klik kursi/sofa = Han duduk, klik nama = kamera ikutin, drag = putar, scroll = zoom.
- **HP**: tap lantai/kursi/nama, geser satu jari = putar, cubit = zoom, dua jari = geser.
- Tombol bawah: lompat ke tiap ruangan, siang/malam, mode dinding (potong / penuh / + atap), kredit.

Karakter (Maya, Han, Nayla, Alya) memakai label nama CSS2D. Maya memakai perbaikan emissive yang sama dengan web kantor (emissiveMap = tekstur warna, intensitas 0.12 siang, naik 0.48 waktu malam).

## Kredit

- **Maya**: avatar "Female_Adult_03", warna dan tekstur dimodifikasi (model yang sama dengan web kantor).
- **Han**: avatar "Sports_Male_04"; lengan, bahu, dada, leher, dan kaki dibikin lebih kekar.
- **Nayla**: "Female_Child_01" · **Alya**: "Female_Child_02".
- Animasi diam, jalan, dan duduk di-retarget ke tiap karakter.

Semua karakter dan animasi dari [Microsoft Rocketbox Avatar Library](https://github.com/microsoft/Microsoft-Rocketbox), © 2020 Microsoft, lisensi MIT (salinan: `models/LICENSE-Microsoft-Rocketbox.md`).

Rumah, perabot, dan kucing dibikin langsung pakai kode. Mesin 3D: [three.js](https://threejs.org) (MIT).
