# Waagh Ghashstabba — Horus Heresy Orks — Revision 3

A combined BattleScribe catalogue for Horus Heresy 1.0 / 7th-edition-era play. It integrates three Ork layers into one Great Crusade Standard-style force organisation:

- Great Crusade Greater Orks from the Xenos of the Great Crusade catalogue.
- Lesser Orks adapted from the archived BSData Codex: Orks (2014) roster.
- Waagh Ghashstabba characters, units, armoury rules, Gargants and Mega-Gargant.

## Force organisation
1–3 HQ, 0–4 Elites, 2–6 Troops, unrestricted Dedicated Transports, 0–3 Fast Attack, 0–3 Heavy Support, 0–1 Lord of War and 0–1 Fortification. The catalogue deliberately does not stack the 7th-edition Ork Horde Detachment benefits on top of the Horus Heresy detachment.

## Combined terminology
**Ork** means Greater and Lesser Orks. **Greater Ork** means the Great Crusade-era Orks and Waagh Ghashstabba units explicitly treated as Greater Orks. **Lesser Ork** means the Codex: Orks (2014) layer. Gretchin are part of the faction but are not Ork models unless a rule specifically includes them. A rule naming *Ork Warriors* applies to that named Great Crusade unit, not every Ork infantry unit.

## Included Lesser-Ork core
Warboss, Big Mek, Weirdboy, Painboy, Boyz, Gretchin, Nobz, Meganobz, Burna Boyz, Tankbustas, Kommandos, Stormboyz, Warbikers, Deffkoptas, Lootas, Mek Gunz, Deff Dread, Killa Kans, Battlewagon, Trukk and Stompa. Lesser Orks retain their own 7th-edition faction rules; these are not automatically granted to Greater Orks.

## Waagh Ghashstabba
Includes Primeork Ghashstabba Bigshanka, Big Grork Niceteef, Sneaky Boss, Sneakyslitta Borewing, Grork (Big Mek), Da Ghashas, Niceteef's Meka-dred, Custom Gargant and Mega-Gargant, plus the combined-armoury reference and Greater-Ork upgrade groups.

The Mega-Gargant is 2,000 points before upgrades, AV15/15/13, 42 HP, Transport 100 and uses **Towering Monstrosity (Warlord Titan)** through *Da Biggerest*. The Custom Gargant remains Towering Monstrosity (Warbringer Titan).

## Sources / implementation
The catalogue uses the supplied Xenos of the Great Crusade file as its Horus Heresy schema/base and the supplied Waagh Ghashstabba document for the custom material. The Lesser-Ork layer is adapted from the archived BSData 7th-edition Orks catalogue rather than importing the 7e detachment bonuses.

Validation performed: XML well-formedness, duplicate-ID scan, exposed-entry/category target checks, archive integrity and repository-index consistency. Native BattleScribe/iOS rendering is not available in this environment, so this revision should be treated as the first field-test build.


## v2 audit fixes
- Linked selectable weapon special rules to roster output (including Spear Launcha: Monster Hunter and Gotcha).
- Added rule/profile output for Ghashstabba character armoury upgrades, including Shovel Shield, Stasis Grenade, Cybork Body, Red Eye, Sparky Bitz and Heavy Ramshackle Armour.
- Mega-Gargant now explicitly displays WS4, S D, I1 and A5 alongside its vehicle armour/HP profile.
- Audited selectable weapon keyword rules across the catalogue.


## Revision/update protocol
Revision 3 repairs repository update detection. The catalogue `revision` and both index copies' `dataRevision` are now advanced together.

For every future release: (1) increase the catalogue `revision`; (2) set the same value in `index.xml` `dataRevision`; (3) rebuild `index.bsi` from that updated `index.xml`; (4) keep the catalogue `dataId` and filename stable; (5) upload/replace the `.catz`, `index.xml`, and `index.bsi` together. This allows an existing BattleScribe repository URL to discover new revisions without being re-added.


## v4 archive-format repair
- Rebuilt `index.bsi` as a standard ZIP archive containing exactly one `index.xml`.
- Rebuilt the `.catz` as a standard ZIP archive containing exactly one `.cat`; the prior v3 `.catz` was incorrectly GZIP-compressed.
- Advanced catalogue and data-index revision to 4 while retaining the stable catalogue ID and filename for future updates.
- Future releases must use ZIP for both `.bsi` and `.catz`, never GZIP.


## v5 statline and rule-output repair
- Additional models such as Big Ounda Squig now have proper Unit profiles. Big Ounda Squig displays WS4 BS0 S5 T5 W3 I3 A D6+2 Ld6 Sv5+ plus Ghashing Bite and Big Ead weapon profiles.
- Heavy Ramshackle Armour now outputs a full owning-model statline with Save 3+.
- Attack Squig now outputs the owning model with +1 Attack.
- Red Eye outputs a clearly labelled stationary-turn alternate statline with +1 BS and its Ignores Cover rule text.
- Equipment rules are embedded directly in the selected equipment entry rather than relying only on infoLinks.
- Weapon special rules are embedded directly beneath the selected weapon. Any weapon Type keyword matching a catalogue shared rule now receives that rule as a direct rule object, including Monster Hunter and Gotcha on Spear Launcha.
- Catalogue and both repository indexes advanced together to revision 5.
