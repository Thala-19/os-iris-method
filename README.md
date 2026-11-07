# The Iris Method — Operating Systems, Ring by Ring

A single self-contained page that reconstructs **COMP6697001 Operating Systems** (seven lecture decks, 272 slides)
as one continuous argument: every concept exists to remove a specific limitation of the concept inside it.

**Live:** https://thala-19.github.io/os-iris-method/

No build step, no dependencies, no network calls — open `index.html` and it works.

## What the page does

The course is laid out as concentric rings. Ring 0 is the bare instruction cycle; each ring outward is an
invention that fixed something the previous ring could not do.

| Ring | Topic | The limit it removed |
| --- | --- | --- |
| 0 | The instruction cycle | — (the foundation) |
| 1 | Interrupts and the resident monitor | a program the machine could not take back |
| 2 | Multiprogramming | a CPU idle during every I/O wait |
| 3 | **The process** (hinge ring) | nothing was resumable or accountable |
| 4 | Lifecycle and the five-state model | "not running" hid two different problems |
| 5 | System calls and modes | user code could not ask for any of it |
| 6 | Threads | a whole address space per unit of work |
| 7 | Scheduling | a ready queue with no policy |
| 8 | Synchronisation and IPC | concurrent reads and writes race |
| 9 | Deadlock | blocking that can never end |
| 10 | Multiprocessor systems | "one instruction stream at a time" was assumed |
| 11 | Beyond | distributed systems, middleware, the open question |

## What is on the page

- An interactive **iris plate**: hover a band or a legend row to pair them; click through to the ring.
- An **interactive five-state process machine** (including the suspend pair) with the transitions spelled out.
- A working **context-switch demo**: two PCBs, one CPU, registers saved and restored.
- Figures for the CPU-utilisation argument, the fork/exec tree, thread sharing, the ULT/KLT quantum timeline,
  a semaphore race table, a resource-allocation graph, dining philosophers, the multicore hardware spectrum.
- Eleven exam-style questions with one-line answers.

## How claims are tagged

Because much of the source material is slide *images* rather than text, every claim carries a tag:

- `SOURCE` — stated in the slides, with slide numbers.
- `INFERRED` — not written down, but the only conclusion the material supports. Marked as deduction.
- `EXTERNAL` — fills a gap the decks leave open (figures whose text is not machine-readable). Labelled as
  outside knowledge.

Two errors in the printed listings are called out rather than reproduced, and the reasoning for each is
given on the page.

## Sources

Rasjid, Z. E. — COMP6697001 Operating Systems: *Introduction to Operating Systems* (43 slides), *Processes*
(39), *Threads* (43), *Multiple Processor Systems* (23), *Process Scheduling* (33), *Synchronization and
Inter-process Communication* (48), *Deadlock* (43). Adapted from Tanenbaum & Bos, *Modern Operating Systems*
5e (ch. 1–8) and Stallings, *Operating Systems: Internals and Design Principles* 9e (ch. 1–13).
