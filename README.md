# SkyMapper P-90 — Планер для фотограмметричного знімання

## Аванпроект | Курс "Бортові системи БПЛА" | KSE

**Варіант завдання:** №2 — Планер для фотограмметричного знімання

**Викладач:** к.т.н., ст. викладач, Іван Володимирович Жежера

---

## Опис проєкту

SkyMapper P-90 — безпілотний літальний апарат фіксованого крила (планер) для аерофотозйомки та фотограмметричного знімання великих територій.

### Основні характеристики

| Параметр | Значення |
|----------|----------|
| Тип | Планер фіксованого крила |
| Розмах крила | 1300 мм |
| Довжина фюзеляжу | 600 мм |
| Хвостове оперення | V-tail, 35° |
| Силова установка | Pusher (штовхаючий) |
| Час польоту | ≥90 хвилин |
| Камера | Full Frame, 42 Мп (Sony RX1R II) |
| Відеозв'язок | Аналоговий 5.8 ГГц |
| Автопілот | Pixhawk 6C (ArduPilot/PX4) |
| Автопосадка | Так |
| Висотомір | Лідарний (TFmini-S) |
| Цільова ціна | $10,000 USD |

---

## Структура репозиторію

```
├── README.md                  — цей файл
├── SkyMapper_P90.FCStd        — 3D-модель (FreeCAD)
├── SkyMapper_P90_v5.py        — Python-скрипт для генерації моделі
└── screenshots/               — скріншоти моделі
```

---

## Звіт (Google Docs)

📄 **[Посилання на звіт у Google Docs] https://docs.google.com/document/d/1QVfTxZOeRC5CV7qlkgYLSXEmG7ef2Do3Ahvey-PQnIU/edit?usp=sharing

Звіт містить:
- Опис проблематики
- Опис рішення
- Аналіз становища на ринку (senseFly eBee X, WingtraOne Gen II, Delair UX11)
- Порівняльна таблиця ТТХ
- Обґрунтування доцільності розробки
- Опис конструкції
- Підбір компонентної бази
- Ескіз прототипу

---

## 3D-модель (ескіз)

Модель створена у **FreeCAD 1.1.0** за допомогою Python-скрипту.

### Як відкрити модель:
1. Встановити [FreeCAD](https://www.freecad.org/downloads.php) (версія ≥ 1.0)
2. Відкрити файл `SkyMapper_P90.FCStd`

### Як згенерувати модель зі скрипту:
1. Відкрити FreeCAD
2. Відкрити Python-консоль: **Вид → Панели → Консоль Python**
3. Ввести:
```python
exec(open(r"шлях/до/SkyMapper_P90_v5.py", encoding="utf-8").read())
```

### Елементи моделі:
- **Fuselage** — фюзеляж (Loft з еліптичних перерізів)
- **Wing_Right / Wing_Left** — крила (NACA-профіль)
- **VTail_Right / VTail_Left** — V-подібне хвостове оперення
- **Motor + Propeller** — штовхаючий двигун з пропелером
- **Camera_Bay + Camera** — ніша під камеру Sony RX1R II
- **GPS** — GPS-антена (зверху)
- **Altimeter** — лідарний висотомір (знизу)

---

## Аналоги на ринку

| Модель | Час польоту | Камера | Ціна |
|--------|-------------|--------|------|
| senseFly eBee X | до 90 хв | S.O.D.A. 20 Мп | $20–25 тис. |
| WingtraOne Gen II | до 59 хв | Sony RX1R II 42 Мп FF | ~$30 тис. |
| Delair UX11 | 59–80 хв | 21.4 Мп | $10–15 тис. |
| **SkyMapper P-90** | **≥90 хв** | **Full Frame 42 Мп** | **$10 тис.** |

---

## Компонентна база

| Компонент | Модель |
|-----------|--------|
| Автопілот | Holybro Pixhawk 6C |
| GPS | Holybro M9N |
| Камера | Sony RX1R II (42 Мп FF) |
| Двигун | T-Motor AT2312 1400KV |
| ESC | Holybro Tekko32 35A |
| Батарея | Tattu 6S 10000mAh |
| Відеопередавач | TBS Unify Pro32 (5.8GHz) |
| Приймач RC | TBS Crossfire Nano |
| Висотомір | Benewake TFmini-S |
| Датчик швидкості | MS4525DO |
| Телеметрія | Holybro SiK Radio V3 |
| Корпус | EPO пінопласт + карбонові лонжерони |

---

## Джерела

1. [senseFly eBee X](https://www.sensefly.com/drone/ebee-x/)
2. [WingtraOne Gen II](https://wingtra.com/mapping-drone-wingtraone/)
3. [Delair UX11](https://delair.aero/delair-commercial-drones-2/professional-mapping-drone-delair-ux11-2/)
4. [Holybro Pixhawk 6C](https://holybro.com/products/pixhawk-6c)
5. [Sony RX1R II](https://www.sony.com/en/interchangeable-lens-cameras/products/dsc-rx1rm2)
6. [FreeCAD](https://www.freecad.org/)
