## Форматування за допомогою `fmt.Printf`

Функція `fmt.Printf` дозволяє форматувати та виводити значення. Нижче наведено огляд найбільш поширених специфікаторів формату:

| Специфікатор | Опис                                                            | Приклад                                  | Вивід                               |
|--------------|-----------------------------------------------------------------|------------------------------------------|-------------------------------------|
| `%v`         | Формат за замовчуванням для будь-якого значення                 | `fmt.Printf("%v", 123)`                  | `123`                               |
| `%+v`        | Формат за замовчуванням із назвами полів структури              | `fmt.Printf("%+v", Person{"Alice", 30})` | `{Name:Alice Age:30}`               |
| `%#v`        | Представлення у Go-синтаксисі                                   | `fmt.Printf("%#v", Person{"Alice", 30})` | `main.Person{Name:"Alice", Age:30}` |
| `%T`         | Виводить тип                                                    | `fmt.Printf("%T", 3.14)`                 | `float64`                           |
| `%t`         | Логічне значення (`true` або `false`)                           | `fmt.Printf("%t", true)`                 | `true`                              |
| `%b`         | Двійкове представлення                                          | `fmt.Printf("%b", 10)`                   | `1010`                              |
| `%c`         | Символ Unicode                                                  | `fmt.Printf("%c", 65)`                   | `A`                                 |
| `%d`         | Десяткове ціле число                                            | `fmt.Printf("%d", 123)`                  | `123`                               |
| `%o`         | Вісімкове ціле число                                            | `fmt.Printf("%o", 64)`                   | `100`                               |
| `%q`         | Символ або рядок у лапках                                       | `fmt.Printf("%q", 65)`                   | `'A'`                               |
|              |                                                                 | `fmt.Printf("%q", "Hello\nGo")`          | `"Hello\nGo"`                       |
| `%x`         | Шістнадцяткове (нижній регістр)                                 | `fmt.Printf("%x", 255)`                  | `ff`                                |
| `%X`         | Шістнадцяткове (верхній регістр)                                | `fmt.Printf("%X", 255)`                  | `FF`                                |
| `%U`         | Формат Unicode (U+1234 'char')                                  | `fmt.Printf("%U", 9731)`                 | `U+2603 '☃'`                        |
| `%e`         | Науковий формат (нижній регістр) для чисел з плаваючою крапкою  | `fmt.Printf("%e", 123.456)`              | `1.234560e+02`                      |
| `%E`         | Науковий формат (верхній регістр) для чисел з плаваючою крапкою | `fmt.Printf("%E", 123.456)`              | `1.234560E+02`                      |
| `%f`         | Десяткове число з плаваючою крапкою                             | `fmt.Printf("%f", 123.456)`              | `123.456000`                        |
| `%F`         | Те саме, що `%f`                                                | `fmt.Printf("%F", 123.456)`              | `123.456000`                        |
| `%g`         | Компактний формат float (обирає %e або %f)                      | `fmt.Printf("%g", 123.456)`              | `123.456`                           |
| `%G`         | Подібно до `%g`, використовує %E, якщо потрібно                 | `fmt.Printf("%G", 123.456)`              | `123.456`                           |
| `%s`         | Звичайний рядок                                                 | `fmt.Printf("%s", "Hello")`              | `Hello`                             |
| `%p`         | Адреса вказівника в шістнадцятковому форматі                    | `fmt.Printf("%p", &x)`                   | `0x...` (адреса)                    |
| `%%`         | Літеральний знак відсотка                                       | `fmt.Printf("%%")`                       | `%`                                 |

**Примітка:** Приклад з `%p` потребує оголошення змінної `x`. Вивід буде адресою пам'яті цієї змінної. Приклад для `%+v` та `%#v` передбачає структуру з іменем `Person` з полями `Name` та `Age`.

Ця таблиця містить стислий огляд найбільш часто використовуваних специфікаторів формату. Зверніться до офіційної документації Go для повного списку та більш детальної інформації.