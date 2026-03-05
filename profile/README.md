> ⚠️ This organization hosts **automated mirrors** of upstream repositories.  
> Development only occurs in the original upstream repositories.

# lrose-mirror

This GitHub organization provides an **automated mirror of LROSE-related repositories** from upstream projects.

The mirror exists to ensure the **long-term continuity, availability, and archival preservation** of the LROSE software ecosystem.

Primary upstream repositories are hosted by:

- **NCAR** – https://github.com/NCAR
- **mmbell** – https://github.com/mmbell

The mirror synchronizes selected repositories into this organization.

---

# Purpose

The goals of this mirror are:

- Provide **redundant hosting** for LROSE code
- Ensure **long-term preservation of repository history**
- Maintain a **stable location for downstream users**
- Reduce dependence on any single hosting organization
- Support long-term community maintenance of LROSE software

All mirrored repositories retain their **complete Git history**, including branches and tags.

---

# Mirrored repositories

Repositories currently mirrored include:

## NCAR LROSE repositories

- `homebrew-lrose`
- `lrose-bootstrap`
- `lrose-cedric`
- `lrose-circleci`
- `lrose-core`
- `lrose-data-examples`
- `lrose-devel`
- `lrose-displays`
- `lrose-docs`
- `lrose-ecco`
- `lrose-emerald`
- `lrose-examples`
- `lrose-field-catalog`
- `lrose-geolib`
- `lrose-grid2ps`
- `lrose-netcdf`
- `lrose-nexrad`
- `lrose-paper-volscan-timing`
- `lrose-projects-eolbase`
- `lrose-projects-lakevic`
- `lrose-projects-precip`
- `lrose-projects-relampago`
- `lrose-refract`
- `lrose-reorder`
- `lrose-sgci`
- `lrose-solo-python`
- `lrose-solo3`
- `lrose-soloii`
- `lrose-sysview`
- `lrose-test`
- `lrose-titan`
- `lrose-uw-general`
- `lrose-uw-olympex`

## Mirrored related repos from MMBELL:

These repositories are also mirrored because they are widely used within the LROSE ecosystem:

- `fractl` – from `mmbell`
- `vortrac` – from `mmbell`
- `samurai` – from `mmbell`

---

# How mirroring works

Mirroring is performed automatically using **GitHub Actions**.

A workflow runs on a scheduled basis (currently every 6 hours) and performs the following steps:

1. Clone each upstream repository as a **Git mirror**
2. Push all branches and tags to the corresponding repository in this organization
3. Preserve the complete Git history

The workflow is maintained in:

```
  mirror-control/.github/workflows/sync-all.yml
```


The automation uses a GitHub Personal Access Token stored as the secret:

```
  MIRROR_TOKEN
```


The token has permissions to update repository contents and workflows.

---

# Repository structure

This organization contains:

| Repository | Purpose |
|-------------|--------|
| `mirror-control` | Infrastructure repository containing synchronization workflows |
| `lrose-*` | Mirrors of upstream LROSE repositories |
| `fractl` | Mirror of `mmbell/fractl` |
| `vortrac` | Mirror of `mmbell/vortrac` |
| `samurai` | Mirror of `mmbell/samurai` |

---

# Contributing

These repositories are **mirrors of upstream projects**.

Issues and pull requests should generally be submitted to the **original upstream repository**, unless the project maintainers decide to transition development here in the future.

---

# Future role of this organization

At present this organization functions as a **read-only mirror**.

However, it also provides a **potential continuity path** for the LROSE ecosystem if upstream repositories become unavailable or if stewardship of the software transitions to the broader community.

---

# Maintainer

This mirror organization was established and is currently maintained by:

**Mike Dixon**

of the National Center for Atmospheric Research (NCAR).

---

# License

Each repository retains the license specified in its upstream source project.

