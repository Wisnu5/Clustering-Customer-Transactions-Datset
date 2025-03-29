# Clustering-Customer-Transactions-Datset
# Klasifikasi dengan Random Forest dan Decision Tree

## Deskripsi Proyek
Proyek ini bertujuan untuk melakukan klasifikasi menggunakan algoritma **Random Forest** dan **Decision Tree** pada dataset hasil clustering. Model dievaluasi menggunakan metrik **Accuracy, F1-Score, Precision, Recall,** dan **Confusion Matrix**.

## Dataset
Dataset yang digunakan adalah hasil clustering dan terdiri dari beberapa fitur numerik. Target klasifikasi adalah label cluster yang telah ditentukan sebelumnya.

## Pembagian Data
Dataset dibagi menjadi **training set (80%)** dan **testing set (20%)** dengan menggunakan **train_test_split** dari **sklearn**.

## Model yang Digunakan
1. **Random Forest Classifier**
2. **Decision Tree Classifier**

## Hasil Evaluasi Sebelum Tuning

### Random Forest
- **Accuracy**: 96.62%
- **F1-Score**: 0.9662
- **Confusion Matrix**:
  ```
  [[498   5  10   2]
   [  6 494   5   6]
   [  4   7 499  13]
   [  3   5   3 480]]
  ```

### Decision Tree
- **Accuracy**: 93.04%
- **F1-Score**: 0.9303
- **Confusion Matrix**:
  ```
  [[494   7   8   6]
   [ 13 470  15  13]
   [ 12  12 475  24]
   [  7   7  18 459]]
  ```

## Hasil Evaluasi Setelah Tuning

### Tuned Random Forest
- **Accuracy**: 96.57%
- **F1-Score**: 0.9657
- **Confusion Matrix**:
  ```
  [[497   6   9   3]
   [  5 493   7   6]
   [  4   7 500  12]
   [  3   5   3 480]]
  ```

### Tuned Decision Tree
- **Accuracy**: 93.82%
- **F1-Score**: 0.9382
- **Confusion Matrix**:
  ```
  [[487  11  11   6]
   [ 13 482   7   9]
   [ 10  10 478  25]
   [  7   9   8 467]]
  ```

## Perbandingan Hasil
| Model | Accuracy Sebelum Tuning | Accuracy Setelah Tuning | F1-Score Sebelum | F1-Score Setelah |
|--------|----------------------|----------------------|----------------|----------------|
| Random Forest | 96.62% | 96.57% | 0.9662 | 0.9657 |
| Decision Tree | 93.04% | 93.82% | 0.9303 | 0.9382 |

## Analisis dan Kesimpulan
- **Random Forest memiliki performa lebih baik dibandingkan Decision Tree** dalam hal akurasi dan F1-Score.
- **Random Forest lebih stabil** karena merupakan model ensemble, sedangkan **Decision Tree lebih rentan terhadap overfitting**.
- Setelah tuning, **Decision Tree mengalami peningkatan akurasi**, sedangkan **Random Forest tetap stabil**.
- **Precision dan Recall kelas tertentu bisa lebih diperbaiki** dengan eksplorasi lebih lanjut terhadap fitur dan parameter tuning.

## Rekomendasi untuk Peningkatan
1. **Coba model lain seperti XGBoost atau SVM** untuk membandingkan performa lebih lanjut.
2. **Gunakan lebih banyak data latih** untuk meningkatkan generalisasi model.
3. **Eksplorasi teknik feature engineering** untuk meningkatkan representasi data.
4. **Lakukan balancing data jika diperlukan**, untuk menangani ketimpangan jumlah sampel antar kelas.

