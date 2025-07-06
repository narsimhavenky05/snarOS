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
│
├── bootloader/            ← Boot code (Assembly) UEFI bootloader code
│   ├── boot.asm
│   └── linker.ld
│
├── kernel/                ← Kernel C code, Main kernel logic (C + ASM)
│   ├── kernel.c
│   ├── main.h
│   ├── panic.c
│   └── panic.h
│
├── arch/                  ← Architecture-specific code (x86_64)
│   ├── x86_64/
│   │   ├── cpu/
│   │   │   ├── gdt.c
│   │   │   ├── idt.c
│   │   │   └── isr.asm
│   │   ├── memory/
│   │   │   ├── paging.c
│   │   │   └── heap.c
│   │   └── interrupt/
│   │       ├── irq.c
│   │       └── irq.h
│
├── drivers/               ← Hardware drivers,  Keyboard, screen, etc.
│   ├── screen.c
│   ├── screen.h
│   ├── keyboard.c
│   └── keyboard.h
│
├── fs/                    ← File system (snarFS)
│   ├── fs.c
│   ├── snarfs.h
│   └── vfs.c
│
├── lib/                   ← Standard library-like functions,  Low-level support functions
│   ├── string.c
│   ├── stdio.c
│   └── memory.c
│
├── proc/                  ← Process management
│   ├── task.c
│   ├── scheduler.c
│   └── context_switch.S
│
├── shell/                 ← Terminal/shell interface
│   ├── shell.c
│   └── shell.h
│
├── user/                  ← User-space applications
│   ├── snarCalc.c
│   ├── snarText.c
│   └── snarGame.c
│
├── include/               ← Common header files, Header files
│   ├── stdio.h
│   ├── string.h
│   ├── memory.h
│   ├── snaros.h
│   └── config.h
│
├── tools/                 ← Build tools (scripts, utils)
│   ├── build.sh
│   ├── qemu_run.sh
│   └── iso_creator.sh
│
├── iso/                   ← Bootable ISO build structure
│   ├── grub/
│   │   └── grub.cfg
│   └── kernel.bin
│
├── logs/                  ← Debug logs (optional)
│   └── boot.log
│
└── docs/                  ← Design docs, architecture plans,  Architecture, design decisions
│    ├── snarOS_Design.md
│    └── snarFS_Spec.pdf
│ 
├── build/              # Output build artifacts (.bin, .img)
├── scripts/            # Shell scripts like build.sh
├── README.md
├── .gitignore
├── backups/
│      ├── snarOS_day1
│      ├── snarOS_day2
│      │ .....   
└── build.sh
