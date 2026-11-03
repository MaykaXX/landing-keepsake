# Keepsake — landing page

Адаптивний односторінковий лендінг дизайн-агенції Keepsake за макетом у Figma (Desktop 1280 / Tablet 768 / Mobile 375).

**Демо:** https://<your-username>.github.io/landing-keepsake/

## Технології та рішення

- **HTML5 + CSS3**, без фреймворків і UI-бібліотек, без JavaScript.
- **Семантика:** `header`, `nav`, `main`, `section`, `article`, `figure`, `footer`, `form`; один `h1`, коректна ієрархія `h2` → `h3`.
- **Mobile first:** базові стилі для 375, далі `@media (min-width: 768px)` та `(min-width: 1280px)`. Сторінка коректна від 320 до 1920 px, контейнер на великих екранах — max 1100 px.
- **CSS-змінні** в `:root`: кольори, шрифти, відступи, розміри типографіки, які змінюються по брейкпоінтах.
- **Flexbox** для розкладки (шапка, послуги, статистика, клієнти, журнал, футер); **CSS Grid** лише для сітки робіт (3 / 2 / 1 колонка).
- **Ілюстрації карточок** намальовано на CSS на «полотні» 357×282 і масштабовано через container query units (`cqw`), тож пропорції збігаються з макетом на будь-якій ширині.
- **Мобільне меню без JS:** `popover` + `popovertarget` (Popover API), бургер перетворюється на хрестик через `:has(.menu:popover-open)`.
- **Фільтр портфоліо без JS:** radio-кнопки + селектор `:checked ~` за атрибутом `data-category`.
- **Ховер карточки** (оверлей, «+», назва, категорія) працює також із клавіатури через `:focus-within`.
- **Форма підписки:** HTML-валідація (`type="email"`, `required`), стан помилки через `:user-invalid`, стан success через `:target`, помилка пов'язана з полем через `aria-describedby`.
- **Fixed header:** на ≥768 стискається при скролі (`animation-timeline: scroll()`, прогресивне покращення для Chromium); кнопка «вгору» завжди на екрані.
- **Доступність:** видимий `:focus-visible`, `aria-label` на іконкових кнопках, skip-link, `prefers-reduced-motion`.
- **Шрифти:** Oswald, Open Sans, Dancing Script, Lora (Google Fonts, `display=swap`).
- **Іконки:** інлайн-SVG (sprite + `<use>`).

## Структура

```
landing-keepsake/
├── index.html
├── css/
│   ├── reset.css
│   └── style.css
├── images/
└── fonts/
```
