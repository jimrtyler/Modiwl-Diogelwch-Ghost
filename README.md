# 👻 Modiwl Diogelwch Ghost
**Offeryn Caledu Diogelwch Windows a Azure yn seiliedig ar PowerShell**

> **Caledu diogelwch rhagweithiol ar gyfer pwyntiau terfynu Windows ac amgylcheddau Azure.** Mae Ghost yn darparu swyddogaethau caledu sy'n seiliedig ar PowerShell a all helpu i leihau fectorau ymosod cyffredin trwy analluogi gwasanaethau a photocol diangen.

## ⚠️ Datganiadau Ymwrthod Pwysig

**MAE ANGEN PROFI**: Profwch Ghost bob amser mewn amgylcheddau nad ydynt yn gynhyrchiol yn gyntaf. Gall analluogi gwasanaethau effeithio ar swyddogaethau busnes cyfreithlon.

**DIM GWARANTAU**: Er bod Ghost yn targedu fectorau ymosod cyffredin, ni all unrhyw offeryn diogelwch atal pob ymosodiad. Mae hwn yn un elfen o strategaeth diogelwch gynhwysfawr.

**EFFAITH WEITHREDOL**: Gall rhai swyddogaethau effeithio ar swyddogaeth y system. Adolygwch bob gosodiad yn ofalus cyn ei ddefnyddio.

**ASESIAD PROFFESIYNOL**: Ar gyfer amgylcheddau cynhyrchiol, ymgynghorwch ag arbenigwyr diogelwch i sicrhau bod gosodiadau'n cyd-fynd ag anghenion eich sefydliad.

## 📊 Y Dirwedd Diogelwch

Cyrhaeddodd difrod Ransomware **$57 biliwn yn 2025**, gydag ymchwil yn dangos bod llawer o ymosodiadau llwyddiannus yn manteisio ar wasanaethau Windows sylfaenol a chamgyfosodiadau. Mae fectorau ymosod cyffredin yn cynnwys:

- Mae **90% o ddigwyddiadau ransomware** yn cynnwys ecsbloetio RDP
- **Gwendidau SMBv1** a alluogodd ymosodiadau fel WannaCry a NotPetya
- Mae **macros dogfennau** yn parhau i fod yn brif ddull dosbarthu malware
- Mae **ymosodiadau sy'n seiliedig ar USB** yn parhau i dargedu rhwydweithiau ag aer-fwlch
- Mae **cam-ddefnydd PowerShell** wedi cynyddu'n sylweddol yn y blynyddoedd diweddar

## 🛡️ Swyddogaethau Diogelwch Ghost

Mae Ghost yn darparu **16 o swyddogaethau caledu Windows** ynghyd ag **integreiddio diogelwch Azure**:

### Caledu Pwyntiau Terfynu Windows

| Swyddogaeth | Diben | Ystyriaethau |
|----------|---------|----------------|
| `Set-RDP` | Rheoli mynediad Bwrdd Gwaith Pell | Gall effeithio ar weinyddu o bell |
| `Set-SMBv1` | Rheoli protocol SMB etifeddol | Angenrheidiol ar gyfer systemau hen iawn |
| `Set-AutoRun` | Rheoli AutoPlay/AutoRun | Gall effeithio ar gyfleustra defnyddiwr |
| `Set-USBStorage` | Cyfyngu dyfeisiau storio USB | Gall effeithio ar ddefnydd USB cyfreithlon |
| `Set-Macros` | Rheoli gweithrediad macros Office | Gall effeithio ar ddogfennau sy'n galluogi macros |
| `Set-PSRemoting` | Rheoli PowerShell remoting | Gall effeithio ar reolaeth bell |
| `Set-WinRM` | Rheoli Windows Remote Management | Gall effeithio ar weinyddu o bell |
| `Set-LLMNR` | Rheoli protocol datrys enwau | Yn gyffredinol yn ddiogel i'w analluogi |
| `Set-NetBIOS` | Rheoli NetBIOS dros TCP/IP | Gall effeithio ar gymwysiadau etifeddol |
| `Set-AdminShares` | Rheoli rhaniadau gweinyddol | Gall effeithio ar fynediad ffeil o bell |
| `Set-Telemetry` | Rheoli casglu data | Gall effeithio ar alluoedd diagnostig |
| `Set-GuestAccount` | Rheoli cyfrif gwestai | Yn gyffredinol yn ddiogel i'w analluogi |
| `Set-ICMP` | Rheoli ymatebion ping | Gall effeithio ar ddiagnosteg rhwydwaith |
| `Set-RemoteAssistance` | Rheoli Cymorth o Bell | Gall effeithio ar weithrediadau helpdesk |
| `Set-NetworkDiscovery` | Rheoli darganfod rhwydwaith | Gall effeithio ar bori rhwydwaith |
| `Set-Firewall` | Rheoli Firewall Windows | Hanfodol ar gyfer diogelwch rhwydwaith |

### Diogelwch Cwmwl Azure

| Swyddogaeth | Diben | Gofynion |
|----------|---------|--------------|
| `Set-AzureSecurityDefaults` | Galluogi diogelwch Azure AD sylfaenol | Caniatâd Microsoft Graph |
| `Set-AzureConditionalAccess` | Ffurfweddu polisiau mynediad | Trwyddedu Azure AD P1/P2 |
| `Set-AzurePrivilegedUsers` | Archwilio cyfrifon breintiedig | Caniatâd Global Admin |

### Opsiynau Defnyddio Menter

| Dull | Achos Defnydd | Gofynion |
|--------|----------|--------------|
| **Gweithrediad Uniongyrchol** | Profi, amgylcheddau bach | Hawliau gweinyddwr lleol |
| **Group Policy** | Amgylcheddau parth | Gweinyddwr parth, rheoli GP |
| **Microsoft Intune** | Dyfeisiau a reolir gan gwmwl | Trwyddedu Intune, Graph API |

## 🚀 Dechrau Cyflym

### Asesu Diogelwch
```powershell
# Llwytho modiwl Ghost
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')

# Gwirio agwedd diogelwch bresennol
Get-Ghost
```

### Caledu Sylfaenol (Profwch yn Gyntaf)
```powershell
# Caledu hanfodol - profwch mewn amgylchedd labordy yn gyntaf
Set-Ghost -SMBv1 -AutoRun -Macros

# Adolygu newidiadau
Get-Ghost
```

### Defnyddio Menter
```powershell
# Defnyddio Group Policy (amgylcheddau parth)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Defnyddio Intune (dyfeisiau a reolir gan gwmwl)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 Dulliau Gosod

### Opsiwn 1: Lawrlwytho Uniongyrchol (Profi)
```powershell
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')
```

### Opsiwn 2: Gosod Modiwl
```powershell
# Gosod o PowerShell Gallery (pan fo ar gael)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### Opsiwn 3: Defnyddio Menter
```powershell
# Copïo i leoliad rhwydwaith ar gyfer defnyddio Group Policy
# Ffurfweddu sgriptiau Intune PowerShell ar gyfer defnyddio cwmwl
```

## 💼 Enghreifftiau Achosion Defnydd

### Busnes Bach
```powershell
# Amddiffyniad sylfaenol gydag effaith leiaf
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### Amgylchedd Gofal Iechyd
```powershell
# Caledu wedi'i ganolbwyntio ar HIPAA
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### Gwasanaethau Ariannol
```powershell
# Ffurfweddiad diogelwch uchel
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Sefydliad Cwmwl-Gyntaf
```powershell
# Defnyddio a reolir gan Intune
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 Manylion Swyddogaethau

### Swyddogaethau Caledu Craidd

#### Gwasanaethau Rhwydwaith
- **RDP**: Rhwystro mynediad bwrdd gwaith pell neu hap-drefnu porth
- **SMBv1**: Analluogi protocol rhannu ffeiliau etifeddol
- **ICMP**: Atal ymatebion ping ar gyfer reconnaissance
- **LLMNR/NetBIOS**: Rhwystro protocolau datrys enwau etifeddol

#### Diogelwch Cymhwysiad
- **Macros**: Analluogi gweithrediad macros mewn cymwysiadau Office
- **AutoRun**: Atal gweithrediad awtomatig o gyfryngau symudadwy

#### Rheolaeth Bell
- **PSRemoting**: Analluogi sesiynau PowerShell pell
- **WinRM**: Stopio Windows Remote Management
- **Remote Assistance**: Rhwystro cysylltiadau cymorth pell

#### Rheolaeth Mynediad
- **Admin Shares**: Analluogi rhaniadau C$, ADMIN$
- **Guest Account**: Analluogi mynediad cyfrif gwestai
- **USB Storage**: Cyfyngu defnydd dyfais USB

### Integreiddio Azure
```powershell
# Cysylltu â thenant Azure
Connect-AzureGhost -Interactive

# Galluogi diofyniadau diogelwch
Set-AzureSecurityDefaults -Enable

# Ffurfweddu mynediad amodol
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# Archwilio defnyddwyr breintiedig
Set-AzurePrivilegedUsers -AuditOnly
```

### Integreiddio Intune (Newydd yn v2)
```powershell
# Cysylltu ag Intune
Connect-IntuneGhost -Interactive

# Defnyddio trwy bolisiau Intune
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ Ystyriaethau Pwysig

### Gofynion Profi
- **Amgylchedd Labordy**: Profwch yr holl osodiadau mewn amgylchedd ynysig yn gyntaf
- **Defnyddio Graddol**: Ehangwch yn raddol i adnabod problemau
- **Cynllun Rhôl-nôl**: Sicrhewch y gallwch wrthdroi newidiadau os oes angen
- **Dogfennaeth**: Cofnodwch pa osodiadau sy'n gweithio ar gyfer eich amgylchedd

### Effaith Bosibl
- **Cynhyrchedd Defnyddiwr**: Gall rhai gosodiadau effeithio ar lif gwaith dyddiol
- **Cymwysiadau Etifeddol**: Efallai y bydd angen protocolau penodol ar systemau hŷn
- **Mynediad Pell**: Ystyriwch yr effaith ar weinyddu pell cyfreithlon
- **Prosesau Busnes**: Gwirio nad yw gosodiadau'n torri swyddogaethau critigol

### Cyfyngiadau Diogelwch
- **Amddiffyn Dwfn**: Mae Ghost yn un haen o ddiogelwch, nid ateb cyflawn
- **Rheolaeth Barhaus**: Mae angen monitro a diweddaru'n barhaus ar ddiogelwch
- **Hyfforddiant Defnyddiwr**: Rhaid cyfuno rheolaeth dechnegol ag ymwybyddiaeth diogelwch
- **Esblygiad Bygythiad**: Gall dulliau ymosod newydd fynd heibio amddiffyniad presennol

## 🎯 Enghreifftiau Senarios Ymosod

Er bod Ghost yn targedu fectorau ymosod cyffredin, mae atal penodol yn dibynnu ar weithrediad a phrofi priodol:

### Ymosodiadau Math WannaCry
- **Lliniaru**: Mae `Set-Ghost -SMBv1` yn analluogi'r protocol bregus
- **Ystyriaeth**: Sicrhewch nad oes unrhyw system etifeddol angen SMBv1

### Ransomware sy'n seiliedig ar RDP
- **Lliniaru**: Mae `Set-Ghost -RDP` yn rhwystro mynediad bwrdd gwaith pell
- **Ystyriaeth**: Efallai y bydd angen dulliau mynediad pell amgen

### Malware sy'n seiliedig ar Ddogfennau
- **Lliniaru**: Mae `Set-Ghost -Macros` yn analluogi gweithrediad macros
- **Ystyriaeth**: Gall effeithio ar ddogfennau sy'n galluogi macros cyfreithlon

### Bygythiadau a ddosberthir gan USB
- **Lliniaru**: Mae `Set-Ghost -USBStorage -AutoRun` yn cyfyngu swyddogaeth USB
- **Ystyriaeth**: Gall effeithio ar ddefnydd dyfais USB cyfreithlon

## 🏢 Nodweddion Menter

### Cefnogaeth Group Policy
```powershell
# Cymhwyso gosodiadau trwy gofrestr Group Policy
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# Mae gosodiadau'n cymhwyso ar draws y parth ar ôl adnewyddu GP
gpupdate /force
```

### Integreiddio Microsoft Intune
```powershell
# Creu polisiau Intune ar gyfer gosodiadau Ghost
Set-IntuneGhost -Settings $GhostSettings -Interactive

# Mae polisiau'n defnyddio'n awtomatig i ddyfeisiau a reolir
```

### Adrodd Cydymffurfiaeth
```powershell
# Cynhyrchu adroddiad asesu diogelwch
Get-Ghost | Export-Csv -Path "Archwiliad-Diogelwch-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Adroddiad agwedd diogelwch Azure
Get-AzureGhost | Out-File "Adroddiad-Diogelwch-Azure.txt"
```

## 📚 Arferion Gorau

### Cyn Defnyddio
1. **Dogfennu Cyflwr Presennol**: Rhedwch `Get-Ghost` cyn newidiadau
2. **Profi'n Drylwyr**: Dilysu mewn amgylchedd nad yw'n gynhyrchiol
3. **Cynllunio Rhôl-nôl**: Gwybod sut i wrthdroi pob gosodiad
4. **Adolygiad Rhandeiliaid**: Sicrhau bod unedau busnes yn cymeradwyo newidiadau

### Yn ystod Defnyddio
1. **Dull Graddol**: Defnyddio i grwpiau peilot yn gyntaf
2. **Monitro Effaith**: Gwylio am gwynion defnyddwyr neu broblemau system
3. **Dogfennu Problemau**: Cofnodi unrhyw broblemau ar gyfer cyfeirio yn y dyfodol
4. **Cyfathrebu Newidiadau**: Hysbysu defnyddwyr am welliannau diogelwch

### Ar ôl Defnyddio
1. **Asesu Rheolaidd**: Rhedeg `Get-Ghost` yn gyfnodol i wirio gosodiadau
2. **Diweddaru Dogfennaeth**: Cadw ffurfweddiadau diogelwch yn gyfredol
3. **Adolygu Effeithiolrwydd**: Monitro digwyddiadau diogelwch
4. **Gwelliant Parhaus**: Addasu gosodiadau yn seiliedig ar dirwedd bygythiad

## 🔧 Datrys Problemau

### Problemau Cyffredin
- **Gwallau Caniatâd**: Sicrhewch sesiwn PowerShell uwchradd
- **Dibyniaethau Gwasanaeth**: Gall fod gan rai gwasanaethau ddibyniaethau
- **Cydnawsedd Cymhwysiad**: Profwch gyda chymwysiadau busnes
- **Cysylltedd Rhwydwaith**: Gwirio bod mynediad pell yn dal i weithio

### Opsiynau Adfer
```powershell
# Ail-alluogi gwasanaethau penodol os oes angen
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 Am yr Awdur

**Jim Tyler** - Microsoft MVP ar gyfer PowerShell
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ tanysgrifiwr)
- **Cylchlythyr**: [PowerShell.News](https://powershell.news) - Cudd-wybodaeth ddiogelwch wythnosol
- **Awdur**: "PowerShell for Systems Engineers"
- **Profiad**: Degawdau o awtomeiddio PowerShell a diogelwch Windows

## 📄 Trwydded ac Ymwrthod

### Trwydded MIT
Darperir Ghost o dan Drwydded MIT ar gyfer defnydd rhad, addasu a dosbarthu.

### Ymwrthod Diogelwch
- **Dim Gwarant**: Darperir Ghost "fel y mae" heb warant o unrhyw fath
- **Profi'n Angenrheidiol**: Profwch bob amser mewn amgylcheddau nad ydynt yn gynhyrchiol yn gyntaf
- **Arweiniad Proffesiynol**: Ymgynghorwch ag arbenigwyr diogelwch ar gyfer defnyddiadau cynhyrchiol
- **Effaith Weithredol**: Nid yw'r awduron yn gyfrifol am unrhyw darfu gweithredol
- **Diogelwch Cynhwysfawr**: Mae Ghost yn elfen o strategaeth ddiogelwch gyflawn

### Cymorth
- **GitHub Issues**: [Adrodd bygiau neu ofyn am nodweddion](https://github.com/jimrtyler/Ghost/issues)
- **Dogfennaeth**: Defnyddiwch `Get-Help <function> -Full` ar gyfer cymorth manwl
- **Cymuned**: Fforymau cymuned PowerShell a diogelwch

---

**🔒 Cryfhewch eich agwedd ddiogelwch gyda Ghost - ond profwch bob amser yn gyntaf.**

```powershell
# Dechreuwch gydag asesu, nid tybiaethau
Get-Ghost
```

**⭐ Rhowch seren i'r ystorfa hon os yw Ghost yn helpu gwella eich agwedd ddiogelwch!**