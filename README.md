# Blog-customizer

**Blog-customizer** — интерактивное React-приложение для кастомизации внешнего вида статьи блога в реальном времени. Пользователь может гибко настраивать параметры отображения статьи через удобную боковую панель.

---

## Основные возможности

- **Выбор шрифта**: поддержка нескольких семейств (Open Sans, Ubuntu, Cormorant Garamond, Days One, Merriweather).
- **Настройка размера шрифта**: выбор из предустановленных размеров.
- **Изменение цвета текста и фона**: палитра из нескольких цветов.
- **Регулировка ширины контента**: широкий и узкий режимы.
- **Применение и сброс настроек**: изменения применяются только после подтверждения, возможен сброс к дефолтным значениям.
- **Адаптивность**: интерфейс оптимизирован для разных размеров экрана.
- **Доступность**: управление возможно с клавиатуры, поддержка aria-атрибутов.

---

## Архитектура и структура

- Все бизнес-компоненты и UI-элементы находятся в папке [`src/components`](src/components/).
- Основная логика параметров и их типов вынесена в [`src/constants/articleProps.ts`](src/constants/articleProps.ts).
- Стилизация реализована через SCSS-модули с использованием CSS-переменных для динамики.
- Приложение построено на хуках React и TypeScript с сильной типизацией.
- Для управления состоянием кастомизации используется локальный state в [`App`](src/components/app/App.tsx).

---

## Ключевые компоненты

- [`App`](src/components/app/App.tsx): корневой компонент, объединяющий форму параметров и статью.
- [`ArticleParamsForm`](src/components/article-params-form/ArticleParamsForm.tsx): боковая панель с формой для настройки параметров.
- [`Article`](src/components/article/Article.tsx): компонент отображения статьи с применением кастомных стилей.
- [`Select`](src/components/select/Select.tsx), [`RadioGroup`](src/components/radio-group/RadioGroup.tsx), [`Button`](src/components/button/Button.tsx): переиспользуемые UI-компоненты.
- Кастомные хуки для UX: [`useClose`](src/components/hooks/useClose.ts), [`useOutsideClickClose`](src/components/select/hooks/useOutsideClickClose.ts), [`useEnterSubmit`](src/components/select/hooks/useEnterSubmit.ts).

---

## Технологии

- **React 18** + **TypeScript**
- **SCSS-модули** и CSS-переменные
- **Webpack** для сборки
- **Storybook** для разработки и тестирования компонентов
- **ESLint**, **Prettier**, **Stylelint** — поддержка качества кода

---

## Быстрый старт

1. Установите зависимости:
   ```
   npm install
   ```
2. Запустите dev-сервер:
   ```
   npm start
   ```
3. Откройте [http://localhost:8080](http://localhost:8080) в браузере.

---

## Скрипты

- `npm run build` — сборка production-версии
- `npm run stylelint` — проверка стилей
- `npm run lint` — линтинг TypeScript/JS
- `npm run format` — автоформатирование кода
- `npm run storybook` — запуск Storybook

---

## Пример использования

1. Нажмите на черную кнопку-стрелку слева для открытия панели параметров.
2. Измените нужные параметры (шрифт, цвет, ширина и т.д.).
3. Нажмите «Применить» для обновления стилей статьи.
4. Для возврата к исходным настройкам используйте кнопку «Сбросить».

---

## Структура src

- [`src/components`](src/components/) — UI и бизнес-компоненты
- [`src/constants`](src/constants/) — константы и типы параметров
- [`src/styles`](src/styles/) — глобальные стили
- [`src/fonts`](src/fonts/) — шрифты
