# Campaign System — Operator & Handoff Guide
Version: 1.1 (Architect Edition)

This repository contains a fully specified tabletop RPG campaign system
designed for deterministic execution by an AI.

This file is NOT a rules document.
It exists to ensure correct loading, execution, and resumption.

---

## 1. PURPOSE OF THIS REPOSITORY
This campaign is defined as a **formal game engine specification**, not a story.

All mechanics, procedures, and state are explicitly defined so that:
- No assumptions are required
- No improvisation is allowed
- No memory outside state is used

If something is not written in the Campaign Bible or an active Appendix,
it does not exist.

---

## 2. FILE AUTHORITY ORDER
Files must be loaded in this order:

1. `/system/ai_system_prompt.md`  
   → Defines execution authority and behavior constraints

2. `/campaign/campaign_bible.md`  
   → Defines all core rules and priorities

3. `/campaign/campaign_state_schema_v1.2.json`  
   → Defines the mandatory GAME_STATE structure

4. `/campaign/procedures.md`  
   → Defines all execution loops

5. `/campaign/appendix_control.md`  
   → Defines appendix activation and locking

6. `/campaign/master_rule_index.json`  
   → Defines rule lookup and source authority

7. `/appendices/*`  
   → Optional systems, only if activated

If a conflict exists, higher files override lower ones.

---

## 3. STARTING A CAMPAIGN
To start a new campaign:

1. Load the AI System Prompt
2. Initialize GAME_STATE using the schema
3. Execute the Campaign Start Procedure
4. Record appendix activation choices
5. Save GAME_STATE

Appendix activation is permanent unless a versioned reconfiguration exists.

---

## 4. RESUMING A CAMPAIGN
To resume after a break:

1. Load the latest saved GAME_STATE
2. Load all files listed in Section 2
3. Do NOT reinterpret prior events
4. Resume at the last active procedure or prompt

The AI must rely exclusively on GAME_STATE.

---

## 5. WHAT THIS SYSTEM DOES NOT DO
This system does NOT:
- Contain plot or story canon
- Contain NPC dialogue
- Contain scene narration
- Contain implied rules
- Allow improvisational mechanics

Narrative content is generated only during execution,
within the constraints of procedures and rules.

---

## 6. USING PUBLISHED ADVENTURES
Published adventures may be referenced ONLY for:
- Encounter structures
- Dungeon layouts
- Environmental mechanics
- Failure consequence models
- Table design patterns

They must NOT be used for:
- Plot
- Named NPCs
- Locations
- Canon events
- Assumed timelines

All narrative content must be original.

---

## 7. GLOSSARY NOTICE (FUTURE-PROOFING)
Campaign terminology is defined in a separate Glossary file.

Rules:
- Glossary changes do NOT alter mechanics
- Mechanics are defined only in rules and appendices
- Undefined terms have no mechanical meaning

---

## 8. VERSIONING RULE
Any change to:
- Rules
- Procedures
- State schema
- Appendices

Requires:
- Version increment
- Explicit change log
- Compatibility note

Execution AIs must not mix versions.

---

## 9. ERROR HANDLING
If an execution AI encounters:
- Missing files
- Missing state fields
- Undefined terms
- Conflicting rules

Execution must halt and report the error.
No fallback behavior is permitted.

---

## 10. FINAL NOTE
This repository defines a **closed system**.

Execution is deterministic.
Authority is explicit.
Canon is locked.

Follow the files.

---

**End of File**
