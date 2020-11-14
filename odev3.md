   ##  .NET Kodu Nedir  :
  NET Foundation topluluğuna devir edilmiş bir yazılım geliştirme platformudur. İçerisinde yer alan kütüphaneler sayesinde  masaüstü, 
 web ve cep telefonu uygulamaları geliştirmeolanağı sağlar . Kolaylıklarından dolayı kullanışlı bir platformfur.
 
 ##  Roslyn Compiler Nedir :
 
 .NET Derleyici Platformu ayrıca takma adıyla bilinen, Roslyn ,bir dizi açık-kaynak derleyicidir.

Proje özellikle C # ve VB.NET derleyicilerinin kendi kendini barındıran sürümlerini içerir. Derleyiciler, geleneksel komut satırı programları aracılığıyla, ancak aynı zamanda 
.NET kodu içinden yerel olarak kullanılabilen API'ler olarak da kullanılabilir. Roslyn , kodun sözdizimsel ( sözcüksel ) analizi, anlamsal analiz, CIL için dinamik derleme
ve kod yayımı için modülleri ortaya çıkarır 

## - Restful Servisler Nasıl Çalışır :
REST, dağıtık mimari uygulamaları oluşturmak için geliştirilen veri transfer yönetimi ve kurallar bütünüdür. İsmi Representational State Transfer olan bu ifade Türkçe olarak 
“Temsili Durum Transferi” olarak geçer. HTTP üzerinde çalışır ve diğer alternatiflere göre daha yalındır. Temel içerik ile veri transferi gerçekleştirildiğinden hız açısından 
alternatiflerinden çok daha verimlidir.  İstemci ve sunucu arasında XML veya JSON verilerini taşıyarak uygulamaların haberleşmesini sağlar. REST standartlarına uygun yazılan web 
servislerine RESTful servisler denir.
REST servisler doğrudan bir URL çağrılarak çalışır ve kaynaklara (Resources) erişir. Arada ek bir bileşen, yöntem veya protokol kullanılmaz. SOAP gibi bir servisi uygulamanıza
dahil edebilmeniz için servisin WSDL’ına ihtiyaç duyarsınız, proxy sınıfları oluşturmanız gerekir, uzaktaki metotları tetikleyecek bileşenlere ihtiyaç vardır. İstemci, SOAP bir
servisle ilgili her şeyi bilmek zorundadır, belirli standartları yerine getirilmeden SOAP bir servisi çağıramaz. Ancak REST ile yazılmış bir servisle çalışmak için ihtiyacınız 
olan tek şey URL. Bir URL’yi çağırırsınız, URL size JSON veya XML döner, dönen cevabı kullanırsınız ve servis entegrasyon tamamlanır. Yani teorik olarak istemci uygulama REST bir 
servisin yapısını ve detaylarını bilmek zorunda değildir. REST’in bu basit standartları dışında uyulması gereken bir kural yoktur, son derece esnek bir yapı vardır.

RESTful servisler veri iletiminde farklı HTTP metotlarını kullanmaktadır. Bunlar GET, POST, PUT, DELETE metotlarıdır. GET okuma, POST yeni kayıt ekleme(insert), PUT kayıt
güncelleme(Update), DELETE ise kayıt silme işlemi için kullanılır. Yapılan HTTP Request’i için çağrılan URL ile beraber HTTP metod bilgisi bahsi geçen 4 metottan biri olarak
seçilir ve sunucu yapılan talebin kayıt üzerine nasıl etki edeceğini buna göre belirler.

Basit yapısı, kolay uygulanması, hızlı çalışması, esnek olması RESTful servislerin artı yönleridir. RESTful servislerinin bazı eksi yönleri de var bulunmaktadır. Güvenlik
bunlardan biri olmakla beraber SOAP servislerde standartlar gereği birçok güvenlik mekanizması otomatik olarak oluşturulabilirken RESTful servislerde güvenlik konuları 
geliştirilen yazılımın bir parçasıdır. İletişim seviyesinde güvenlik(Transport Level Security) genellikle token aracılığıyla yapılır. İstemci kritik işlemleri çağırmadan 
önce bir “Giriş” isteği gönderir. Bu istek sonucunda istemciye “Sessin Token” vb. bir değer verilir ve bundan sonra yapacağı istekler bu değer ile yapılır. Mesaj seviyesinde
güvenlik(Message Level Security) konusu da yine geliştirilen yazılımların içerisinde dikkat edilmesi gereken önemli bir konudur. Üçüncü parti araçlar kullanılarak hem iletişim
hem de mesaj seviyesinde gerekli güvenlik fonksiyonları geliştirilen yazılımlara rahatlıkla uygulanabilir.
### Alternatifleri Nelerdir :
* Falcor : Falcor modeli Netflix tarafından geliştirilen bir JavaScirpt kütüphanesidir. Tüm uzak veri kaynaklarının sanal bir JSON graph aracılığıyla tek bir domian model 
aracılığyla temsil edilmesini sağlar. Veri toplamak için hala REST yapısını kullanır. Yani, bir request için farklı endpoint'lere istek gönderilir ve her resourse için JSON
object döndürülür.
* OData : Yapısal olarak istemciden gönderilen sorgu isteği sunucu tarafında işlenerek sonuç üretilmekte ve clienta gönderilmektedir. Ayriyetten istemci tarafından talep 
edilen metadata belgesi ile OData kullandığı entitylerin detaylarından istemciyi bilgilendirebilmektedir.

##  Extension method nedir? Nasıl yazılır?

Extension metodlar herhangi bir yeni nesne oluşturmadan, üzerinde işlem yaptığınız nesne üzerinden çağrılabilen "genişletilmiş" manasına gelen çok pratik metodlardır.
Bu metodları kullanarak hem extra iş yükünden kurtulmuş olursunuz, hem de sürekli aynı kodları yazmak zorunda kalmazsınız.
Extension metodlar statik metodlar ve statik classlardan oluşmaktadır. Fakat referans olarak oluşturduğunuz obje üzerinden çağrılırlar. Extension metodların aldığı 
ilk parametre, bu metodun hangi nesne üzerinde çalışacağını belirtir. Ve alacağı ilk parametrenin önüne "this" anahtar kelimesi getirilir. Böylece metodun bu nesne
üzerinde işlem yapacağı belirtilmiş olur.
Extension metodların kullanımı da çok kolaydır. Extension metodları kullanacağınız kaynak koda, using anahtar kelimesini kullanarak eklediğinizde bu metodlarınızı
kullanabilirsiniz. Bu kadar açıklamadan sonra artık uygulamaya geçebiliriz.
Extension metod eklemenin ilk adımı normal bir class ekler gibi projemize class ekliyoruz. Ben extension metodlarımı saklamak için kullanacağım classa HelpExtensions 
adını vereceğim. Eklediğimiz bu class statik olmak zorunda. Ve daha sonra yukarıdaki yönergelere uygun şekilde metodlarımızı yazabiliriz. 

Extension metodlar öncelikle static bir class içerisinde static olarak tanımlanmalıdır.Sonra Extend edilecek class ilgili extension metoda metodun ilk parametresi
olarak verilip önünde this keyword'ü ile tanımlanmalıdır.Extension metod da tanımlı parametrelerden sadece 1 tanesi this keyword'ü ile tanımlanır.

##  MVC'nin alternatifleri nelerdir?


- MVA (Model View Adapter)
- PAC (Presentation Abstraction Control)
- ADR (Action-Domain-Responder)
- MVVM (Model-View-ViewModel)

## Architectural pattern nedir? Neden ihtiyaç duyuyoruz?

Mimari modeller, yazılım tasarım modellerine benzer ancak daha geniş bir kapsama sahiptir.
Mimari modeller , bilgisayar donanımı performans sınırlamaları, yüksek kullanılabilirlik ve bir iş riskinin en aza indirilmesi gibi
yazılım mühendisliğindeki çeşitli sorunları ele alır . Yazılım çerçevelerinde bazı mimari modeller uygulanmıştır .

## ViewData, ViewBag, TempData farkları nelerdir? Çalıştığımız proje üzerinde başka bir branch açarak bunları deneyiniz?

### ViewData:
* ViewData , denetleyiciden görüntülemeye veri iletmek için kullanılır
* ViewDataDictionary sınıfından türetilmiştir.
* Yalnızca mevcut istek için kullanılabilir
* Karmaşık veri türleri için tipleme gerektirir ve hatayı önlemek için boş değerleri kontrol eder
* Yeniden yönlendirme oluşursa, değeri boş olur
### ViewBag:
* ViewBag ayrıca denetleyiciden ilgili görünüme veri iletmek için kullanılır
* ViewBag , C # 4.0'daki yeni dinamik özelliklerden yararlanan dinamik bir özelliktir
* Ayrıca sadece mevcut istek için de mevcuttur
* Yeniden yönlendirme oluşursa, değeri boş olur
* Karmaşık veri türleri için yazım gerektirmez
### TempData:
* TempData, TempDataDictionary sınıfından türetilir
* TempData, mevcut talepten sonraki isteğe veri aktarmak için kullanılır
* Bilgileri bir HTTP İsteğinin süresi boyunca tutar. Bu, yalnızca bir sayfadan diğerine anlamına gelir. Bir denetleyiciden başka bir denetleyiciye veya bir eylemden diğerine geçtiğimizde verileri korumaya yardımcı olur
* Karmaşık veri türü için tipleme gerektirir ve hatayı önlemek için boş değerleri kontrol eder. Genellikle, hata mesajları ve doğrulama mesajları gibi sadece bir seferlik mesajları saklamak için kullanılır.
