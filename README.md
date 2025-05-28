# 🗑️ Garbage Classification with CNN

Proyek ini bertujuan untuk membangun model klasifikasi gambar sampah ke dalam 9 kategori menggunakan Convolutional Neural Network (CNN) di TensorFlow/Keras. Model ini diharapkan mampu membantu proses pemilahan sampah otomatis berdasarkan jenisnya.

---

## 📂 Dataset

Dataset terdiri dari gambar-gambar sampah yang terbagi ke dalam 9 kelas:

- Battery
- Biological
- Cardboard
- Clothes
- Glass
- Metal
- Paper
- Plastic
- Shoes

Dataset telah diproses untuk:
- Menyamakan ukuran (rasio 1:1)
- Augmentasi data (terutama pada kelas yang jumlahnya rendah, seperti Battery, Biological, dan Metal)

### 📊 Pembagian Dataset:
- 70% Training Set
- 15% Validation Set
- 15% Testing Set

---

## 🧠 Arsitektur Model

Model dikembangkan menggunakan arsitektur Convolutional Neural Network (CNN) berlapis, dimulai dari lapisan konvolusi dan pooling, diikuti oleh lapisan normalisasi dan dropout untuk mencegah overfitting, dan diakhiri dengan lapisan dense untuk klasifikasi multi-kelas.

Model menggunakan fungsi aktivasi ReLU di lapisan konvolusi dan softmax di lapisan output. 

---

## 🚀 Proses Training

Pelatihan model dilakukan menggunakan data yang telah dibagi dan distandarisasi. Beberapa callback digunakan untuk meningkatkan performa pelatihan, seperti:
- **EarlyStopping**: Menghentikan pelatihan jika validasi tidak membaik dalam beberapa epoch.
- **ModelCheckpoint**: Menyimpan model terbaik selama pelatihan.
- **ReduceLROnPlateau**: Mengurangi learning rate jika validasi loss stagnan.

---

## 🔧 Cara Install / Requirements

Memeriksa apakah GPU NVIDIA tersedia di lingkungan (seperti Google Colab):

```bash
!nvidia-smi
```

Menginstal TensorFlow dan Tensorflow.js:

```bash
pip install tensorflow tensorflowjs
```

Untuk menginstall tesk requirement gunakan perintah:

```bash
!pip freeze requirements.txt
```
