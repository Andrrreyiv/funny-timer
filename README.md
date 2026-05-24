# 🐷 Funny Timer — Таймер 5 секунд

Простой одностраничный веб-таймер с обратным отсчётом и смешным звуком.

🔗 **Живая страница:** [andrrreyiv.github.io/funny-timer](https://andrrreyiv.github.io/funny-timer/)

## Функционал

- Логотип игры (заглушка — легко заменить на свой)
- Большая красная кнопка «НАЖМИ МЕНЯ»
- Обратный отсчёт: 5 → 4 → 3 → 2 → 1
- Смешной звук (поросячий визг) по окончании
- Автоматический сброс — цикл повторяется при следующем нажатии
- Анимированный фон с частицами
- Адаптивный дизайн (смартфон / планшет / ПК)

## Технологии

- Чистый HTML / CSS / JS — без зависимостей
- Google Fonts (Nunito, Rubik Mono One)
- Звук генерируется через Web Audio API — не нужны внешние файлы
- GitHub Pages — автоматический деплой при каждом изменении

## Структура файлов

```
index.html   — главная страница (разметка)
style.css    — все стили и анимации
script.js    — логика таймера, звук, частицы
README.md    — этот файл
```

## Как редактировать с любого устройства

### Вариант 1: Прямо на GitHub (самый простой)

1. Откройте нужный файл в репозитории: [github.com/Andrrreyiv/funny-timer](https://github.com/Andrrreyiv/funny-timer)
2. Нажмите иконку карандаша ✏️ (Edit this file)
3. Внесите изменения
4. Нажмите **Commit changes**
5. Через 1–2 минуты изменения появятся на сайте

Это работает с **любого устройства** — телефон, планшет, ноутбук. Нужен только браузер.

### Вариант 2: GitHub Mobile (приложение)

1. Скачайте [GitHub Mobile](https://github.com/mobile) (iOS / Android)
2. Войдите в аккаунт
3. Откройте репозиторий `Andrrreyiv/funny-timer`
4. Редактируйте файлы прямо в приложении

### Вариант 3: На компьютере (для разработчиков)

```bash
git clone https://github.com/Andrrreyiv/funny-timer.git
cd funny-timer
# Редактируйте файлы в любом редакторе
# Откройте index.html в браузере для локального просмотра
git add .
git commit -m "описание изменений"
git push
```

## Как заменить логотип

В `index.html` найдите:
```html
<div class="logo-placeholder">
    <span class="logo-icon">🎮</span>
    <span class="logo-text">ЛОГОТИП ИГРЫ</span>
</div>
```

Замените на:
```html
<img src="logo.png" alt="Логотип" style="max-width: 280px; height: auto;">
```

Загрузите файл `logo.png` в репозиторий (через GitHub: **Add file → Upload files**).

## Как заменить звук

Если нужен другой звук вместо поросячьего визга:

1. Загрузите аудиофайл (например `sound.mp3`) в репозиторий
2. В `index.html` перед `</body>` добавьте:
   ```html
   <audio id="finishSound" src="sound.mp3" preload="auto"></audio>
   ```
3. В `script.js` замените строку:
   ```js
   var soundDuration = createPigSqueal();
   ```
   на:
   ```js
   document.getElementById("finishSound").play();
   var soundDuration = 1.5;
   ```

## Автодеплой

Сайт размещён на **GitHub Pages**. Любое изменение в ветке `main` автоматически обновляет живую страницу по адресу:

👉 **https://andrrreyiv.github.io/funny-timer/**

Обычно обновление занимает 1–2 минуты после коммита.
