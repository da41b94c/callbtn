# CallBtn

Лёгкая CSS-кнопка звонка для мобильных лендингов и сайтов услуг. Работает без JavaScript и сборщика.

[Демонстрация](https://developer.donnoval.ru/callbtn/)

## Возможности

- фиксированная или встроенная в контент кнопка;
- пульсация и мягкая анимация телефонной трубки;
- настройка размера, цвета, положения и `z-index` через CSS-переменные;
- видимый `focus` для клавиатурной навигации;
- поддержка `prefers-reduced-motion`;
- учёт safe area на устройствах с вырезами;
- без внешних изображений, шрифтов и JavaScript.

## Подключение

Подключите файл стилей:

```html
<link rel="stylesheet" href="css/core.css">
```

Добавьте кнопку и замените номер телефона:

```html
<a class="callBtn" href="tel:+70000000000" aria-label="Позвонить по телефону">
	<span class="callBtnLabel">Позвонить</span>
</a>
```

`aria-label` и текст внутри `.callBtnLabel` должны описывать действие. Это важно для скринридеров.

## Настройка

Переопределите CSS-переменные на самой кнопке или в своём файле стилей:

```css
.callBtn {
	--callBtnSize: 4.5rem;
	--callBtnColor: #2563eb;
	--callBtnColorHover: #1d4ed8;
	--callBtnPulseColor: rgb(37 99 235 / 35%);
	--callBtnOffsetInline: 1.5rem;
	--callBtnOffsetBlock: 1.5rem;
	--callBtnZIndex: 1000;
}
```

### Кнопка внутри контента

Добавьте модификатор `.callBtn--static`:

```html
<a class="callBtn callBtn--static" href="tel:+70000000000" aria-label="Позвонить по телефону">
	<span class="callBtnLabel">Позвонить</span>
</a>
```

## Доступность

Компонент использует обычную ссылку `tel:`, остаётся доступным с клавиатуры и показывает фокус. При включённой в системе настройке уменьшения движения пульсация и вибрация отключаются автоматически.

## Структура

```text
.
├── css/
│   ├── core.css    # компонент
│   └── demo.css    # оформление демонстрационной страницы
├── index.html      # демонстрация
└── README.md
```

## Лицензия

MIT. См. [LICENSE](LICENSE).
