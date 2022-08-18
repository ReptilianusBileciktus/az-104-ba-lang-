# Az-104 Sınavına Hazırlık

## Azure portalı
**Azure portalı** , basit web uygulamalarından karmaşık bulut uygulamalarına kadar her şeyi tek bir birleşik konsolda oluşturmanıza, yönetmenize ve izlemenize olanak tanır.
## Azure Cloud Shell
Azure Cloud Shell, Azure kaynaklarını yönetmek için etkileşimli, tarayıcı tarafından erişilebilir bir kabuktur. Çalışma şeklinize en uygun kabuk deneyimini seçme esnekliği sağlar. Linux kullanıcıları bir Bash deneyimini seçebilirken, Windows kullanıcıları PowerShell'i seçebilir.

## Azure Cloud Shell özellikleri
-   Geçicidir ve yeni veya mevcut bir Azure Dosyaları paylaşımının bağlanmasını gerektirir.
- Kaynaklarınıza anında erişim için otomatik olarak kimlik doğrulaması yapar.
- Etkileşimli etkinlik olmadan 20 dakika sonra zaman aşımına uğrar.
- Bir kaynak grubu, depolama hesabı ve Azure Dosya paylaşımı gerektirir.
- Hem Bash hem de PowerShell için aynı Azure dosya paylaşımını kullanır.
- İzinler, Bash'te normal bir Linux kullanıcısı olarak ayarlanır.

## Azure PowerShell
Azure PowerShell, Azure aboneliğinize bağlanmanıza ve kaynakları yönetmenize olanak sağlamak için Windows PowerShell veya PowerShell Core'a eklediğiniz bir modüldür. 

ÖRNEK
>New-AzVm `
>
    -ResourceGroupName "CrmTestingResourceGroup" `
    -Name "CrmUnitTests" `
    -Image "UbuntuLTS"
    ...
**Az modülü nedir?**
**Az** , Azure özellikleriyle çalışmak için cmdlet'leri içeren Azure PowerShell modülünün resmi adıdır. Her Azure kaynağının neredeyse her yönünü denetlemenize olanak tanıyan yüzlerce cmdlet içerir. Aşağıdaki özelliklerle ve daha fazlasıyla çalışabilirsiniz:

-   Kaynak grupları
-   Depolamak
-   sanal makineler
-   Azure AD
-   Konteynerler
-   Makine öğrenme

## Azure CLI

Azure CLI, Azure'a bağlanmak ve Azure kaynaklarında yönetim komutları yürütmek için kullanılan bir komut satırı programıdır. Linux, macOS ve Windows üzerinde çalışır ve yöneticilerin ve geliştiricilerin komutlarını bir web tarayıcısı yerine bir terminal, komut satırı istemi veya komut dosyası aracılığıyla yürütmelerine olanak tanır. Örneğin, bir sanal makineyi yeniden başlatmak için aşağıdaki gibi bir komut kullanırsınız:
>az vm restart -g MyResourceGroup -n MyVm
>
CLI'deki komutlar, _gruplar_ ve _alt_ gruplar halinde yapılandırılmıştır . Her grup, Azure tarafından sağlanan bir hizmeti temsil eder ve alt gruplar, bu hizmetler için komutları mantıksal gruplara böler. Örneğin grup, **hesap** , **blob** , **paylaşım** ve **kuyruk**`storage` dahil olmak üzere alt gruplar içerir .

Peki, ihtiyacınız olan belirli komutları nasıl bulacaksınız? Örneğin, bir depolama bloğunu yönetmenize yardımcı olabilecek komutları bulmak istiyorsanız aşağıdaki find komutunu kullanabilirsiniz: 
>az find blob

İstediğiniz komutun adını zaten biliyorsanız, bu komutun `--help`argümanı size komut hakkında ve bir komut grubu için mevcut alt komutların bir listesi hakkında daha ayrıntılı bilgi verecektir. Örneğin, blob depolamayı yönetmek için alt grupların ve komutların listesini şu şekilde alabilirsiniz:
>az storage blob --help

## Örnek Sorular

1.Şirketiniz, kullanıcı tarafından oluşturulan video içeriği için çevrimiçi depolama sunacak bir video düzenleme uygulaması geliştiriyor. Videolar Azure Bloblarında depolanacak. Bir Azure depolama hesabı, blobları içerecektir. Tüm kullanıcı videolarını sileceğinden, depolama hesabının kaldırılması ve yeniden oluşturulması pek olası değildir. Depolama hesabını oluşturmanın en hızlı ve en kolay yolu nedir ?


	**A-  Azure portalı**
	
	
	**B- Azure PowerShell**
	
	
	**C- Azure CLı**

>**Azure Portal**, uzun ömürlü bir depolama hesabı oluşturmak gibi tek seferlik işlemler için iyi bir seçimdir. Portal, tüm depolama hesabı özelliklerini içeren bir GUI sağlar ve kuruluşun ihtiyaçları için doğru seçeneklerin seçilmesine yardımcı olacak araç ipuçları sağlar.

2.Azure CLI aşağıdakilerden hangisine yüklenebilir?


**A- Linux**


**B- Windows**


**C- Hem Linux hemde Windows**
>CLI ;
> Linux, macOS ve Windows'a kurulabilir.

3.Bir kullanıcı azure powershell kullanmaya karar verdiğinde ilk olarak hangi komutu çalıştırmalıdır.

**A- Connect-AzAccount**

**B- Get-AzResourceGroup**

**C- Get-AzSubscription**

>Yapılacak ilk şey Azure'a bağlanmak ve kullanıcı kimlik bilgilerini sağlamaktır.

