# Lab 04 · CI/CD: automaatne kontroll, ehitus ja tarne · ülesanne

**Loeng:** <https://hkhk-automation.github.io/devops-lite/week04/lecture/>
**Praktikum:** <https://hkhk-automation.github.io/devops-lite/week04/lab/>
**Kodune õpe ja kodutöö:** <https://hkhk-automation.github.io/devops-lite/week04/homework/>

See fail on ülesande kirjeldus, seda ei pea muutma. Klassitöö vastused kirjutad faili **`README.md`**, mis on mall. Workflow ja rolli muudatused teed praktikumi juhendi järgi.

## Mis repositooriumis alguses on

| Fail | Mis see on |
|---|---|
| `site.yml`, `inventory.ini`, `ansible.cfg`, `group_vars/`, `roles/` | K3 lahendus: Docker ja Compose'i pinu vm3-s |
| `stack/` | K3 Compose-fail, rakendus ja proxy seaded |
| `.yamllint`, `.ansible-lint` | lint'i reeglid |
| `.github/workflows/abi-teavitus.yml` | teavitab juhendajat, kui avad abi-issue |
| `vead/` | kodutöö H5 jaoks, ära kasuta klassitöös |

Eeldus: vm1-st töötab `ssh vm3` võtmega (K2 osa A).

## Mis peab lõpuks repositooriumis olema

**Klassis (praktikum):**

| Fail | Kust |
|---|---|
| `.github/workflows/ci.yml` | A1–A5, B1 |
| rollide parandused (`ansible-lint` on roheline) | A3 |
| `group_vars/docker/vault.yml` (krüptitud), `group_vars/all.yml` | B2 |
| `stack/compose.yaml`, `roles/stack/` (image GHCR-ist) | B2 |
| `logid/tarne.txt`, `logid/tarne_kontroll.txt` | B3 |
| `README.md` täidetud, liidetud PR-iga | B4, Esitamine |

**Kodus (kodune õpe ja kodutöö, vabatahtlik boonus):**

| Fail | Kust |
|---|---|
| `markmed.md`, `vastused.md` | I, H2, III |
| `ci.yml` suitsutest | H1 |
| `ci.yml` Trivy, `logid/trivy.txt` | H2 |
| `logid/tagasi.txt` | H3 |
| `.github/dependabot.yml`, action'id räsiga | H4 |
| `vead.md` | H5 |

## Kontrollnimekiri (Issues ja projekt)

Repositooriumi **Issues** all on selle nädala issue **Lab 04 · CI/CD**. Märgi ruut, kui osa on tehtud. Kui kõik on tehtud, sulge issue.

Kui jääd kinni: **Issues → New issue → Vajan abi**. Juhendaja saab teate.

## Kontroll

Igal push'il main harusse käivitub automaatne kontroll **Autograde** (vahekaart **Actions**). Hinne: K1–K5 (45 p). README ja kodutöö on vabatahtlik boonus: punane rist tähendab ainult, et boonus on tegemata.

| Kontroll | Punkte |
|---|---|
| K1–K5: failid, workflow, lint, tarne, tõendid | 45 |
| BOONUS README mall täidetud | boonus |
| BOONUS H1 suitsutest, H2 Trivy, H3 tagasipööramine | boonus |
| BOONUS H4 action'id räsiga, H5 kolleegi vead | boonus |
| BOONUS I märkmed ja vastused | boonus |

## Esitamine

Autograde hindab main haru. Kui main on kaitstud (B4), läheb iga muudatus harusse ja sealt pull request'iga main harusse. Tähtaeg on kirjas Classroom 50-s. Reposse ei lähe paroole ega tokeneid avatud kujul ega `.env` faili.
