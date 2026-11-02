# ft_printf

*Because ft_putnbr() and ft_putstr() aren't enough.*

## 📖 Description

**ft_printf** is a recreation of the standard C library function `printf()`.

The goal of this project is to understand variadic functions in C and learn how formatted output works by implementing a simplified version of `printf()` from scratch.

The function handles different data types and format specifiers, converting and printing arguments according to the provided format string.

## 🛠️ Supported Conversions

The project supports the following format specifiers:

| Specifier | Description |
|:---:|---|
| `%c` | Prints a single character |
| `%s` | Prints a string |
| `%p` | Prints a pointer address in hexadecimal |
| `%d` | Prints a decimal number |
| `%i` | Prints an integer |
| `%u` | Prints an unsigned decimal number |
| `%x` | Prints a number in lowercase hexadecimal |
| `%X` | Prints a number in uppercase hexadecimal |
| `%%` | Prints a percent sign |

## 📂 Project Structure

```text
ft_printf/
│
├── includes/
│   └── ft_printf.h
│
├── src/
│   ├── ft_printf.c
│   ├── ft_putchar.c
│   ├── ft_putstr.c
│   ├── ft_putnbr.c
│   ├── ft_putunsigned.c
│   ├── ft_puthex.c
│   └── ft_putptr.c
│
├── Makefile
└── README.md
```

*The structure above is an example. Adjust it to match your actual project files.*

## ⚙️ Compilation

To compile the library, clone the repository and run:

```bash
git clone <repository-url>
cd ft_printf
make
```

This generates the static library:

```text
libftprintf.a
```

### Makefile Rules

| Command | Description |
|---|---|
| `make` | Compiles the library |
| `make clean` | Removes object files |
| `make fclean` | Removes object files and the library |
| `make re` | Recompiles everything |

## 🚀 Usage

Include the header file in your C source code:

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello, %s!\n", "World");
    ft_printf("Number: %d\n", 42);
    ft_printf("Hexadecimal: %x\n", 255);

    return (0);
}
```

Compile your program with the library:

```bash
cc main.c -L. -lftprintf -Iincludes -o program
```

Run it:

```bash
./program
```

**Output:**

```text
Hello, World!
Number: 42
Hexadecimal: ff
```

## 🧠 Concepts Learned

- Variadic functions (`va_list`, `va_start`, `va_arg`, `va_end`).
- String parsing and format specifiers.
- Type conversion and number representation.
- Pointer and hexadecimal manipulation.
- Memory management and modular programming.
- Static libraries and Makefiles.

## 🧪 Testing

You can test the implementation by comparing its output and return value with the original `printf()` function.

Example:

```c
int original;
int custom;

original = printf("Value: %d\n", 42);
custom = ft_printf("Value: %d\n", 42);

printf("printf return: %d\n", original);
printf("ft_printf return: %d\n", custom);
```

Make sure to test:
- Empty strings and NULL strings.
- Negative and positive integers.
- Zero values.
- Large unsigned integers.
- NULL pointers.
- Uppercase and lowercase hexadecimal output.
- Multiple format specifiers in one string.
- Invalid or unsupported format specifiers.

## 📚 Resources

- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [Variadic Functions – GNU C Library](https://www.gnu.org/software/libc/manual/html_node/Variadic-Functions.html)
- [printf – Linux Manual](https://man7.org/linux/man-pages/man3/printf.3.html)

## 👤 Author

**gvasylie**

---

*This project was developed as part of the 42 School Common Core curriculum.*
