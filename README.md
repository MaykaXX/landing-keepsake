# Keepsake — Landing Page

Адаптивний лендінг для дизайн-агенції Keepsake, виконаний суто за допомогою чистого HTML5 та CSS3 без використання JavaScript або CSS-фреймворків.

## Посилання
- **Demo**: [https://<username>.github.io/landing-keepsake/](https://<username>.github.io/landing-keepsake/)
- **Репозиторій**: `landing-keepsake`

## Технології та рішення
- **Семантичний HTML5**: `header`, `nav`, `main`, `section`, `article`, `footer`, `form`. Ієрархія `h1`–`h3` без порушень.
- **Mobile First**: базові стилі для 375px, медіа-запити на `@media (min-width: 768px)` та `@media (min-width: 1280px)`.
- **CSS-only мобільне меню**: нативний Popover API (`popover`, `popovertarget`, `popovertargetaction="hide"`) із перетворенням бургера на хрестик через `:has(.menu:popover-open)`.
- **Фільтрація робіт**: через приховані радіокнопки `[type="radio"]` та селектор `~`.
- **Стани форми підписки**: валідація поля email через `:user-invalid` та екран успіху без перезавантаження через `:target`.
- **Продуктивність**: оптимізовані WebP-зображення з атрибутами `width`, `height` та `loading="lazy"`. Інлайн-SVG спрайт для піктограм.