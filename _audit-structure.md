# Аудит структуры fedat-public-wiki

Дата: 2026-05-16  
Сайт: http://wiki.fedat.ru · локаль: `ru` · главная: `/ru/home`

---

## Фаза 1 — таблица миграции

| Файл | Статус | Новый путь | Старый URL | Новый URL |
|------|--------|------------|------------|-----------|
| `home.md` | **активно** (переписан) | `home.md` | `/ru/home` | `/ru/home` |
| `README.md` | **активно** (минимальный, `published: 0`) | `README.md` | `/ru/README` | `/ru/README` |
| `dlya-sportsmena/kak-sozdat-profil.md` | **активно** (новый) | `dlya-sportsmena/kak-sozdat-profil.md` | — | `/ru/dlya-sportsmena/kak-sozdat-profil` |
| `dlya-sportsmena/chto-takoe-ssylka.md` | **активно** (новый) | `dlya-sportsmena/chto-takoe-ssylka.md` | — | `/ru/dlya-sportsmena/chto-takoe-ssylka` |
| `dlya-sportsmena/scenarii.md` | **активно** (новый) | `dlya-sportsmena/scenarii.md` | — | `/ru/dlya-sportsmena/scenarii` |
| `dlya-sportsmena/faq.md` | **активно** (новый) | `dlya-sportsmena/faq.md` | — | `/ru/dlya-sportsmena/faq` |
| `o-proekte/o-proekte.md` | **активно** (новый) | `o-proekte/o-proekte.md` | — | `/ru/o-proekte/o-proekte` |
| `o-proekte/manifest.html` | **активно** | `o-proekte/manifest.html` | `/ru/manifest` | `/ru/o-proekte/manifest` |
| `whitepaper.md` | **архив** | `arhiv/whitepaper.md` | `/ru/whitepaper` | `/ru/arhiv/whitepaper` |
| `presale.md` | **архив** | `arhiv/presale.md` | `/ru/presale` | `/ru/arhiv/presale` |
| `frozen-economy.md` | **архив** | `arhiv/frozen-economy.md` | `/ru/frozen-economy` | `/ru/arhiv/frozen-economy` |
| `trader-package.md` | **архив** | `arhiv/trader-package.md` | `/ru/trader-package` | `/ru/arhiv/trader-package` |
| `user-package.html` | **архив** | `arhiv/user-package.html` | `/ru/user-package` | `/ru/arhiv/user-package` |
| `project-map.md` | **стратегия** | `strategiya/project-map.md` | `/ru/project-map` | `/ru/strategiya/project-map` |
| `стратегические-цели-2030.md` | **стратегия** | `strategiya/стратегические-цели-2030.md` | `/ru/стратегические-цели-2030` | `/ru/strategiya/стратегические-цели-2030` |
| `брикс.md` | **стратегия** | `strategiya/брикс.md` | `/ru/брикс` | `/ru/strategiya/брикс` |
| `наблюдатели.md` | **стратегия** | `strategiya/наблюдатели.md` | `/ru/наблюдатели` | `/ru/strategiya/наблюдатели` |
| `roadmap.html` | **стратегия** | `strategiya/roadmap.html` | `/ru/roadmap` | `/ru/strategiya/roadmap` |

**Объединить:** дубль `home` + `README` — снят: `README` служебный (`published: 0`), контент только в `home.md`. Два формата «пакет участника» (`trader-package.md` + `user-package.html`) — оба в `arhiv/`, не объединялись (разный редактор).

---

## Дерево навигации Wiki.js (предложение)

Топ-уровень (видимые в меню):

```
Для спортсмена/
├── Как создать профиль      → /ru/dlya-sportsmena/kak-sozdat-profil
├── Что такое ссылка         → /ru/dlya-sportsmena/chto-takoe-ssylka
├── Сценарии                 → /ru/dlya-sportsmena/scenarii
└── FAQ                      → /ru/dlya-sportsmena/faq

О проекте/
├── О проекте (кратко)       → /ru/o-proekte/o-proekte
└── Манифест                 → /ru/o-proekte/manifest
```

Главная сайта (вне дерева или первый пункт): **/ru/home**

**Не в топ-3** (скрыть в навигации или вложить глубже):

```
Стратегия/                    [published, низкий приоритет]
├── Проектная карта
├── Цели 2030
├── БРИКС
├── Совет наблюдателей
└── Дорожная карта

Архив/                       [можно скрыть целиком в Wiki.js]
├── Белая бумага
├── Пресейл
├── Frozen-экономика
├── Пакет участника (md)
└── Пакет пользователя (html)
```

---

## Редиректы (настроить вручную в Wiki.js)

| От (старый путь) | К (новый путь) |
|------------------|----------------|
| `/ru/whitepaper` | `/ru/arhiv/whitepaper` |
| `/ru/presale` | `/ru/arhiv/presale` |
| `/ru/frozen-economy` | `/ru/arhiv/frozen-economy` |
| `/ru/trader-package` | `/ru/arhiv/trader-package` |
| `/ru/user-package` | `/ru/arhiv/user-package` |
| `/ru/project-map` | `/ru/strategiya/project-map` |
| `/ru/стратегические-цели-2030` | `/ru/strategiya/стратегические-цели-2030` |
| `/ru/брикс` | `/ru/strategiya/брикс` |
| `/ru/наблюдатели` | `/ru/strategiya/наблюдатели` |
| `/ru/roadmap` | `/ru/strategiya/roadmap` |
| `/ru/manifest` | `/ru/o-proekte/manifest` |

Редирект **не нужен:** `/ru/home`, `/ru/README` (при желании README → `/ru/home`).

---

## Фаза 2 — выполнено

- [x] `home.md` — компас спортсмен/родитель, CTA fedat.ru, ссылки `dlya-sportsmena/*`
- [x] `README.md` — минимальный, `published: 0`
- [x] Раздел `dlya-sportsmena/` (4 страницы)
- [x] `arhiv/` — 5 файлов + единый дисклеймер
- [x] `strategiya/` — 5 файлов
- [x] `o-proekte/` — landing + `manifest.html`
- [x] YAML/HTML frontmatter сохранён

---

## После push в GitHub

1. Дождаться sync Wiki.js.  
2. В **Administration → Navigation** — дерево как выше; архив/стратегия — скрыть или свернуть.  
3. **Redirects** — таблица выше.  
4. Проверка: с `/ru/home` за 30 с понятно «иду на fedat.ru» и есть ссылка на инструкцию.
