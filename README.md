# admin-toolbox

Sahada iş yaparken yazdığım Bash ve PowerShell scriptleri, bir de ufak araçlar.
Çoğu belli bir işi çözmek için çıktı; işime yaradıkça buraya ekliyorum.

## İçerik

| Klasör | Ne var |
|---|---|
| [`bash/`](bash/) | Linux / macOS scriptleri |
| [`powershell/`](powershell/) | Windows, Active Directory ve benzeri işler için scriptler |
| [`tools/`](tools/) | Tek script'e sığmayan küçük araçlar |

Her scriptin başında ne yaptığı, hangi parametreleri aldığı ve nasıl çalıştırılacağı yazıyor.

## Scriptler

| Script | Ne yapar |
|---|---|
| [`powershell/AD-Guvenlik-Denetimi.ps1`](powershell/AD-Guvenlik-Denetimi.ps1) | Active Directory'de 55 temel güvenlik kontrolü (Kerberoasting, AS-REP, inaktif ve devre dışı hesaplar, yetki devri, LAPS, parola politikası, DC'lerde TLS 1.0/1.1, SMBv1, SMB imzalama, NTLMv1, LDAP imzalama, ADCS şablon ve CA kontrolleri ESC1-4, 6-9, 15, DCSync ve AdminSDHolder ACL'leri...). Salt okunur, sonuçları CSV ve özet olarak yazar. |
| [`bash/wazuh-ajan-durumu.sh`](bash/wazuh-ajan-durumu.sh) | Wazuh API'sinden bütün ajanları çekip sorunlu olanları listeler: bağlantısı kopmuş, uzun süredir gelmeyen (silme adayı), hiç bağlanmamış, sürümü yöneticiden eski, gruba atanmamış, grup yapılandırması senkron olmayan, IP'si başka ajanla çakışan. Salt okunur, CSV ve özet yazar; bulgu varsa 2 ile çıkar, cron ya da izleme sisteminden çağrılabilir. |

## Kullanım

```bash
git clone https://github.com/fatihyuksektepe/admin-toolbox.git
cd admin-toolbox
```

Bash:

```bash
chmod +x bash/script-adi.sh
./bash/script-adi.sh --help
```

PowerShell:

```powershell
Get-Help .\powershell\Script-Adi.ps1 -Full
.\powershell\Script-Adi.ps1
```

İnternetten indirilen `.ps1` dosyalarını Windows engelleyebilir. Scripti okuyup güvendiysen
`Unblock-File .\powershell\Script-Adi.ps1` ile açabilirsin.

## Uyarı

Scriptleri çalıştırmadan önce oku, mümkünse önce test ortamında dene. Bazıları sistem
ayarlarını, kullanıcıları ya da dosyaları değiştiriyor. Kendi ortamında çalıştırmanın
sorumluluğu sende.

## Katkı

Hata bulursan ya da bir öneri varsa issue açabilirsin.

## Lisans

[GPL-3.0](LICENSE). Değiştirip dağıtabilirsin; dağıttığın sürüm de GPL-3.0 altında kalmalı.
