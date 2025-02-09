# Tailwind CSS Cheat Sheet 📌

## 1️⃣ Text Size (`text-{size}`)
| Class        | Size (Pixels) |
|-------------|-------------|
| `text-xs`   | 12px |
| `text-sm`   | 14px |
| `text-base` | 16px (default) |
| `text-lg`   | 18px |
| `text-xl`   | 20px |
| `text-2xl`  | 24px |
| `text-3xl`  | 30px |
| `text-4xl`  | 36px |
| `text-5xl`  | 48px |
| `text-6xl`  | 60px |

**Example:**
```html
<p class="text-3xl">This is large text</p>
<p class="text-xs">This is small text</p>
```

---

## 2️⃣ Text Color (`text-{color}-{shade}`)
| Class | Color |
|-------|--------------|
| `text-red-500` | Red |
| `text-green-500` | Green |
| `text-blue-500` | Blue |
| `text-gray-700` | Dark Gray |

**Example:**
```html
<p class="text-red-500">This is red text</p>
<p class="text-green-600">This is green text</p>
```

---

## 3️⃣ Font Weight (`font-{weight}`)
| Class | Weight |
|-------|--------|
| `font-thin` | 100 (Thin) |
| `font-light` | 300 (Light) |
| `font-normal` | 400 (Normal) |
| `font-medium` | 500 (Medium) |
| `font-semibold` | 600 (Semi-bold) |
| `font-bold` | 700 (Bold) |
| `font-extrabold` | 800 (Extra-bold) |
| `font-black` | 900 (Black) |

**Example:**
```html
<p class="font-bold">This is bold text</p>
<p class="font-light">This is light text</p>
```

---

## 4️⃣ Background Color (`bg-{color}-{shade}`)
| Class | Color |
|-------|--------------|
| `bg-red-500` | Red |
| `bg-green-500` | Green |
| `bg-blue-500` | Blue |
| `bg-yellow-500` | Yellow |

**Example:**
```html
<div class="bg-blue-500 text-white p-4">
    This has a blue background
</div>
```

---

## 5️⃣ Padding (`p-{size}`) and Margin (`m-{size}`)
| Class | Size (Pixels) |
|-------|--------------|
| `p-2` | 8px padding |
| `p-4` | 16px padding |
| `m-2` | 8px margin |
| `m-4` | 16px margin |

**Example:**
```html
<div class="bg-gray-200 p-4 m-4">
    This has padding and margin
</div>
```

---

## 6️⃣ Border and Rounded Corners (`border-{size}` and `rounded-{size}`)
| Class | Effect |
|-------|--------|
| `border` | 1px border |
| `border-2` | 2px border |
| `border-4` | 4px border |
| `border-8` | 8px border |
| `rounded` | Slightly rounded |
| `rounded-md` | Medium rounded |
| `rounded-lg` | More rounded |
| `rounded-full` | Fully rounded |

**Example:**
```html
<div class="border-2 border-gray-500 rounded-lg p-4">
    This has a thicker border and rounded corners
</div>
```

---

## 7️⃣ Width and Height (`w-{size}` and `h-{size}`)
| Class | Effect |
|-------|--------------|
| `w-1/4` | 25% width |
| `w-1/2` | 50% width |
| `w-3/4` | 75% width |
| `w-full` | 100% width |
| `h-10` | 40px height |
| `h-20` | 80px height |
| `h-screen` | Full screen height |

**Example:**
```html
<div class="w-1/2 h-20 bg-blue-500">
    50% width and 80px height
</div>
```

---

## 8️⃣ Flexbox (`flex`, `justify-{}` and `items-{}`)
| Class | Effect |
|-------|--------|
| `flex` | Enables Flexbox |
| `flex-row` | Items in a row |
| `flex-col` | Items in a column |
| `justify-start` | Align items to start |
| `justify-center` | Center items horizontally |
| `justify-end` | Align items to end |
| `items-start` | Align items at the start vertically |
| `items-center` | Center items vertically |
| `items-end` | Align items at the end vertically |

**Example:**
```html
<div class="flex flex-col items-center justify-center h-screen bg-gray-100">
    <div class="bg-white p-8 rounded-lg shadow-lg">
        Centered Box with Flexbox
    </div>
</div>
```

---

## 9️⃣ Responsive Design (`sm:`, `md:`, `lg:`)
```html
<div class="bg-green-500 p-4 md:bg-blue-500 lg:bg-red-500">
  Background color changes on different screen sizes.
</div>
```

---

## 🔟 Transitions & Hover Effects (`transition-all`, `hover:bg-{}`)
```html
<button class="bg-blue-500 text-white px-4 py-2 rounded transition-all duration-300 hover:bg-blue-700">
  Hover me!
</button>
```

---



