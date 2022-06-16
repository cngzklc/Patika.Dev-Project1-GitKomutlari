># Markdown nedir?
Metinden HTML'e dönüşüm için kullanılan hafif bir işaretleme dilidir.

---
>## Başlıklar (Header)  

"#" karakteri ile başlık oluşturulabiliyor. Burada önemli olan "#" karakterinden sonra boşluk bırakmaktır. Bir adet # işaretieklenir.   
Büyük başlık kullanmak için tek # işareti veya Başlığın altına "-" işareti,  
Küçük başlık kullanmak için çift ## işareti veya başlığın altına "=" işareti kullanılır.     
Başlık ku

---
>## Eğik Yazı (italic)
Eğik yazı için kelime ya da cümlenin başına ve sonuna "_" veya "*" karakterleri eklenir.    
_italic_    
*italic*

---
> Not: * işaretinin görülebilmesi için başına \ işareti koymak gerekiyor.   
\ işareti, #, . gibi işaretleri devre dışı bırakmal için kullanılır.
---
>## Kalın Yazı (Bold)
Eğik yazı için kelime ya da cümlenin başına ve sonuna çift "__" veya çift "**" karakterleri eklenir.  
__Bold__    
**Bold**

---
>## Kalın Eğik Yazı (Italic Bold)
Eğik yazı için kelime ya da cümlenin başına ve sonuna üç adet "___" veya üç adet "***" karakterleri eklenir.  
___Italic Bold___    
***Italic Bold***

---
>## Link
Link, HTML'den aşina olduğumuz `<a>` etiketi yerine Markdown'da Köşeli Parantez[] ve normal parantez() ile yapılır.     
**Örnek :** [Kodluyoruz Sayfası](https://www.kodluyoruz.org/)     

---
>## Image
Bağlantı resimleri de Link gibi aynı şekilde eklenir. Sadece köşeli parantezden önce ! işareti eklenmelidir.

![Kodluyoruz Logo](https://cdn.sanity.io/images/9kdepi1d/production/65c832d202a503b15d99e628f4313782f3ef50db-300x62.png)

---
>## Tablolar
Tablo oluşturmak için aşağıdaki yapı kullanılır. Satır çizgisi için kullanılan - karakterine : işareti eklenerek tabloda sola, sağa ve ortaya hizalama yapılabilir.

|ProductID| ProductName| Price|
| :--- | :---: | ---: |
| 1 | Book | 100 TL |
| 2 | Pen | 15 TL |
| 3 | Notebook | 6750 TL |
| 4 | Desktop PC | 8950 TL |


---
>## Listeler
HTML'de `<ul> </ul>` ve `<li> </li>` etiketleri ile oluşturulan listeler MArkdown formatında - ve * işaretleri ile oluşturulur.

- Liste Elemanı 1
- Liste Elemanı 2 
- Liste Elemanı 3

Sıralı liste elde etmek için yapılması gerek liste elemanlarının başına sıra numarası ve . işareti eklemek.

1. Liste Elemanı 1
2. Liste Elemanı 2 
3. Liste Elemanı 3

Makdown'da sıra numaralı farklı verilmiş olsa dahi sıra numaralarını otomatik biçimlendirerek ardışık olarak vermektedir.

7. Liste Elemanı 1
8. Liste Elemanı 2 
13. Liste Elemanı 3
25. Liste Elemanı 4
2. Liste Elemanı 5 
3. Liste Elemanı 6
---
Makdown'da iç içe listeler yapmak için alt listelere tab ile girinti verildiğinde otomatik olarkak nested list yapısına dönüşecektir.

1. Liste Elemanı 1
    - Liste Elemanı 1'in Alt Liste Elemanı 1
    - Liste Elemanı 1'in Alt Liste Elemanı 2
2. Liste Elemanı 2 
3. Liste Elemanı 3
---
1. Liste Elemanı 1
    1. Liste Elemanı 1'in Alt Liste Elemanı 1
    2. Liste Elemanı 1'in Alt Liste Elemanı 2
2. Liste Elemanı 2 
3. Liste Elemanı 3
---

>## Kod Blokları
Kod blokları (Alt GR+;) tuşları ile backticks karakteri ( ` ) arasına alınaraak yapılıyor.

Kod satırı için iki `` backticks karakteri arasına kodlarımızı yazmamız gerekiyor.     

`Console.Writeline("Helo World");`  
`Console.Writeline("Helo World");`

Kod Bloğu için satır üstünü 3 adet backticks karakteri ve satır altına 3 adet backticks karakteri yazmak gerekiyor.

``` C#
for (int i =0; i< count; i++)
{
    Console.WriteLine("Hello Word");
}
```

