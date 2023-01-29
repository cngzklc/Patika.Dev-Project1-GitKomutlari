># Git Notları 
https://app.patika.dev/courses/git/git-bash-ile-git-temel-komutlari

># Git Terimleri 
**untracted (izlenmeyen)   :** GIT tarafından henüz takip edilmeyen, yani yeni oluşturulmuş dosyaları ifade eder.   
**unstaged (hazırlanmamış) :** Güncellenmiş ancak commit'lenmek için hazırlanmış dosyaları ifade eder.  
**staged (hazırlanmış)     :** Commit'lenmeye hazır dosyaları ifade eder.   
**deleted (silinmiş)       :** Projeden silinmiş ama GIT üzerinden kaldırılmamış dosyaları ifade eder.

># Git Komutları
**explorer .               :** Project folder'ı açar.   
**git init                 :** Henüz versiyon kontrolü altında olmayan bit projenin dizininde, boş bir git deposu oluşturmak için kullanılır.   
**git config               :** Git'in bir çok konfigürasyon ayarları vardır. Bunlardan ikisi user.name ve user.email olanlardır. Git'i ilk kurduğumuzda genellikle ilk hata bu konfigürasyon ayarlarını yapmaığımız için gelir. Ayrıca komutlarda da görüldüğü gibi bu ayarlar --global yani sistem genelinde geçerlidir. Proje bazlı bu ayarı değiştirebiliriz.

```
git config --global user.name "Name Surname"
git config --global user.email "test@email.com"
```

`git config --list`        : Bütün konfigürasyon ayarlarını görmek için bu komut kullanılır.

` :q ` komutu komut satırına dönmemizi sağlar. 

---
**Not:** windows işletim sisteminde böyle bir hata ile karşılaşabiliriz. **"warning: LF will be replaced by CRLF in kaynak/dosya/yolu"**
Bu hatanın çözümü için; `git config core.autocrlf true`

---

`git add <dosya veya klasor_name>`          : Yeni eklenen veya üzerinde değişiklik yapılan dosyaları staged ortamına göndermek için kullanılır.    
`git add .` veya `git add *` veya `git add -A`  : Tek seferde bütün dosyaları eklemek için kullanılan komutlardır. Buradaki `-A` (all) tümü anlamındadır. `"."` ise tüm dosya uzantılarını ifade eder.  
`git rm`                   : Staged ortamına eklenmiş bir dosyanın takibinin bırakılmasını yani untracked hale getirilmesini sağlayan komuttur.     
`git rm --cached <dosya veya klasor_name>`  
`git rm <dosya veya klasor_name>` : Dosyayı klasörden silmek istiyorsak bu komut kullanılır.    
`git status`               : Üzerinde çalışılan bir projenin o anki durumu hakkında bilgi verir. Yapılan değişiklikler, eklenen ve silinen dosyalar gibi bilgileri listeler.

># git status Terimleri 

>**On branch main                :** Main branch'inde (dalında) olduğumuzu,  
**Changes to be commited        :** Commit'lenmeye hazır değişiklikler olduğunu,    
**Modified                      :** modified: index.html -> index.html dosyasında değişiklik yaptığımızı,   
**Deleted                       :** deleted: styles.css -> styles.css dosyasını sildiğimiz,     
**Changes not staged for commit :** Üzerinde değişiklik yapılan ama staged ortamına (add edilmemiş) gönderilmemiş dosyaları ifade eder.     
**Untracked files               :**  Takibi yapılmayan dosyaları ifade eder. 

>**git commit               :** Commit staged ortamına alınan (add edilen) dosyaların Local Repository' gönderilmesidir. En iyi uygulama yöntemi; her kayıt sırasında yapılan değişikliklere açıklayıcı bir mesaj eklemktir. Ayrıca her commit benzersiz bir kimliğe (Unique ID) sahip olur. Bu sayade eski bir commit'e geri dönülebilir ve herhangi bir kayıp yaşanmaz.   
**git commit -m "ilk commit mesajı" :** Buradaki -m (message) mesaj anlamındadır.

>**git log                  :** Proje commit geçmişimizi görüntülememizi sağlar. Bütün commit'ler; ID's, yazarı, tarihi ve mesajı ile beravber listelenir.

>**git branch               :** Local veya remote Repository üzerinden yeni bir branch (dal, kol, şube anlamına gelmektedir.) eklemek, silmek veya listelemek için kullanılır.   
Projeye yeni bir branch eklemek için; `git branch <branch_name>`
Tüm uzak ve yerel branch'ları listelemek için; git branch -a
Bir branch'ı silmek için; `git branch -d <branch_name>`

>**git checkout             :** Branch'lar arası veya commit'ler arası geçiş yapmak için kullanılır. 
Mevcutta var olan bir branch'a geçiş yapmak için; `git checkout <branch_name>`  
Yeni bir branch oluşturup bu branch'a geçmek için; `git checkout -b <branch_name>`  
Commit'ler arası geçiş yapmak için (Eski versiyona dönmek istenildiği zaman); `git checkout <commit_ID>`

>**git push --set-upstream origin <branch_name> :** Oluşturulan branch'ı uzak depoya (Remote Repository) kayıt etmek için kullanılan komuttur.   
**git merge                :** Başka bir branch'da olan değişiklikleri, bulunduğumuz branch ile birleştirmek için kullanılır.   
`git merge <branch_name>`

>**git clone                :** Mevcut bir Remote Repository'de bulunan dosyaların bilgisayarımıza kopyasının oluşturulmasını sağlar.
git clone <remote_URL>  

>**git push                 :** Projemizde aldığımız commit'leri, Remote Repository'e gönderir.  
`git push origin <branch_name>`     
>Burada belirtilen origin Remote Repository'nin kök dizinidir ve sabit bir isimdir. 

>**git pull                 :** Remote Repository'den Local Repository'ye güncel dosyaları çekmek için kullanırız.

>**git remote add origin https://github.com/cngzklc/Patika.Dev-Project1-GitKomutlari** : Bu komut ile local depoyu uzak depoya bağlanır.

>**git diff                 :** Repository üzerinde yapılan değişikliklerden sonra oluşan farkları gösterir.     
Çalışma dizini ile repository (HEAD) arasındaki farkları görmek için; `git diff HEAD`   
İki commit arasındaki farkları görmek için; `git diff <<commit_id_1>..<commit_id_2>>`   
Çalışma dizini ve staged ortamı arasındaki farkları görmek için; `git diff --staged`

## Kaynaklar

https://medium.com/fedeveloper/git-bash-ile-komut-komut-versiyonlama-a354efd3063f
https://www.jrebel.com/blog/git-cheat-sheet
http://guides.beanstalkapp.com/version-control/common-git-commands.html

># gitignore

.gitignore dosyası projemizin kök dizinine oluşturulan bir bir metin dosyasıdır. Bu dosya içerisinde yazdığımız dosya yolları veya uzantıları Remote Repository'e kayıt edilmeyerek başkaları ile paylaşması engellenebilir.

Başka başka projeler için her seferinde gitignore dosyası eklememek için;   
* Windows kullanıcısı iseniz C:\Users\{myusername}\ adresine giderek .gitignore_global dosyası oluşturup içerisine global olmasını istediğiniz dosyaları ekledikten sonra git bash terminalinizi açarak aşağıdakı komut ile konfigürasyon sağlayabilirsiniz.    
`git config --global core.excludesfile "%USERPROFILE%\.gitignore"`

* Dosyanızın doğru çalıştığını kontrol etmek için ise aşağıdaki komutu çalıştırarak aşağıdaki çıktıyı aldığınızda sorunsuz çalıştırabilmişsinizdir. (Aşağıdaki kodu kopyala yapıştır yapmadan önce kullanıcı adını değiştirin.)     

`git config --global core.excludesfile`     
`>C:/Users/user-name/.gitignore_global` 

* Son olarak hangi .gitignore dosyalarını eklemeliyim derseniz; buradan hangi dil, framework vs kullanıyorsanız ona ait .gitignore dosyalarını bulabilirsiniz. Global olarak düzenlemek istediğiniz .gitignore dosyalarına da buradan erişebilirsiniz.

>**gitignore Kaynaklar:**

https://docs.github.com/en/free-pro-team@latest/github/using-git/ignoring-files
https://www.pluralsight.com/guides/how-to-use-gitignore-file
http://git-scm.com/docs/gitignore
https://sebastiandedeyne.com/setting-up-a-global-gitignore-file/

