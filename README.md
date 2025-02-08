# 📖 Get_Next_Line

A function that reads a line from a file descriptor, part of the 42 curriculum.

## 🎯 Function Prototype

```c
char *get_next_line(int fd);
```

## 📋 Features

- Read from multiple file descriptors
- Dynamic buffer size using BUFFER_SIZE macro
- Memory leak free
- Handles standard files, redirection, stdin

## 🚀 Usage

```c
#include "get_next_line.h"

int main(void)
{
    int     fd;
    char    *line;

    fd = open("test.txt", O_RDONLY);
    while ((line = get_next_line(fd)))
    {
        printf("%s", line);
        free(line);
    }
    close(fd);
    return (0);
}
```

## ⚙️ Compilation

```bash
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=42 *.c
```

## ⚡ Performance

- Efficient memory usage
- Minimal system calls
- Optimized buffer management
- No memory leaks

## 🔍 Return Values

- Line read: returns the line
- EOF reached: returns NULL
- Error: returns NULL

## ⚠️ Error Handling

- Invalid file descriptor
- Read errors
- Memory allocation failures
- NULL pointer handling
- Buffer size validation

## 🎓 Learning Outcomes

- Static variables
- File descriptors
- Memory management
- Buffer handling
- EOF conditions

## ⭐ Show your support

Give a ⭐️ if this project helped you!
