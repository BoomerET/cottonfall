# Cottonfall — Project Bible and Development Reference

> **GM / developer spoilers.** This document will be publicly accessible in the GitHub repository. Players should avoid reading it before playing.
>
> **Source-of-truth rule:** The repository's files and tagged releases are authoritative for *implemented* content. This document records canon, creative decisions, and plans. Brainstorming does not automatically become canon; planned features are not shipped features.

_Last consolidated: October 10, 2026._

## Project identity

- **Repository:** https://github.com/BoomerET/cottonfall
- **Setting:** Cottonfall, Texas, fictional Tolliver County
- **Platform:** Foundry Virtual Tabletop v14
- **System:** GURPS Fourth Edition, unofficial GURPS 4E Game Aid (`gurps`)
- **Required module:** FXMaster (`fxmaster`), per the v0.2.0 manifest
- **Tone:** Small-town investigative horror, absurd bureaucracy, and cosmic unease; influences include *Welcome to Night Vale*, *Delta Green*, and *The X-Files*.
- **Motto:** “A Nice Place to Live. Please Remain Where You Are.”
- **Distribution:** Free, noncommercial. Refer to `LICENSE` and `CREDITS.md` for exact terms.

The PCs are lifelong or established residents, not visitors arriving to investigate a strange town. Cottonfall's unusual rules are familiar and accepted. Horror emerges when those rules stop behaving consistently.

## Release and implementation status

### Verified from the repository's main-branch files

- `module.json` identifies the unified module as **`cottonfall`**, version **0.2.0**.
- Minimum and verified Foundry compatibility: **14**.
- Adventure compendium: `cottonfall-adventure`, path `packs/cottonfall-adventure`.
- Main JavaScript entry: `scripts/cottonfall-fx.js`.
- Stylesheet: `styles/cottonfall-fx.css`.
- Socket support enabled.
- Download URL in the manifest points to `v0.2.0/cottonfall-v0.2.0.zip`.

These are manifest and README facts; they do not independently prove that every release asset or runtime effect has been retested today.

### Milestones

| Version | Status | Scope |
| --- | --- | --- |
| v0.1.0 | Previously released and clean-install tested | *The Missing Resident* standalone Adventure; imported journals, actors, scene, images, and audio |
| v0.2.0 | Current version in `module.json` | Unified Cottonfall Adventure and Cottonfall FX |
| v0.3.0 | **Planned / in development** | *The Resident Who Never Existed*; do not represent as shipped |

Consult the root `README.md` for current installation instructions and feature descriptions.

## Established setting canon

### Cottonfall

- Fictional small Texas town in **Tolliver County**.
- Normal population shown on the town sign: **18,742**.
- Institutions include Emergency Management, the *Cottonfall Clarion*, Fire & EMS, the Sheriff's Office, a veterinary clinic, and local ranches.
- Townspeople take unusual civic rules seriously without necessarily explaining them.

### The 3:17 Rule

- Tornado sirens are normally tested **at noon on the first Wednesday of each month**.
- If sirens sound at **3:17 a.m.**, residents stay indoors, do not look outside, and do not try to photograph or record the event.
- If someone outside calls a resident's name, that voice has mistaken them for somebody else. **Do not correct them.**
- The origin and mechanism of the rule are unresolved.

### Bodark

- Bodark is an anomalous, supposedly former town whose past and present contradict one another.
- The sign **“BODARK — 2 MILES”** cannot be trusted as a measurement; residents are advised not to measure the route.
- **Bodark Elementary** has exactly **317 students** every year, with remarkable test results and few credible memories of former pupils.
- Do not definitively explain Bodark's geography, history, school, or relationship to Cottonfall.

## Episode 01 — The Missing Resident

**Status:** Introductory Adventure compendium in the repository.

### Premise

The population sign changes from **18,742** to **18,741**. Nobody recalls a resident leaving. At **3:17 a.m.**, Emergency Management receives a terrified male voicemail about being forgotten. A tornado siren is audible in the recording, but the warning-system log records **no activation**, and nobody reports hearing it.

### GM continuity from adventure development

The erased resident is **Dr. Samuel “Sam” Bell**, a large-animal veterinarian, approximately 49, and longtime friend/colleague of **Dr. Maggie Foster**.

Established design chronology:

1. Sam makes an after-hours visit to **Holloway Ranch**.
2. He encounters the Bodark sign and follows an impossible stretch of road.
3. He returns terrified and leaves a written warning identifying himself, Maggie, the siren, and Bodark.
4. His abandoned white Ford F-250 has **98 unexplained miles**.
5. **Calvin Rusk** picks him up; the vehicle overheats, and Sam's footprints inexplicably end.
6. **Evelyn Harrell** has a related encounter.
7. **Marcus** has an EMS monitoring record spanning **03:11:24–03:17:00**.
8. A voicemail arrives at **3:17 a.m.**, with a siren that neither the system nor witnesses corroborate.

**Verification note:** This chronology records prior GM design decisions. Before using individual details as published evidence, cross-check the actual packaged Foundry journals and handouts.

### What remains unresolved

- Sam existed, but the town has forgotten him.
- Contradictory evidence survives imperfectly.
- His ultimate fate, the mechanism of forgetting, the siren's source, the identity of “it,” and Bodark's true nature remain unexplained.
- The scenario need not culminate in Sam's rescue or a complete supernatural explanation.

### Pregenerated player characters

| Character | Role |
| --- | --- |
| **Eli Mercer** | Cottonfall Emergency Manager |
| **June Pruitt** | Editor of the *Cottonfall Clarion* |
| **Marcus “Doc” Whitfield** | Paramedic, Volunteer Fire & EMS |
| **Rosa Delgado** | Deputy, Tolliver County Sheriff's Office |
| **Wade Tillman** | Ranch hand and weekend saddle-bronc rider |

Each character begins with a different contradiction. Design scenes so no single character, including Eli, monopolizes the investigation.

### Investigation design principle

> We know the truth of what happened. We do not know how the players will discover it.

Essential clues should not be gated behind successful skill rolls. Rolls can reveal deeper context, speed discovery, or provide advantages. Reasonable player approaches must remain viable.

## Foundry structure and development conventions

### Repository directories

- `module.json` — module metadata, dependencies, and compendium declaration
- `packs/cottonfall-adventure/` — packaged Adventure
- `scripts/` — Cottonfall FX implementation
- `styles/` — FX styles
- `templates/` — UI templates
- `assets/`, `images/` — media
- `.github/workflows/` — automation
- `README.md` — public documentation
- `LICENSE`, `CREDITS.md` — permissions and attribution

### Adventure journal organization

- `00 - Player's Guide` — what residents know
- `01 - Locations`
- `02 - People`
- `03 - Organizations` — intentionally unpopulated in the initial release
- `04 - Weirdness` — GM-only recurring phenomena
- `05 - Mysteries` — clues and case materials
- `06 - Episodes` — GM instructions and scenes
- `07 - GURPS` and `08 - Player Notes` — organizational concepts; not necessarily shipped

Keep player and GM information separated using Foundry ownership settings. Foundry journal pages use HTML content; avoid repeating the page title as a redundant first `<h1>`.

### Cottonfall FX — documented in v0.2.0 README

- **Visual Glitch:** Subtle, VHS, Hard
- **Reality:** Reality Lurch, Full Break
- **Events:** 3:17 Event
- **Atmosphere:** Fog In, Clear Fog, Flicker
- **Something in the Fog:** timed shadow apparition
- **Emergency Broadcast:** Shelter in Place, Missing Resident, Unidentified Transmission, 3:17 Protocol, plus custom title/message/duration and broadcast/dismiss controls

The actual scripts and README determine exact runtime behavior. Test player synchronization, cleanup, permissions, and scene changes before publishing modifications.

### Release checklist

1. Commit source changes; keep tagged releases immutable.
2. Update `module.json` version and release URLs together.
3. Validate manifest JSON, ZIP paths, dependencies, and asset references.
4. Test a public-manifest installation in a clean Foundry v14/GURPS world.
5. Import the Adventure and inspect actors, journals, scenes, handouts, audio, ownership, and FX.
6. Never package GURPS rulebook PDFs or third-party copyrighted rules text.

## Episode 02 / v0.3.0 — The Resident Who Never Existed

**Status: design in progress; not verified as implemented.**

### Accepted creative constraints

- Keep the cause of the disappearance **deliberately ambiguous**.
- The voice on the recording is **definitely male**.
- The caller's identity is **completely unknown**. Do not casually identify him as Sam Bell.
- The tornado siren is unmistakably audible on the recording.
- Cottonfall's warning system records **no siren activation at 3:17 a.m.**, and no residents report hearing one.
- Preserve this as a deliberate contradiction, not a continuity mistake to be smoothed away.

### Audio transcript supplied during design

> “Please. My name is—”  
> *[four seconds of static]*  
> “They're going to forget me. Please don't let them—”  
> *[tornado siren]*  
> “Oh God. It's here.”  
> *[END]*

**Established canon — The 3:17 Voicemail:** Episode 01 (*The Missing Resident*) and Episode 02 (*The Resident Who Never Existed*) reference the **same original audio recording**, not two separate incidents.

The caller is unmistakably male, but his identity remains unknown. The recording must not be definitively attributed to Dr. Samuel Bell.

A tornado siren is clearly audible in the recording, despite Cottonfall's warning system showing **no activation at 3:17 a.m.** and no residents reporting hearing a siren.

**These contradictions are intentional and must be preserved.**

### Work still to do

- Establish the new inciting incident and distinguish it from Episode 01.
- Map evidence and multiple investigative paths without single-point-of-failure clues.
- Give all five PCs meaningful roles.
- Draft GM-only and player-facing Foundry journals, NPC responses, and handouts.
- Audit existing images/audio before creating replacements.
- Package and clean-install test the release.

## Deliberately unresolved mysteries

Do **not** supply definitive explanations without an explicit creative decision:

- What causes 3:17 phenomena
- Who or what operates the impossible siren
- What “it” is in the recording
- Why Bodark's distance, history, and school records contradict reality
- Why Bodark Elementary always has 317 students
- How Cottonfall forgets people, or whether every erasure has the same cause
- What ultimately happened to Sam Bell
- Who the unidentified male caller is in the planned second episode

Individual cases may have discoverable truths without explaining the entire cosmology.

## Next session checklist

1. Cross-check this reference against current compendium journals, media, scripts, and release tags.
2. Reconcile the Episode 01 and Episode 02 voicemail references **without assuming they're identical**.
3. Identify what v0.3.0 work is actually committed versus discussed only in chat.
4. Design Episode 02's playable investigation and player choices.
5. Implement and test Foundry content incrementally.
6. Update this file whenever canon is accepted, features ship, or open questions are resolved.

## Working across ChatGPT conversations

Start a new development conversation with the repository URL, the path `docs/COTTONFALL_PROJECT.md`, and the immediate task. Ask the assistant to read the **current** project file and relevant source files before making changes. Never assume that a previous chat's plan was implemented.

---

*Cottonfall is a nice place to live. Please remain where you are.*
