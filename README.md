
---

# Zaman Serileri ile Feature Engineering

Bu proje, Milli Teknoloji Akademisi Yapay Zeka Uzmanlık Programı kapsamında Tübitak'ın vermiş olduğu Veri Yoğun Uygulamalar Modül Projesi kapsamında tamamlanmıştır. Farklı sektörlerden elde edilen zaman serileri üzerinde yapılan feature engineering işlemlerini içermektedir.  
Aşağıda proje adımları ve kullanılan teknikler hakkında detaylı bilgiler bulunmaktadır.

## Proje Adımları

1. **Veri Toplama:**
   - Sektörlerin listesine web scraping yöntemiyle erişildi.
   - Veriler yfinance kütüphanesi ile toplandı.

2. **Zaman Serileri Elde Etme:**
   - 2005-01-01 tarihinden itibaren haftalık getirilerden oluşan kapanış mometum serileri elde edildi.

3. **Faktör Hesaplama:**
   - 3 büyük sektör (Finans, Sağlık, Teknoloji) üzerinden getirilerin faktörleri hesaplandı, örneğin momentum.

4. **Feature Engineering:**
   - Tsfresh kütüphanesi kullanılarak feature extraction işlemleri gerçekleştirildi.
   - İmputing, encoding, transformation, scaling, outliers gibi feature engineering işlemleri ColumnTransformer ve Pipeline ile uygulandı.

5. **Model Kurma:**
   - Yeni elde edilen feature ve sektör sınıfları üzerinden bir classification modeli kuruldu.
   - En iyi model seçimi yapıldı.

6. **Sektör Benzerliklerinin Belirlenmesi:**
   - Diğer sektörlerden örnekler alınarak aynı feature engineering yöntemleri uygulandı.
   - Hangi sektöre (Finans, Sağlık, Teknoloji) benzediğine karar verildi.

## Kullanılan Teknolojiler
- Python
- Pandas
- Numpy
- Sklearn
- Tsfresh
- Beautiful Soup
- Matplotlib, Seaborn
- feature_engine