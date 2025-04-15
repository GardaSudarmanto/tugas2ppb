Berikut adalah isi `README.md` untuk proyek Flutter CRUD menggunakan Hive yang telah kamu buat:

---

# 📒 Hive CRUD Flutter App

Aplikasi Flutter sederhana untuk **menyimpan, mengedit, dan menghapus catatan (notes)** menggunakan **Hive**, database lokal NoSQL ringan dan cepat.

---

## 📦 Fitur Utama

- Tambah, ubah, dan hapus catatan (notes)
- Menyimpan data lokal menggunakan Hive
- UI yang sederhana dan intuitif
- Reactive UI dengan `ValueListenableBuilder`

---

## 🚀 Getting Started

### 1. Clone Repository

```bash
git clone https://github.com/username/hive_crud_flutter.git
cd hive_crud_flutter
```

### 2. Install Dependencies

```bash
flutter pub get
```

### 3. Generate Hive Adapter

```bash
flutter pub run build_runner build
```

### 4. Jalankan Aplikasi

```bash
flutter run
```

---

## 🧱 Struktur Proyek

```
lib/
├── main.dart           // Entry point dan inisialisasi Hive
├── models/
│   └── note.dart       // Model Hive dengan anotasi @HiveType
├── notes_page.dart     // UI utama aplikasi CRUD
```

---

## 📂 Model Hive

Model `Note` dibuat menggunakan Hive annotations dan terdiri dari:

```dart
@HiveType(typeId: 0)
class Note extends HiveObject {
  @HiveField(0)
  String title;

  @HiveField(1)
  String content;
}
```

Setelah membuat model, generate file `.g.dart` dengan:
```bash
flutter pub run build_runner build
```

---

## 🧠 Cara Kerja

- Hive digunakan untuk menyimpan data `Note` ke dalam box `notes`.
- Setiap perubahan data otomatis memicu rebuild UI karena menggunakan `ValueListenableBuilder`.
- Aplikasi menampilkan semua notes dan memungkinkan pengguna untuk menambah, mengedit, atau menghapus note melalui dialog form.

---

## 📸 Tampilan

| Halaman Utama | Tambah/Edit Note |
|---------------|------------------|
| ![main](https://via.placeholder.com/200x400.png?text=Main+Page) | ![form](https://via.placeholder.com/200x400.png?text=Form+Dialog) |



---

## 🧪 Stack Teknologi

- **Flutter** – UI Toolkit
- **Hive** – NoSQL Database Lokal
- **build_runner** & **hive_generator** – Untuk membuat adapter model

---

## 📌 Catatan

- Hive menyimpan data dalam bentuk file binary lokal.
- Cocok untuk aplikasi offline, ringan, dan cepat.

---

## 👨‍💻 Author

Garda Sudarmanto – 5025221268

---
