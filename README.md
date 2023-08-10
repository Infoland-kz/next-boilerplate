# Infoland Next + TS + Eslint + Prettier boilerplate

## Документация

Скоро будет...

## Techstack

[![npm](https://img.shields.io/static/v1?label=npm&message=9.4.0&color=2c8ebb&style=for-the-badge&logo=npm)](https://www.npmjs.com//)
[![node](https://img.shields.io/static/v1?label=node&message=19.6.0&color=026E00&style=for-the-badge&logo=node.js)](https://nodejs.org/en/)
[![next](https://img.shields.io/static/v1?label=next.js&message=3.6&color=01C58E&style=for-the-badge&logo=next.js)](https://nextjs.org/docs)
[![typescript](https://img.shields.io/static/v1?label=typescript&message=5.0&color=3278C7&style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
[![tailwindcss](https://img.shields.io/static/v1?label=tailwindcss&message=3.3&color=37BCF8&style=for-the-badge&logo=tailwindcss)](https://tailwindcss.com/)
[![prettier](https://img.shields.io/static/v1?label=prettier&message=2.8.7&color=F7B93E&style=for-the-badge&logo=prettier)](https://prettier.io/)
[![eslint](https://img.shields.io/static/v1?label=eslint&message=8.4&color=4B32C3&style=for-the-badge&logo=eslint)](https://eslint.org/)

## Основые комманды

Обязательно установите зависимости:

```bash
npm install
```

Для запуска сервера для разработки

```bash
npm run dev
```

Для сборки проекта

```bash
npm run build
```

Локальная предварительная версия продакшн сборки

```bash
npm run preview
```

## Структура проекта

В шаблоне присуствуют некоторые архитектурные паттерны:

- `types` - дирректория, которая хранит в себе структуры данных или их типы/интерфейсы/абстракции
- `repositories` - дирректория, которая хранит в себе классы, которые делают запросы по API. Для HTTP запросов внутри есть базовый NetAPI класс, который по DI принимает Http клиент и делает запросы по внешним API. Также есть базовый LocalAPI, который записывает или берет данные с локального хранилища. Для работы с последующими репозиториями, надо наследоваться от одного из базовых классов.
- `services` - дирректория, которая хранит в себе классы, которые производят какие либо вычесления, или служат оберткой для сторонних зависимостей.

Также, в шаблоне структурированы компоненты по Atomic Design. Компоненты деляться на:

- `components/atoms/*` – тут расположены примитивные компоненты: кнопки, заголовки, поля ввода и пр.
- `components/molecules/*` – тут расположены связки/группы примитивов: группы кнопок, карточки и пр.
- `components/organisms/*` – тут расположены связки/группы молекул. То есть компоненты, которая состоит из молекул, которые состоят из примитивов: шапка, списки карточек, модальные окна и пр.
- `components/templates/*` – тут расположены шаблоны страницы

Подробнее можно почитать:

- [Atomic Design Methodology](https://atomicdesign.bradfrost.com/chapter-2/)
- [Atomic Design in practice](https://blog.ippon.tech/atomic-design-in-practice/)
