# Задача 1. Акаунт користувача

 

Перед звільненням розробник зламав вихідний код управління акаунтами користувачів. Виконай рефакторинг методів об'єкта `customer`, додавши ключове слово `this` при зверненні до властивостей.

### Стартовий код:
```javascript
const customer = {
  username: "Mango",
  balance: 24000,
  discount: 0.1,
  orders: ["Burger", "Pizza", "Salad"],
  // Change code below this line
  getBalance() {
    return balance;
  },
  getDiscount() {
    return discount;
  },
  setDiscount(value) {
    discount = value;
  },
  getOrders() {
    return orders;
  },
  addOrder(cost, order) {
    balance -= cost - cost * discount;
    orders.push(order);
  },
  // Change code above this line
};

customer.setDiscount(0.15);
console.log(customer.getDiscount()); // 0.15
customer.addOrder(5000, "Steak");
console.log(customer.getBalance()); // 19750
console.log(customer.getOrders()); // ["Burger", "Pizza", "Salad", "Steak"]
```

 

# Задача 2. Склад

**Файл: `task-2.js`**

Створи клас `Storage`, який оперує приватною властивістю `items` (масив товарів).

### Метод класу:
- `getItems()` — повертає `items`
- `addItem(newItem)` — додає новий товар
- `removeItem(itemToRemove)` — видаляє товар

### Тестовий код:
```javascript
const storage = new Storage(["Nanitoids", "Prolonger", "Antigravitator"]);
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator"]
storage.addItem("Droid");
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]
storage.removeItem("Prolonger");
console.log(storage.getItems()); // ["Nanitoids", "Antigravitator", "Droid"]
```

 

# Задача 3. Конструктор рядків
 

Створи клас `StringBuilder` з приватною властивістю `value`.

### Метод класу:
- `getValue()` — повертає значення
- `padEnd(str)` — додає в кінець
- `padStart(str)` — додає на початок
- `padBoth(str)` — додає на початок і кінець

### Тестовий код:
```javascript
const builder = new StringBuilder(".");
console.log(builder.getValue()); // "."
builder.padStart("^");
console.log(builder.getValue()); // "^."
builder.padEnd("^");
console.log(builder.getValue()); // "^.^"
builder.padBoth("=");
console.log(builder.getValue()); // "=^.^="
```

 
