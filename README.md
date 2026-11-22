<p align="center">
  <img src="images/maelk-rankup-banner.png" alt="MÆLK Rankup HUD — Dit næste rank. Ét overblik." width="100%">
</p>

<h1 align="center">MÆLK Rankup HUD</h1>

<p align="center">Et kompakt overblik over krav, pris og fremskridt til dit næste rank på MÆLK.</p>

<p align="center">
  <strong>Minecraft Java 26.3 · Fabric · Rank 1–100 · Kun på klienten</strong>
</p>

<p align="center">
  <a href="https://github.com/RolfDenDanske/maelk-rankup-hud-download/releases/latest"><strong>Download moddet</strong></a>
  · <a href="#installation">Installation</a>
  · <a href="#flyt-boksen">Flyt boksen</a>
</p>

## Dit næste rank, samlet ét sted

- **100 rankovergange:** 404 krav og prisen for hvert rankup.
- **Fremskridt pr. krav:** Antal og procenter fra inventory og dine samlede Minecraft-statistikker.
- **Samlet procent:** Se, hvor langt du er fra næste rank, inklusive pengekravet.
- **Kun det, du mangler:** Opfyldte krav skjules og kommer tilbage, hvis du ikke længere opfylder dem.
- **Pris frem for balance:** Boksen viser rankup-prisen og det beløb, du eventuelt mangler.
- **Klar besked:** Når alle aflæselige krav er bekræftet opfyldt, står der **“Skriv /Rankup”**. Du sender selv kommandoen.

<img src="images/maelk-rankup-features.png" alt="Rank 1–100, fremskridt, tilpasning via Esc-menuen og rankup-besked" width="100%">

*Billederne er markedsføringsillustrationer skabt med ImageGen, ikke skærmbilleder fra spillet.*

## Installation

Du skal bruge **Minecraft Java 26.3**, **Fabric Loader 0.20.1 eller nyere** og **Fabric API 0.166.2+26.3 eller nyere til 26.3**.

1. Installer [Fabric til Minecraft 26.3](https://fabricmc.net/use/installer/).
2. Hent [Fabric API til 26.3](https://modrinth.com/mod/fabric-api/versions?g=26.3&l=fabric).
3. Åbn [seneste release](https://github.com/RolfDenDanske/maelk-rankup-hud-download/releases/latest), og hent **`maelk-rankup-hud-1.3.0.jar`** under **Assets**.
4. Læg moddet og Fabric API i `mods`-mappen i din Fabric-profils spilmappe.
5. Start Fabric-profilen, og gå ind på MÆLK-serveren.

**Opdatering:** Luk Minecraft og fjern den gamle mod-JAR, før du lægger den nye ind. Behold konfigurationen: placering, størrelse og tilpassede krav bevares. Manglende ranks tilføjes automatisk, og den tidligere konfiguration sikkerhedskopieres.

**Vælg JAR-filen under Assets.** GitHubs automatiske “Source code”-arkiver på denne downloadside indeholder kun sidens beskrivelse og billeder. Moddets kildekode ligger ikke i dette repository.

## Flyt boksen

Åbn **Esc → Rankup HUD**.

| Handling | Sådan gør du |
| --- | --- |
| Flyt boksen | Træk den med venstre museknap. |
| Ændr størrelse | Brug **Mindre** eller **Større**. |
| Gendan standard | Klik **Nulstil**. |
| Se flere krav på små skærme | Scroll i boksen i redigeringstilstand. |
| Gem og gå tilbage | Tryk **Esc** eller klik **Gem / luk**. |

Der er ingen keybind til flytning. **Esc-menuen er den eneste adgang til at flytte og ændre størrelse.**

## Sådan virker det

Din aktuelle rank og balance læses fra scoreboardet. Balancen bruges kun til at kontrollere, om du har råd, og vises ikke i boksen. Inventory og scoreboard aflæses ved hver HUD-visning. Hop og almindelig crafting får lokale live-opdateringer efter første synkronisering og afstemmes med serverens svar. Andre statistikker opdateres, når serverdata ankommer.

Ranknummeret i serverens rankmenu er den rank, du køber: **[46] betyder 45 → 46**. Kataloget dækker 0 → 1 til 99 → 100. Ved rank 100 vises **“Maksimal rank”**.

Den samlede procent er gennemsnittet af alle krav, inklusive prisen. Statistikkerne bruger hele den historik, serveren stiller til rådighed. Items i kister, ender chest, indhold inde i shulker boxes og items på musen tælles ikke med.

## Kendte begrænsninger

- **MIA Egg på 99 → 100:** Vises som **“Tjek servermenu”**, fordi fremskridtet ikke er tilgængeligt for klientmoddet. Det bliver ikke automatisk godkendt. Du kan selv prøve `/Rankup`, når serverens krav er opfyldt.
- **Bryg 100 Potions:** Bruger **Potion → Fremstillet / Times Crafted** og det tal, serveren har registreret. Splash og Lingering Potions er separate statistikposter og medregnes ikke i denne Potion-tæller.
- **Serverens regler:** Særlige plugin-tællere kan afvige fra almindelige Minecraft-statistikker. Serveren afgør altid, om et rankup kan gennemføres.

Moddet sender aldrig `/Rankup` automatisk. Ukendte data bliver aldrig behandlet som et opfyldt krav.

## Fejl og hjælp

Hvis noget ikke stemmer, så [opret en fejlrapport](https://github.com/RolfDenDanske/maelk-rankup-hud-download/issues/new) med modversion, Minecraft-version, aktuel rank og et billede af det relevante krav.

Version 1.3.0 er bygget og har bestået **30 automatiske tests**. Den er endnu ikke gennemtestet på MÆLK-serveren.

## Licens

Moddet distribueres under [MIT-licensen](LICENSE). Dette repository indeholder downloadsiden og billederne; moddets kildekode er ikke offentlig her.

*Et uafhængigt modprojekt. Ikke et officielt Minecraft-produkt og ikke godkendt af eller tilknyttet Mojang eller Microsoft.*
