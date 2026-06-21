# 🔐 Simple Keylogger

## PRODIGY_CS_04 - Prodigy InfoTech Cybersecurity Internship Task 04

---

## Description
A Python program that records and logs every keystroke made on the keyboard and saves them to a text file. This project demonstrates how keyloggers work from a cybersecurity perspective.

---

## Features
- Records all keystrokes in real-time
- Captures special keys like Space, Enter, Esc
- Automatically saves keystrokes to `keylog.txt`
- Lightweight and runs in background
- Press `F9` to stop the keylogger

---

## How It Works
- `pynput.keyboard.Listener` listens to all keyboard events
- `on_press()` function triggers every time a key is pressed
- Each keystroke is written to `keylog.txt` using file handling
- Special keys like Space, Enter are recorded as `Key.space`, `Key.enter`
- Program stops when `F9` is pressed

---

## Code Explanation
- `Listener()` creates a background keyboard listener
- `on_press(key)` captures every key press event
- `open("keylog.txt", "a")` opens file in append mode
- `f.write(str(key))` converts key to string and saves it
- `return False` stops the listener when F9 is pressed

---

## Technologies Used
- Python 3.13
- pynput (Keyboard Listener Library)

---

## How to Run
- `py -m pip install pynput`
- Open `keylogger.py` in IDLE
- Press F5 to run
- Type anything on keyboard
- Press F9 to stop
- Open `keylog.txt` to see recorded keystrokes

---

## Example

### Input (Keys Pressed): subbu[space]lakshmi 
### Output (keylog.txt):
's'
'u'
'b'
'b'
'u'
Key.space
'l'
'a'
'k'
's'
'h'
'm'
'i'
Key.esc
