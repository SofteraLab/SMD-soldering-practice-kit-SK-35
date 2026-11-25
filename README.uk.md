<p align="center">
  <a href="https://www.softeralab.com/">
    <img src="docs/assets/images/uk/logo.png" alt="Softera Lab" width="96">
  </a>
</p>

<h1 align="center">SMD Solder Kit · SK-35</h1>

<p align="center"><strong>Навчальний набір Softera Lab — NE555 · CD4017 · LED-черга · тренування 1206 → 0201 · USB-C 5 В · SK-35</strong></p>

<p align="center">
  <a href="README.md"><img alt="EN" src="https://img.shields.io/badge/EN-README.md-F97316?style=flat-square"></a>
  <a href="https://www.softeralab.com/"><img alt="Сайт" src="https://img.shields.io/badge/softeralab.com-09090B?style=flat-square&labelColor=18181B"></a>
  <a href="https://www.instagram.com/softeralab/"><img alt="Instagram" src="https://img.shields.io/badge/Instagram-09090B?style=flat-square&labelColor=18181B"></a>
  <a href="https://www.youtube.com/@SofteraLab"><img alt="YouTube" src="https://img.shields.io/badge/YouTube-09090B?style=flat-square&labelColor=18181B"></a>
  <img alt="USB-C" src="https://img.shields.io/badge/USB--C-5V-09090B?style=flat-square&labelColor=F97316">
</p>

<p align="center"><strong>Мови:</strong> <a href="README.md">English</a> · Українська (ця сторінка)</p>

<p align="center">
  <img src="docs/assets/images/uk/banner.png" alt="Банер SMD Solder Kit" width="720">
</p>

**SMD Solder Kit · SK-35** — навчальна плата Softera Lab для пайки SMD. Тренуєте п’ять типорозмірів резисторів — **1206, 0805, 0603, 0402, 0201** — і плата сама перевіряє роботу: коли весь стовпчик одного типорозміру запаяно правильно, **світлодіоди 0805** вмикаються **по черзі** й показують, що цей ряд зібрано вірно.

Мікроконтролера немає, прошивати нічого. Такт дає **NE555 (U1, SOIC-8)**, кроки по LED — лічильник **CD4017 (U2, SOIC-16)**. Живлення — **USB Type-C, 5 В**. Обв’язка логіки (**R**, **C**) — **0805**.

На другому боці — мікросхеми, площадки SOT для тренування та таблиця Metric/Inch.

Цей репозиторій — **сторінка продукту й нотатки збірки**. Це **не open-source hardware**: Gerber і виробничі файли публічно не викладаються.

> © Softera Lab. All rights reserved.

<p align="center">
  <img src="docs/assets/images/uk/poster.png" alt="Постер SMD Solder Kit" width="720"><br>
  <em>Сторона тренування зі світлом · сторона логіки з NE555 + CD4017</em>
</p>

## Як працює

1. Підключіть **USB Type-C** — плата працює від **5 В**  
2. **NE555** задає такт  
3. **CD4017** крокує по світлодіодах  
4. Запаюєте **повний стовпчик** резисторів одного типорозміру (**1206 → 0201**)  
5. Якщо ряд правильний — відповідні LED приєднуються до черги  

## Огляд плати

<p align="center">
  <img src="docs/assets/images/uk/designators.png" alt="Карта плати" width="720">
</p>

| Зона | Що є |
| --- | --- |
| **Живлення** | **USB Type-C** · **5 В** · площадки **+ / −** на боці логіки |
| **Такт** | **NE555** (**U1**, **SOIC-8**) |
| **Лічильник** | **CD4017** (**U2**, **SOIC-16**) |
| **Індикація** | **LED 0805** — черга + перевірка стовпчиків |
| **Тренування** | П’ять стовпчиків: **1206 · 0805 · 0603 · 0402 · 0201** (R1–R25) |
| **Обв’язка** | Логічні **R** / **C** у **0805** |
| **Довідник** | Таблиця Metric/Inch · площадки **SOT-23 / 25 / 26** |

### Сторона тренування

<p align="center">
  <img src="docs/assets/images/uk/board-practice.png" alt="Сторона тренування" width="720"><br>
  <em>Драбина 1206 → 0201 · LED6–LED10 · USB-C</em>
</p>

### Сторона логіки / продакшн

<p align="center">
  <img src="docs/assets/images/uk/board-logic.png" alt="Сторона логіки" width="720"><br>
  <em>U1 NE555 · U2 CD4017 · SOT · Metric/Inch</em>
</p>

## Що в наборі

<p align="center">
  <img src="docs/assets/images/uk/kit-contents.png" alt="Набір з першого погляду SK-35" width="720"><br>
  <em>Сторона тренування · сторона логіки · що входить у SK-35</em>
</p>

1. Чорна плата — сторона тренування + сторона логіки  
2. **NE555** (**SOIC-8**) і **CD4017** (**SOIC-16**)  
3. Роз’єм **USB Type-C** (female)  
4. SMD світлодіоди **0805** для черги / перевірки  
5. SMD резистори **1206 · 0805 · 0603 · 0402 · 0201**  
6. Логічні SMD резистори й конденсатори **0805** (**C1**, **C2**, …)  

## Характеристики

| Параметр | Значення |
| --- | --- |
| Продукт | **SMD Solder Kit · SK-35** |
| Живлення | **5 В** через **USB Type-C** |
| Такт | **NE555** (**U1**, **SOIC-8**) |
| Лічильник | **CD4017** (**U2**, **SOIC-16**) |
| LED | **0805** |
| Типорозміри | **1206 · 0805 · 0603 · 0402 · 0201** |
| Обв’язка | **0805** |
| МК / прошивка | **Немає** |
| Перевірка | LED по черзі, якщо стовпчик типорозміру запаяно правильно |

## Збірка

<p align="center">
  <img src="docs/assets/images/uk/desk.png" alt="На верстаку" width="720">
</p>

<p align="center">
  <img src="docs/assets/images/uk/solder-order.png" alt="Порядок пайки" width="720">
</p>

Рекомендований порядок:

1. **USB Type-C**  
2. **U1 NE555** + обв’язка **C1 / C2 / R31 / R32** (**0805**)  
3. **U2 CD4017** + **R26–R30**  
4. Тренувальні **LED 0805** (полярність)  
5. Стовпчики резисторів **від великих до малих**: **1206 → 0805 → 0603 → 0402 → 0201**  
6. Підключіть **5 В** — спочатку весь стовпчик одного типорозміру; LED підтверджує ряд  

## Соцмережі / каталог

<p align="center">
  <img src="docs/assets/images/uk/cover.png" alt="Прев’ю" width="720">
</p>

Рядок для каталогу:

```text
- [SMD Solder Kit SK-35](https://github.com/SofteraLab/smd-solder-kit-sk35) — NE555 + CD4017 LED-черга · тренування 1206–0201 · USB-C 5 В · SK35
```

## Посилання

- Сайт: [softeralab.com](https://www.softeralab.com/)  
- Курс: [Базова пайка](https://www.softeralab.com/course-basic-soldering/)  
- Instagram: [@softeralab](https://www.instagram.com/softeralab/)  
- YouTube: [@SofteraLab](https://www.youtube.com/@SofteraLab)  

## Авторське право

Див. [COPYRIGHT.md](COPYRIGHT.md). Усі права захищені. Не open-source hardware.
