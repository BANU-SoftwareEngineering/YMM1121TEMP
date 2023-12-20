# Fonksiyonlar (Functions)
Programlamada çok tekrar ettiğimiz kod satırlarını ya da kod bloklarını lazım olduğu her yerde yeniden yazmak yerine, yahut kopyala yapıştır yapmak yerine, söz konusu bloğu bir fonksiyon olarak tanımlar ve gerektiği yerde fonksiyonu çağırarak bunu bir rutin haline getirebiliriz.
C++'da fonksiyonlar parametrik olarak tanımlanabilirler, yani, bir fonksiyona değer gönderebiliriz. Fonksiyonun tanımlandığı tipe göre bir dönüşü olmak zorundadır, tipsiz dediğimiz ```void``` tanımlaması için bu durum istisnadır.
Programlama dillerindeki fonksiyon kullanımı matematiksel fonksiyonları andırmaktadır ve aynı zamanda matematiksel fonksiyonlar programlama dillerindeki fonksiyonların esin kaynağıdır. C++ için fonksiyon tanımının tam karşılığı (procedure) prosedür kelimesi olsa gerek.
Bu manada tam olarak matematiksel fonksiyonlarla eşleştirmek doğru olmayabilir.
Fonksiyonlar genellikle belirli bir işlevi yerine getirmek içindir ve bir programın herhangi bir yerinden çağırılabilirler, bunun için azami şart fonksiyonun varlığının bildirilmesi(declaration) ve tanımlanmasıdır (definition).
C++ için bu fonksiyon bildirimleri, -bildirim denmesinin sebebi fonksiyonun sadece prototipinin yazılıp içeriğinin, yani yaptığı/yapacağı işlemlerin kodlanmadığı kısım olmasıdır-
hem ana kod içerisinde kalabalık etmemesi açısından hem de programın farklı kaynak kodu sayfalarında çağırılabilip kullanılabilmesinin kolaylaştırılması açısından .h uzantılı header files dediğimiz dosyalar içerisinde yapılır.
Bir programı yazmak kadar, o programlama dilinin kod yazma disiplinine hakim olmak ve o disiplini uygulamak da önemlidir.


## Fonksiyon Bildirimleri (Function Declarations)
Bir fonksiyon bildirimi, derleyiciye bu fonksiyonun var olduğunu, fonksiyonun bir prototipini yazarak bildirilmesine denir. Söz dizimi aşağıdaki gibidir:

```cpp
int topla(int a, int b);
```

Satır sonunda noktalı virgül olduğuna dikkat edin. Bu satırla derleyiciye benim ```int``` tipinde geri dönüşü olan parametre olarak iki tane integer tipinde sayı alan ve adı topla olan bir fonksiyonum var ileride ya da kodun başka bir yerinde bu fonksiyonu yazacağım demiş oluyoruz.
Burada a ve b tiplerini fonksiyonun gövdesi dediğimiz kısımda kullanacağız.

Fonksiyon bildirimi yapılırken değişken isimlerini yazmak zorunda da değiliz:

```cpp
int topla(int, int);
```

iki örnek için de bir geri dönüş tipi belirledik bu fonksiyonlar geriye bir dönüş yapmak zorundadır, fonksiyonumuz sadece bir iş yapacak ve geriye hiçbir değer döndürmesine gerek yoksa void tipinde tanımlanabilirler:

```cpp
void ekranaYaz(const char* metin);
```

İçerisine parametre olarak verdiğimizi metini ekrana yazması için bir fonksiyon yazıyorsak bize bir değer döndürmesine ihtiyaç duymayız.
