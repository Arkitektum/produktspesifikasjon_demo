#### Arealplan

dataobjekt for igangsatt planlegging etter plan- og bygningsloven, slik det formidles i OGC API-Features fra Direktoratet for byggkvalitet

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>objid</td>
      <td>tjenestens interne identifikator for objektet (feature-id i OGC API)<br />OGC-rolle: id</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>nasjonal<wbr />Arealplan<wbr />Id</td>
      <td>landsdekkende entydig og unik identifikasjon av en arealplan (pbl. §§ 6-4, 9-1 og 12-1, samt kart- og planforskriften § 9 andre og sjette ledd)<br /><br />Denne identifikatoren tildeles planen når planprosessen starter, og den kan ikke endres undervegs av forslagstiller</td>
      <td>Nasjonal<wbr />Arealplan<wbr />Id<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- planid</td>
      <td>entydig identifikasjon av en plan innen vedkommende administrative enhet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- kommunenummer</td>
      <td>kode som viser til offisiell nummerering av kommuner, alltid 4 siffer med eventuell ledende null</td>
      <td><a href="#kodeliste-kommunenummer">Kommunenummer</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>identifikasjon</td>
      <td>unik identifikasjon av et objekt i et datasett, forvaltet av den ansvarlige produsent/forvalter, og kan benyttes av eksterne applikasjoner som stabil referanse til objektet.<br /><br />Merknad: Denne unike identifikatoren skal ikke endres i løpet av objektets levetid, og skal ikke gjenbrukes i andre objekt.</td>
      <td>Identifikasjon<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- lokal<wbr />Id</td>
      <td>lokal identifikator av et objekt.<br /><br />Skal være en uuid, slik at den er unik, uavhengig av navnerommet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- navnerom</td>
      <td>navnerom som unikt identifiserer datakilden til et objekt.<br /><br />For plan anbefales navnerommet <a href="http://data.geonorge.no/sosi/plan">http://data.geonorge.no/sosi/plan</a></td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- versjon<wbr />Id</td>
      <td>identifikasjon av en spesiell versjon av et geografisk objekt (instans)</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>plannavn</td>
      <td>planens offisielle navn</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>plantype</td>
      <td>type reguleringsplan (pbl. §§ 12-2 og 12-3); angir om planen er en områderegulering eller detaljregulering</td>
      <td><a href="#kodeliste-rpplantype">Rp<wbr />Plantype</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>kunngjøringsdato<wbr />Varsel<wbr />Om<wbr />Planoppstart</td>
      <td>dato da varsel om oppstart av planarbeid ble kunngjort og sendt til berørte parter som naboer, sektormyndigheter og lag/foreninger med interesser i planen (pbl. § 12-8)</td>
      <td>Date</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>forslagsstillertype</td>
      <td>om forslagsstiller er privat eller offentlig planmyndighet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>lovreferanse</td>
      <td>kode for hvilken lov planen vedtas etter. For planlegging igangsatt er lovreferanse = 6 (pbl. 2008)</td>
      <td><a href="#kodeliste-lovreferanse">Lovreferanse</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>forste<wbr />Digitaliseringsdato</td>
      <td>dato når en representasjon av objektet i digital form første gang ble etablert</td>
      <td>Date<wbr />Time</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>oppdateringsdato</td>
      <td>tidspunkt for siste endring på dataobjektet</td>
      <td>Date<wbr />Time</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>link</td>
      <td>lenke (URL) til nærmere informasjon om planen, for eksempel planinnsyn eller varselet om planoppstart</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
  </tbody>
</table>

Relasjoner

**Assosiasjoner**
Planområde – rolle: planomrade – kardinalitet: 0..*
Varselområde – rolle: varselomrade – kardinalitet: 0..*
Plandokument – rolle: plandokument – kardinalitet: 0..*
BerørtPart – rolle: varslingsliste – kardinalitet: 0..*
Planbehandling – rolle: planbehandling – kardinalitet: 0..*

#### Planområde

område for planlegging igangsatt etter pbl. 2008, med tilhørende metadata fra varsel om oppstart av planarbeid, slik det formidles i OGC API-Features fra Direktoratet for byggkvalitet.<br /><br />Området skal være sammenhengende i grunnriss, men kan dekke flere vertikalnivåer.

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>geometri</td>
      <td>planområdets avgrensning i grunnriss. Området skal være sammenhengende i grunnriss, men kan dekke flere vertikalnivåer</td>
      <td>GM_<wbr />Surface</td>
      <td>1</td>
    </tr>
    <tr>
      <td>objid</td>
      <td>tjenestens interne identifikator for objektet (feature-id i OGC API)<br />OGC-rolle: id</td>
      <td>Integer</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>identifikasjon</td>
      <td>unik identifikasjon av et objekt i et datasett, forvaltet av den ansvarlige produsent/forvalter, og kan benyttes av eksterne applikasjoner som stabil referanse til objektet.<br /><br />Merknad: Denne unike identifikatoren skal ikke endres i løpet av objektets levetid, og skal ikke gjenbrukes i andre objekt.</td>
      <td>Identifikasjon<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- lokal<wbr />Id</td>
      <td>lokal identifikator av et objekt.<br /><br />Skal være en uuid, slik at den er unik, uavhengig av navnerommet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- navnerom</td>
      <td>navnerom som unikt identifiserer datakilden til et objekt.<br /><br />For plan anbefales navnerommet <a href="http://data.geonorge.no/sosi/plan">http://data.geonorge.no/sosi/plan</a></td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- versjon<wbr />Id</td>
      <td>identifikasjon av en spesiell versjon av et geografisk objekt (instans)</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>arealplan</td>
      <td>referanse (objid) til arealplanen planområdet tilhører</td>
      <td>Integer</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>nasjonal<wbr />Arealplan<wbr />Id</td>
      <td>landsdekkende entydig og unik identifikasjon av en arealplan (pbl. §§ 6-4, 9-1 og 12-1, samt kart- og planforskriften § 9 andre og sjette ledd)<br /><br />Denne identifikatoren tildeles planen når planprosessen starter, og den kan ikke endres undervegs av forslagstiller</td>
      <td>Nasjonal<wbr />Arealplan<wbr />Id<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- planid</td>
      <td>entydig identifikasjon av en plan innen vedkommende administrative enhet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- kommunenummer</td>
      <td>kode som viser til offisiell nummerering av kommuner, alltid 4 siffer med eventuell ledende null</td>
      <td><a href="#kodeliste-kommunenummer">Kommunenummer</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>plannavn</td>
      <td>planens offisielle navn</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>plantype</td>
      <td>type reguleringsplan (pbl. §§ 12-2 og 12-3); angir om planen er en områderegulering eller detaljregulering</td>
      <td><a href="#kodeliste-rpplantype">Rp<wbr />Plantype</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>kunngjøringsdato<wbr />Varsel<wbr />Om<wbr />Planoppstart</td>
      <td>dato da varsel om oppstart av planarbeid ble kunngjort og sendt til berørte parter som naboer, sektormyndigheter og lag/foreninger med interesser i planen (pbl. § 12-8)</td>
      <td>Date</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>forslagsstillertype</td>
      <td>om forslagsstiller er privat eller offentlig planmyndighet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>lovreferanse</td>
      <td>kode for hvilken lov planen vedtas etter. For planlegging igangsatt er lovreferanse = 6 (pbl. 2008)</td>
      <td><a href="#kodeliste-lovreferanse">Lovreferanse</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>første<wbr />Digitaliseringsdato</td>
      <td>dato når en representasjon av objektet i digital form første gang ble etablert</td>
      <td>Date<wbr />Time</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>oppdateringsdato</td>
      <td>tidspunkt for siste endring på dataobjektet</td>
      <td>Date<wbr />Time</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>link</td>
      <td>lenke (URL) til nærmere informasjon om planen, for eksempel planinnsyn eller varselet om planoppstart</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
  </tbody>
</table>

Relasjoner

**Assosiasjoner**
Arealplan – rolle: plan – kardinalitet: 0..1

#### Varselområde

område som omfatter eiendommene til partene som er varslet om oppstart av planarbeidet (pbl. § 12-8), slik det formidles i OGC API-Features fra Direktoratet for byggkvalitet.<br /><br />Varselområdet er normalt større enn planområdet, og tar typisk med eiendommer som grenser til planområdet eller ligger nær det, for eksempel på andre siden av en veg (forslag – må verifiseres)

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>geometri</td>
      <td>varselområdets avgrensning i grunnriss, som et polygon rundt eiendommene til de varslede partene (forslag – må verifiseres)</td>
      <td>GM_<wbr />Surface</td>
      <td>1</td>
    </tr>
    <tr>
      <td>objid</td>
      <td>tjenestens interne identifikator for objektet (feature-id i OGC API)<br />OGC-rolle: id</td>
      <td>Integer</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>identifikasjon</td>
      <td>unik identifikasjon av et objekt i et datasett, forvaltet av den ansvarlige produsent/forvalter, og kan benyttes av eksterne applikasjoner som stabil referanse til objektet.<br /><br />Merknad: Denne unike identifikatoren skal ikke endres i løpet av objektets levetid, og skal ikke gjenbrukes i andre objekt.</td>
      <td>Identifikasjon<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- lokal<wbr />Id</td>
      <td>lokal identifikator av et objekt.<br /><br />Skal være en uuid, slik at den er unik, uavhengig av navnerommet</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- navnerom</td>
      <td>navnerom som unikt identifiserer datakilden til et objekt.<br /><br />For plan anbefales navnerommet <a href="http://data.geonorge.no/sosi/plan">http://data.geonorge.no/sosi/plan</a></td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- versjon<wbr />Id</td>
      <td>identifikasjon av en spesiell versjon av et geografisk objekt (instans)</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>arealplan</td>
      <td>referanse (objid) til arealplanen varselområdet tilhører</td>
      <td>Integer</td>
      <td>0..1</td>
    </tr>
  </tbody>
</table>

Relasjoner

**Assosiasjoner**
Arealplan – rolle: plan – kardinalitet: 0..1

#### Plandokument

referanse til dokument som er knyttet til arealplanen (kart- og planforskriften § 9 første ledd). Et plandokument kan knyttes til den aktuelle planbehandlingen som det gjelder for.

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>dokumenttype</td>
      <td>type plandokument etter kodelisten Plandokumenttype i SOSI Planregister 5.0. For dokumenter ved varsel om oppstart brukes normalt KORR (planinitiativ, referat fra oppstartsmøte, varsel om oppstart, liste over varslede parter), KART (planavgrensning), PLANPROG (planprogram) og VEDTAK (vedtak om planoppstart), jf. KS/Geointegrasjon «Dokumenttyper for ePlansak»</td>
      <td><a href="#kodeliste-plandokumenttype">Plandokumenttype</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>vedleggstype</td>
      <td>vedleggstype dokumentet ble innsendt med i Fellestjenester PLAN (planvarsel), f.eks. Planvarsel, PlanomraadeSosi, PlanomraadePdf, Planinitiativ, ReferatOppstartsmoete, Planprogram eller Annet. Gir finere inndeling enn dokumenttype (forslag – må verifiseres)</td>
      <td><a href="#kodeliste-vedleggstype">Vedleggstype</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>tittel</td>
      <td>dokumentets tittel eller filnavn</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>referanse<wbr />Dokumentfil</td>
      <td>lenke (URL) for nedlasting av dokumentfilen. Tilsvarer arkivreferanse i SOSI Planregister 5.0</td>
      <td>Character<wbr />String</td>
      <td>1</td>
    </tr>
    <tr>
      <td>dokumentdato</td>
      <td>dokumentets egen dato (datert eller godkjent), ikke dato for innsending eller registrering</td>
      <td>Date</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>mime<wbr />Type</td>
      <td>filformat angitt som medietype (MIME-type) etter IANA, f.eks. application/pdf</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>sjekksum</td>
      <td>sjekksum for dokumentfilen, brukt til å kontrollere at filen er uendret (forslag – må verifiseres)</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>sjekksum<wbr />Algoritme</td>
      <td>algoritmen sjekksummen er beregnet med, f.eks. SHA-256 (forslag – må verifiseres)</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>beskrivelse</td>
      <td>fritekst som beskriver dokumentets innhold</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>arkivnavn</td>
      <td>navn på arkivet eller systemet der dokumentet er lagret</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
  </tbody>
</table>

#### BerørtPart

part som berøres av planarbeidet og skal varsles om oppstart av planarbeidet etter pbl. § 12-8, identifisert ved eiendom (matrikkelnummer) og/eller virksomhet (organisasjonsnummer) (forslag – må verifiseres)

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>matrikkelnummer</td>
      <td>identifikasjon av eiendommen som parten er berørt gjennom (struktur etter SOSI Matrikkelen – må verifiseres)</td>
      <td>Matrikkelnummer<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- kommunenummer</td>
      <td>kode som viser til offisiell nummerering av kommuner, alltid 4 siffer med eventuell ledende null</td>
      <td><a href="#kodeliste-kommunenummer">Kommunenummer</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- gårdsnummer</td>
      <td>gårdsnummer i matrikkelen (forslag – må verifiseres)</td>
      <td>Integer</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- bruksnummer</td>
      <td>bruksnummer i matrikkelen (forslag – må verifiseres)</td>
      <td>Integer</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- festenummer</td>
      <td>festenummer i matrikkelen (forslag – må verifiseres)</td>
      <td>Integer</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- seksjonsnummer</td>
      <td>seksjonsnummer i matrikkelen (forslag – må verifiseres)</td>
      <td>Integer</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>organisasjonsnummer</td>
      <td>organisasjonsnummer fra Enhetsregisteret (9 siffer) (forslag – må verifiseres)</td>
      <td>Character<wbr />String</td>
      <td>0..1</td>
    </tr>
  </tbody>
</table>

#### Planbehandling

tidfestet behandling av en arealplan, både fram til planen trer i kraft, og etterpå

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>planbehandlingsdato</td>
      <td>dato for planbehandlingen (forslag – må verifiseres)</td>
      <td>Date</td>
      <td>1</td>
    </tr>
    <tr>
      <td>planbehandlingstype</td>
      <td>type planbehandling, for eksempel planlegging igangsatt/oppstartsmøte avholdt (8) eller varsel om planoppstart (9) (forslag – må verifiseres)</td>
      <td><a href="#kodeliste-planbehandlingstype">Planbehandlingstype</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>navn</td>
      <td>navn på eller kort beskrivelse av planbehandlingen (forslag – må verifiseres)</td>
      <td>Character<wbr />String</td>
      <td>1</td>
    </tr>
    <tr>
      <td>saksnummer</td>
      <td>kommunens saksnummer for planbehandlingen (forslag – må verifiseres)</td>
      <td>Saksnummer<br />(datatype)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- saksår</td>
      <td>året saken ble opprettet (forslag – må verifiseres)</td>
      <td>Integer</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- sakssekvensnummer</td>
      <td>løpenummer for saken innen saksåret (forslag – må verifiseres)</td>
      <td>Integer</td>
      <td>1</td>
    </tr>
  </tbody>
</table>

Relasjoner

**Assosiasjoner**
Plandokument – rolle: plandokument – kardinalitet: 0..*

### Kodelister

#### <a id="kodeliste-kommunenummer"></a>«CodeList» Kommunenummer

**Definisjon:** ekstern kodeliste for kommunenummer

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="https://register.geonorge.no/sosi-kodelister/inndelinger/inndelingsbase/kommunenummer">https://register.geonorge.no/sosi-kodelister/inndelinger/inndelingsbase/kommunenummer</a></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-rpplantype"></a>«CodeList» RpPlantype

**Definisjon:** ekstern kodeliste for type reguleringsplan

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="https://register.geonorge.no/sosi-kodelister/plan/reguleringsplanforslag/rpplantype">https://register.geonorge.no/sosi-kodelister/plan/reguleringsplanforslag/rpplantype</a></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-lovreferanse"></a>«CodeList» Lovreferanse

**Definisjon:** ekstern kodeliste for gjeldende pbl.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="https://register.geonorge.no/sosi-kodelister/plan/reguleringsplanforslag/lovreferanse">https://register.geonorge.no/sosi-kodelister/plan/reguleringsplanforslag/lovreferanse</a></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-plandokumenttype"></a>«CodeList» Plandokumenttype

**Definisjon:** Dokumenttyper for plansaker

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="https://register.geonorge.no/sosi-kodelister/plan/planregister/plandokumenttype">https://register.geonorge.no/sosi-kodelister/plan/planregister/plandokumenttype</a></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-vedleggstype"></a>«CodeList» Vedleggstype

**Definisjon:** vedleggstyper i Fellestjenester PLAN (DiBK) for varsel om oppstart av planarbeid. Ingen publisert kodeliste funnet – verdier hentet fra plandata.ft.dibk.no (forslag – må verifiseres)

#### <a id="kodeliste-planbehandlingstype"></a>«CodeList» Planbehandlingstype

**Definisjon:** ekstern kodeliste for type planbehandling

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="https://register.geonorge.no/sosi-kodelister/plan/planregister/planbehandlingstype">https://register.geonorge.no/sosi-kodelister/plan/planregister/planbehandlingstype</a></td>
    </tr>
  </tbody>
</table>
