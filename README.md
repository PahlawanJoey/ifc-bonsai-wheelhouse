# Bonsai wheelhouse

Bewaarde Bonsai-build `0.8.6-alpha260823` voor Python 3.12, gebruikt door `IFC_Demarcatie_01`.

**Release:** [bonsai-0.8.6-alpha2608231542](https://github.com/PahlawanJoey/ifc-bonsai-wheelhouse/releases/tag/bonsai-0.8.6-alpha2608231542)

| Platform | Bestandsnaam | SHA-256 | Herkomst |
| --- | --- | --- | --- |
| Windows x64 | `bonsai_py312-0.8.6-alpha260823-windows-x64.zip` | `35201ef40b4fd363062b5a32220fa58aa39bbeb99711852e16dc21d49cb62a83` | Ongewijzigde kopie van de oorspronkelijke Bonsai-release |
| Linux x64 | `bonsai_py312-0.8.6-alpha260823-linux-x64.zip` | `bf49bed67e5deb9052f467af5d3e5c00d9172f3df3fe0d81b6594a00ed9f976c` | Herbouwd via GitHub Actions |

## Linux-build reproduceren

Workflow: [`.github/workflows/rebuild-bonsai-linux.yml`](.github/workflows/rebuild-bonsai-linux.yml) — [geslaagde run](https://github.com/PahlawanJoey/ifc-bonsai-wheelhouse/actions/runs/42450939029).

- Bronproject: [IfcOpenShell/IfcOpenShell](https://github.com/IfcOpenShell/IfcOpenShell)
- Bronbranch: `v0.8.0`
- Vastgepinde broncommit: `144696c8b993a8ab10b3b604a3a4509f04b5dba1` (23 augustus 2026)
- Vastgepinde IfcOpenShell-binary: `v0.8.6-e333c1c-linux64` voor Python 3.12
- Buildcommando: `make dist PLATFORM=linux PYVERSION=py312 VERSION_DATE=260823`
- Doelrelease: `bonsai-0.8.6-alpha2608231542`

De workflow controleert bronversie, ZIP-integriteit, Blender-manifest (`linux-x64` en juiste versie), aanwezigheid van de Linux IfcOpenShell-wheel en publiceert alleen de Linux-ZIP naast de Windows-ZIP.

**Let op:** de Linux-ZIP is gereconstrueerd uit historische broncode met de bijbehorende vooraf gecompileerde IfcOpenShell-binary. Overige downloads worden niet allemaal op historische SHA's vastgezet. Daarom is dit niet gegarandeerd byte-voor-byte gelijk aan het oorspronkelijke, inmiddels verwijderde Linux-artifact. De workflow test de verpakking, niet de volledige Blender-runtime.

Licenties: Bonsai GPL-3.0-or-later; IfcOpenShell LGPL-3.0-or-later.
