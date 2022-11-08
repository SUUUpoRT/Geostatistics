<!--
author:   Your Name
email:    your@email.com
version:  0.1.0
language: uk
narrator: Ukrainian Female

icon: ./Images/GS_icon.png

comment:  This simple description of your course.
          Multiline is also okay.

link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css

script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js

translation: українська https://liascript.github.io/course/?https://github.com/SUUUpoRT/Geostatistics/blob/main/GS_lecture_1_en.md

-->

# Огляд у ймовірності та статистиці

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://liascript.github.io/course/?https://github.com/SUUUpoRT/Geostatistics/blob/main/GS_lecture_1_uk.md)

## Мети навчання

> Студенти відновлюють свої попередні знання з базових понять у ймовірності та статистиці, які стосуються цього курсу.

Ключові поняття включають

- Імовірність та умовна ймовірність
- Випадкова величина
- Очікування та дисперсія
- Випадкова функція (кілька випадкових величин)
- Коваріація та кореляція
- Функція розподілу Гауса

Релевантна література: будь-який підручник із ймовірності та статистики, наприклад, відповідні розділи в Dekking, Frederik Michel, ed. [A Modern Introduction to Probability and Statistics: Understanding why and how](https://katalog.ub.tu-freiberg.de/Record/0-1644977052). Springer, 2005.

Примітка. Ця глава не призначена як вступ до цих тем. Це скоріше повторення ключових понять, необхідних для курсу. Студент повинен визначити прогалини в знаннях і зміцнити розуміння індивідуально, перш ніж перейти до наступних розділів

## Випадкові випробування/експерименти

- **Випадкове випробування** або **випадковий експеримент** це експеримент, **результат** якого заздалегідь невідомий.

- **Простір вибірки** Ω – це набір усіх можливих результатів. Окремі результати іноді називають точками вибірки або **зразками**.

- приклади: 

  - Гральний кубик Ω={1,2,3,4,5,6} – дискретний
  - Буріння розвідувальної свердловини на товщину пласта Ω=[0,∞) – продовжується

## Об'єднання подій

 - **Об’єднання подій**: тоді нехай A і B позначають дві події

 - *Об’єднання* подій A і B, позначене A ∪ B, складається з усіх результатів A, або B, або обох.

 - *Перетин* подій A і B, позначене A ∩ B, складається з усіх результатів обох, A і B.

 - Якщо A є подією, тоді AC (*A доповнення чи не A*) є подією, що A не відбувається.

 - Набір A є *підмножиною* множини B, або, еквівалентно, B є надмножиною A, якщо A «міститься» всередині B, тобто всі результати A також є результатами B. A ⊂ B

 - *Порожню множину* ∅ називають неможливою подією, а її доповнення Ω *певною подією*.

## Діаграми Венна

![Venn diagram](./Images/GS_Venn.png)
Діаграма Венна

![Event C](./Images/GS_Venn_Event_C.png)
Подія C

![Event Cc](./Images/GS_Venn_Event_Cc.png)
Копія події

![Event F ∩ G](./Images/GS_Venn_Event_FuG.png)
Подія F ∩ G

![Event F U G](./Images/GS_Venn_Event_FuG.png)
Подія F U G

![Event F ∩ Gc U C](./Images/GS_Venn_Event_FiGcuC.png)
Подія F ∩ Gc UC

## Ймовірність

**Відносна частота**  події A h(A): Приклад – підкидання монети

![Coin flip](./Images/GS_coinflip.png)
$$ \huge {h(A)=\frac{1}{n}h_n(A)} $$
$ n  $ = Кількість випробувань, $ h_n(A) $ = Кількість позитивних подій

Межа h (якщо n стає дуже великим) називається **ймовірністю**. Вона визначається як функція P(A) з такими властивостями:

 - P(Ω) 	=1
 - P(ø)  	=0
 - 0 ≤ P(A) ≤ 1
 - P(Ac)=1 - P(A)
 - P(A U B) = P(A) + P(B) (для взаємного виключення)
 - P(A U B) = P(A) + P(B) – P(A ∩ B) (загальне)

## Умовна ймовірність

> **Умовна ймовірність** — це міра ймовірності настання події за умови, що відбулася інша подія.

![Probabaility AiB](./Images/GS_AiB.png)
Умовна ймовірність A при B дорівнює:
$$ \Huge {P(A|B) = \frac{P(A ∩ B)}{P(B)}} $$

![Calorific value](./Images/GS_Calorific_value.png)
Приклад: яка ймовірність CV > 22 МДж/кг (подія A), якщо ми знаємо, що вміст золи < 19% (подія B) P(A | B)?

## Теорема Байєса

$$ \begin{drcases}
   \text{P(A|B)⋅P(B) = P(A ∩ B) } \\
   \text{P(B|A)⋅P(A) = P(A ∩ B) }
   \end{drcases}
   \text{P(B|A)⋅P(A) = P(A|B)⋅P(B) } $$

> $$ P(A|B) = \frac{P(B|A)}{P(B)}⋅P(A) $$

    P(A), апріорна ймовірність , є початковим ступенем віри в A.

P(A | B), умовна ймовірність або апостеріорна ймовірність, — це ступінь віри в те, що A враховує B.

частка P(B | A)/P(B) представляє опору B, яку забезпечує A.

 - P(A), [апріорна ймовірність](http://en.wikipedia.org/wiki/Prior_probability), є початковим ступенем віри в A.
 - P(A|B), [умовна ймовірність](http://en.wikipedia.org/wiki/Prior_probability) або апостеріорна ймовірність, — це ступінь віри в те, що A враховує B.
 - частка P(B | A)/P(B) представляє опору B, яку забезпечує A.

> Як ми зв’язуємо це з даними про буріння свердловин і оцінками блоків?

## Остання сторінка

### Оцінка 1

!?[1](https://youtu.be/vmG2S1qE2Vs)

### Оцінка 2

!?[2](https://youtu.be/ZwNw0zGQ4p8)

