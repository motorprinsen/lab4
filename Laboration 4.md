# Laboration 4

## Continuous Integration

Med Continuous Integration menas att kod från sido-grenar i repot merge'as in i main-grenen med (oftast) ganska korta intervaller.
Upplägget kan skilja sig mellan team beroende på vald branch-strategi och annat.
Ju längre arbete som utförs i en dev-gren desto större blir risken att main-grenen har ändras så pass mycket sen man grenade av att merge-konflikter uppstår.
Dessa går ofta relativt enkelt att lösa, men ibland händer det att rätt komplicerade konflikter dyker upp (om t.ex. flera feature-team har ändrat mycket på samma ställe)
vilket då leder till att man kan behöva sammankalla alla inblandade för att gemensamt lösa konflikten.

Genom att istället försöka göra mindre merge'ningar ofta minskar man risken för detta.
Ett vanligt arbetsflöde är att utvecklaren grenar av koden, gör sina ändringar och verifierar att alla enhetstester går igenom lokalt _innan_ man skapar en PR mot main-grenen.
Vanligtvis har man sedan ett antal tester/checkar som går mot PR'en, och krav på att dessa ska gå igenom för att kunna göra en merge.
Efter detta granskas PR'en för att sedan merge'as in till main-grenen, där ytterligare tester körs.

Ibland händer det att vissa features måste merge'as in fastän de inte är helt färdiga 😮, och de inaktiveras då mha. feature-toggling innan koden rullas ut i produktion.

## Continuous Delivery

Continuous Delivery är att automatisera flödet från källkod till release-bar produkt där varje körning av ett flöde ska vara en förutsägbar och kontrollerad process.
Detta brukar innebära att koden byggs och paketeras för att sedan deployas till t.ex. en staging-miljö för vidare testning.
Ex: flödet bygger en container-image som push'as till ett registry för att sedan deployas ut i ett kluster.  
Det viktigt att varje utvecklare är medveten om att allt som comittas/merge'as till main-grenen potentiellt kan släppas ut till produktion nästan direkt.
För vårat är detta en kvalitetshöjande insikt. Ingen vill vara den som "sköt sönder prod" och därmed lägger man automatiskt mer tid på testning och validering innan man merge'ar in sin PR. 

## Continuous Deployment - ons

## Agila metoder - tors

## SCRUM - tors

## Kanban - tors

## SAFe - tors

## DevOps - fre

## QA (Quality Assurance) - fre

## Exempel på testverktyg + CI-verktyg som kan användas för att automatisera 

### Enhetstester - fre

### Integrationstester (API) - fre

### Systemtester - lör

### Acceptanstester - lör

### Ge exempel på ytterligare två typer av mjukvarutester och hur de kan genomföras (manuellt eller automatiserat) - lör

### Beskriv hur CI/CD kan användas tillsammans med olika branscher i ett repository för att skapa ett arbetsflöde för att utveckla, testa och publicera kod enligt en agil metod. Använd gärna illustration. - sön

## VG-del / reflekterande del

### Vad för olika typer av tester lämpar sig bra att automatisera och varför? - sön

### Vad för olika typer av tester lämpar sig mindre bra att automatisera och varför? - sön

### Vad är fördelar och nackdelar med avseende på kvalitetssäkring då DevOps används som metod? - mån

### Beskriv ett realistiskt exempel på valfri applikations livscykel utifrån testperspektiv och förklara vilka olika typer av tester som skulle kunna lämpa sig att implementera (gärna från hela “testpyramiden”). Beskriv även vilka av de testerna som skulle vara automatiserade respektive manuella. - mån
