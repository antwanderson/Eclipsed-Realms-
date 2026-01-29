# Appendix Control & Activation System
Version: 1.2

Appendices are sealed rule modules.
Activation occurs **once at campaign start**.

---

## 1. APPENDIX REGISTRY

| Appendix ID | File | Purpose |
|-------------|------|--------|
| writs | appendix_writs_system.md | Effort & Writs |
| fray | appendix_fray_system.md | Combat Pressure |
| epic_levels | appendix_epic_archetypes.md | Epic progression |
| transformations | Grim Hollow | Corruption & Mutation |
| dominion | reserved | World alteration & governance |
| mythic_gme | mythic_gme_flow.md | Oracle & uncertainty |
| eidolon_framework | systems/eidolon_framework/* | Digimon-style companion |

---

## 2. ACTIVATION PROCEDURE

1. Present appendix list
2. Player enables/disables
3. Record in `GAME_STATE.appendices`
4. Lock selections permanently

---

## 3. ENFORCEMENT

- False → all related rules ignored
- True → rules active, procedures executable, fields mandatory
- Violation halts execution

---

## 4. GLOSSARY DECOUPLING

- Appendix rules may reference glossary
- Mechanical meaning comes only from rules
- Glossary may change independently

---

## 5. FUTURE APPENDICES

- Must declare required state fields
- Must declare procedures
- Must declare conflicts and glossary references
