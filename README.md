# Onlinefact Addon

Rapporten, brutomarges en margecalculator voor Onlinefact in Google Chrome op Windows.

## Download

[Download de nieuwste release](https://github.com/Jaze360/onlinefact-addon/releases/latest). Kies het installatiepakket onder Assets, pak het uit en lees START-HIER.html. De volledige programmabron en het bouwscript staan in dit pakket; de automatisch door GitHub aangeboden Source code-archieven bevatten alleen deze repositorypagina.

## Bijwerken vanaf versie 1.5.0

1. Wacht tot lopende rapporten klaar zijn.
2. Open **Updates** in Onlinefact Marges.
3. Klik **Bijwerken**.
4. Open `chrome://extensions` en klik bij Onlinefact Marges op **Opnieuw laden**.
5. Vernieuw Onlinefact.

Lokale API-toegang, rapporten, runtime-instellingen en kostafspraken blijven behouden. De vorige programmabestanden worden bewaard onder `backups/update-*`. Downloads worden op volledigheid en SHA-256 gecontroleerd. De updater accepteert alleen nieuwere definitieve releases uit deze repository.

## Eenmalig overstappen vanaf een oudere versie

Neem de programmabestanden van versie 1.5.0 over in dezelfde installatiemap. Behoud `native/runtime-config.json`, `native/host-manifest.json`, `native/host.cmd` en `native/cost-estimates.json`. Vervang de lokale kostafspraken niet door het lege voorbeeldbestand uit het publieke pakket. Herlaad daarna de extensie. De API-toegang hoeft niet opnieuw ingevoerd te worden.

Het publieke pakket bevat geen API-geheimen, verkooprapporten of bedrijfsspecifieke kostafspraken. Nieuwe installaties gebruiken de standaard voorraadkosten; specifieke kostafspraken worden lokaal beheerd.

## Nieuwe versie publiceren

Verhoog `extension/manifest.json` version en voer met Node.js `node build-update.cjs release` uit vanuit het uitgepakte programmapakket. Test de wijziging en publiceer een definitieve GitHub-release met tag `v<VERSIE>`. Voeg `onlinefact-update.json` en `onlinefact-update.sha256` uit de map release toe met exact deze namen en markeer de release als Latest. Voeg voor nieuwe installaties ook een bijgewerkt installatiepakket zonder lokale gegevens toe. Werknemers kunnen daarna zelf via Bijwerken de versie ophalen.
