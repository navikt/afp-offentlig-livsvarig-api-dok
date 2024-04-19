# AFP Offentlig Livsvarig
Dokumenterer sammenhengen mellom APIer eksponert fra NAV til samhandlere i forbindelse med AFP Offentlig Livsvarig (for de som er født fra og med 1963)

AFP Offentlig livsvarig er en ytelse som tjenestepensjonsordningene har behandlingsansvar for, men de trenger informasjon fra NAV for å kunne vilkårsvurdere og beregne ytelsen.

## Vilkårsvurdering
For å kunne vilkårsvurdere AFP Offentlig Livsvarig trenger tjenestepensjonsordrningene følgende informasjon fra NAV:
* For unntak av tidskrav om sammenhengende ansettelse: 
  * [Perioder med sykepenger](https://spapi.ekstern.dev.nav.no/swagger)
  * [Perioder med arbeidsavklaringspenger](https://aap-api.ekstern.dev.nav.no/swagger)
  * [Perioder med uføreutbetalinger](https://navikt.github.io/pensjon-ekstern-api/api/uforetrygd/Uforetrygd.html#/default/uforeperioder)
* For kravet til at man ikke kan ha løpende AFP Privat og AFP Offentlig Livsvarig:
  * [Informasjon om bruker har løpende AFP Privat](https://navikt.github.io/pensjon-ekstern-api/api/afpprivat/AfpPrivat.html)
* For kravet at man ikke kan ha fått uføretrygd utbetalt etter fylte 62 år:
  * [Informasjon om bruker har fått uføretrygd utbetalt etter fylte 62 år](https://navikt.github.io/pensjon-ekstern-api/api/uforetrygd/Uforetrygd.html#/default/harMottattUforeEtter62)

## Beregning
For å kunne beregne AFP Offentlig Livsvarig, trenger tjenestepensjonsordningene følgende informasjon fra NAV:
* Pensjonsbeholdning medregnet opptjening til og med det 61. året:
  * [AFP Offentlig Livsvarig Beholdning grunnlag](https://navikt.github.io/pensjon-ekstern-api/api/afpgrunnlagbeholdning/afp-grunnlag-beholdning.html#/default/beregn)

## Simulering
I tillegg til APIer for saksbehandling av AFP Offentlig Livsvarig, trenger tjenestepensjonsordningene informasjon om simulert AFP Beholdning grunnlag, basert på antatt inntekt frem til uttak:
* [Simulert AFP Offentlig Livsvarig grunnlag](https://navikt.github.io/pensjon-ekstern-api/api/afpgrunnlagbeholdning/afp-grunnlag-beholdning.html#/default/simuler)

Det blir også utviklet nye API for simulereringer som tar hensyn til AFP Offentlig Livsvarig for denne brukergruppen (de som er født fra og med 1963), og som tjenestepensjonsordningene kan bruke feks i sine pensjonskalkulatorer:
* [Simuler Alderspensjon fra folketrygden](https://pensjonssimulator.ekstern.dev.nav.no/swagger-ui/index.html#/alderspensjon-controller/simulerFolketrygdbeholdning)
* [Simulert Folketrygdbeholdning](https://pensjonssimulator.ekstern.dev.nav.no/swagger-ui/index.html#/beholdning-controller/simulerFolketrygdbeholdning_1)
* [Simulert tidlisgst mulige uttak](https://pensjonssimulator.ekstern.dev.nav.no/swagger-ui/index.html#/uttak-controller/tidligstMuligUttak)