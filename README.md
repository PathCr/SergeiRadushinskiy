<h1 align="center">Сергей Радушинский</h1>

<p align="center">
  <strong>PHP Backend-разработчик</strong> · Laravel · Yii2<br>
  <sub>22 года</sub>
</p>

<p align="center">
  <img alt="PHP" src="https://img.shields.io/badge/-PHP-777BB4?style=flat-square&logo=php&logoColor=white">
  <img alt="Laravel" src="https://img.shields.io/badge/-Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white">
  <img alt="Yii2" src="https://img.shields.io/badge/-Yii2-1F6FEB?style=flat-square">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white">
  <img alt="Redis" src="https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white">
  <img alt="Docker" src="https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img alt="Git" src="https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white">
  <img alt="Linux" src="https://img.shields.io/badge/-Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
</p>

<p align="center">
  <a href="https://t.me/Sergei_radushinskiy"><img alt="Telegram" src="https://img.shields.io/badge/Telegram-@Sergei_radushinskiy-26A5E4?style=flat-square&logo=telegram&logoColor=white"></a>
  <a href="https://github.com/PathCr"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-PathCr-181717?style=flat-square&logo=github&logoColor=white"></a>
  <a href="./resume/Sergey_Radushinsky_PHP_Backend.pdf"><img alt="Резюме PDF" src="https://img.shields.io/badge/%D0%A0%D0%B5%D0%B7%D1%8E%D0%BC%D0%B5-PDF-B30B00?style=flat-square&logo=adobeacrobatreader&logoColor=white"></a>
  <a href="./resume/Sergey_Radushinsky_PHP_Backend.docx"><img alt="Резюме DOCX" src="https://img.shields.io/badge/%D0%A0%D0%B5%D0%B7%D1%8E%D0%BC%D0%B5-DOCX-2B579A?style=flat-square&logo=microsoftword&logoColor=white"></a>
</p>

---

## О себе

PHP-разработчик с коммерческим опытом разработки и сопровождения веб-приложений на Yii2 и Laravel. Разрабатываю backend, REST API и интеграции с внешними сервисами, работаю с PostgreSQL и Redis, пишу feature-тесты и разворачиваю проекты в Docker.

Сейчас участвую в разработке ERP-системы для управления топливными картами: операции с картами, платежи и интеграция с внешним API E100.

**Открыт к предложениям** на позицию PHP/Laravel-разработчика.

## Опыт работы

### AliotFleet — PHP/Laravel-разработчик

<sub>Сентябрь 2026 — настоящее время</sub>

ERP-система для управления топливными картами автопарков. Laravel 13, PHP 8.3, PostgreSQL, Redis, Blade + Bootstrap 5, Docker.

- Разрабатывал backend-функциональность по задачам в отдельных Git-ветках: операции с топливными картами (привязка и отвязка к договору, перевод между клиентами, смена PIN, активация, блокировка), платежи и авансы, управление менеджерами и договорами, группировка карт в кабинете компании.
- Работал с внешним API E100 через сервисный слой (Endpoints/*Service): добавлял методы для карт, платежей, менеджеров и клиентов; использовал кэширование токенов в Redis, retry и обработку ошибок 401/403, логирование запросов.
- Реализовал REST API для внешних клиентов: вход по логину и паролю с выдачей application-токена (Redis, TTL), middleware-аутентификация, API Resources, эндпоинт с информацией о водителе и его картах.
- Реализовал учёт платежей и авансов: история платежей, запись изменений баланса в balance_history, изменение кредитного лимита и предоплаты договора, аудит действий администраторов.
- Покрыл ключевые сценарии feature-тестами (Pest/PHPUnit, моки внешнего API) — 8 тестовых наборов: карты, оплаты, авансы, блокировки клиентов, лимиты.
- Добавил Docker/Podman-окружение (Dockerfile, docker-compose, entrypoint); проходил CI-проверки: Laravel Pint, Larastan (PHPStan level 5), тесты на PostgreSQL.

### ООО «Лемборган Техно» — Разработчик ПО

<sub>Февраль 2025 — Июль 2025</sub>

Веб-приложения на Yii2.

- Разрабатывал новые страницы и функциональность на Yii2: вывод данных из БД через SQL-запросы, работа с MVC-архитектурой.
- Дорабатывал существующий функционал, анализировал причины ошибок и исправлял их.
- Работал с Git/GitHub (ветки, коммиты, push, merge), уточнял требования с руководителем, получал code review.

## Проекты

### Сервис отзывов для сайтов компаний

<sub>Pet-проект · Laravel 13 · PostgreSQL · Sanctum · Docker / Sail · PHPUnit · OpenAPI</sub>

[github.com/PathCr/Laravel13](https://github.com/PathCr/Laravel13)

- Спроектировал структуру БД (пользователи, сайты, отзывы) и REST API для управления сайтами и отзывами.
- Реализовал регистрацию и аутентификацию на Laravel Sanctum, разграничение доступа через Policies и валидацию через FormRequest.
- Добавил модерацию отзывов со статусами pending, approved и rejected, а также фильтрацию по статусу.
- Настроил события, Listener и очереди для уведомлений, OpenAPI-документацию (Scramble) и Docker-окружение; написал автоматические тесты.

### Uptime Monitor — сервис мониторинга сайтов

<sub>Pet-проект · Laravel 13 · Redis / Horizon · PostgreSQL · Vue 3 · Telegram Bot API · Pest · Docker Compose</sub>

- Реализовал проверку сайтов и API по расписанию на очередях: инциденты, защита от ложных срабатываний, дневная агрегация и uptime за 24 ч / 7 дн. / 30 дн.
- Сделал уведомления в Telegram и на email, дашборд на Vue 3 с графиками и публичные статус-страницы.

## Навыки

- **Backend:** PHP 8+, Laravel 13, Yii2, REST API, ООП, MVC, паттерн Action, Eloquent ORM, Laravel Sanctum, Policies, FormRequest, очереди, Redis, Pest / PHPUnit, Larastan (PHPStan), Laravel Pint
- **Базы данных:** PostgreSQL, MySQL, SQL, миграции, Eloquent
- **Инструменты:** Git / GitHub, Docker, Docker Compose, Podman, Laravel Sail, Linux (Ubuntu), OpenAPI / Scramble, Horizon, GitHub Actions
- **Frontend:** Blade, Bootstrap 5, HTML, CSS, JavaScript, Vue 3 (базовый уровень)

## Образование

**ИМСИТ, Краснодар**

- Среднее профессиональное — «Информационные системы и программирование», техникум окончен
- Высшее — «Прикладная информатика», 2026 — настоящее время

## Языки

- Русский — родной
- Английский — A2–B1 (читаю техническую документацию)

---

<p align="center"><sub>Резюме также доступно в <a href="./resume/Sergey_Radushinsky_PHP_Backend.pdf">PDF</a> и <a href="./resume/Sergey_Radushinsky_PHP_Backend.docx">DOCX</a></sub></p>
