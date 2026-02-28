# Rencana Pemanfaatan Codex 7 Hari

Dokumen ini membantu memulai penggunaan Codex secara praktis untuk alur kerja harian developer.

## Tujuan utama
- Mengurangi waktu implementasi fitur.
- Mempercepat debugging dan penulisan test.
- Membuat workflow coding lebih konsisten.

## Hari 1 — Setup fondasi kerja
**Fokus:** menyiapkan konteks project agar hasil Codex relevan.

Checklist:
- Rapikan `README.md`: cara run, test, struktur folder.
- Buat daftar command standar (misalnya build, lint, test).
- Siapkan template prompt untuk task umum:
  - "Bantu implement endpoint X"
  - "Analisis error Y dan beri akar masalah"
  - "Refactor modul Z tanpa ubah perilaku"

Output hari ini:
- 1 halaman dokumentasi setup.
- 3 prompt template siap pakai.

## Hari 2 — Implementasi fitur kecil end-to-end
**Fokus:** pakai Codex untuk menyelesaikan 1 task kecil penuh.

Checklist:
- Pilih fitur kecil (scope 1–3 file).
- Minta Codex usulkan rencana implementasi sebelum menulis kode.
- Implementasi bertahap: model/data -> logic -> handler/UI.
- Review manual hasil diff sebelum commit.

Output hari ini:
- 1 fitur kecil selesai.
- Catatan "bagian mana yang paling terbantu".

## Hari 3 — Debugging terstruktur
**Fokus:** gunakan Codex sebagai partner investigasi bug.

Checklist:
- Ambil 1 bug nyata dari backlog.
- Beri Codex log error + langkah reproduksi + ekspektasi.
- Minta hipotesis penyebab (minimal 3 kemungkinan).
- Validasi per hipotesis sampai dapat root cause.
- Terapkan fix + test regresi.

Output hari ini:
- 1 bug terselesaikan.
- Dokumentasi pola debugging yang efektif.

## Hari 4 — Testing acceleration
**Fokus:** mempercepat coverage test dengan bantuan Codex.

Checklist:
- Pilih 1 modul yang belum punya test memadai.
- Minta Codex identifikasi skenario utama + edge cases.
- Generate unit/integration test.
- Jalankan test, revisi assertion yang terlalu longgar.

Output hari ini:
- Penambahan test untuk modul prioritas.
- Daftar edge case yang sebelumnya belum tertangkap.

## Hari 5 — Refactor aman
**Fokus:** merapikan kode lama tanpa mengubah perilaku.

Checklist:
- Pilih file/komponen yang sulit dibaca.
- Minta Codex usulkan opsi refactor bertahap.
- Lakukan perubahan kecil, commit per langkah logis.
- Jalankan test tiap langkah.

Output hari ini:
- 1 area kode lebih rapi dan mudah dirawat.
- Catatan prinsip refactor yang dipakai tim.

## Hari 6 — Otomasi workflow
**Fokus:** mengurangi tugas berulang dengan script.

Checklist:
- Identifikasi 1–2 aktivitas repetitif (mis. setup env, generate file, check kualitas).
- Minta Codex membuat script otomasi.
- Tambahkan command ke dokumentasi proyek.
- Uji script pada environment bersih.

Output hari ini:
- Script otomasi yang dipakai harian.
- Pengurangan waktu untuk task repetitif.

## Hari 7 — Evaluasi dan standardisasi
**Fokus:** menjadikan penggunaan Codex sebagai kebiasaan tim.

Checklist:
- Evaluasi metrik sederhana:
  - waktu implementasi,
  - jumlah bug yang terselesaikan,
  - waktu review.
- Simpan prompt-prompt terbaik sebagai "playbook".
- Tetapkan aturan quality gate:
  - wajib lint/test,
  - wajib review manual sebelum merge.

Output hari ini:
- Playbook internal penggunaan Codex.
- SOP mini untuk kolaborasi manusia + AI.

## Template prompt siap pakai

### 1) Implementasi fitur
"Bantu implement [fitur] di [file/modul].
Konteks: [aturan bisnis].
Batasan: [library/arsitektur].
Minta rencana dulu, lalu patch bertahap + test yang relevan."

### 2) Debugging
"Saya dapat error: [pesan error].
Langkah reproduksi: [langkah].
Ekspektasi: [hasil].
Tolong beri 3 hipotesis root cause paling mungkin, cara validasi, lalu usulan fix minimal."

### 3) Refactor
"Refactor kode ini agar lebih mudah dibaca tanpa ubah perilaku.
Tolong jelaskan risiko, buat perubahan kecil, dan sertakan test/regression check."

### 4) Code review
"Review patch ini dari sisi bug risk, performa, security, dan maintainability.
Prioritaskan temuan berdasarkan dampak + effort perbaikan."

## Metrik sederhana yang bisa dipantau mingguan
- Rata-rata waktu penyelesaian task kecil.
- Jumlah bug yang tertangkap sebelum release.
- Persentase task yang disertai test.
- Waktu dari coding sampai PR siap review.

## Prinsip penting
- Codex mempercepat, tetapi keputusan akhir tetap di developer.
- Selalu verifikasi output dengan test dan review manual.
- Hindari copy-paste buta untuk area kritis (auth, pembayaran, data sensitif).
