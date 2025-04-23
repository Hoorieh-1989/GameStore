# 🚀 Deploymentdokumentation: Gamestore på Azure App Service

Detta dokument beskriver steg-för-steg hur jag har klonat, testat, deployat och säkrat webbapplikationen Gamestore på Azure App Service.
---

## 1. 💻 Klona och testa applikationen lokalt

1. Klona GitHub-repot till dator
   
2. Öppna projektet i Visual Studio.
   
2. Kör applikationen lokalt för att säkerställa att allt fungerar innan deployment.

---

## 2. ☁️ Skapa Azure App Service & publicera applikationen

### 🔐 Logga in på Azure


### 🛠️ Skapa resurser via CLI



### 📦 Alternativt via Azure Portal:
1. Gå till "Skapa en resurs" > "Webb" > "Webbapp".
2. Fyll i nödvändiga uppgifter: resursgrupp, namn, region, plan etc.

### 🔄 Automatisera deployment via GitHub:
1. Gå till din App Service i Azure Portal.
2. Välj **Deployment Center** och koppla till  GitHub-repo.
3. Välj **GitHub Actions** för automatiserad deployment.



---

## 3. 📊 Aktivera Application Insights

1. I Azure Portal, öppna din App Service.
2. Gå till **Application Insights** och klicka på **Aktivera**.
3. Skapa eller koppla en befintlig instans.
4. Verifiera data via **Live Metrics** eller **Loggar**.

---

## 4. 🔒 Implementera grundläggande säkerhet

### 👥 IAM (Identity and Access Management):
1. Navigera till App Service > **Åtkomstkontroll (IAM)**.
2. Lägg till eller ta bort användare/roller för att styra åtkomst.

### 🌐 SSL (HTTPS):
1. Gå till **TLS/SSL-inställningar**.
2. Aktivera **HTTPS Only** för säker trafik.
3. Gratis SSL-certifikat för `azurewebsites.net` domäner ingår.

---

## 5. 📋 Dokumentation av processen

✅ Klona repot och testa lokalt  
✅ Skapa App Service och resurser i Azure  
✅ Koppla GitHub-repo & GitHub Actions  
✅ Aktivera Application Insights  
✅ Implementera IAM, miljövariabler & SSL  
✅ Verifiera funktion & säkerhet i produktion  

---

## ✅ Sammanfattning

- 🌐 Applikationen är live på Azure App Service  
- 📈 Application Insights samlar in loggar och prestandadata  
- 🔐 Säkerheten är förbättrad med IAM, miljövariabler och SSL  

---

## 🚧 Utmaningar och hinder

### 🧩 Utvecklingsmiljö & .NET-installation
- Jag började i VS Code, men insåg snabbt att rätt versioner av .NET SDK och runtime saknades.
- Installationen och konfigurationen i VS Code var tidskrävande, och vissa funktioner fungerade inte som förväntat.

#### 🔄 Lösning:
- Jag bytte till Visual Studio, där allt fungerade direkt.
- Jag kunde köra och testa applikationen utan problem.

---

### 🔁 CI/CD med Azure DevOps
- Jag försökte sätta upp en CI/CD-pipeline med Azure DevOps, men fick problem med kopplingen mellan GitHub och DevOps.
- Trots flera försök fungerade inte deploymenten automatiskt som tänkt via Azure DevOps.

---

### 💸 Valde fel App Service-plan
- Jag råkade välja en App Service-plan (B1) som kostar pengar – något jag inte märkte först. Detta gjorde att det började ticka kostnader på mitt Azure-konto.

#### 🧨 Lösning:
- När jag var klar med testningen och deploymenten tog jag bort hela resursgruppen från Azure för att undvika fortsatt debitering.

---

### ⚠️ Glöm inte:
- **Använd kostnadsfria resurser om du bara testar!**
- **Radera resursgruppen när du är klar för att slippa onödiga avgifter!**


🧾 Denna README fungerar som komplett dokumentation.
