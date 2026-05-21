# Kıyak İçerik Deposu

Bu depoda Kıyak uygulamasının gösterdiği indirimler tutulur.

## Nasıl güncellerim?

1. Bu sayfada `discounts.json` dosyasına tıkla.
2. Sağ üstte kalem simgesine (Edit) bas.
3. Bir indirimi değiştir / yenisini ekle / sil. JSON formatına dikkat et (virgüller, tırnaklar).
4. En altta "Commit changes" tuşuna bas.
5. 1-2 dakika içinde uygulamadaki herkesin telefonunda görünür.

## Yeni indirim eklemek

Listenin sonundaki son `}` virgülünden sonra şöyle bir blok ekle:

```json
,
{
  "id": "7",
  "merchantName": "Esnaf Adı",
  "category": "Yeme-İçme",
  "discountText": "%20 indirim",
  "address": "Adres bilgisi, Bandırma",
  "conditions": "İndirimin geçerli olduğu koşullar.",
  "note": null
}
```

`category` alanı şu seçeneklerden biri olmalı:
`Yeme-İçme`, `Kuaför`, `Kırtasiye`, `Spor`, `Eğlence`, `Sağlık`

`note` alanı boş bırakılacaksa `null` yazılır.

`id` her indirime özel olmalı (1, 2, 3 ... gibi tekrarlamayan sayı).

Her güncellemede `updatedAt` alanını bugünün tarihiyle değiştir: `"2026-05-21"` gibi.
