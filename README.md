
# git-dersleri-2

Git Dersleri Config

Configurasiya siyahisi
git config --list 

User adi yaratmaq
git config --global user.name

User email yaratmaq
git config --global user.email

User adi ve mailin hansi olduguna baxmaq
git config --global user.name
git config --global user.email



////////////////////////////////////////////////


Git Repository

Her hansi papka daxilinde yazildiqda hemin papkani git repository edir.
git init

Papka icherisindeki fayli repository-ye elave etmek
git add fayladi


////////////////////////////////////////////////

Stage Area, git add, git status

Git ish yeri 3 hisseden ibaretdir.
Ish Yeri
Stage Bolmesi
Repository
Ish yerinde ishlenen fayli stage gondermek uchun
git add fayladi
Papkada olan butun fayllari stage gondermek uchun
git add .
istifade olunur. Ish yerinde ki fayllarin hansi bolmede oldugunu oyrenmek uchun
git status
yazilir bu zaman qirmizi olanlar ish yerinde qalan yeni ki add olmayan, yashil olanlar ise stage bolmesinde olanlardir. Yashil rengde olanlar novbeti defe commit ile repo-ya gonderilecek, ya da stage bolmesinden ayirmaq uchun
git rm --cached fayladi  (faylt uchun)
git rm -r --cached .  (papka uchun)

Stagde olan her hansi file -i ish yerinde deyishdikde ve git status dedikde hemin faylin hem statusda yashil hem de modified qirmizi halda oldugu gorunur eger git add olmadan commit olarsa evvelki stage commit olacaq ve yeni deyishiklik add olunmayinca commit uchun hazir olmayacaq


////////////////////////////////////////////////


Git Commit

Commit emeliyyati uchun
git commit - m "Commit haqqinda melumat"
istifade olunur.
git log
ile evvelki commitlere aid melumamtlar chixardilir.

git log --oneline
loglari 1 setrde gosterir daha seligeli


////////////////////////////////////////////////


Gir Reset

 git reset logid --hard
log idni git log commandi ile aliriq ve ya git log --oneline --hard bayragi  ile logidnin gosterildiyi yere qayitdiqda onnan sonra olan versiyalar  silinir

  git reset logid --soft
commandi çalışdıqda log id olan yerə qayıdır ancaq stage -da qalır və commiti gözləyir.

 git revert  logid
burada  logda commit olunmush text qalir ancaq commit olunan deyishiklik legv olur. Burada meqsed her hansi versiyada her hansi deyishikliyi evvele almaq

git commit --amend -m "title"
bu command ile son commit olunan mesaji deyishmek olur

git commit --amend
Eger son commit -den sonra yeni deyishiklik olmushsa ve bu deyishikliyi evvelki commite birleshdirmek isteyirikse bu commanddan istifade edirik.

////////////////////////////////////////////////


Git Branch

Git repository yaradilarken yalnizca master brach olur. Yeni brach yaratma uchun

git brach brachadi
istifade olunur

git checkout brachadi
ile oldugumuz brachdan digerine kechid edirik, qisa olaraq ashagidaki command ile de hem brach yaradib hem de o bracha deyishmek mumkundur
git checkout  -b brachadi

Eger yeni yaradilan brachda her hansi etdiyimiz deyishiklik ve ya elave hemin brachda commit edildikden sonra  diger branchlara kechilerken gorunmur. Yeni yaranan branchi silmek uchun

git branch -d branchadi
istifade olunur,  eger hemin branch marge olunmayibsa bashqa bir branch ile warning verir. Eger hard delete etmek isteyirikse d herfini boyuk yaziriq.
Branch larin siyahisina baxmaq uchun

git branch -a
istifade olunur.
Branchlari birleshdirmek uchun , birleshmek istediyimiz branchi aktiv edib

git marge branchadi
deyirik

/////////////////////////////////////////////////


Github push


