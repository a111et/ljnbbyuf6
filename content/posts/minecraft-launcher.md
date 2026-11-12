---
title: "🐍 Лаунчер для Minecraft"
date: 2026-11-12T14:00:00+02:00
author: "a111et"
description: "Гайд по установке Java и лаунчеров для Minecraft — Prism Launcher, Cracked и Freesm."
pinned: true
tags: ["minecraft", "гайд", "java"]
---

## Для Майнкрафт нужна Java — качаем

[Скачать Java 8, 11, 17, 21 (Adoptium)](https://adoptium.net/temurin/releases/?os=windows&arch=x64&package=jdk)

Или можно воспользоваться командой в PowerShell, которая установит сама нужные версии Java:

```powershell
winget install -e --id EclipseAdoptium.Temurin.8.JDK
winget install -e --id EclipseAdoptium.Temurin.11.JDK
winget install -e --id EclipseAdoptium.Temurin.17.JRE
winget install -e --id EclipseAdoptium.Temurin.21.JDK
```

### :link: Ссылки на лаунчеры

> :warning: **Примечание:** сборки MinGW менее протестированы, чем сборки MSVC и могут содержать ошибки и баги.
> Как указано на сайте PrismLauncher.

### :ice_cube: Prism Launcher

:large_blue_diamond: **[Скачать Prism Launcher](https://prismlauncher.ru/download)**

***Включаем в Prism Launcher автономную учётную запись:***

1. Закрой лаунчер
2. Нажми Win + R
3. В открывшееся окно напиши `cmd` и нажми Enter на клавиатуре
4. В командную строку вставь код ниже:

```cmd
echo {"accounts": [{"entitlement": {"canPlayMinecraft": true,"ownsMinecraft": true},"type": "Offline"}],"formatVersion": 3} > %appdata%/PrismLauncher/accounts.json
```

5. Нажми Enter
6. Запусти Prism Launcher и добавь автономную учётную запись

[Больше информации по поводу этого](https://github.com/antunnitraj/Prism-Launcher-PolyMC-Offline-Bypass)

### :key: Prism Launcher Cracked

*Включены автономные учётные записи из коробки с помощью команды выше*

:large_blue_diamond: **[Скачать Prism Launcher Cracked](https://github.com/Diegiwg/PrismLauncher-Cracked/releases)**

### :game_die: Freesm Launcher — форк Prism Launcher

*Форк Prism Launcher — автономные учётные записи включены, и есть дополнительные функции. На странице GitHub можно больше ознакомиться с тем, что добавлено.*

:large_blue_diamond: **[Скачать Freesm Launcher](https://github.com/FreesmTeam/FreesmLauncher/releases)**
