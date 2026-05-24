# 🐧 DistroDeck

**Автоматическое развертывание Arch Linux внутри Steam Deck (SteamOS)**

DistroDeck — это удобный скрипт, который создаёт полноценную **Arch Linux** среду внутри SteamOS с помощью **Distrobox + Podman**.  
Теперь вы можете устанавливать любые пакеты из Pacman и AUR, запускать Linux-приложения и при этом они отлично интегрируются в интерфейс SteamOS (включая Gaming Mode).

---

## ✨ Возможности

- Полноценная Arch Linux в изолированном контейнере
- Установка пакетов через `pacman` и **yay** (AUR)
- Автоматическая интеграция приложений в меню SteamOS
- Сохранение данных при переустановке/обновлении SteamOS
- Установка графических библиотек и инструментов "из коробки"
- Простая установка **одной командой**

---

## 🚀 Быстрая установка

Выполните одну команду в терминале Steam Deck (в Desktop Mode):

```bash
curl -L -o ~/Downloads/distrodeck.sh https://github.com/rosakodu/distrodeck/releases/download/v0.1.0/distrodeck.sh && chmod +x ~/Downloads/distrodeck.sh && ~/Downloads/distrodeck.sh
```

## ✨ Как использовать:

  1. Открыть терминал Arch Linux:
     distrobox enter arch

  2. Установить программу с автоматическим экспортом ярлыка:
     distrobox-install firefox

  3. Экспортировать все уже установленные ярлыки:
     distrobox-export-all

  4. Вручную экспортировать конкретное приложение:
     distrobox enter arch -- distrobox-export --app имя_приложения

  5. Экспортировать бинарник в ~/.local/bin:
     distrobox enter arch -- distrobox-export --bin /usr/bin/программа --export-path ~/.local/bin

  6. Установить пакет из AUR:
     distrobox enter arch -- yay -S пакет

