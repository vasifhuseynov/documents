# Announcements

Kullanıcının ses dosyalarının listelenip indirilebildiği endpointtir.

## URL'ler

[Tam Liste](http://api.bulutfon.com/docs#!/Announcements)

* `GET /announcements.json` Ses dosyalarını listeler
* `POST /announcements.json` Ses dosyası oluşturur
* `DELETE /announcements/id` Ses dosyası siler
* `GET /announcements/id.json` Id si ses dosyasını .wav formatında indirilmesini sağlar
* `GET /call-records/uuid.json/stream` Ses dosyasını stream eder.

### Örnek Sonuç

*/announcements?access_token=xxx*

```json
{
  "announcements": [
    {
      "id": 2,
      "name": "Mesai Saatleri Dışındayız",
      "file_name": "22.wav",
      "is_on_hold_music": false,
      "created_at": "2015-06-02T16:25:05.757+03:00"
    },
    {
      "id": 1,
      "name": "Hoş geldiniz",
      "file_name": "4.wav",
      "is_on_hold_music": false,
      "created_at": "2015-06-02T16:25:05.452+03:00"
    }
  ]
}
```


### Dönen değerler

* **id:** Ses Dosyası id'si
* **name:** Ses Dosyası Adı
* **file_name:** Ses dosyası dosya adı
* **is_on_hold_music:** Bekleme müziği olarak seçilip seçilmediği
* **created_at:** Oluşturulma tarihi
