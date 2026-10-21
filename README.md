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
