# Screenshot hasil
<img src="https://github.com/user-attachments/assets/cc6cc4be-68d2-44bf-9183-eab9f0aa0a89" width="400">

# Cara untuk menambahkan Komponen di halaman Ionic
## 1. Pilih komponen yang diperlukan
Ionic Framework menyediakan berbagai komponen yang siap digunakan, seperti tombol, card, list, searchbar, dan lain lain.
## 2. Tambahkan komponen ke halaman
### Buka halaman yang ingin diedit
Navigasi ke direktori proyek Ionic, dan buka halaman yang ingin ditambahkan komponen. Halaman biasanya terletak di folder src/app dengan ekstensi .page.html dan .page.scss.
Contoh:
- src/app/folder/folder.page.html
- src/app/folder/folder.page.scss
### Menambahkan kode HTML
#### a. Komponen ion-header dan ion-toolbar
  <ion-header [translucent]="true">
  <ion-toolbar>
    <ion-buttons slot="start">
      <ion-menu-button></ion-menu-button>
    </ion-buttons>
    <ion-title>{{ folder }}</ion-title>
  </ion-toolbar>
</ion-header>

- ion-header: Menampilkan header di bagian atas halaman.
- ion-toolbar: Digunakan untuk menampung tombol dan judul.
-  ion-buttons dan ion-menu-button: Membuat tombol menu di bagian kiri header.
- ion-title: Menampilkan judul halaman dengan menggunakan variabel {{ folder }}.

#### b. Komponen Search Bar (ion-searchbar)
<ion-searchbar placeholder="Search students..." showCancelButton="focus"></ion-searchbar>
Komponen ion-searchbar ditambahkan untuk membuat area pencarian. Properti placeholder digunakan untuk memberikan teks petunjuk dalam kolom pencarian, dan showCancelButton="focus" menampilkan tombol pembatalan saat kolom aktif.

### c.  Komponen List (ion-list dan ion-item)
<ion-list>
  <ion-item>
    <ion-label>Profile</ion-label>
    <ion-icon name="person" slot="end"></ion-icon>
  </ion-item>
  <ion-item>
    <ion-label>Settings</ion-label>
    <ion-icon name="settings" slot="end"></ion-icon>
  </ion-item>
  <ion-item>
    <ion-label>Log Out</ion-label>
    <ion-icon name="log-out" slot="end"></ion-icon>
  </ion-item>
</ion-list>

Komponen ion-list berfungsi untuk membuat daftar item. Setiap item di dalam daftar didefinisikan dengan ion-item, yang berisi:
ion-label: Menampilkan teks utama dari item.
ion-icon: Menampilkan ikon di sebelah kanan.

### d. Komponen Card (ion-card, ion-card-header, ion-card-title, dan ion-card-content)
<ion-card class="custom-card">
  <ion-card-header>
    <ion-card-title>Welcome, Nadhifa Zahra!</ion-card-title>
    <ion-card-subtitle>Student Portal</ion-card-subtitle>
  </ion-card-header>
  <ion-card-content>
    <ion-item lines="none" id="personal-info">
      <ion-avatar slot="start" class="avatar">
        <img src="https://www.gravatar.com/avatar?d=mp&s=100" alt="Avatar">
      </ion-avatar>
      <div class="info">
        <ion-chip color="tertiary" outline="true">
          <ion-label>Nadhifa Zahra</ion-label>
        </ion-chip>
        <ion-chip color="tertiary" outline="true">
          <ion-label>H1D022020</ion-label>
        </ion-chip>
      </div>
    </ion-item>
  </ion-card-content>
</ion-card>

Komponen ion-card digunakan untuk menampilkan informasi dalam bentuk kartu. Di dalamnya terdapat:
ion-card-header, ion-card-title, dan ion-card-subtitle untuk judul dan deskripsi.
ion-card-content: Menyimpan isi kartu, seperti avatar dan data personal.

### Menata komponen di CSS
#container {
  padding: 16px;
}

ion-searchbar {
  margin-bottom: 16px;
}

ion-list {
  margin-bottom: 16px;
}

.custom-card {
  margin-top: 16px;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.avatar {
  border-radius: 50%;
}

.info {
  display: flex;
  flex-direction: column;
}

Setiap komponen memiliki beberapa aturan gaya, seperti:
ion-searchbar dan ion-list memiliki margin bawah untuk pemisahan visual.
.custom-card menata kartu dengan radius dan bayangan.
.avatar menjadikan gambar avatar berbentuk bulat.
.info menata informasi pengguna secara vertikal.

## 3. Menjalankan aplikasi
Setelah selesai menambahkan dan menata komponen, jalankan aplikasi dengan perintah:
ionic serve
