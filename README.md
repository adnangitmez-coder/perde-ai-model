# Perde AI isim tanıma modeli

Perde AI tarayıcı eklentisinin cihazda çalışan isim, kurum ve adres tanıma modeli.
Eklenti bu dosyaları ilk kurulumda **bir kez** indirir, parmak izini (SHA-256)
kontrol eder ve tarayıcının içinde saklar. Bu depoya hiçbir kullanıcı metni gelmez;
buradan yalnız model dosyaları indirilir.

- Kaynak model: [emi08/maske](https://huggingface.co/emi08/maske) (ModernBERT-tr tabanlı, Apache-2.0)
- Biçim: ONNX, int8 (`onnx/model_quantized.onnx`, GitHub'ın 100 MB dosya sınırı yüzünden iki parça; eklenti sırayla birleştirir)
- Lisans: Apache-2.0 (bkz. LICENSE ve NOTICE)

Dosyaları değiştirmeyin: eklenti her dosyanın parmak izini bilir ve uymayanı kullanmaz.
Yeni model sürümü yeni bir commit olarak eklenir, eklenti o commit'e sabitlenir.

---

On-device name/organization/address model used by the Perde AI browser extension.
Derived from emi08/maske (Apache-2.0), exported to ONNX and quantized to int8.
The ONNX file is split in two parts (GitHub's 100 MB file limit); concatenate in order.
