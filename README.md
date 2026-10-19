# Persistent-CLI-Expense-Management-System-in-C.
Persistent CLI expense tracker built in C using linked lists, dynamic memory allocation, and file I/O. Supports adding, viewing, deleting expenses, and category-wise summaries. Data is saved to a flat file and reloaded on startup — no database needed. Demonstrates manual memory management, struct design, and input validation.


Expense Manager

A persistent command-line expense tracker written in C. No database, no dependencies — just a plain C program that saves your expenses to a file and reloads them every time you run it.

Features
Add expenses with date, category, description, and amount
View all expenses in a formatted table
Delete an expense by ID
Category-wise summary with grand total
Auto-fills today's date when adding
Data persists across sessions via a flat file (expenses.dat)
Getting Started

Requirements

GCC or any C compiler
Linux / macOS / Windows (with MinGW)

Compile

bash
gcc -Wall -o expense_manager expense_manager.c

Run

bash
./expense_manager
Usage
========= Expense Manager =========
  1. Add expense
  2. View all expenses
  3. Delete expense by ID
  4. Category summary
  5. Save & Exit

When adding an expense, just press Enter to accept today's date or type a custom one in YYYY-MM-DD format.

How Data is Stored

Expenses are saved in expenses.dat in the same directory as the binary. The format is pipe-delimited plain text:

1|2026-10-19|Food|Lunch at cafe|250.00
2|2026-10-19|Transport|Auto to office|80.00
3|2026-10-19|Bills|Electricity|1500.00

The file is written on exit and read on startup. Delete the file to start fresh.

Project Structure
expense_manager.c   — full source, single file
expenses.dat        — auto-generated data file (created on first save)
README.md           — this file
Concepts Demonstrated
Linked list implementation from scratch
Dynamic memory management (malloc / free)
File I/O with error handling (fopen, fgets, fprintf)
Input validation and safe string handling
Modular C code with single-responsibility functions
Known Limitations
Max 64 unique categories in the summary view
No edit functionality (delete and re-add as workaround)







