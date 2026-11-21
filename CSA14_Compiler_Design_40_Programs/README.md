# CSA14 – Compiler Design Lab (40 Programs)

This repository contains **40 separate source files**, one for each experiment in the supplied lab manual.

## Folder structure

```text
CSA14_Compiler_Design_40_Programs/
├── programs/        # 40 individual C and FLEX/LEX source files
├── sample_inputs/  # Example input files used by selected programs
├── README.md
└── .gitignore
```

## Programs

- Experiments 1–20: C programs (`.c`)
- Experiments 21–40: FLEX/LEX programs (`.l`)
- Experiments 33 and 34 explicitly refer to the programs in Experiments 32 and 31 in the lab manual. Separate files are included for them so that all 40 experiments can be uploaded individually.

## Running C programs

Install a C compiler such as GCC. From the repository folder, compile an individual program:

```bash
gcc programs/01_lexical_analyzer_tokens.c -o program
./program
```

On Windows:

```bash
gcc programs/01_lexical_analyzer_tokens.c -o program.exe
program.exe
```

Some programs in the supplied manual use older Turbo C functions or headers such as `conio.h`, `getch()`, `gets()` and `strcmpi()`. These are not supported by every modern GCC environment. Such programs may need small compatibility changes or an older compatible compiler.

## Running FLEX/LEX programs

Install Flex and GCC. Generate the scanner and compile it:

```bash
flex programs/27_capital_words.l
gcc lex.yy.c -o scanner
./scanner
```

For programs that read a source file, pass the input filename as an argument when the program expects `argv[1]`. Check the individual source file for its input method. The examples in `sample_inputs/` are provided as starting inputs.

## Notes

- The source programs are transcribed from the uploaded CSA14 lab manual.
- Two obvious `printf` transcription slips in Experiments 5 and 17 were corrected.
- The sample input files are supporting examples; the 40 source files remain separate in `programs/`.
- Review each program before submission and follow your faculty's exact compiler and execution requirements.
