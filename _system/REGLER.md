# Regler for Tripletex HTML/CSS-prototyper

Disse reglene gjelder for alle som lager prototyper i dette systemet – inkludert Claude.

---

## Kilder og arbeidsflyt

### Primærkilde — Atlas på GitHub
Alle regler, tokens, komponenter og ikoner slås opp i:
**[github.com/Tripletex-AS/tripletex-frontend/tree/main/design-system](https://github.com/Tripletex-AS/tripletex-frontend/tree/main/design-system)**

Bruk denne som fasit ved tvil om tokens, komponentstruktur eller ikonpaths. Alternativt: [atlas.tripletex.dev](https://atlas.tripletex.dev) — komponenteksempler og ikoner finnes i **[Atlas Storytime](https://atlas.tripletex.dev/#/Components/Accordion)**.

### Lokalt `_system/` — sandkasse for eksperimenter
Filene i denne mappen (`tokens.css`, `components.css`, `layout.css`) er en **lokal kopi** av Atlas tilpasset HTML/CSS-prototyping. De brukes som:
- Sandkasse for nye komponenter og justerte tokens under utvikling
- Holder for eksperimenter som ikke er klare for Atlas ennå
- Prototyping av mønstre som skal merges inn i GitHub-repoet senere

**Arbeidsflyt:**
1. Slå opp regler og tokens i GitHub-repoet
2. Implementer i lokalt `_system/` for prototyping
3. Merge godkjente endringer tilbake til `Tripletex-AS/tripletex-frontend` når klart

---

## Absolutte regler

1. **Ingen hardkodede hex-farger** — aldri `#0a41fa`, alltid `var(--action-primary-rest)`
2. **Ingen hardkodede px-verdier** — aldri `padding: 16px`, alltid `padding: var(--space-16)`
3. **Ikke bruk globale tokens direkte** — aldri `var(--global-blue-100)` i komponenter, bare i `tokens.css`
4. **Bruk semantiske tokens** — de beskriver hensikt (hva elementet er), ikke farge
5. **Aldri bruk bold skrift** — `font-weight: bold` og `font-weight: 700` er forbudt. Medium (`font-weight: 500`) er maks vekt
6. **Font-smoothing alltid på** — `body` skal alltid ha `-webkit-font-smoothing: antialiased` og `-moz-osx-font-smoothing: grayscale` (allerede satt i `components.css`)
7. **Kun Atlas-godkjente tekststørrelser** — 12px, 14px, 16px, 20px, 30px. Ingen andre.
8. **Ingen kursiv tekst** — bruk aldri `font-style: italic`. Bruk `font-weight: 500` for betoning.
9. **Ingen emoji i UI-strenger** — labels, knapper, titler, navigasjon, systemmmeldinger. Bruk ikoner fra Atlas-biblioteket.

---

## Tokenoversikt

### Farger – handling (`action-*`)
Brukes på knapper og klikkbare elementer.

| Token | Bruksområde |
|-------|-------------|
| `--action-primary-rest/hover/active` | Fylt primærknapp (blå) |
| `--action-secondary-rest/hover/active` | Sekundærknapp (lys blå) |
| `--action-tertiary-rest/hover/active` | Ghost-knapp (transparent) |
| `--action-neutral-rest/hover/active` | Nøytrale elementer som tabellrader |

### Farger – bakgrunner (`surface-*`)
| Token | Bruksområde |
|-------|-------------|
| `--surface-background` | Ytterbakgrunn på siden |
| `--surface-default` | Hvit bakgrunn for kort, panel, modal |
| `--surface-nav` | Sidebar og topbar (turkis tint) |
| `--surface-disabled` | Deaktiverte elementer |
| `--surface-tooltip` | Tooltip-bakgrunn (mørk) |
| `--surface-footer` | Footer-bakgrunn |
| `--surface-modal` | Modal-overlay |

Statustilstander finnes i fire nivåer for info, warning, error, success og automation:

| Suffiks | Bruk |
|---------|------|
| `-rest` | Standardbakgrunn |
| `-hover` | Hover-tilstand |
| `-highlight` | Uthevet / valgt |
| `-active` | Fylt aksentfarge |

| Tilstand | `-rest` | `-active` |
|----------|---------|-----------|
| Info | #f2f5ff | #0a41fa |
| Warning | #fffcf5 | #f7c137 |
| Error | #fef4f5 | #e83645 |
| Success | #f4fbf4 | #33ac2e |
| Automation | #f9f6ff | #7043cc |

### Farger – tekst (`text-*`)
| Token | Bruksområde |
|-------|-------------|
| `--text-primary` | Standard brødtekst og overskrifter |
| `--text-muted` | Sekundær tekst, hjelpetekst, metadata |
| `--text-placeholder` | Plassholdertekst i inputs |
| `--text-disabled` | Tekst på deaktivert element |
| `--text-on-action` | Tekst oppå farget knapp (alltid hvit) |
| `--text-action` | Blå tekst som indikerer handling |
| `--text-active` | Aktiv-tilstandstekst (blå) |
| `--text-link` | Klikkbare lenker — blå tekst, regular vekt, ingen underline |
| `--text-footer-primary` | Primærtekst i footer |
| `--text-footer-link` | Lenker i footer |

### Farger – kanter (`border-*`)
| Token | Bruksområde |
|-------|-------------|
| `--border-faint` | Nesten usynlig skillelinje |
| `--border-muted` | Lett synlig kant rundt kort |
| `--border-primary` | Tydelig kant rundt input i hvile |
| `--border-secondary` | Mykere kant |
| `--border-disabled` | Kant på deaktivert element |
| `--border-focus` | Blå kant når input er i fokus |
| `--border-hover` | Kant ved hover |
| `--border-active` | Aktiv/fokusert kant (blå) |
| `--border-underline` | Understrek-aksent |
| `--border-info` | Info-statuskant |
| `--border-warning` | Advarsel-statuskant |
| `--border-error` | Feil-statuskant |
| `--border-success` | Suksess-statuskant |
| `--border-automation` | Automation-statuskant |

### Spacing
Bruk alltid `--space-*` for `padding`, `gap` og `margin`. Atlas-godkjent skala:

```
--space-1   1px    Minimal justering
--space-2   2px    Minimal luft
--space-4   4px    Tett luft
--space-8   8px    Standard liten luft
--space-12  12px   Middels luft
--space-16  16px   Standard luft
--space-20  20px   Romslig luft
--space-24  24px   Stor luft (standard side-padding)
--space-28  28px   
--space-32  32px   Ekstra romslig
--space-36  36px   
--space-40  40px   Svært romslig
--space-44  44px   
--space-48  48px
--space-64  64px
```

### Størrelser
Bruk `--size-*` (eller Atlas-aliasene `--element-height-*`) for høyde på knapper, inputs og elementer.

```
--size-tiny   / --element-height-tiny    20px   Svært kompakt
--size-small  / --element-height-small   24px   Kompakt (tags, chips)
--size-medium / --element-height-medium  32px   Standard liten (ikonknapper, small-knapp)
--size-large  / --element-height-large   40px   Standard stor (knapper, inputs) ← Atlas default
--size-xl                                48px   Topbar, store inputs
--size-xxl                               64px   Hero-elementer
```

### Tekststørrelser (Atlas)
```
12px  — Decoration / hjelpetekst / metadata
14px  — Standard brødtekst, labels, tabellceller  ← standard
16px  — Stor tekst / fremhevet innhold
20px  — Overskrift / seksjonstittel
30px  — Sideittel / hero-overskrift
```

### Border-radius
Atlas godkjenner kun disse to:
```
--radius-default   4px      Nesten alt: knapper, inputs, kort, navigasjon
--radius-full      9999px   Pille-form: chips, badges, søkefelt
```

Prototype-only (ikke i Atlas):
```
--radius-none      0px      Ingen avrunding
--radius-mobile    16px     Bunn-sheet på mobil
```

---

## Komponentklasser

### Knapper
Atlas har 3 varianter: Primary, Secondary, Tertiary. Bruk aldri `btn-ghost`.

```html
<button class="btn btn-primary">Lagre</button>       <!-- Fylt blå — én per mål -->
<button class="btn btn-secondary">Avbryt</button>    <!-- Lys blå -->
<button class="btn btn-tertiary">Se mer</button>     <!-- Transparent/ghost -->
```

**Rekkefølge (høyrejustert):** Primary lengst til høyre → Secondary → Tertiary  
**Rekkefølge (venstrejustert):** Primary → Secondary → Tertiary (venstre til høyre)  
**Mellomrom:** `--space-8` mellom knapper  
**Størrelse:** Medium = 40px (`--size-large`), Small = 32px (`--size-medium`)  
**Ikon:** plasseres alltid til HØYRE for label. Medium knapp → `--icon-size-medium` (24px). Small knapp → `--icon-size-small` (20px). Unntak: tilbake-knapper i flerstegsprosesser kan ha venstrevendt pil til VENSTRE for label (`[← Forrige steg]`), men bare hvis knappen er venstrejustert.  
**Skriftvekt:** alltid Regular (400) — aldri 500 på knapp-labels  
**Label-tekst:** alltid setningsfrase — «Send faktura», ikke «Send Faktura» eller «SEND FAKTURA». Start med verb.  
**Ikonknapper:** alltid `btn-tertiary`, alltid med `title`-attributt (tooltip)

### Skjemaelementer
```html
<div class="form-group">
  <label class="input-label">Foretaksnavn <span class="required">*</span></label>
  <input class="input" type="text" placeholder="F.eks. Acme AS">
  <span class="input-hint">Hint-tekst her</span>
</div>

<!-- Med feil -->
<div class="form-group">
  <label class="input-label">Org.nr.</label>
  <input class="input input-error" type="text" value="123">
  <span class="input-error-msg">Ugyldig organisasjonsnummer</span>
</div>

<!-- Select -->
<div class="form-group">
  <label class="input-label">Kundegruppe</label>
  <select class="input">
    <option>Velg gruppe...</option>
  </select>
</div>

<!-- Textarea -->
<div class="form-group">
  <label class="input-label">Kommentar</label>
  <textarea class="input"></textarea>
</div>
```

### Content Switcher (Atlas: ContentSwitcher)

Brukes til å bytte mellom visninger eller filtrere innhold. Grå beholder med hvit pille for valgt element. Standard høyde 32px.

```html
<!-- Standard (32px) -->
<div class="content-switcher" role="group">
  <button class="content-switch content-switch--active">Alle</button>
  <button class="content-switch">Aktive</button>
  <button class="content-switch">Avvik</button>
</div>

<!-- Liten (24px) -->
<div class="content-switcher content-switcher--small" role="group">
  <button class="content-switch content-switch--active">Alle</button>
  <button class="content-switch">Mine</button>
</div>
```

Bruk gjerne dette JS-mønsteret for å togge aktiv tilstand:
```js
document.querySelectorAll('.content-switcher').forEach(sw => {
  sw.addEventListener('click', e => {
    const btn = e.target.closest('.content-switch');
    if (!btn) return;
    sw.querySelectorAll('.content-switch').forEach(b => b.classList.remove('content-switch--active'));
    btn.classList.add('content-switch--active');
  });
});
```

**Ikke forveksle med `.switcher`** — det er en eldre segmentert knapperad med synlige kanter. Bruk `content-switcher` på nye flater.

### Chip og status

```html
<!-- Chip: nøytral etikett (ingen fargevariant) -->
<span class="chip">Etikett</span>

<!-- Status: farget prikk + tekst — bruk ALLTID status-dot, aldri egne badge-klasser -->
<span class="status-dot status-dot--success">Aktiv</span>
<span class="status-dot status-dot--warning">Krever handling</span>
<span class="status-dot status-dot--error">Avvist</span>
<span class="status-dot status-dot--neutral">Inaktiv</span>
<span class="status-dot status-dot--info">Ny</span>
```

### Alert

Fem varianter: `alert--info`, `alert--success`, `alert--warning`, `alert--error`, `alert--automation`.

**Avvisnbarhet:** Info, Success, Warning og Automation kan avvises (vis lukk-knapp). **Error kan IKKE avvises** — den forsvinner kun når den underliggende feilen er rettet.

```html
<!-- Warning -->
<div class="alert alert--warning">
  <svg class="alert-icon" viewBox="0 0 24 24" fill="none">
    <circle cx="12" cy="12" r="9.5" stroke="currentColor" stroke-width="1.5"/>
    <path d="M12 8v5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
    <circle cx="12" cy="15.5" r="0.75" fill="currentColor"/>
  </svg>
  <p class="alert-message">Melding her. <a href="#">Les mer</a></p>
  <button class="alert-close" onclick="this.closest('.alert').remove()">
    <svg viewBox="0 0 16 16" fill="none"><path d="M3 3l10 10M13 3L3 13" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/></svg>
  </button>
</div>

<!-- Info -->
<div class="alert alert--info">
  <svg class="alert-icon" viewBox="0 0 24 24" fill="none">
    <circle cx="12" cy="12" r="9.5" stroke="currentColor" stroke-width="1.5"/>
    <path d="M12 11v5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
    <circle cx="12" cy="8.5" r="0.75" fill="currentColor"/>
  </svg>
  <p class="alert-message">Melding her. <a href="#">Les mer</a></p>
</div>

<!-- Success -->
<div class="alert alert--success">
  <svg class="alert-icon" viewBox="0 0 24 24" fill="none">
    <circle cx="12" cy="12" r="9.5" stroke="currentColor" stroke-width="1.5"/>
    <path d="M8 12l3 3 5-5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
  </svg>
  <p class="alert-message">Melding her.</p>
</div>

<!-- Error (ingen lukk-knapp — kan ikke avvises) -->
<div class="alert alert--error">
  <svg class="alert-icon" viewBox="0 0 24 24" fill="none">
    <path d="M10.3 4.5l-7.8 13.5A2 2 0 004.2 21h15.6a2 2 0 001.7-3L13.7 4.5a2 2 0 00-3.4 0z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/>
    <path d="M12 10v4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
    <circle cx="12" cy="16.5" r="0.75" fill="currentColor"/>
  </svg>
  <p class="alert-message">Melding her. <a href="#">Les mer</a></p>
</div>

<!-- Automation (lilla) -->
<div class="alert alert--automation">
  <svg class="alert-icon" viewBox="0 0 24 24" fill="none">
    <path d="M12 3l1.5 4.5L18 9l-4.5 1.5L12 15l-1.5-4.5L6 9l4.5-1.5L12 3z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/>
  </svg>
  <p class="alert-message">Melding her. <a href="#">Les mer</a></p>
  <button class="alert-close" onclick="this.closest('.alert').remove()">
    <svg viewBox="0 0 16 16" fill="none"><path d="M3 3l10 10M13 3L3 13" stroke="currentColor" stroke-width="1.4" stroke-linecap="round"/></svg>
  </button>
</div>
```

### Tabell
```html
<div class="table-container">
  <div class="table-toolbar">
    <button class="btn btn-secondary">Filter</button>
    <input class="input" type="search" placeholder="Søk...">
  </div>
  <table class="tx-table table-standard">
    <thead>
      <tr>
        <th>Navn</th>
        <th class="col-num">Beløp</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Acme AS</td>
        <td class="col-num">12 345</td>
      </tr>
    </tbody>
  </table>
</div>
```

Tabellvarianter: legg til `table-compact`, `table-standard` eller `table-detailed` på `<table>`.

**Hover-adferd:**
- Rad-hover: `var(--surface-info-rest)` (#f2f5ff) — definert i `components.css`, ikke overstyr
- Icon-btn hover: `var(--action-neutral-hover)` (#ced9fe) — mørkere blå, synlig oppå rad-hover
- `icon-btn` har `background: transparent` som default (ikke hover-farge)

**Tekst i tabellceller:**
- Bruk `<span class="td-name">` for fet primærtekst i celle — ikke `<a>`-lenker med underline
- For handlingsikoner, bruk `<a class="icon-btn">` eller `<button class="icon-btn">` — begge er transparente som default

### Kort
```html
<div class="card">
  <div class="card-header">
    <div>
      <div class="card-title">Tittel</div>
      <div class="card-subtitle">Undertittel</div>
    </div>
    <button class="btn btn-primary">Handling</button>
  </div>
  <div class="card-body">
    Innhold her
  </div>
</div>
```

### App-shell
```html
<div class="app-shell">
  <header class="app-topbar">
    <div class="topbar-left">
      <span class="topbar-logo">Tripletex</span>
    </div>
  </header>
  <div class="app-body">
    <nav class="sidebar">
      <a href="#" class="nav-item nav-item--active">
        <span class="nav-icon-active"><!-- svg --></span>
        Faktura
      </a>
      <a href="#" class="nav-item">
        <span class="nav-icon"><!-- svg --></span>
        Regnskap
      </a>
    </nav>
    <main class="main-content">
      <div class="page">
        <div class="page-header">
          <h1 class="page-title">Sidetittel</h1>
          <div class="page-actions">
            <button class="btn btn-primary">Ny</button>
          </div>
        </div>
        <!-- innhold -->
      </div>
    </main>
  </div>
</div>
```

---

## Mappestruktur og konvensjoner

```
tripletex-prototypes/
  _system/          ← rør ikke disse filene
    tokens.css
    components.css
    layout.css
    REGLER.md
  _templates/       ← startpunkter for nye prototyper (bruk alltid disse som base)
  prototyper/       ← her lagres ferdige prototyper
    kebab-case-navn/
      index.html
      (ekstra sider om nødvendig)
```

Navngiving: bruk alltid `kebab-case` for mapper og filer.

---

## HTML-head for nye prototyper

```html
<!DOCTYPE html>
<html lang="no">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sidetittel – Tripletex</title>
  <link rel="stylesheet" href="../../_system/tokens.css">
  <link rel="stylesheet" href="../../_system/components.css">
  <link rel="stylesheet" href="../../_system/layout.css">
  <link rel="stylesheet" href="https://cdn.tripletex.no/google-fonts/rubik-400-500-800.css">
</head>
```

Juster `../../` til riktig relativ sti basert på plasseringen til filen din.

---

## Maler — bruk alltid som startpunkt

Kopier riktig mal og bytt ut innholdet. Ikke bygg app-shell fra scratch.

| Mal | Bruk når |
|-----|----------|
| `_templates/side-med-tabell.html` | Siden viser en tabell med filterlinje (`table-container`, `table-toolbar`, `tx-table`) |
| `_templates/side-med-skjema.html` | Siden har et skjema med felter og knapper |

### Nøkkelkomponenter fra malen (alltid system-klasser, aldri egendefinerte)

**Tabellside:**
```html
<!-- Wrapper rundt tabell -->
<div class="table-container">

  <!-- Filterlinje -->
  <div class="table-toolbar">
    <div class="table-toolbar-filters">
      <button class="btn btn-secondary">Filter …</button>

      <!-- Søk med ikon -->
      <div class="input-search-wrap">
        <input class="input" type="search" placeholder="Søk...">
        <svg class="input-search-icon" …></svg>
      </div>

      <!-- Periodenavigator -->
      <div class="period-nav">
        <span class="period-nav-label">Mars 2026</span>
        <div class="period-nav-arrows">
          <button class="period-nav-btn">←</button>
          <button class="period-nav-btn">→</button>
        </div>
      </div>

      <!-- Segmentert knapperad -->
      <div class="switcher">
        <button class="switcher-btn switcher-btn--active">Alle</button>
        <button class="switcher-btn">Aktive</button>
      </div>

      <select class="input toolbar-select">…</select>
    </div>

    <div class="table-toolbar-actions">
      <button class="icon-btn">…</button>
    </div>
  </div>

  <!-- Tabell -->
  <table class="tx-table table-standard">…</table>
</div>
```

**Topbar** — kopier alltid fra mal, ikke fra gamle prototyper:
```html
<header class="app-topbar">
  <div class="topbar-left">
    <button class="topbar-icon-btn" title="Meny">…</button>
    <span class="topbar-logo">tripletex</span>
    <span class="topbar-sep"></span>
    <div class="topbar-company">
      <span class="topbar-company-badge">T</span>
      <span class="topbar-company-name">Tripletex AS</span>
    </div>
  </div>
  <div class="topbar-right">
    <div class="topbar-search">…Søk</div>
    <button class="topbar-assistant">Assistent ✦</button>
    <!-- 7 icon-knapper: Favoritter, Last ned, Varsler, Meldinger, Hjelp, Kunngjøringer, Rapporter -->
    <button class="topbar-user-btn">…</button>
  </div>
</header>
```

---

## Diagram/chart-farger

Diagram-farger er **ikke tokenisert i Atlas ennå** — dette er bekreftet i GitHub-repoet. Bruk disse globale referansene direkte i diagramkode (ikke i vanlige komponenter):

| Bruk | Global token | Hex |
|------|-------------|-----|
| Inntekter (lys blå) | `--global-blue-40` | `#9db3fd` |
| Resultat positiv (mørk blå) | `--global-blue-100` | `#0a41fa` |
| Utgifter (lys rosa) | `--global-red-20` | `#fbd6da` |
| Resultat negativ (mørk rosa) | `--global-red-80` | `#ec5e6a` |

---

## Spørsmål?

Kilde: **Atlas** — Tripletex sitt offisielle designsystem  
GitHub: `Tripletex-AS/tripletex-frontend/design-system/`  
Nettsted: [atlas.tripletex.dev](https://atlas.tripletex.dev)
