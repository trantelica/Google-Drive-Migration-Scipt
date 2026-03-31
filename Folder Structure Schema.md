# FOLDER MODEL: OPERATING RULES (AUTHORITATIVE)
## ORGANIZING PRINCIPLE
The Source folder (-S) is the atomic unit of work.
Everything else exists to help humans find, use, or govern that unit.
Governance is applied inside the unit, not by splitting the unit across the system.
Human usability is pre-eminent. Structure, not memory, enforces correctness.
## CORE RULE
There must be exactly one canonical, current, active version of any document at any point in time. Folder placement alone must allow a human to infer whether a file is authoritative, historical, supporting, or externally shared.
### 1) NAVIGATION FOLDERS (-N)
#### PURPOSE
Provide categorical and hierarchical navigation to Source folders. Navigation exists to help humans find the right atomic unit of work.
#### STRUCTURAL RULES
 * May contain other -N folders (nested hierarchy is expected).
 * May contain -S folders at any level.
 * May contain -N folders adjacent to -S folders.
 * May NOT contain files.
 * No personal or named folders permitted.
#### NAMING GUIDANCE
 * Describe the domain, process, or conceptual grouping.
 * Use nouns or noun phrases.
 * Avoid personal names, "misc," or catch-all terms.
 * Avoid dates unless the navigation concept itself is time-bound.
#### INTENT
A person unfamiliar with the team should be able to predict what kinds of Source folders exist beneath a given -N.
### 2) SOURCE FOLDERS (-S)
#### PURPOSE
The Source folder is the atomic unit of work. It is the canonical container for a work product or deliverable and the unit of ownership, accountability, and lifecycle management.
All governance is applied inside this unit.
#### STRUCTURAL RULES
 * Must live inside exactly one -N folder.
 * The root of the -S folder may contain ONLY the current, active version(s).
 * Files in the root of -S are, by definition:
   * Current
   * Authoritative
   * Actively maintained
#### HARD RULE (NON-NEGOTIABLE)
A file may NOT exist simultaneously:
 * In the root of -S, and
 * In any other folder (including -X)
This enforces the single, current, active version rule.
##### ALLOWED CONTENTS
 * Canonical files (current versions only)
 * Sub-folders (-sub)
 * Optional externally shared folder (-X)
##### NAMING GUIDANCE
 * Describe the business object or work product, not the activity.
 * Must make sense both in isolation and in the navigation path.
 * Prefer stable names over transient ones.
 * Include year or cycle only when it meaningfully distinguishes the object.
 * Do NOT include status words (draft, final) or people's names as the sole reference (e.g. Nate's folder).
### 3) FILES IN THE ROOT OF -S
#### RULES
 * Represent the current and authoritative version(s) of the work.
 * File names align to the Source folder name.
 * Do NOT encode lifecycle, versioning, or editorial history in filenames.
#### NAMING GUIDANCE
 * Use document type, audience, or form only when helpful.
 * Avoid version numbers, "final," or editor names.
#### INTENT
The folder identifies the work.
The filename identifies the form.
### 4) SUB-FOLDERS (-sub)
#### PURPOSE
Contain non-canonical materials that support, justify, or precede the current version, without splitting the unit of work.
All supporting context remains inside the Source folder.
#### STRUCTURAL RULES
 * May exist only inside an -S folder.
 * Files in -sub folders are NEVER current or authoritative.
#### COMMON EXAMPLES
 * versions-sub
 * approvals-sub
 * supporting docs-sub
 * deletion_candidates-sub
 * temporary-sub or desktop-sub
 * Use-case-specific variants as needed
#### NAMING GUIDANCE
 * Describe the role the files play relative to the Source.
 * Prefer functional, repeatable labels over bespoke phrasing.
### 5) EXTERNALLY SHARED FOLDERS (-X)
#### PURPOSE
Provide controlled external access without fragmenting the unit of work. Acts as a permission boundary, not a separate publishing system.
#### STRUCTURAL RULES
 * May exist only inside an -S folder.
 * Permissions are granted at the -X folder level, not the document level.
 * Contains only files intended for external consumption.
#### CANONICAL VERSION RULE
 * A file is canonical if it is the most recent, active version.
 * A canonical file must exist in ONE place only:
   * Internally active -> root of -S
   * Externally shared -> -X
 * A file may not exist in both locations at the same time.
#### OPERATIONAL INTENT
 * Moving a file into -X signals stability and approval for external use.
 * Updates, replacements, or deprecation are handled by managing files in -X.
#### EXCEPTION
Document-level sharing is permitted only for one-off, single-use scenarios.
#### NAMING GUIDANCE
 * Files retain their original names when moved to -X.
 * Movement, not renaming, signals the change in sharing state.
### SYSTEM GUARANTEES
 * The Source folder remains the atomic unit of work.
 * Navigation scales without splitting content.
 * Canonical status is inferable from location alone.
 * External sharing does not require repeated permission maintenance.
 * Supporting materials remain co-located with their Source.
 * The system remains usable, resilient, and understandable under turnover.

