# 2020.06.08
After Convid-19 quarantine, I come back Espoo to resume Hive Helsinki projects. 
## Target
* Transfer all TUT and hive projects and to github. 
* finnish personal blog website.  
* Learning English plan.
* LeetCode problem everyday.
* Find a intership in time(before black hole)


## Requirement
* Clean up the room
* Don't welter in phone.
* Do nothing on bed except reading book. Don't touch the bed in daytime.
* Physical exercise daily.
* Mustn't eat food after 20:00.



## There are some new actions.
1. Learn to use MarkDown.
2. Synchronize  repositories between github and vogsphere
3. Write down the study. 

## Hive Project ft_printf
1. Reading the subject file.

    The feature of the C language - variadic functions

    ```c
    man 3 printf 
    man 3 stdarg
    ```

    [How to read Markdown file on Chrome browser](https://imagecomputing.net/damien.rohmer/teaching/general/markdown_viewer/index.html)

2. Searching Reference

    Article : [Yineng Zhang from 42 Silicon Valley](https://medium.com/@zhang.yine/ft-printf-d95747b7aa5a)
    There are already 2472 test cases.

    Test Case: [testcase project](https://github.com/gavinfielder/pft)

    Example: [ft_printf](https://github.com/nouraellm/ft_printf.git)
        structure(make file) and main()

    Usefull tools to look up source code in github
    chrome extension: Sourcegraph 

    From the website: [gnu.org/software/libc/](https://www.gnu.org/software/libc/), we can download the source code of C language library. The latest version is 2.31. 

    go through the "main" function at first. 'printf.c'

```c
#include <libioP.h>
#include <stdarg.h>
#include <stdio.h>

#undef printf

/* Write formatted output to stdout from the format string FORMAT.  */
/* VARARGS1 */
int
__printf (const char *format, ...)
{
  va_list arg;
  int done;

  va_start (arg, format);
  done = __vfprintf_internal (stdout, format, arg, 0);
  va_end (arg);

  return done;
}

#undef _IO_printf
ldbl_strong_alias (__printf, printf);
ldbl_strong_alias (__printf, _IO_printf);
```
```c
int
__printf (const char *format, ...)
```
[可变参数说明中文](https://zhidao.baidu.com/question/376625773.html)

[可变参数说明英文](https://www.tutorialspoint.com/c_standard_library/c_function_printf.htm)




