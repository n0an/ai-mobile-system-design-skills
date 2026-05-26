# Mobile System Design — AI Skill for Claude Code

AI-скилл для Claude Code, синтезированный из четырёх книг по мобильной инженерии. Покрывает системный дизайн, декомпозицию задач, оценку, масштабирование, карьерный рост и подготовку к интервью.

---

## Быстрый старт

```bash
/mobile-design как спроектировать Instagram-ленту?
/mobile-design оцени задачу: экран истории транзакций с пагинацией и офлайном
/mobile-design как перейти с Senior на Staff Engineer?
```

---

## Источники знаний

Скилл синтезирован из четырёх книг. Каждая даёт отдельный слой экспертизы.

---

### 1. Mobile System Design: Resourceful Engineering

| Атрибут | Значение |
|---|---|
| Автор | Tjeerd in 't Veen |
| Должность | iOS Tech Lead в ING, Staff Engineer в Twitter/X |
| Издание | Early Release Edition |
| Фокус | Timeless principles, mental models, holistic-driven development |

**Структура книги (16 глав):**

| Глава | Тема |
|---|---|
| 1 | About this book — System Design vs Architecture |
| 2 | Turning a briefing into a strong plan (Landscape-подход) |
| 3 | Holistic-Driven Development — turning a plan into code |
| 4 | System-wide testing |
| 5 | Cross-domain testing |
| 6 | Dependency Injection foundations |
| 7 | Sane DI without fancy frameworks |
| 8 | DI at a larger scale |
| 9 | UI frameworks, architectures, and supporting multiple products |
| 10 | Delivering reusable UI views — art of decomposing a design |
| 11 | Reasoning about Views, Components, Screens, and Bindings |
| 12 | Pragmatically implementing UI |
| 13 | Delivering self-sufficient features, part I — staying nimble |
| 14 | Delivering self-sufficient features, part II — self-loading features |
| 15 | Delivering self-sufficient features, part III — making features portable |
| 16 | Reusing views across flows |

**Ключевые концепции из книги:**

- **Landscape approach** — перед кодом рисуешь граф сущностей (nodes = domain objects, edges = relationships). Никакого UI, никакого кода — только структура данных.
- **Holistic-Driven Development (HDD)** — начинаешь от domain-моделей, движешься наружу к UI. Stub-значения разблокируют UI-команду, не дожидаясь реального API.
- **12 UI Principles** — от "defer implementing the UI" до "feature views aren't always full-screen". Принцип №3: представь фичу как CLI-инструмент — если бизнес-логика не работает без UI, архитектура неправильная.
- **Self-sufficient features** — фича сама загружает данные, сама обрабатывает ошибки, переносима между экранами.
- **DI без фреймворков** — ABC problem, composition root, lazy dependencies через фабрики.

---

### 2. Building Mobile Apps at Scale: 39 Engineering Challenges

| Атрибут | Значение |
|---|---|
| Автор | Gergely Orosz |
| Должность | Principal iOS @ Skyscanner → Senior Android + EM @ Uber |
| ISBN | 978-1-63795-844-5 (ebook) |
| Издание | First Edition, v1.02 |
| Контрибьюторы | 30+ инженеров из Uber, Twitter, Amazon, Flipkart, Square, Capital One |
| Сайт | www.MobileAtScale.com |

**Структура (39 вызовов в 5 частях):**

```
PART 1: Challenges Due to the Nature of Mobile Applications
├── 1.  State Management
├── 2.  Mistakes Are Hard to Revert
├── 3.  The Long Tail of Old App Versions
├── 4.  Deeplinks
├── 5.  Push and Background Notifications
├── 6.  App Crashes
├── 7.  Offline Support
├── 8.  Accessibility
├── 9.  CI/CD & The Build Train
├── 10. Third-Party Libraries and SDKs
├── 11. Device and OS Fragmentation
└── 12. In-App Purchases

PART 2: Challenges Due to App Complexity
├── 13. Navigation Architecture Within Large Apps
├── 14. Application State & Event-Driven Changes
├── 15. Localization
├── 16. Modular Architecture & Dependency Injection
├── 17. Automated Testing
└── 18. Manual Testing

PART 3: Challenges Due to Large Engineering Teams
├── 19. Planning and Decision Making
├── 20. Architecting Ways to Avoid Stepping on Each Other's Toes
├── 21. Shared Architecture Across Several Apps
├── 22. Tooling Maturity for Large Engineering Teams
├── 23. Scaling Build & Merge Times
└── 24. Mobile Platform Libraries and Teams

PART 4: Languages and Cross-Platform Approaches
├── 25. Adopting New Languages and Frameworks
├── 26. Kotlin Multiplatform and KMM
├── 27. Cross-Platform Feature Development
├── 28. Cross-Platform App Development versus Native
└── 29. Web, PWA & Backend-Driven Mobile Apps

PART 5: Challenges Due to Stepping Up Your Game
├── 30. Experimentation (A/B Testing)
├── 31. Feature Flag Hell
├── 32. Performance
├── 33. Analytics, Monitoring and Alerting
├── 34. Mobile On-Call
├── 35. Advanced Code Quality Checks
├── 36. Compliance, Privacy and Security
├── 37. Client-Side Data Migrations
├── 38. Forced Upgrading
└── 39. App Size
```

**Почему эта книга ценна:** опыт Uber Rider и Driver apps (100M+ MAU, 60+ стран, 300+ native engineers). Не академические паттерны, а реальные решения реальных проблем на масштабе.

---

### 4. Mobile System Design Interview: An Insider's Guide

| Атрибут | Значение |
|---|---|
| Автор | Manuel Vicente |
| Опыт | Mobile engineer at Capital One, Google, YouTube |
| Фокус | Interview-specific methodology, 5-step MSD framework, worked case studies |

**Структура (10 глав + чит-лист):**

| Глава | Тема |
|---|---|
| 1–2 | Введение, методология и как работает MSD-интервью |
| 3 | Design a News Feed (Facebook-style) |
| 4 | Design a Map App (Google Maps-style) |
| 5 | Design a Design System (UI component library) |
| 6 | Design a Hotel Booking App |
| 7 | Design an App Like Google Drive (file sync) |
| 8 | Design Logging Blocks (analytics SDK) |
| 9 | Design an App Like YouTube (video streaming) |
| 10 | Design Building Blocks (cross-cutting patterns) |
| 11 | Comprehensive Cheat Sheet |

**Уникальный вклад книги:**

- **5-шаговый интервью-фреймворк** с тайм-аллокацией для 45-минутного интервью
- **Рубрика оценщика** по уровням: Entry / Mid / Senior / Staff+ — что смотрит интервьюер
- **8 проработанных кейсов** как симуляции интервью (не академические примеры)
- **Акцент на шаг API Design** — отдельный шаг, которого нет в других книгах
- **Чит-лист** по 4 доменам: Network, Data Management, Feature Development, Performance
- **Философия интервью**: стратегический выбор > попытка покрыть всё; Staff+ сигнал = демонстрация суждения о приоритетах

---

### 3. Growing as a Mobile Engineer

| Атрибут | Значение |
|---|---|
| Автор | Gergely Orosz |
| Подзаголовок | Getting to and Breaking the Mobile Engineering Glass Ceiling |
| ISBN | 978-1-63795-843-8 (ebook) |
| Издание | First Edition, v1.02 |
| Объём | 30 pieces of advice for mobile engineers and engineering managers |

**Структура (5 частей, 30 советов):**

```
PART 1: Growing as a Mobile Engineer (советы 1–6)
├── 1. Map Out Opportunities to Grow
├── 2. Typical Mobile Engineering Level Definitions
├── 3. Professional Growth Versus Promotions
├── 4. Mentoring
├── 5. Changing Jobs
└── 6. Down-Leveling When Changing Jobs

PART 2: Growing to Senior (советы 7–12)
├── 7.  Master Your Main Stack
├── 8.  Get Familiar With the Other Stack(s)
├── 9.  Become More Product-Minded
├── 10. Get More Feedback
├── 11. Lead a Full-Stack Project
└── 12. Ask For That Promotion

PART 3: Beyond Senior Levels (советы 13–21)
├── 13. The Challenge of Moving Beyond the Senior Level
├── 14. The "Glass Ceiling" for Mobile Engineers
├── 15. Go Broad or Go Deep
├── 16. Understand the Business and Get Involved
├── 17. Quantify Your Impact
├── 18. Connect with Industry Peers
├── 19. Public Writing and Speaking
├── 20. Leaving Mobile Engineering to Further Your Career
└── 21. It's Not Meant to Be Easy

PART 4: Mobile Engineering Management (советы 22–24)
├── 22. Mobile Platform Teams
├── 23. Mobile-Only Career Limitations for Managers
└── 24. Advocating for Senior+ Mobile Engineering Roles

PART 5: Mobile Learnings From My Time at Uber (советы 25–30)
├── 25. Platforms and Programs
├── 26. What Good Mobile Architecture Looks Like
├── 27. Hundreds of Mobile Engineers Working Together
├── 28. I'm Actually Not an Android / iOS Engineer
├── 29. Core and Optional Mobile Code & Modules
└── 30. Mobile Oncall
```

**Уровни (модель Uber):**

| Уровень | Роль | Что делает |
|---|---|---|
| L3 | Software Engineer | Guided work, established practices, learning |
| L4 | Software Engineer 2 | Independent in team, addresses tech debt, helps juniors |
| L5 | Senior Engineer | Spans multiple teams, plans impactful projects |
| L5B | Senior Engineer 2 | Long-term cross-team efforts, mentors |
| L6 | Staff Engineer | Company-level strategic problems, industry recognition |
| L7 | Senior Staff | Forecasts future, creates vision, industry-wide expert |

---

## Что умеет скилл

### Framework 1: Системный дизайн мобильных фич

Разбирает любую фичу по слоям, используя Landscape-подход:

```
Briefing → Landscape (entity graph) → Layers → API contracts → Trade-offs
```

**Пример запроса:**
```
/mobile-design спроектируй мессенджер с офлайн-поддержкой
```

**Что получишь:**
- Entity graph: `User ←→ Conversation ←→ Message ←→ Attachment`
- Слои: Domain → MessageRepository → NetworkLayer → StateManager → ChatUI
- Offline strategy: optimistic updates + conflict resolution (last-write-wins vs CRDT)
- Push: APNS/FCM token storage, silent push для синхронизации
- Secondary requirements: сортировка по timestamp, delivery receipts, typing indicators

---

### Framework 2: Декомпозиция задачи (Landscape Approach)

Пошаговый процесс от брифинга до плана работ:

**Шаг 1 — Граф сущностей (до кода)**
```
[User] ──has──> [Cart] ──contains──> [CartItem] ──references──> [Product]
                  │
                  └──> [Order] ──has──> [Payment]
```

**Шаг 2 — Слои**
```
Domain Models → Service/Repository → Networking → State → UI
```

**Шаг 3 — Work items (каждый ≤ 2 дня)**

| Категория | Пример |
|---|---|
| Domain models | Определить CartItem, Order, PaymentStatus |
| Networking | POST /orders, обработка ошибок платёжного шлюза |
| Repository | CartRepository: add/remove/clear, LocalCart (Core Data/Room) |
| State | CartViewModel, transitions: empty → loading → success → error |
| UI components | CartItemCell, TotalView, EmptyCartView |
| Feature UI | CartViewController, wire ViewModel |
| Testing | Unit-тесты CartRepository, snapshot CartItemCell |
| Secondary | Accessibility labels, аналитика add_to_cart, deep link /cart |
| Release | Feature flag, kill switch, analytics dashboard |

---

### Framework 3: Оценка с мобильными мультипликаторами

Базовая оценка × мультипликаторы = реальный range:

| Фактор | Мультипликатор | Когда применять |
|---|---|---|
| Unknown unknowns буфер | ×1.3–1.5 | Всегда |
| Вторичные требования не учтены | ×1.4–1.7 | Если error/empty/loading/offline/a11y не оценены |
| Незнакомая область / новый SDK | ×1.5–2.0 | Первый раз в модуле или новое API |
| API разрабатывается параллельно | ×1.3–1.4 | Риск изменения контракта |
| Бинарная дистрибуция | ×1.2 | Всегда (нет быстрого фикса без релиза) |
| Фрагментация устройств (Android) | ×1.2–1.3 | Custom UI, Camera/Media |
| App Store Review (дедлайн) | +2–7 дней | Любой хард-дедлайн |
| iOS + Android параллельно | ×1.0 per platform | Каждая платформа — отдельная оценка |

**Пример:**
```
/mobile-design оцени задачу: профиль пользователя с редактированием и аватаркой
```

Базовая оценка: 5 дней
- ×1.4 (вторичные требования: empty state, upload error, offline) = 7 дней
- ×1.3 (неизвестно поведение image picker на старых iOS) = ~9 дней
- +3 дня (App Store Review если хард-дедлайн)
- **Итог: "9–12 дней при условии финализации API-контракта на этой неделе"**

---

### Framework 4: 39 инженерных вызовов на масштабе

Готовые ответы на реальные вопросы. Примеры:

**State Management (Challenge #1)**
```
Events → State → UI
```
- Реактивное программирование: один источник истины, иммутабельные модели
- App lifecycle events (foreground/background/suspend) — first-class state transitions
- Использовано в Uber, Airbnb, N26

**Crash Handling (Challenge #6)**
- Инструменты: Bugsnag, Firebase Crashlytics
- Метрика: crash-free rate, не raw crash count
- OOM kills часто не считаются crashes — отслеживать отдельно
- Символикация обязательна для native crashes

**Performance (Challenge #32)**
- Cold launch < 2s — цель; измерять Time to Interactive (TTI)
- 60fps — Instruments/Android Profiler для поиска dropped frames
- Инструменты: Xcode Instruments, Android Profiler, perf.dev, Firebase Performance

**Feature Flag Hell (Challenge #31)**
- Слишком много флагов → комбинаторный взрыв состояний
- Флаги временные, не постоянные; устанавливать TTL
- Lifecycle: create → experiment → cleanup
- Dead flags — технический долг, автоматизировать cleanup

---

### Framework 5: Dependency Injection

Три уровня сложности из книги Tjeerd in 't Veen:

**Уровень 1 — Основы (гл. 6)**
- Зачем DI: testability, flexibility, modularity
- Проблема singletons: hinder modularization and testability
- Singleton допустим только для: shared, stateless, thread-safe (logger, analytics)

**Уровень 2 — Sane DI without frameworks (гл. 7)**
```swift
// ABC Problem: A зависит от B зависит от C
// Решение: Composition Root — создать все зависимости наверху

// Не так:
class FeatureA {
    let b = FeatureB()  // B создаёт C внутри себя — нет контроля
}

// Так:
let c = ServiceC()
let b = FeatureB(c: c)  // Composition Root
let a = FeatureA(b: b)
```

**Уровень 3 — DI at scale (гл. 8)**
- Каждый модуль экспонирует factory/component с явными зависимостями
- Reduce tight coupling на границах модулей через protocols/interfaces
- Lazy dependencies через фабрики для условных флоу (например, payment)

---

### Framework 6: 12 UI Принципов

Из книги Tjeerd in 't Veen (гл. 9–12):

| # | Принцип | Что означает |
|---|---|---|
| 1 | Defer implementing the UI | Сначала домен, потом UI |
| 2 | UI architectures come and go | Нет идеальной (MVC, MVVM, MVI, VIPER, TCA — у всех trade-offs) |
| 3 | Feature = Command Line Tool | Бизнес-логика не знает об UI |
| 4 | UI не диктует архитектуру | Fat business domain, lean UI domain |
| 5 | Name after what it IS | `UserAvatarView`, не `HeaderProfileImage` |
| 6 | Don't name after styling | `PrimaryButton`, не `BlueRoundedButton` |
| 7 | Composition over smart views | Маленькие, single-responsibility компоненты |
| 8 | View components contain logic/bindings | View primitives (dumb) vs components (smart) |
| 9 | Features can have local components | Не всё должно быть в shared library |
| 10 | Feature views connected via bindings | ViewModel, Combine, RxSwift |
| 11 | Feature views aren't always full-screen | Фича = widget, section, card |
| 12 | View components unaware of business logic | Данные входят, события выходят |

---

### Framework 7: Карьера и интервью (из Growing as a Mobile Engineer)

**Что оценивают на Mobile System Design (не как backend SD):**
- Mobile-specific constraints: lifecycle, offline, binary distribution, device fragmentation
- API contract с backend: версионирование, error codes, pagination
- State management: реактивный vs императивный, single source of truth
- Testing strategy: что на каком уровне

---

### Framework 9: 5-шаговый MSD-интервью фреймворк (из Manuel Vicente)

Конкретная методология для 45-минутного интервью:

| Шаг | Время | Суть |
|---|---|---|
| 1. Понять задачу | 5–10 мин | Уточнить what/who/for whom, scale, platform |
| 2. API Design | 5–10 мин | Протокол, data models, пагинация, real-time |
| 3. High-Level Architecture | 10–15 мин | Диаграмма компонентов, data flows |
| 4. Design Deep Dive | 15–20 мин | 2–3 темы вглубь, по реакции интервьюера |
| 5. Wrap-Up | 0–5 мин | Summary, edge cases, future scale |

**Рубрика оценщика по уровням:**

| Уровень | Что ожидают |
|---|---|
| Entry | Базовые паттерны, инициатива, state management awareness |
| Mid | Связный high-level design, альтернативные решения |
| Senior | End-to-end ownership, проактивная идентификация проблем, обоснованные trade-offs |
| Staff+ | Стратегическое мышление, business impact, failure recovery, минимум промптинга |

**Ключевой принцип:** стратегический выбор тем > попытка покрыть всё. Объяснение ПОЧЕМУ ты фокусируешься на этих темах — Staff+ сигнал.

---

## Примеры использования

### Пример 1: Новая фича

**Запрос:**
```
/mobile-design помоги спроектировать экран корзины покупок
с офлайн-поддержкой и синхронизацией при восстановлении сети
```

**Скилл покроет:**
- Entity graph: Cart → CartItem → Product, LocalCartStorage
- Offline strategy: Local DB (Room/Core Data) как источник истины, sync queue
- Conflict resolution: server-authoritative (корзина с сервера побеждает)
- Secondary requirements: empty state ("Корзина пуста"), loading skeleton, error banner
- Questions for backend: PUT /cart vs PATCH /cart/items, idempotency, version field?
- Оценка: 8–12 дней с мобильными мультипликаторами

---

### Пример 2: Оценка для спринта

**Запрос:**
```
/mobile-design оцени задачу: push-уведомления для order status updates.
Бэкенд уже готов, нужно только клиентская часть. iOS.
```

**Скилл покроет:**
- Декомпозиция: APNS registration → token storage → notification handling → deep link routing → UI update
- Known unknowns: поведение при foreground/background/terminated, payload структура, silent vs visible
- Вторичные: opt-out flow, disabled notifications graceful degradation, notification settings screen
- Мультипликаторы: ×1.2 (binary distribution risk), +2–7 дней (App Store)
- Оценка: "3–5 дней core, +2 дня secondary, +3 дня App Store buffer"

---

### Пример 3: Подготовка к интервью

**Запрос:**
```
/mobile-design помоги подготовиться к mobile system design интервью.
Задача: спроектировать Uber-like ride tracking с real-time location updates
```

**Скилл покроет:**
- Requirements clarification script: что спрашивать у интервьюера (offline? precision? battery constraints?)
- Entity graph: Ride → Driver → Location → Route
- Location updates: WebSocket vs long polling vs MQTT; trade-offs battery vs latency
- State machine: `idle → searching → matched → in_progress → completed`
- Mobile constraints: background location permissions, battery optimization (significant location change API)
- Trade-off: нативный vs cross-platform, почему важно для Uber

---

### Пример 4: Архитектурный вопрос

**Запрос:**
```
/mobile-design в чём реальная разница между MVVM и MVI для iOS?
Когда что выбирать?
```

**Скилл покроет:**
- Принцип #2: "UI architectures come and go — treat them as alignment tools"
- MVVM: state как набор свойств, mutations explicit/implicit — работает для linear flows
- MVI: state как immutable snapshot + Intent + Reducer — работает для complex state machines
- Реальный trade-off: MVI сложнее onboard, но предсказуемее для отладки
- Когда MVVM: простые CRUD-экраны, небольшая команда
- Когда MVI: сложные state machines, большая команда, много concurrent mutations

---

### Пример 5: Симуляция интервью по 5-шаговому фреймворку

**Запрос:**
```
/mobile-design проведи со мной MSD-интервью на уровень Senior.
Задача: спроектировать приложение для синхронизации файлов типа Google Drive
```

**Скилл покроет:**
- Шаг 1 (scope): что конкретно строим? Offline? Conflict resolution? Платформа?
- Шаг 2 (API design): REST vs gRPC для upload/download, delta sync protocol, chunked upload
- Шаг 3 (архитектура): File → Chunk → SyncQueue → LocalDB → NetworkLayer → ConflictResolver
- Шаг 4 (deep dive): выбор между 2–3 темами — конфликт-резолюшн, background sync, или security
- Шаг 5 (wrap-up): edge cases (file deleted on both sides), future scale (100× файлов)
- Обратная связь по рубрике Senior: что показано хорошо, что не хватает до Staff+

---

### Пример 6: Карьерный вопрос

**Запрос:**
```
/mobile-design как мобильному инженеру пробить "стеклянный потолок" и выйти на Staff?
```

**Скилл покроет:**
- "Glass ceiling" для mobile (гл. 14 из Growing as a Mobile Engineer): mobile-only работа редко видна на уровне L6+
- Go Broad vs Go Deep: staff engineer чаще идут broad (backend/infra awareness) чем deep (platform expert)
- Конкретные шаги: lead full-stack project, quantify impact, public speaking, RFC authorship
- Mobile Platform Teams: путь через платформенную команду как наиболее быстрый к Staff в мобайл-first компаниях

---

## Установка

Установить скилл одной командой:

```bash
npx skills add levabond/ai-mobile-system-design-skills --all
```

CLI спросит, в каких агентов (Claude Code, Codex, Cursor, Gemini, ...) добавить скилл и куда установить — в текущий проект или глобально.

Если нет `npx`, поставьте Node (`brew install node`); если нет `brew`, сначала [поставьте Homebrew](https://brew.sh).

### Альтернатива

**Claude Code** (ставит как plugin):

```bash
/plugin install levabond/ai-mobile-system-design-skills
```

После установки можно вызывать скилл естественным языком, например:

```
Используй mobile-design чтобы спроектировать ленту Instagram.
```

Или через слеш-команду (если репозиторий склонирован в проект — тогда `/mobile-design` подхватится из `.claude/commands/mobile-design.md`):

```bash
/mobile-design как спроектировать Instagram-ленту?
```

---

## Структура репозитория

```
ai-mobile-system-design-skills/
├── README.md                          # Этот файл
├── mobile-design/
│   ├── SKILL.md                       # Определение скилла (Agent Skills format)
│   └── agents/openai.yaml             # Метаданные для Codex и др.
├── .claude-plugin/plugin.json         # Claude Code plugin manifest
├── gemini-extension.json              # Gemini extension manifest
└── .claude/
    └── commands/
        └── mobile-design.md           # Слеш-команда (для обратной совместимости)
```

---

## Источники и авторы

| Книга | Автор | Издатель | Год |
|---|---|---|---|
| *Mobile System Design: Resourceful Engineering* | Tjeerd in 't Veen | Self-published | 2023 (Early Release) |
| *Building Mobile Apps at Scale: 39 Engineering Challenges* | Gergely Orosz | pragmaticengineer.com | 2021 |
| *Growing as a Mobile Engineer* | Gergely Orosz | pragmaticengineer.com | 2021 |
| *Mobile System Design Interview: An Insider's Guide* | Manuel Vicente | Self-published | 2024 |

**Gergely Orosz** — автор The Pragmatic Engineer Newsletter (крупнейший tech-newsletter на Substack), бывший Principal iOS @ Skyscanner, Senior Android EM @ Uber. Его книги основаны на опыте Uber Rider и Driver apps с 100M+ MAU.

**Tjeerd in 't Veen** — iOS Tech Lead в ING Bank, Staff Engineer в Twitter/X. Специализируется на timeless engineering principles в отличие от trend-driven подходов.

**Manuel Vicente** — mobile engineer с опытом в Capital One и Google/YouTube. Его книга — единственный источник в коллекции, написанный специально под формат интервью, с рубрикой оценщика и проработанными кейсами как симуляциями.
