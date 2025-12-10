# Panduan Kontribusi

Terima kasih telah tertarik untuk berkontribusi pada Sistem Manajemen Koperasi! Berikut adalah panduan untuk berkontribusi.

## Cara Berkontribusi

### 1. Fork Repository

Fork repository ini ke akun GitHub Anda dengan mengklik tombol "Fork" di halaman repository.

### 2. Clone Repository Anda

```bash
git clone https://github.com/Indra77ya/koperasi.git
cd koperasi
```

### 3. Buat Branch Baru

```bash
git checkout -b fitur/nama-fitur-anda
# atau untuk bug fix
git checkout -b bugfix/deskripsi-bug
```

### 4. Lakukan Perubahan

- Lakukan perubahan pada kode
- Pastikan kode Anda mengikuti standar yang ada
- Test perubahan Anda secara menyeluruh

### 5. Commit Perubahan

```bash
git add .
git commit -m "Deskripsi singkat perubahan"
```

Gunakan pesan commit yang jelas dan deskriptif:
- ✅ Good: `Tambah fitur validasi email untuk anggota baru`
- ❌ Bad: `Fix bug` atau `Update file`

### 6. Push ke Repository Anda

```bash
git push origin fitur/nama-fitur-anda
```

### 7. Buat Pull Request

1. Buka repository Anda di GitHub
2. Klik tombol "Compare & pull request"
3. Isi deskripsi pull request secara detail
4. Klik "Create Pull Request"

## Standar Kode

### PHP

- Ikuti PSR-2 coding standard
- Gunakan indentasi 4 spaces
- Tambahkan comment untuk logika kompleks
- Gunakan meaningful variable names

### JavaScript

- Gunakan indentasi 4 spaces
- Hindari global variables
- Gunakan `const` atau `let`, bukan `var`
- Tambahkan JSDoc comments untuk functions

### HTML/CSS

- Gunakan semantic HTML
- Organise CSS dengan baik
- Gunakan kebab-case untuk class names
- Responsive design adalah requirement

## Testing

Sebelum submit pull request:

1. Test secara manual di browser
2. Test di berbagai browser (Chrome, Firefox, Safari, Edge)
3. Test di mobile dan desktop
4. Pastikan tidak ada error di console

## Laporan Bug

Jika menemukan bug:

1. Buka issue baru
2. Gunakan template berikut:

```markdown
## Deskripsi Bug
[Jelaskan bug tersebut]

## Langkah Reproduksi
1. [Langkah 1]
2. [Langkah 2]
3. [Langkah 3]

## Expected Behavior
[Yang seharusnya terjadi]

## Actual Behavior
[Yang terjadi sebenarnya]

## Environment
- Browser: [Chrome/Firefox/etc]
- OS: [Windows/Mac/Linux]
- Versi PHP: [versi]
```

## Request Fitur

Untuk request fitur baru:

1. Buka issue dengan label "enhancement"
2. Jelaskan fitur yang diinginkan
3. Jelaskan use case dan benefit
4. Berikan contoh atau screenshot jika memungkinkan

## Kode Etik

- Bersikap profesional dan ramah
- Hormati pendapat developer lain
- Hindari harassment atau diskriminasi
- Fokus pada improvement kode

## Pertanyaan?

Jika ada pertanyaan, silakan buka discussion atau hubungi maintainer.

Terima kasih telah berkontribusi! 🎉
