# Analysis-Dataset-Heart-Disease
Proyek ini bertujuan untuk menganalisis dataset Heart Disease (Cleveland) dengan bantuan AI untuk menemukan pola, insight, dan memberikan rekomendasi strategis dalam pencegahan penyakit jantung.
# Dataset Link
https://archive.ics.uci.edu/dataset/45/heart+disease
- Fitur utama:
  - age → usia pasien
  - sex → jenis kelamin (1 = pria, 0 = wanita)
  - cp → jenis nyeri dada (0–3)
  - trestbps → tekanan darah saat istirahat
  - chol → kolesterol
  - fbs → gula darah puasa >120 mg/dl (1/0)
  - restecg → hasil EKG istirahat
  - thalach → denyut jantung maksimum
  - exang → angina akibat olahraga (1/0)
  - oldpeak → depresi ST
  - slope, ca, thal → fitur tambahan jantung
  - num → label (0 = sehat, 1 = ada penyakit jantung)
# Notebook Analytics
https://colab.research.google.com/drive/1zNbMhe3kIx0LORZgk-I3FyGlZxl4BCOW?usp=sharing
# Analytical Result
- Accuracy = 88.5% → model sangat baik untuk dataset kecil seperti ini.
- Precision & Recall:
  - Kelas 0 (sehat): precision 0.89, recall 0.86 → model cukup andal membedakan pasien sehat.
  - Kelas 1 (penyakit jantung): precision 0.88, recall 0.91 → model sangat bagus dalam mendeteksi pasien sakit.
- Confusion Matrix:
  - 25 pasien sehat benar diklasifikasi sehat, 4 salah diklasifikasi sakit.
  - 29 pasien sakit benar diklasifikasi sakit, hanya 3 salah diklasifikasi sehat.
Secara keseluruhan, model logistic regression cukup akurat dan seimbang (tidak bias hanya ke salah satu kelas).
# Insight & Findings
- Model mampu mendeteksi pasien dengan penyakit jantung dengan baik (recall 91%), yang penting dalam konteks medis karena lebih baik “false alarm” daripada melewatkan pasien sakit.
- Kesalahan prediksi masih ada (4 pasien sehat dikira sakit, 3 pasien sakit dikira sehat), tapi jumlahnya kecil.
- Variabel seperti usia, kolesterol, tekanan darah, denyut jantung maksimum kemungkinan besar berkontribusi besar dalam klasifikasi (bisa dicek dengan feature importance/coefficients).
- Dataset yang relatif kecil (303 baris) tetap bisa memberi hasil stabil dengan logistic regression sederhana.
# AI Support Explanation
- Analytical Result
Hasil evaluasi model Logistic Regression untuk dataset penyakit jantung menunjukkan beberapa metrik yang penting untuk dipahami:
  - Akurasi: Model ini memiliki akurasi sebesar 0,8852, artinya sekitar 88,52% dari prediksi yang dilakukan oleh model ini adalah benar.
  - Precision:
    - Untuk kelas 0 (sehat), precision sebesar 0,89 berarti bahwa dari semua orang yang diprediksi sehat, sekitar 89% di antaranya memang benar-benar sehat.
    - Untuk kelas 1 (penyakit jantung), precision sebesar 0,88 berarti bahwa dari semua orang yang diprediksi memiliki penyakit jantung, sekitar 88% di antaranya memang benar-benar memiliki penyakit jantung.
  - Recall:
    - Untuk kelas 0 (sehat), recall sebesar 0,86 berarti bahwa dari semua orang yang sebenarnya sehat, sekitar 86% di antaranya berhasil diprediksi sebagai sehat oleh model.
    - Untuk kelas 1 (penyakit jantung), recall sebesar 0,91 berarti bahwa dari semua orang yang sebenarnya memiliki penyakit jantung, sekitar 91% di antaranya berhasil diprediksi sebagai memiliki penyakit jantung oleh model.
  - Confusion Matrix: Matriks kebingungan menunjukkan bahwa dari 34 orang yang sehat, 25 orang diprediksi dengan benar sebagai sehat dan 4 orang salah diprediksi sebagai memiliki penyakit jantung. Dari 32 orang yang memiliki penyakit jantung, 29 orang diprediksi dengan benar sebagai memiliki penyakit jantung dan 3 orang salah diprediksi sebagai sehat.
- Insight & Findings
Beberapa temuan penting dari hasil analisis ini adalah:
  - Model ini memiliki kemampuan yang cukup baik dalam memprediksi penyakit jantung, dengan akurasi yang relatif tinggi.
  - Precision dan recall yang tinggi untuk kedua kelas menunjukkan bahwa model ini dapat membedakan dengan baik antara orang sehat dan orang dengan penyakit jantung.
  - Namun, ada sedikit ketidakseimbangan dalam recall antara kelas 0 dan kelas 1, yang mungkin perlu diperbaiki untuk meningkatkan kinerja model secara keseluruhan.
  - Jumlah false negative (3 orang) dan false positive (4 orang) relatif kecil, menunjukkan bahwa model ini memiliki kemampuan yang baik dalam menghindari kesalahan diagnosa yang serius.
- Recommendations
Berdasarkan hasil analisis, beberapa saran tindakan atau langkah strategis yang dapat dilakukan adalah:
  - Optimasi Model: Coba untuk mengoptimasi parameter model atau menggunakan teknik lain seperti cross-validation untuk lebih meningkatkan akurasi dan keseimbangan antara precision dan recall.
Pengembangan Dataset: Pertimbangkan untuk mengembangkan dataset dengan menambahkan lebih banyak sampel atau fitur yang relevan untuk meningkatkan kemampuan model dalam memprediksi penyakit jantung.
  - Implementasi Klinis: Model ini dapat diimplementasikan dalam pengaturan klinis sebagai alat bantu diagnosa, tetapi harus digunakan dengan hati-hati dan dalam kombinasi dengan penilaian klinis yang tepat untuk menghindari kesalahan diagnosa.
  - Pemantauan dan Evaluasi: Lakukan pemantauan dan evaluasi terus-menerus terhadap kinerja model dalam pengaturan klinis untuk memastikan bahwa model ini tetap efektif dan akurat dalam jangka panjang.
