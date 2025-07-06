# snarOS

# snarOS 🐍🧠

**snarOS** is a completely independent operating system being built from scratch by [Sargam Narsimha Rao](https://github.com/narsimhavenky05). It uses a custom UEFI bootloader, kernel in C/Assembly, and is designed to be a full-featured modern OS built solo and modularly.

## 🔧 Current Features

- ✅ UEFI Bootloader
- ✅ C/Assembly Hybrid Kernel
- ✅ Text-mode screen output
- ✅ Physical Memory Management
- ✅ Virtual Paging
- ✅ Keyboard Input Driver
- 🔄 Coming Soon: Process Creation, File System (snarFS), snarShell, snarCalc

## 📁 Folder Structure

```bash
snarOS/
├── bootloader/         # UEFI bootloader code
├── kernel/             # Main kernel logic (C + ASM)
├── drivers/            # Keyboard, screen, etc.
├── lib/                # Low-level support functions
├── include/            # Header files
├── build/              # Output build artifacts (.bin, .img)
├── scripts/            # Shell scripts like build.sh
├── docs/               # Architecture, design decisions
├── README.md
├── .gitignore
└── build.sh
