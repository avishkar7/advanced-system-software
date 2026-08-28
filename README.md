# Advanced System Software

Coursework in operating systems and low-level systems software, built on a
bare-metal RISC-V + QEMU environment and the xv6 teaching kernel. Topics span
process management and scheduling, traps and system calls, memory and stack
layout, software security, and kernel performance.

Each assignment lives in its own repository with a write-up, source, and (where
applicable) a report. They are wired into this hub as **git submodules** (`hw1`
… `hw5`), so the whole course can be checked out at once:

```bash
git clone --recurse-submodules https://github.com/avishkar7/advanced-system-software.git
# already cloned?
git submodule update --init --recursive
```

## Assignments

| # | Topic | What it does | Repo |
|---|-------|--------------|------|
| HW1 | Bare-metal RISC-V intro | Foundation for the RISC-V + QEMU track | [advanced-system-software-hw1](https://github.com/avishkar7/advanced-system-software-hw1) |
| HW2 | Bare-metal RISC-V | Builds on the HW1 environment | [advanced-system-software-hw2](https://github.com/avishkar7/advanced-system-software-hw2) |
| HW3 | Scheduling & traps | Cooperative multitasking kernel: `ecall`-driven scheduler with yield/resume and per-process state | [advanced-system-software-hw3](https://github.com/avishkar7/advanced-system-software-hw3) |
| HW4 | Software security | Stack buffer overflow and `ret2win` control-flow hijack, plus a GCC stack-protector defense | [advanced-system-software-hw4](https://github.com/avishkar7/advanced-system-software-hw4) |
| Final | Kernel performance | Adaptive dynamic tick interval in xv6, with a fixed-vs-dynamic performance study | [advanced-system-software-hw5](https://github.com/avishkar7/advanced-system-software-hw5) |

## Skills demonstrated

- Bare-metal / freestanding C and RISC-V assembly (no libc, custom linker scripts)
- Machine-mode trap handling, `ecall` dispatch, cooperative scheduling
- RISC-V calling convention, stack-frame analysis, exploit development (GDB, objdump)
- Kernel modification and empirical performance evaluation on xv6
- Build tooling with `make` and QEMU

## Repository conventions

This portfolio follows one repeatable structure per course, reused across
subjects:

- **One repo per dense assignment**, named `<course-slug>-hwN`, each with its own
  README, `src/`, `docs/handout.pdf`, and a `report/` where a write-up exists.
- **A course hub repo** (this one), named `<course-slug>`, indexing every
  assignment.
- Build artifacts and OS cruft are git-ignored; only source and documents are
  committed.
