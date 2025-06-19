## Penerapan Machine Learning untuk Memprediksi Harga Mobil pada Data Saudi Arabia Used Car

### Latar Belakang
Pasar mobil bekas di Arab Saudi telah berkembang pesat dalam beberapa tahun terakhir, didorong oleh pertumbuhan populasi, peningkatan daya beli, serta perubahan gaya hidup masyarakat. Industri mobil bekas di Arab Saudi telah tumbuh  yang signifikan berdasarkan nilai transaksi bruto dan volume penjualan selama periode 2017-2021. Ketersediaan berbagai opsi pembiayaan, pertumbuhan pesat pasar lelang dan iklan baris daring, serta meningkatnya penetrasi ponsel pintar dan internet menyebabkan peningkatan penjualan dari tahun 2017-2022. Data yang diambil dari https://www.goodcarbadcar.net/saudi-arabia-car-sales-data/ menunjukan bahwa terjadi peningkatan pembelian signifikan dari tahun 2018 hingga 2019 dan tahun 2021 hingga tahun 2022. Ukuran pasar mobil bekas di Arab Saudi mencapai USD 6,87 miliar pada tahun 2025 dan diproyeksikan mencapai USD 10,37 miliar pada tahun 2030 Source: https://www.mordorintelligence.com/industry-reports/saudi-arabia-used-car-market. 
### Permasalahan
Dalam pasar mobil bekas Arab Saudi yang sangat kompetitif dan terus berkembang, penentuan harga jual kendaraan menjadi salah satu tantangan utama bagi pengusaha. Banyak dealer atau pelaku bisnis menetapkan harga berdasarkan intuisi atau acuan harga historis yang tidak memperhitungkan kondisi pasar secara real-time, fitur kendaraan, atau perilaku konsumen.
Ketidaktepatan dalam menetapkan harga dapat berdampak langsung pada:
- Lamanya mobil terjual (slow moving stock),
- Potensi kerugian karena undervaluasi,
- Kehilangan pelanggan karena overpricing.
Dengan volume data kendaraan yang besar dan beragam, pengusaha mobil bekas membutuhkan sistem yang mampu memprediksi harga pasar secara akurat dan efisien, agar dapat membuat keputusan penetapan harga yang optimal, kompetitif, dan berbasis data.
### Tujuan 
Berdasarkan permasalahan tersebut, diperlukan prediksi harga yang akurat agar perusahaan atau dealer mobil tetap mendapatkan keuntungan yang optimal, mengurangi resiko kesalahan penetapan harga, meningkatkan kepuasan pelanggan, dan mudah mengatur stok mobil yang akan dibeli sesuai dengan cashflow perusahaan.
### Analytic Approach
Jadi, yang perlu kita lakukan adalah menganalisis data untuk dapat menemukan pola dari fitur-fitur yang ada, yang membedakan satu mobil dengan mobil yang lain
Selanjutnya, kita akan membangun suatu model regresi yang akan membantu perusahaan untuk dapat menyediakan 'tool' prediksi harga mobil yang akurat untuk perusahaan penjualan mobil atau dealer mobil. 
### Metric Evaluation
Evaluasi metrik yang akan digunakan adalah RMSE, MAE, dan MAPE, di mana RMSE adalah nilai rataan akar kuadrat dari error, MAE adalah rataan nilai absolut dari error, sedangkan MAPE adalah rataan persentase error yang dihasilkan oleh model regresi. Semakin kecil nilai RMSE, MAE, dan MAPE yang dihasilkan, berarti model semakin akurat dalam memprediksi harga mobil sesuai dengan limitasi fitur yang digunakan.
### Data Understanding
- Dataset merupakan data saudi arabia used cars
- Setiap baris data merepresentasikan informasi tentang mobil

**Attributes Information**

| **Attribute** | **Data Type** | **Description** |
| --- | --- | --- |
| Type | Object | Type of used car |
| Region | Object | The region in which the used car was offered for sale |
| Make | Object | The company name |
| Gear_Type | Object | Gear type size of used car |
| Origin | Object | Origin of used car |
| Options | Object | Options of used car |
| Year | Integer | Manufacturing year |
| Engine_Size | Float | The engine size of used car |
| Mileage | Integer | Mileage of used car	 |
| Negotiable | Boolean | True if the price is 0, that means it is negotiable |
| Price | Integer | Used car price|
### Proses 
1.Exploratory Data Analysis
2.Define X,y
3.Data Splitting
4.Data preprocessing
5.Cross Validation Beberapa Model Machine Learning
6.Predict data menggunakan model terbaik dari cross validation
7.Melakukan tunning pada model terbaik
8.Membandingkan hasil dari model tunning vs sebelum tunning
9.Melihat fitur/kolom yang berpengaruh terhadap penentuan prediksi harga
### Kesimpulan 
Machine learning yang dibuat untuk memprediksi harga mobil di arab saudi menggunakan model XGBRegressor karena setelah dilakukan beberapa perlakuan dengan membandingkan beberapa model, model ini mendapatkan hasil terbaik. Setelah dilakukan tunning, hasil yang didapat ternyata model sebelum ditunning mendapat hasil yang lebih baik daripada setelah ditunning walaupun dengan hasil perbedaan yang tidak terlalu signifikan dan akan menggunakan model sebelum ditunning untuk melakukan prediksi harga. Metric evaluasi untuk machine learning ini menggunakan RMSE,MAE,dan MAPE. Nilai MAPE sebelum ditunning adalah 123% yang memiliki arti bahwa prediksi harga rata - rata mobil akan meleset kurang lebih 123% dari harga aktualnya. Kolom yang paling mempengaruhi prediksi harga kolom options yang merupakan kolom terkait fitur yang tersedia di mobil tersebut, merk mobil atau kolom make, dan tahun pembuatan mobil.
### Rekomendasi 
Model Machine Learning ini dapat digunakan dalam kondisi Saat tersedia data kendaraan yang lengkap dan valid (fitur penting seperti tahun, jarak tempuh, brand, dan kondisi kendaraan). Model ini juga dapat digunakan untuk kendaraan dengan karakteristik umum/populer yang sering muncul dalam data latih, karena model telah belajar dari pola tersebut Ketika dealer ingin menetapkan harga awal pasar berdasarkan data historis dan tren aktual. Model memiliki kelemahan untuk memprediksi harga mobil yang langka, eksklusif, atau baru masuk pasar (karena belum ada data historis yang cukup).Penggunaan model ini dapat mengurangi waktu pengambilan keputusan dan mengoptimalkan strategi penjualan berdasarkan data serta emungkinkan perencanaan stok dan pembelian mobil bekas secara lebih efisien karena harga lebih terprediksi. Namun Model Machine learning masih perlu dievaluasi dan ditingkatkan akurasinya dengan penggunaan gridsearch  agar dapat menemukan price prediction yang lebih akurat dengan persentase MAPE yang bisa lebih ditekan. Akurasi model ini masih belum terlalu akurat dikarenakan juga keterbatasan data yang diperoleh.


