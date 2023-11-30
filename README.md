# 🤯 HEAD

Ein einfacher Leitfaden zu den HTML-<head>>-Elementen

[![Mitwirkende](https://img.shields.io/github/contributors/joshbuchea/head.svg?style=for-the-badge)](https://github.com/joshbuchea/HEAD/graphs/contributors)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg?style=for-the-badge)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Folge @joshbuchea auf Mastodon](https://img.shields.io/badge/Follow_@joshbuchea-purple?logo=mastodon&logoColor=white&style=for-the-badge)](https://hachyderm.io/@joshbuchea)

## Inhaltsverzeichnis

- [Empfohlenes Minimum](#recommended-minimum)
- [Elemente](#elements)
- [Meta](#meta)
- [Link](#link)
- [Icons](#icons)
- [Social](#social)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Twitter-Karte](#twitter-card)
  - [Twitter Datenschutz](#twitter-privacy)
  - [Schema.org](#schemaorg)
  - [Pinterest](#pinterest)
  - [Facebook Instant Articles](#facebook-instant-articles)
  - [OEmbed](#oembed)
  - [QQ/Wechat](#qqwechat)
- [Browser/Plattformen](#browsers--platforms)
  - [Apple iOS](#apple-ios)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Browser (Chinesisch)](#browsers-chinese)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [App-Links](#app-links)
- [Andere Ressourcen](#other-resources)
- [Verwandte Projekte](#related-projects)
- [Andere Formate](#other-formats)
- [Übersetzungen](#-translations)
- [Mitwirkende](#-mitwirkende)
  - [Mitwirkende](#mitwirkende)
- [Autor](#-author)
- [Lizenz](#-license)

## Empfohlenes Minimum

Im Folgenden findest du die wichtigsten Elemente für jedes Webdokument (Websites/Apps):

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  Die obigen 2 Meta-Tags *müssen* im <head> an erster Stelle stehen
  um die korrekte Darstellung des Dokuments zu gewährleisten.
  Jedes andere Kopf-Element sollte *nach* diesen Tags kommen.
 -->
<title>Seitentitel</title>
```

meta charset" - definiert die Kodierung der Website, "utf-8" ist der Standard

`meta name="viewport"` - Viewport-Einstellungen, die sich auf die mobile Reaktionsfähigkeit beziehen

`width=device-width` - verwendet die physische Breite des Geräts (ideal für Mobilgeräte!)

Initial-scale=1" - der anfängliche Zoom, 1 bedeutet kein Zoom

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Elemente

Gültige `<head>` Elemente sind `meta`, `link`, `title`, `style`, `script`, `noscript`, und `base`.

Diese Elemente enthalten Informationen darüber, wie ein Dokument von Webtechnologien, z. B. Browsern, Suchmaschinen, Bots usw., wahrgenommen und gerendert werden soll.

```html
<!--
  Lege die Zeichenkodierung für dieses Dokument fest, so dass
  alle Zeichen innerhalb des UTF-8-Raums (z. B. Emoji)
  korrekt wiedergegeben werden.
-->
<meta charset="utf-8">

<!-- Setzt den Titel des Dokuments -->
<title>Seitentitel</title>

<!-- Lege die Basis-URL für alle relativen URLs innerhalb des Dokuments fest -->
<base href="https://example.com/page.html">

<!-- Link zu einer externen CSS-Datei -->
<link rel="stylesheet" href="styles.css">

<!-- Wird für das Hinzufügen von In-Document-CSS verwendet -->
<style>
  /* ... */
</style>

<!-- JavaScript & No-JavaScript Tags -->
<script src="script.js"></script>
<script>
  // Funktion(en) gehen hier hin
</script>
<noscript>
  <!-- Keine JS-Alternative -->
</noscript>
```

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Meta

```html
<!--
  Die folgenden 2 Meta-Tags *müssen* zuerst im <head> stehen
  um eine korrekte Darstellung des Dokuments zu gewährleisten.
  Jedes andere head-Element sollte *nach* diesen Tags kommen.
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
  Ermöglicht die Kontrolle darüber, woher die Ressourcen geladen werden.
  Platziere es so früh wie möglich im <head>, da das Tag
  nur für Ressourcen gilt, die nach ihm deklariert werden.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Name der Webanwendung (sollte nur verwendet werden, wenn die Website als App genutzt wird) -->
<meta name="application-name" content="Anwendungsname">

<!-- Theme-Farbe für Chrome, Firefox OS und Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Kurze Beschreibung des Dokuments (maximal 150 Zeichen) -->
<!-- Dieser Inhalt *kann* als Teil der Suchmaschinenergebnisse verwendet werden. -->
<meta name="description" content="Eine Beschreibung der Seite">

<!-- Kontrolliere das Verhalten von Suchmaschinen beim Crawlen und Indizieren -->
<meta name="robots" content="index,follow"><!-- Alle Suchmaschinen -->
<meta name="googlebot" content="index,follow"><!-- Google spezifisch -->

<!-- Sagt Google, dass es die Sitelinks-Suchbox nicht anzeigen soll -->
<meta name="google" content="nositelinkssearchbox">

<!-- Sagt Google, dass es keine Übersetzung für dieses Dokument bereitstellen soll -->.
<meta name="google" content="notranslate">

<!-- Überprüfe den Besitz der Website -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Identifiziere die Software, mit der das Dokument erstellt wurde (z.B. - WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Kurze Beschreibung des Themas deines Dokuments -->
<meta name="subject" content="Das Thema deines Dokuments">

<!-- Gibt eine allgemeine Alterseinstufung basierend auf dem Inhalt des Dokuments -->
<meta name="rating" content="Allgemein">

<!-- Ermöglicht die Kontrolle darüber, wie Referrer-Informationen übergeben werden -->
<meta name="referrer" content="no-referrer">

<!-- Deaktiviere die automatische Erkennung und Formatierung von möglichen Telefonnummern -->
<meta name="format-detection" content="telephone=no">

<!-- DNS-Prefetching komplett deaktivieren, indem du es auf "off" setzt -->.
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Gibt das Dokument an, das in einem bestimmten Frame erscheinen soll -->
<meta http-equiv="Window-Target" content="_value">

<!-- Geo-Tags -->
<meta name="ICBM" content="Breitengrad, Längengrad">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Ländercode (ISO 3166-1): obligatorisch, Staatencode (ISO 3166-2): optional; z.B. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- z.B. content="New York City" -->

<!-- Web Monetization https://webmonetization.org/docs/getting-started -->
<meta name="monetization" content="$paymentpointer.example">
```

- 📖 [Meta-Tags, die Google versteht](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM auf Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [Geotagging auf Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Link

```html
<!-- Zeigt auf ein externes Stylesheet -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Hilft, Probleme mit doppeltem Inhalt zu vermeiden -->
<link rel="canonical" href="https://example.com/article/?page=2">

<!-- Links zu einer AMP-HTML-Version des aktuellen Dokuments -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Links zu einer JSON-Datei, die die "Installations"-Anmeldedaten für die Webanwendungen angibt -->
<link rel="manifest" href="manifest.json">

<!-- Links zu Informationen über den/die Autor(en) des Dokuments -->
<link rel="author" href="humans.txt">

<!-- Verweist auf eine Copyright-Erklärung, die für den Kontext des Links gilt -->
<link rel="license" href="copyright.html">

<!-- Gibt einen Verweis auf eine Stelle in deinem Dokument an, die in einer anderen Sprache sein kann -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Liefert Informationen über einen Autor oder eine andere Person -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Links zu einem Dokument, das eine Sammlung von Aufzeichnungen, Dokumenten oder anderen Materialien von historischem Interesse beschreibt -->
<link rel="archives" href="https://example.com/archives/">

<!-- Links zur obersten Ebene der Ressource in einer hierarchischen Struktur -->
<link rel="index" href="https://example.com/article/">

<!-- Bietet eine Selbstreferenz - nützlich, wenn das Dokument mehrere mögliche Referenzen hat -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- Das erste, letzte, vorherige und nächste Dokument in einer Reihe von Dokumenten -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Wird verwendet, wenn ein Dienst eines Drittanbieters genutzt wird, um einen Blog zu pflegen -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Erzeugt einen automatischen Kommentar, wenn ein anderer WordPress-Blog auf deinen WordPress-Blog oder Beitrag verlinkt -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Benachrichtigt eine URL, wenn du auf sie in deinem Dokument verlinkst -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Ermöglicht das Posten auf deiner eigenen Domain mit einem Micropub-Client -->
<link rel="micropub" href="https://example.com/micropub">

<!-- Offene Suche -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Search Title">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prefetching, Preloading, Prebrowsing -->
<!-- Mehr Infos: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Link Relations](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Icons

```html
<!-- Für IE 10 und niedriger -->
<!-- Platziere favicon.ico im Stammverzeichnis - kein Tag notwendig -->

<!-- Icon in der höchsten Auflösung, für die wir es brauchen -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Apple Touch Icon (reuse 192px icon.png) -->
<link rel="apple-touch-icon" href="/pfad/zu/apple-touch-icon.png">

<!-- Safari Pinned Tab Icon -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [Alles über Favicons (und Touch-Symbole)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Pinned Tab Icons erstellen](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Favicon Spickzettel](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Icons & Browserfarben](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Sozial

### Facebook Open Graph
> Die meisten Inhalte werden auf Facebook als URL geteilt. Deshalb ist es wichtig, dass du deine Website mit Open Graph-Tags kennzeichnest, um die Kontrolle darüber zu haben, wie deine Inhalte auf Facebook erscheinen. [Mehr über Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup)

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Inhalt Titel">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:image:alt" content="Eine Beschreibung dessen, was auf dem Bild ist (keine Bildunterschrift)">
<meta property="og:description" content="Beschreibung hier">
<meta property="og:site_name" content="Seitenname">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [Open Graph Protokoll](http://ogp.me/)
- 🛠 Teste deine Seite mit dem [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card
> Mit Twitter Cards kannst du Fotos, Videos und Medienerlebnisse an Tweets anhängen und so den Traffic auf deiner Website erhöhen. [Mehr über Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Inhalt Titel">
<meta name="twitter:description" content="Inhaltsbeschreibung weniger als 200 Zeichen">
<meta name="twitter:image" content="https://example.com/image.jpg">
<meta name="twitter:image:alt" content="Eine Textbeschreibung des Bildes, die das Wesentliche eines Bildes für sehbehinderte Nutzer vermittelt. Maximal 420 Zeichen.">
```

- 📖 [Erste Schritte mit Karten - Twitter Developers](https://dev.twitter.com/cards/getting-started)
- 🛠 Teste deine Seite mit dem [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Twitter Datenschutz
Wenn du Tweets in deine Website einbettest, kann Twitter Informationen von deiner Website nutzen, um Inhalte und Vorschläge für Twitter-Nutzer/innen anzupassen. [Mehr über die Datenschutzoptionen von Twitter](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- verhindere, dass Twitter die Informationen deiner Website für Personalisierungszwecke verwendet -->
<meta name="twitter:dnt" content="on">
```

### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Inhalt Titel">
      <meta itemprop="description" content="Inhaltsbeschreibung weniger als 200 Zeichen">
      <meta itemprop="image" content="https://example.com/image.jpg">
```

**Hinweis:** Für diese Meta-Tags müssen die Attribute `itemscope` und `itemtype` zum `<html>`-Tag hinzugefügt werden.

- 📖 [Erste Schritte - schema.org](https://schema.org/docs/gs.html)
- 🛠 Teste deine Seite mit dem [Rich Results Test](https://search.google.com/test/rich-results)

### Pinterest

Auf Pinterest kannst du verhindern, dass Leute Dinge von deiner Website speichern, wie du [im Hilfecenter] (https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site) nachlesen kannst. Die `Beschreibung` ist optional.

```html
<meta name="pinterest" content="nopin" description="Tut mir leid, du kannst auf meiner Website nicht speichern!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- Die URL der Webversion deines Artikels -->
<link rel="canonical" href="https://example.com/article.html">

<!-- Der Stil, der für diesen Artikel verwendet werden soll -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Artikel erstellen - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Code-Beispiele - Sofortige Artikel](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profil: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profil: XML">
```

- 📖 [oEmbed Format](https://oembed.com/)

### QQ/Wechat

Nutzer, die Webseiten auf qq wechat teilen, erhalten eine formatierte Nachricht

```html
<meta itemprop="name" content="share title">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="share content">
```
- 📖 [Code Format Docs](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Browser / Plattformen

### Apple iOS

```html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Deaktiviere die automatische Erkennung und Formatierung von möglichen Telefonnummern -->
<meta name="format-detection" content="telephone=no">

<!-- Startsymbol (180x180px oder größer) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Bild des Startbildschirms -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Titel des Startsymbols -->
<meta name="apple-mobile-web-app-title" content="App Titel">

<!-- Aktiviere den Standalone-Modus (Vollbildmodus) -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Aussehen der Statusleiste (hat keinen Effekt, wenn der Standalone-Modus nicht aktiviert ist) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS App Deep Linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Webanwendungen konfigurieren](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Zum Startbildschirm hinzufügen -->
<meta name="mobile-web-app-capable" content="yes">
<!-- Mehr Infos: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android App Deep Linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Übersetzungsaufforderung deaktivieren -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- IE 8/9/10 zwingen, seine neueste Rendering-Engine zu verwenden -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Deaktiviere die automatische Erkennung und Formatierung möglicher Telefonnummern durch die Skype Toolbar Browsererweiterung -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Kacheln -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Minimal erforderliches Xml-Markup für `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <quadrat150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <quadrat310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

- 📖 [Referenz des Browser-Konfigurationsschemas](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Browser (Chinesisch)

### 360 Browser

```html
<!-- Wähle die Reihenfolge der Rendering-Engines -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

```html
<!-- Sperrt den Bildschirm in der angegebenen Ausrichtung -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Dieses Dokument im Vollbildmodus anzeigen -->
<meta name="x5-fullscreen" content="true">

<!-- Das Dokument wird im "Anwendungsmodus" (Vollbild, etc.) angezeigt -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

```html
<!-- Sperrt den Bildschirm in der angegebenen Ausrichtung -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Dieses Dokument im Vollbildmodus anzeigen -->
<meta name="full-screen" content="yes">

<!-- Der UC-Browser zeigt Bilder an, auch wenn er im "Textmodus" ist -->
<meta name="imagemode" content="force">

<!-- Das Dokument wird im "Anwendungsmodus" angezeigt (Vollbild, verbietende Gesten, etc.) -->
<meta name="browsermode" content="application">

<!-- Deaktiviert den "Nachtmodus" des UC-Browsers für dieses Dokument -->
<meta name="nightmode" content="disable">

<!-- Vereinfache das Dokument, um die Datenübertragung zu reduzieren -->
<meta name="layoutmode" content="fitscreen">

<!-- Deaktiviere die Funktion des UC-Browsers, die Schrift zu skalieren, wenn es viele Wörter in diesem Dokument gibt" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [UC Browser Docs](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## App Links

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="App Links">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="App Links">
<meta property="al:android:package" content="org.applinks">

<!-- Web Fallback -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [App Links](https://developers.facebook.com/docs/applinks)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Andere Ressourcen

- 📖 [HTML5 Boilerplate Docs: Das HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [HTML5 Boilerplate Docs: Erweitern und Anpassen](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Verwandte Projekte

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom-Paket für "HEAD"-Snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text-Paket für `HEAD`-Snippets
- head-it](https://github.com/hemanth/head-it) - CLI-Schnittstelle für `HEAD`-Snippets
- vue-head](https://github.com/ktquez/vue-head) - Manipulation der Meta-Informationen des `HEAD` Tags für Vue.js

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## Andere Formate

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## 🌐 Übersetzungen

- 🇮🇩 [Bahasa](https://github.com/rijdz/HEAD)
- 🇧🇷 [Brasilianisches Portugiesisch](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinesisch (Vereinfacht)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [Deutsch](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Italienisch](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japanisch](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Koreanisch](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russisch/Русский](https://github.com/Konfuze/HEAD)
- 🇪🇸 [Spanisch](https://github.com/alvaroadlf/HEAD)
- 🇹🇷 [Türkisch/Türkçe](https://github.com/mkg0/HEAD)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**

## 🤝 Beitragend

**Eröffne ein Issue oder einen Pull Request, um Änderungen oder Ergänzungen vorzuschlagen.**

### Leitfaden

Das **HEAD** Repository besteht aus zwei Zweigen:

#### 1. Meister

Dieser Zweig besteht aus der Datei "README.md", die auf der Website [htmlhead.dev](https://htmlhead.dev/) zu finden ist. Alle Änderungen am Inhalt des Handbuchs sollten in dieser Datei vorgenommen werden.

Bitte befolge diese Schritte für Pull Requests:

{:.list-style-default}
- Ändere jeweils nur ein Tag oder eine zusammenhängende Gruppe von Tags
- Verwende doppelte Anführungszeichen für Attribute
- Füge keinen abschließenden Schrägstrich in selbstschließende Elemente ein - die HTML5-Spezifikation sagt, dass sie optional sind.
- Erwäge, einen Link zur Dokumentation aufzunehmen, die deine Änderung unterstützt.

#### 2. `gh-Seiten`

Dieser Zweig ist für die Website [htmlhead.dev](https://htmlhead.dev/) verantwortlich. Wir verwenden [Jekyll](https://jekyllrb.com/), um die Markdown-Datei "README.md" auf [GitHub Pages](https://pages.github.com/) bereitzustellen. Alle Änderungen an der Website sollten in diesem Zweig vorgenommen werden.

Es kann hilfreich sein, die [Jekyll Docs](https://jekyllrb.com/docs/home/) zu lesen und zu verstehen, wie Jekyll funktioniert, bevor du in diesem Zweig arbeitest.

## 🌟 Mitwirkende

Schau dir all die super tollen [Mitwirkenden](https://github.com/joshbuchea/HEAD/graphs/contributors) an 🤩

## 👤 Autor

**Josh Buchea**

- GitHub: [@joshbuchea](https://github.com/joshbuchea)
- Mastodon: [@joshbuchea@hachyderm.io](https://hachyderm.io/@joshbuchea)

## 💛 Unterstützung

Wenn dieses Projekt für dich oder deine Organisation hilfreich war, überlege bitte, meine Arbeit direkt zu unterstützen:

- 💛 [Unterstütze mich auf GitHub](https://github.com/sponsors/joshbuchea)
- ⭐️ [Sternchen für dieses Projekt auf GitHub](https://github.com/joshbuchea/HEAD)
- 🐙 [Folge mir auf GitHub](https://github.com/joshbuchea)
- 🐘 [Folge mir auf Mastodon](https://hachyderm.io/@joshbuchea)

Alles hilft, danke! 🙏

- Josh

## 📝 Lizenz

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ zurück zum Anfang](#Inhaltsverzeichnis)**
