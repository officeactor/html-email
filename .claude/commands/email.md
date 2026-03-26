Erstelle eine professionelle HTML-Email im OfficeActor-Stil basierend auf den folgenden Firmeninfos:

$ARGUMENTS

---

## Anleitung

### 1. Firmeninfos analysieren

Extrahiere aus den Argumenten:
- **Firmenname** (Pflicht)
- **Branche / Was sie machen** (Pflicht)
- **Quelle** (Optional: Arbeitsagentur, StepStone, meinestadt.de, LinkedIn, Indeed, etc.)
- **Kontext** (Optional: nach Telefonat, Social Media Aktivit&auml;t, spezifische Stellenanzeige, etc.)
- **Ort / Region** (Optional)
- **Sonstige Details** (Optional: alles was der User sonst noch erw&auml;hnt)

### 2. Template lesen

Lies `email-mollgruppe.html` als Strukturvorlage. Kopiere die **exakte HTML-Struktur** 1:1 &mdash; nur die variablen Sections werden angepasst.

### 3. Variable Sections schreiben

Passe **nur** diese Sections an:

#### a) `<title>` Tag
```
OfficeActor &ndash; Content &amp; Video f&uuml;r [FIRMENNAME]
```

#### b) Preheader (hidden div)
Ein kurzer Satz der in der Inbox-Vorschau erscheint. Bezug auf die Firma, max. 1-2 S&auml;tze.

#### c) H1 Heading
Kontextabh&auml;ngig:
- **Mit Jobportal-Quelle**: "Ihre Stellenanzeige auf [Quelle]"
- **Nach Telefonat**: "Vielen Dank f&uuml;r das Gespr&auml;ch"
- **Mit Social-Media-Bezug**: "Ihr [Plattform] Auftritt hat uns angesprochen"
- **Ohne Quelle**: Finde einen nat&uuml;rlichen, spezifischen Einstieg basierend auf der Branche oder dem Kontext. Beispiele:
  - "Content f&uuml;r [Branche] &ndash; eine Idee"
  - "Videoproduktion f&uuml;r [Firmenname]"
  - "Eine kurze Vorstellung"

#### d) Subtitle (p unter H1)
Kontextabh&auml;ngig:
- **Mit Stellenanzeige**: "Wir haben gesehen, dass Sie im Bereich [Social Media/Marketing/Content] Verst&auml;rkung suchen, und m&ouml;chten uns kurz vorstellen."
- **Nach Telefonat**: "Wie besprochen senden wir Ihnen hier alle wichtigen Infos zu unserem Angebot."
- **Ohne Quelle**: "Wir m&ouml;chten uns kurz vorstellen und Ihnen zeigen, wie wir [Firmenname] im Bereich Videocontent unterst&uuml;tzen k&ouml;nnten."

#### e) Opening (Section C) &mdash; 3-4 Paragraphen

**Paragraph 1**: Immer "Sehr geehrte Damen und Herren,"

**Paragraph 2 (Einstieg + Br&uuml;cke)**: Hier entsteht der **individuelle Einstieg**. Die Br&uuml;cke muss nat&uuml;rlich sein und zum Kontext passen:

- **Jobportal-Quelle vorhanden**:
  "&Uuml;ber [Quelle] sind wir auf Ihre Stellenanzeige aufmerksam geworden. Auch wenn Sie vermutlich eine feste Besetzung anstreben, m&ouml;chten wir die Gelegenheit nutzen, uns einmal vorzustellen. [Individuelle Erg&auml;nzung basierend auf der Firma]."

- **Nach Telefonat**:
  "vielen Dank f&uuml;r das nette Gespr&auml;ch [heute/am Telefon]. Wie versprochen senden wir Ihnen hier eine &Uuml;bersicht &uuml;ber uns und unser Angebot."

- **Social-Media-Bezug**:
  "Wir haben gesehen, dass [Firmenname] bereits auf [Plattform] aktiv ist, und das hat unser Interesse geweckt. [Nat&uuml;rlicher &Uuml;bergang warum OfficeActor relevant sein k&ouml;nnte]."

- **Nur Branche bekannt (kein Jobportal, kein Telefonat)**:
  Finde einen nat&uuml;rlichen Einstieg &uuml;ber die Branche. Denke dar&uuml;ber nach, was die Firma konkret macht und warum Video/Content f&uuml;r genau diesen Bereich sinnvoll w&auml;re. Beispiele:
  - "Gerade im [Branche] spielt [relevanter Aspekt] eine gro&szlig;e Rolle, und genau das l&auml;sst sich &uuml;ber authentischen Videocontent gut transportieren."
  - "Wir besch&auml;ftigen uns intensiv mit Videoproduktion f&uuml;r [Branche/Bereich] und sind dabei auf [Firmenname] aufmerksam geworden."
  - Wichtig: Nicht generisch bleiben &mdash; immer einen konkreten Bezug zur Firma herstellen.

**Paragraph 3**: Immer die Team-Vorstellung:
"Mein Name ist Marlon Bensching, ich bin Content Manager bei OfficeActor. Gemeinsam mit meinem Kollegen Fabian, der als Videograf f&uuml;r uns arbeitet, bilden wir ein kleines, eingespieltes Team."

**Paragraph 4**: Immer der Leistungs&uuml;berblick:
"Wir unterst&uuml;tzen Unternehmen dabei, einen professionellen und authentischen Social Media Auftritt aufzubauen. Von der Strategie &uuml;ber die Produktion bis hin zur Ver&ouml;ffentlichung begleiten wir den gesamten Prozess."

#### f) "Warum wir schreiben" Relevanz-Abschnitt (Section G)

**Paragraph 1**: Ein bis zwei S&auml;tze die erkl&auml;ren, warum Video/Content f&uuml;r genau DIESE Firma sinnvoll ist.
- Beschreibe was die Firma macht in einfachen Worten &mdash; keine Fachbegriffe oder Buzzwords
- Erkl&auml;re nat&uuml;rlich, warum Video hier einen Unterschied machen k&ouml;nnte
- Referenz-Beispiel (Mollgruppe): "Produkte, die man im Alltag nicht sieht, brauchen umso mehr gute Erkl&auml;rung. Mit kurzen Videos l&auml;sst sich schnell und anschaulich zeigen, was pro clima Produkte leisten und warum sie wichtig sind."

**Paragraph 2**: Immer der gleiche Closing-Satz:
"Falls das f&uuml;r Sie interessant klingt, w&uuml;rden wir uns &uuml;ber ein kurzes, unverbindliches Gespr&auml;ch freuen. :)"

#### g) Dateiname
`email-[firmenname-lowercase-keine-sonderzeichen].html` im gleichen Verzeichnis wie die anderen Emails.

### 4. Fixe Sections (1:1 aus Template &uuml;bernehmen)

Diese Sections werden **NICHT** ver&auml;ndert &mdash; exakt aus `email-mollgruppe.html` kopieren:
- Logo Header (Section A)
- Team Cards (Section D) &mdash; inkl. Fotos, Bios, Team-Closing
- Was wir anbieten (Section F) &mdash; alle 9 Services
- Portfolio Link (Section F2) &mdash; inkl. CTA Button mit VML
- Closing (Section H) &mdash; "Wir freuen uns, von Ihnen zu h&ouml;ren" + "Mit freundlichen Gr&uuml;&szlig;en"
- Footer (Section J) &mdash; Kontaktdaten + Social Links

### 5. Tonrichtlinien (KRITISCH)

- **NIEMALS** "trotzdem versuchen", "Gl&uuml;ck versuchen", "auf nette Art versuchen" oder &auml;hnliche Formulierungen verwenden
- **NIEMALS** "Warum wir trotzdem schreiben" &mdash; immer nur "Warum wir schreiben"
- **NIEMALS** "Kein Druck, einfach nur ein ehrliches Kennenlernen" oder &auml;hnlich formulaische S&auml;tze
- **NIEMALS** k&uuml;nstlich klingende Fachbegriffe &uuml;ber die Firma verwenden, nur um interessiert zu wirken
- **NIEMALS** Bindestriche in Komposita: "Social Media Videos" nicht "Social-Media-Videos"
- **NIEMALS** Gedankenstriche (&ndash;) benutzen um S&auml;tze zu verbinden oder Einsch&uuml;be zu machen. Stattdessen Kommas, Punkte oder Umformulierungen verwenden.
- Formelle Anrede mit "Sie" durchgehend
- Ton: Selbstbewusst, nat&uuml;rlich, professionell &mdash; wie ein normaler Mensch der eine Email schreibt
- Beschreibungen der Firma kurz und simpel halten &mdash; so als w&uuml;rde man es einem Freund erkl&auml;ren

### 6. Technische Regeln

- HTML-Entities f&uuml;r alle Umlaute: `&uuml;` `&ouml;` `&auml;` `&Uuml;` `&Ouml;` `&Auml;` `&szlig;`
- HTML-Entity f&uuml;r &: `&amp;`
- HTML-Entity f&uuml;r Gedankenstrich: `&ndash;`
- Alle Styles inline (kein `<style>` Block au&szlig;er im MSO Conditional)
- Table-based Layout, `role="presentation"` auf allen Tables
- 650px max-width Container
- MSO Conditional Comments f&uuml;r Outlook
- VML `v:roundrect` f&uuml;r den Portfolio-Button

### 7. Ausgabe

Erstelle die komplette HTML-Datei mit dem Write Tool. Gib danach eine kurze Best&auml;tigung mit dem Dateinamen.
