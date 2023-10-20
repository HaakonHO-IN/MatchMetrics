
**To Do**
-finne på spørsmål
-koble disse spørsmålene sammen, og få et midlertidig svar
-komme med fler spørsmål
-lage et score system som skal bli brukt til resultat
-lage en side der resultat kommer opp
-skrive informasjon "om oss"
-fikse på utseende med hjelp av css




**MatchMetrics**
min nettside er en nettside der du skal sjekke om du matcher med meg. denne siden er inspirert av [denne nettsiden](https://kamelrechner.eu/en). Du skal svare på noen spørsmål og få en poengsum, dette vil svare på om du er en match med meg eller ikke. men jeg fikk problemmer emd poeng summen og fikk det ikke til, derfor er den ikke helt ferdig. Nettsiden består av at du må svare på noen spørsemål om deg selv, og jo næremere du er min fasit(det jeg mener), jo større match er du.

**design**
Jeg rakk ikke å lage noe design til nettsiden, siden jeg brukte for lang tid til å prøve å fikse poeng tellingen 
**Hva mangler**
det som mangler er en css, og at alle inputene, og variablene har en value og at dette setter opp til et poeng system. jeg mangler også å skrive om meg selv, og hvem som har lagd nettsiden. Hvis jeg skulle gjordt noe annerledes hadde jeg ikke brukt for lang tid å prøve på poengsystemet, og brukt mer tid til å få den til å se bedre ut. resten av oppgaven er jeg ganske fornøyd med. 
```js

// store.js
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)

