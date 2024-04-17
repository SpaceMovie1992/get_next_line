# get_next_line
## Get Next Line - Reading a line from a file descriptor is way too tedious

This project involves writing a function called `get_next_line()` that reads a line from a file descriptor and returns it.

### Mandatory Part

#### Function name: get_next_line

- Prototype: `char *get_next_line(int fd);`
- Turn in files: `get_next_line.c`, `get_next_line_utils.c`, `get_next_line.h`
- Parameters: `fd` - The file descriptor to read from
- Return value:
  - Read line: Correct behavior
  - `NULL`: There is nothing else to read, or an error occurred
- External functions allowed: `read`, `malloc`, `free`
- Description:
  - Write a function that returns a line read from a file descriptor.
  - Repeated calls to `get_next_line()` should let you read the text file pointed to by the file descriptor, one line at a time.
  - The function should return the line that was read. If there is nothing else to read or if an error occurred, it should return `NULL`.
  - The returned line should include the terminating `\n` character, except if the end of file was reached and does not end with a `\n` character.
  - The header file `get_next_line.h` must at least contain the prototype of the `get_next_line()` function.
  - Add all the helper functions you need in the `get_next_line_utils.c` file.

### Compilation Instructions

- Because you will have to read files in `get_next_line()`, add this option to your compiler call: `-D BUFFER_SIZE=n`.
- Example compilation command: `cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 <files>.c`.
- We must be able to compile this project with and without the `-D BUFFER_SIZE` flag in addition to the usual flags. You can choose the default value of your choice.

### Project Requirements

- Avoid reading the whole file and then processing each line. Try to read as little as possible each time `get_next_line()` is called.
- It's forbidden to use your `libft` library in this project.
- `lseek()` is forbidden.
- Global variables are forbidden.

### Bonus Part

#### Bonus Requirements

- Develop `get_next_line()` using only one static variable.
- Your `get_next_line()` should manage multiple file descriptors at the same time.
- Append the `_bonus.[c/h]` suffix to the bonus part files.

### Submission

Submit the required files to your assigned git repository. Ensure that your project follows the norms outlined in the project requirements to avoid penalties during evaluation.
