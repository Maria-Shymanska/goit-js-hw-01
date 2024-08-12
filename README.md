# goit-js-hw-01

 Виконуй це завдання у файлі task-1.js

## Завдання: makeTransaction

## Опис завдання

Станція з продажу ремонтних дроїдів готова до запуску. Потрібно написати програмне забезпечення для відділу продажів.

Оголосіть функцію `makeTransaction`, яка очікує два параметри:

- `quantity` — кількість замовлених дроїдів (число)
- `pricePerDroid` — вартість одного дроїда (число)

## Функція повинна повернути рядок з повідомленням про покупку дроїдів

де:

- `<quantity>` — це кількість замовлених дроїдів
- `<totalPrice>` — це загальна вартість замовлення, тобто вартість усіх замовлених дроїдів

## Код

```javascript
// Оголошення функції makeTransaction
function makeTransaction(quantity, pricePerDroid) {
  // Обчислення загальної вартості замовлення
  const totalPrice = quantity * pricePerDroid;

  // Повернення рядка з повідомленням про покупку
  return `You ordered ${quantity} droids worth ${totalPrice} credits!`;
}

// Перевірка роботи функції за допомогою прикладів
console.log(makeTransaction(5, 3000)); // "You ordered 5 droids worth 15000 credits!"
console.log(makeTransaction(3, 1000)); // "You ordered 3 droids worth 3000 credits!"
console.log(makeTransaction(10, 500)); // "You ordered 10 droids worth 5000 credits!"

Виконуй це завдання у файлі task-2.js

# Завдання: getShippingMessage

## Опис завдання

Оголосіть функцію `getShippingMessage`, яка очікує три параметри:

- `country` — країна доставки (рядок)
- `price` — загальна вартість товару (число)
- `deliveryFee` — вартість доставки товару (число)

Функція повинна повернути рядок з повідомленням про доставку товару:


де:

- `<country>` — це країна доставки
- `<totalPrice>` — це загальна вартість замовлення, яка включає вартість товару та вартість доставки.

## Код

```javascript
// Оголошення функції getShippingMessage
function getShippingMessage(country, price, deliveryFee) {
  // Обчислення загальної вартості замовлення
  const totalPrice = price + deliveryFee;

  // Повернення рядка з повідомленням про доставку
  return `Shipping to ${country} will cost ${totalPrice} credits`;
}

// Перевірка роботи функції за допомогою прикладів
console.log(getShippingMessage("Australia", 120, 50)); // "Shipping to Australia will cost 170 credits"
console.log(getShippingMessage("Germany", 80, 20)); // "Shipping to Germany will cost 100 credits"
console.log(getShippingMessage("Sweden", 100, 20)); // "Shipping to Sweden will cost 120 credits"



# Завдання: getElementWidth

## Опис завдання

Оголосіть функцію `getElementWidth`, яка очікує три параметри:

- `content` — ширина контенту (рядок формату "Npx", де N — число, ціле або дробове)
- `padding` — значення горизонтального падінгу для кожної зі сторін (рядок формату "Npx")
- `border` — значення товщини бордера для кожної зі сторін (рядок формату "Npx")

Функція повинна повертати число — загальну ширину елемента. При розрахунку загальної ширини орієнтуйтесь на те, що значення `box-sizing` дорівнює `border-box`.

## Код

```javascript
// Оголошення функції getElementWidth
function getElementWidth(content, padding, border) {
    // Перетворення рядків у числа, видаливши "px" і перетворивши на число
    const contentValue = parseFloat(content);
    const paddingValue = parseFloat(padding);
    const borderValue = parseFloat(border);

    // Обчислення загальної ширини елемента (border-box)
    const totalWidth = contentValue + (paddingValue * 2) + (borderValue * 2);

    return totalWidth;
}

// Перевірка роботи функції за допомогою прикладів
console.log(getElementWidth("50px", "8px", "4px")); // 74
console.log(getElementWidth("60px", "12px", "8.5px")); // 101
console.log(getElementWidth("200px", "0px", "0px")); // 200
