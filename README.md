[README.md](https://github.com/user-attachments/files/30378984/README.md)
# СДЭЧ — Служба доставки экспресс-чар

Автономный статический лендинг. Разворачивается на любом статик-хостинге (GitHub Pages, Netlify, Vercel, Nginx, Apache).

## Структура

```
site/
├─ index.html         — страница
├─ css/styles.css     — шрифты (@font-face), keyframes, hover, медиа-запросы
├─ js/support.js      — рантайм рендеринга (локально)
├─ fonts/             — Anticva (заголовки), Iosevka regular/semibold (текст)
└─ images/            — сова, дракон, печати, бумажная текстура
```

## Запуск локально

Из-за относительных путей открывать через локальный сервер, а не `file://`:

```bash
cd site
python3 -m http.server 8000
# затем http://localhost:8000
```

## Деплой

Залить содержимое папки `site/` в корень хостинга — точка входа `index.html`.

## Зависимости

React и ReactDOM 18.3.1 подгружаются с публичного CDN unpkg (постоянные ссылки с SRI). Остальные ресурсы — локальные. Для работы полностью офлайн замените CDN-ссылки в `<head>` на локальные копии `react.production.min.js` / `react-dom.production.min.js` в `js/`.

## Шрифты

- **Anticva** — заголовки
- **Iosevka Extended** (regular / semibold) — наборный текст, метки, кнопки
  
