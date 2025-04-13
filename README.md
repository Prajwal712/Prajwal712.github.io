
# File Management Tool (ICS Project)

This is a console-based file management utility written in C. It helps users organize files within a specified directory by sorting them into category folders based on their extensions and by identifying and handling duplicate files. It also provides functionality to revert these changes.


## Features

*   **File Sorting:**
    *   Sorts files into specific folders based on their file extensions (e.g., `.jpg`, `.png` -> `Photos`; `.pdf`, `.docx` -> `Documents`).
    *   Uses a predefined set of extension-to-folder mappings.
    *   Allows users to view, add, edit, and remove these mappings.
    *   Supports recursive sorting (processes subdirectories) and non-recursive sorting (current directory only).
*   **Duplicate File Handling:**
    *   Identifies duplicate files within the target directory (and optionally subdirectories).
    *   Duplicates are identified first by file size, then by byte-by-byte content comparison.
    *   Moves *one instance* of each set of duplicate files to a dedicated `Trash` folder created within the target directory.
    *   Deletes the other duplicate instances.
    *   Tracks the original paths of all duplicates corresponding to the single file moved to the `Trash`.
*   **Revert Operations:**
    *   Can revert the file sorting operations (moves files back to their original locations, removes created sorting folders).
    *   Can restore files from the `Trash` folder back to *all* their original duplicate locations.
*   **User-Friendly Console Interface:**
    *   Menu-driven navigation for easy operation.
    *   Provides feedback on operations (e.g., success messages, error messages).
*   **Path Safety:**
    *   Includes checks to prevent excessively long file paths (`MAX_PATH_LENGTH`).
    *   Handles potential file name collisions during moves by appending counters (e.g., `(1)file.txt`, `(2)file.txt`).


## Building

You can compile the project using GCC:

gcc b24mt1041_b24cs1055_b24bb1038_b24cs1080_main.c b24mt1041_b24cs1055_b24bb1038_b24cs1080_duplicate_files.c b24mt1041_b24cs1055_b24bb1038_b24cs1080_sort_files.c b24mt1041_b24cs1055_b24bb1038_b24cs1080_ui.c -o managefile
