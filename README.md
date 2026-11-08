# One Prompt, Eleven Rings

A single self-contained page that turns **COMP6697001 Operating Systems** (seven decks, 272 slides) into
one continuous story. You type a line into an agentic AI; each ring is another layer of the machine that
has to answer before you see a reply.

**Live:** https://thala-19.github.io/os-iris-method/

No build step, no dependencies, no network calls — open `index.html` and it works.

## The one example

> "Find the TODO in this repo, fix one, and commit it."

Every ring asks the same two questions about that prompt: **what is the machine doing at this layer**, and
**what would break without it**. The jargon stays — process, PCB, fork, pre-emption, semaphore, deadlock —
but each term is defined where it first appears, in plain words.

Ring 0 is the bare instruction cycle. Each ring outward removed a limit of the ring inside it, which is why
the course is one argument rather than seven topics.

| Ring | Topic | What it does for the prompt |
| --- | --- | --- |
| 0 | The instruction cycle | turns your text into instructions, one at a time |
| 1 | Interrupts and the resident monitor | lets a timer take the CPU back from the agent |
| 2 | Multiprogramming | runs something else while the agent waits on the network |
| 3 | **The process** (hinge ring) | saves the half-written answer so it can be resumed |
| 4 | Lifecycle and the five-state model | tells "waiting for a reply" apart from "waiting for a turn" |
| 5 | System calls and modes | lets the agent read a file without owning the disk |
| 6 | Threads | runs the stream, the stop button and three tools together |
| 7 | Scheduling | shares the CPU fairly when eight agents are ready |
| 8 | Synchronisation and IPC | makes the transcript one write at a time |
| 9 | Deadlock | (this ring is the bill for ring 8) a spinner that never settles |
| 10 | Multiprocessor systems | runs three tools genuinely at the same instant |
| 11 | Beyond | reaches a tool on someone else's machine |

## What is on the page

- An interactive **iris plate**: hover a band or a legend row to pair them; click through to the ring.
- An **interactive five-state process machine** (including the suspend pair) with the transitions spelled out.
- A working **context-switch demo**: two PCBs, one CPU, registers saved and restored.
- Figures for the CPU-utilisation argument, the fork/exec tree, thread sharing, the ULT/KLT quantum timeline,
  a semaphore race table, a resource-allocation graph, dining philosophers, the multicore hardware spectrum.
- A closing table that runs the one prompt end to end, ring by ring.
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
