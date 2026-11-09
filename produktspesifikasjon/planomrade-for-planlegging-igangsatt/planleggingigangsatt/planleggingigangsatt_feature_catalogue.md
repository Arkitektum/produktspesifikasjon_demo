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
