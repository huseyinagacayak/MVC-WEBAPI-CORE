# MVC-WEBAPI-CORE
Identfy(Kimlik İşlemleri) Hazır Kullanıldı
Startup'a Razor Page servisi, Authentication app'ı eklendi ve endpoint sonlandırıcı eklendi.

Kullanıcı için ek bilgiler eklendi.
String veriler nvarchar(karakter sayısı) ile,
Integer veriler int ile oluşturulabilir.
	      [PersonalData]
        [Column(TypeName = "nvarchar(100)")]
        public string FirstName { get; set; }
        [PersonalData]
        [Column(TypeName = "int")]
        public int Numara { get; set; }
        (using Microsoft.EntityFrameworkCore.Migrations; Kullanılacak)
Nuget Package Manager - Console ile 
Add-Migration "Intial-Create" , Update-Database komutları çalıştırılarak veritabanı oluşturuldu. 

Personel Girişi Tamamlandı.
Gerekli Veritabanları Oluşturuldu.



  
