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


Tablodan veri çekmek için web-api oluşturulacak.
.net core web app + api (KTUNApi)
models klasörünün altında yeni bir nesne oluşturuldu.(Tablo adıyla)

prop lar eklendi.

Data Klasörü Oluşturuldu.Context nesnesi oluşturuldu.(using Microsoft.EntityFrameworkCore;)
Context: DbContext{
 public Context(DbContextOptions<Context> options): base(options)
        {}
  public DbSet<ModelDekiNesne> students {get;set;}
  
  Servis Eklenecek
services.AddDbContext<Context>(Options => Options.UseSqlServer(Configuration.GetConnectionString("Baglanti Adi")));
  
  Contoller Eklenecek
  namespace ProjeAdi.Controllers
{
    [Route("api/[Controller]")]
    public class LanguageController : Controller
    {
        private Context _context;
        public  LanguageController(Context context)
        {
            _context = context;
        }
        [HttpGet]

        public List<LanguageModels> Get()
        {
            return _context.languages.ToList();
        }
    }
}

  
  Add-Migration First 
  Update-Database
  
  
  
  
