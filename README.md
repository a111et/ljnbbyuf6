# Минималистичный блог на Hugo

Блог в стиле [telegra.ph](https://telegra.ph) — чистая типографика, узкая колонка чтения, ничего лишнего. Автоматический деплой на GitHub Pages.

## 🚀 Быстрый старт

### Локальный запуск

1. [Установите Hugo](https://gohugo.io/installation/) (extended-версия).
2. Склонируйте репозиторий и запустите сервер:

```bash
git clone https://github.com/username/hugo-blog.git
cd hugo-blog
hugo server -D
```

3. Откройте [http://localhost:1313](http://localhost:1313) в браузере.

### Деплой на GitHub Pages

1. Создайте новый репозиторий на GitHub и загрузите файлы:

```bash
cd hugo-blog
git init
git add .
git commit -m "init: Hugo blog"
git branch -M main
git remote add origin https://github.com/ВАШ-ЮЗЕРНЕЙМ/hugo-blog.git
git push -u origin main
```

2. В настройках репозитория: **Settings → Pages → Source** — выберите **GitHub Actions**.

Готово. При каждом пуше в `main` сайт автоматически пересобирается и деплоится.

> **Не забудьте** заменить `baseURL` в `hugo.toml` на адрес вашего сайта:
> `https://ВАШ-ЮЗЕРНЕЙМ.github.io/hugo-blog/`

## 📝 Как писать статьи

Создайте файл в папке `content/posts/`:

```bash
hugo new posts/my-article.md
```

Или просто создайте `.md`-файл вручную:

```markdown
---
title: "Заголовок статьи"
date: 2026-11-12
author: "Ваше имя"
description: "Краткое описание для соцсетей"
---

Текст статьи в формате Markdown.
```

### Изображения

Картинки кладите в `static/images/` и ссылайтесь на них в статьях:

```markdown
![Описание](/images/photo.jpg)
```

Для подписи используйте HTML-тег `<figure>`:

```markdown
{{</* figure src="/images/photo.jpg" caption="Подпись к фотографии" */>}}
```

## 🎨 Кастомизация

- **Название и описание блога** — `hugo.toml` → `title` и `params.description`
- **Стили** — `assets/css/style.css`
- **Шаблоны** — `layouts/`

Тёмная тема включается автоматически через `prefers-color-scheme`.

## 📂 Структура проекта

```
├── assets/css/style.css       # Стили
├── content/posts/             # Статьи в Markdown
├── layouts/
│   ├── _default/
│   │   ├── baseof.html        # Базовый шаблон с мета-тегами
│   │   ├── single.html        # Шаблон статьи
│   │   └── list.html          # Шаблон списка
│   └── index.html             # Главная страница
├── static/images/             # Картинки
├── .github/workflows/hugo.yml # CI/CD
└── hugo.toml                  # Конфигурация Hugo
```
