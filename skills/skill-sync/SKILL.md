---
name: skill-sync
description: Обновить/распространить скилл одинаково во все места (репа-источник, Claude, Codex). Используй когда пользователь говорит «обнови этот скилл», «прокинь скилл везде».
---

# Sync скилла во все места

Скилл обязан быть БАЙТ-в-байт одинаков в трёх местах (Windows):

| Место | Путь к `SKILL.md` |
|---|---|
| Репа-источник (git) | `C:\Users\ikotlyarov\Documents\AI\skills\skills\<name>\SKILL.md` |
| Claude global | `C:\Users\ikotlyarov\.claude\skills\<name>\SKILL.md` |
| Codex global | `C:\Users\ikotlyarov\.codex\skills\<name>\SKILL.md` |

`<name>` — слаг скилла (имя папки). Источник правды — репа.

## Процедура
1. Записать **одинаковый** текст SKILL.md во все три пути (новый скилл — сперва создать папку `<name>/` в каждом).
2. Сверить: `diff` репа↔Claude и репа↔Codex — должны совпасть.
3. В репе `Documents\AI\skills` (ветка `main`, remote `origin` → github `Kromeshn/skills`) закоммитить по правилам [[git-commit]] (тип-префикс: `chore:` для правки, `feat:` для нового скилла) и запушить в `origin`.
