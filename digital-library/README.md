# AICHEATCODE Digital Library — Tingkatan 1

Aplikasi pendidikan statik tanpa backend. Fail `index.html` mengandungi HTML, CSS, JavaScript dan data pengenalan bagi **11 mata pelajaran**.

## Ciri pengguna
- Carian dan navigasi 11 mata pelajaran.
- Nota ringkas, kad imbasan dan kuiz bersemakan bagi setiap subjek.
- 2 topik dan 2 soalan permulaan per subjek (**bukan bank soalan lengkap**).
- Prompt AI boleh salin dan sunting.
- Baca PDF dipilih daripada peranti (hanya sesi semasa).
- Pautan PDF HTTPS boleh disimpan pada peranti sendiri. Ia **bukan CMS penerbitan awam**.
- Rekod skor disimpan dalam `localStorage` apabila dibenarkan.
- Diagnostik struktur data dan butang padam skor setempat.

## Cara guna tanpa pemasangan
1. Buka `index.html` dalam browser (jika fail telah disimpan di komputer).
2. Untuk Google Sites: **Insert → Embed → Embed code**, tampal keseluruhan kod `index.html`, tekan **Next → Insert → Publish**. Perbesarkan ruang embed sehingga kandungan tidak terpotong.
3. Alternatif hosting statik: letakkan `index.html` sebagai fail indeks pada Netlify/GitHub Pages; untuk repo ini, direktori projek ialah `digital-library/`.
4. Untuk PDF terbuka kepada semua pengguna, hoskan fail **hanya selepas izin pemilik hak cipta**, kemudian masukkan pautan HTTPS yang diluluskan ke dalam kod. **Pautan yang diisi pengguna pada antaramuka tidak menjadi tetapan awam.**

Rujukan Google Sites rasmi: https://support.google.com/sites/answer/90569

## QA dalaman (9 November 2026)
**Disahkan melalui semakan data/simulasi DOM (bukan browser sebenar):**
- Kod JavaScript berjaya dihuraikan tanpa ralat sintaks.
- Bilangan subjek 11, unik; setiap subjek mempunyai dua nota, dua kad dan dua soalan.
- Semua kuiz mempunyai empat pilihan unik dan jawapan yang sah.
- Render nota, flip kad, input kuiz, peralihan soalan, skor 100% serta penyimpanan skor dalam storan mock.
- PDF belum dipilih: mesej ralat yang jelas.
- URL bukan HTTPS ditolak; URL HTTPS diterima dalam ujian mock.
- Prompt boleh disunting.
- Diagnostik memaparkan 6/6 semakan asas.
- Carian subjek menapis paparan.

**Belum diuji:**
- Peranti Android/iOS fizikal; Safari/Firefox/Edge; Google Sites embed diterbitkan; pembaca PDF sebenar; rangkaian lambat; WCAG automatik/manual; pengujian penetrasi; beban trafik; kebolehcapaian pelayan selepas diterbitkan.

## Perubahan kurikulum 2027
KPM menyatakan Kurikulum Persekolahan 2027 dijadual bermula bagi Tingkatan 1 pada tahun 2027. Kandungan prototaip ini berpandukan buku KSSM yang dimuat naik dan **belum dipetakan kepada kurikulum 2027**. Sumber KPM: https://www.moe.gov.my/index.php/kurikulum-persekolahan-2027

## Sekatan keluaran awam
- Buku PDF asal tidak disertakan kerana terma hak cipta dalam buku yang dimuat naik. Dapatkan izin pengedaran atau pautan rasmi KPM yang membenarkan pengguna membaca.
- Kandungan semasa ialah nota dan soalan pengenalan, **bukan liputan lengkap KSSM**. Perlu semakan kandungan guru mengikut dokumen kurikulum semasa sebelum projek dikategorikan siap untuk sekolah.
- Tiada akaun pengguna, dashboard guru berbilang peranti, backend, pentadbir dengan login atau penyelarasan data; penggunaan data pelajar ialah setempat sahaja.
- Bukan laman rasmi atau produk yang diluluskan KPM.

## Matriks ujian pra-produksi yang perlu dilaksanakan pada laman diterbitkan
| Kes | Ujian | Kriteria |
|---|---|---|
| P01 | Muat laman dalam Chrome Android, Safari iOS, Edge Windows | Tiada ralat konsol atau skrol mendatar |
| P02 | Cari setiap subjek | Tepat dan jelas apabila tiada hasil |
| P03 | Navigasi dengan Tab, Enter, Space dan pembaca skrin | Semua kawalan boleh dicapai |
| P04 | Tukar 11 subjek dan 6 tab | Tidak hilang data, tidak pecah susun atur |
| P05 | Flip kad depan/belakang | Paparan jawapan betul |
| P06 | Kuiz satu jawapan tepat, satu salah, kemudian ulang | Markah dan pembetulan betul |
| P07 | Tutup dan buka semula | Skor kekal jika storan dibenarkan |
| P08 | Private browsing / localStorage disekat | Aplikasi tidak crash |
| P09 | PDF yang benar, PDF palsu/rosak dan fail besar | Mesej sesuai, tiada crash |
| P10 | PDF HTTPS dibenarkan/403/404/disekat iframe | Buka tab baharu sebagai alternatif |
| P11 | Google Sites selepas Publish | Iframe, copy dan navigasi berfungsi |
| P12 | 320px, 375px, 768px, desktop, pembesaran 200% | Tiada elemen bertindih / tersembunyi |
| P13 | Audit Lighthouse dan axe, manual screen reader | Selesaikan isu sebelum dakwa WCAG |
| P14 | Semak hak cipta setiap PDF dan semakan guru terhadap semua nota | Ada rekod kelulusan |
| P15 | Sahkan caching/CDN serta servis hosting | Monitor uptime dan 404/5xx |
| P16 | Respons insiden kebocoran atau serangan | SOP, pemilik tugasan dan pemulihan disahkan |

## Penyelenggaraan
Semak pautan PDF setiap minggu setelah ia dipasang dalam laman awam; pantau 404/403, prestasi halaman, pembetulan nota dan aduan pengguna melalui proses yang dikendalikan oleh pemilik laman. Jangan letak API key atau kata laluan dalam HTML atau JavaScript di pelayar.

## Sumber kurikulum yang digunakan untuk prototaip
Isi kandungan buku Tingkatan 1 yang dimuat naik: Matematik, Science DLP, Bahasa Melayu, Sejarah, Asas Sains Komputer, Pendidikan Islam, Pendidikan Moral, Pendidikan Jasmani dan Kesihatan, Pendidikan Seni Visual, Pendidikan Muzik dan Waspada Budaya Kita. Pelajaran contoh dihuraikan menggunakan konsep asas umum; **tidak semua bab telah disemak penuh**.

MYDS Accessibility: https://design.digital.gov.my/en/docs/develop/accessibility
