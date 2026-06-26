# Laporan SEO Readiness - Bakpia Malino

Production URL: https://bakpiamalino.dekatlokal.com/

## Audit Singkat Kondisi Awal
- Project static HTML dengan homepage di `index.html`.
- Title dan meta description masih umum, belum memakai URL production final.
- Belum ada canonical, robots meta eksplisit, Open Graph, Twitter Card, dan JSON-LD.
- Belum ada `robots.txt` dan `sitemap.xml`.
- Produk, harga, gambar, alamat, WhatsApp, Instagram, dan email sudah tampil di HTML awal.
- FAQ tidak terlihat di halaman, sehingga FAQ schema tidak ditambahkan agar tidak mismatch.
- Google Maps dan jam operasional belum tersedia sebagai data valid.

## File yang Diubah
- `index.html`
- `robots.txt`
- `sitemap.xml`
- `seo-report.md`
- `favicon.ico`
- `favicon-48x48.png`
- `favicon-192x192.png`
- `apple-touch-icon.png`

## Perbaikan yang Sudah Dieksekusi
- Title production: `Bakpia Malino | Bakpia Aneka Rasa Khas Gowa Makassar - DekatLokal`.
- Meta description unik 144 karakter dengan brand, produk, lokasi, value proposition, dan CTA halus.
- Favicon production ditambahkan untuk tab browser dan Search appearance: `favicon.ico`, `favicon-48x48.png`, `favicon-192x192.png`, dan `apple-touch-icon.png`.
- Canonical absolute ke `https://bakpiamalino.dekatlokal.com/`.
- Robots meta `index, follow` dengan preview snippet/image/video yang aman untuk Google.
- Open Graph dan Twitter Card lengkap dengan URL dan image production.
- JSON-LD valid untuk `WebSite`, `WebPage`, `Bakery`/LocalBusiness, `OfferCatalog`, `Product`, `Offer`, dan `BreadcrumbList`.
- Product snippets readiness untuk 6 produk yang terlihat di halaman: Markisa, Coklat, Ubi Ungu, Keju, Kacang Hijau, dan Mix.
- Merchant listing readiness dasar disiapkan karena harga dan availability tampil konsisten, tetapi transaksi masih via WhatsApp.
- Product heading diperkuat menjadi `h3` tanpa mengubah layout.
- Alt text gambar dibuat lebih deskriptif dengan brand, produk, dan lokasi.
- Gambar penting diberi width/height; gambar bawah fold diberi `loading="lazy"` dan `decoding="async"`.
- CTA WhatsApp memakai `wa.me`, nomor internasional, pesan encoded, dan menyebut website DekatLokal.
- `robots.txt` mengizinkan crawling halaman publik dan menautkan sitemap production.
- `sitemap.xml` memakai URL canonical production dan image sitemap untuk hero serta produk utama.

## Checklist Google Search Console Pasca-Deploy
1. Buka `https://bakpiamalino.dekatlokal.com/` dan pastikan status 200.
2. Buka `https://bakpiamalino.dekatlokal.com/robots.txt`.
3. Buka `https://bakpiamalino.dekatlokal.com/sitemap.xml`.
4. View source homepage dan cek title, meta description, canonical, robots meta, OG, Twitter Card, dan JSON-LD.
5. Uji JSON-LD dengan Rich Results Test dan Schema Markup Validator.
6. Daftarkan Domain Property `dekatlokal.com` di Google Search Console.
7. Opsional: tambah URL-prefix property `https://bakpiamalino.dekatlokal.com/` untuk monitoring UMKM ini.
8. Submit sitemap: `https://bakpiamalino.dekatlokal.com/sitemap.xml`.
9. Jalankan URL Inspection untuk homepage.
10. Jalankan Live Test dan Request Indexing jika live test valid.
11. Pantau Page Indexing: indexed, discovered/crawled not indexed, duplicate canonical, blocked robots, noindex, 404, dan 5xx.
12. Pantau Enhancements: Product snippets, Merchant listings jika eligible, Breadcrumbs, dan structured data lainnya.
13. Pantau Experience dan Core Web Vitals setelah data tersedia.
14. Pantau Performance: queries, pages, countries, devices, CTR, impressions, dan average position.
15. Jika impression tinggi tapi CTR rendah, revisi title/meta description berdasarkan query nyata.
16. Jika local query rendah, tambah konten pendukung di halaman atau direktori DekatLokal dengan anchor "Bakpia Malino bakpia aneka rasa khas Malino Gowa".

## Instruksi Manual Tim DekatLokal
- Pastikan Vercel deploy memakai folder `bakpia-malino` sebagai root static site atau memastikan file `index.html`, `robots.txt`, dan `sitemap.xml` berada di root deployment.
- Tambahkan backlink internal dari direktori Teman Lokal di `dekatlokal.com` menuju `https://bakpiamalino.dekatlokal.com/` dengan anchor deskriptif.
- Jika UMKM punya Google Business Profile, tambahkan website URL ini dan samakan NAP: Bakpia Malino, Kel. Bonto Lerung Kec. Tinggimoncong Kab. Gowa, +62 852-6121-4130.
- Tambahkan link Google Maps dan jam operasional ke halaman jika datanya sudah valid.
- Jika ada sertifikat Halal/P-IRT/NIB resmi, simpan nomor sertifikat yang valid sebelum ditampilkan atau dimasukkan ke schema.

## Risiko/Data Belum Tersedia
- Status 200, HTTPS, canonical pilihan Google, dan akses `robots.txt`/`sitemap.xml` perlu diverifikasi setelah deploy production aktif.
- Google Maps URL dan jam operasional belum tersedia, sehingga tidak dipaksakan ke UI/schema.
- FAQ schema tidak ditambahkan karena FAQ tidak tampil di halaman.
- Beberapa PNG produk berukuran sekitar 2.1-2.7 MB; disarankan membuat versi WebP/AVIF terkompresi setelah desain final dikunci.
- File `video_test.html` tidak dimasukkan sitemap dan diblokir di `robots.txt` karena bersifat halaman preview/test.
