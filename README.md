# Machine Readable Datasheet (MRD)

## A Machine-Readable Hardware Contract for Embedded Devices, Interfaces, Constraints, and Errata

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See license.md for more information.

Part of the [EmbeddedX platform](https://github.com/telespial/EmbeddedX-Specs).

* * *

## Abstract

Machine Readable Datasheet (MRD) captures the firmware-visible information engineers repeatedly need from datasheets, programming manuals, and errata.

MRD does not replace a vendor datasheet. It extracts the parts of the datasheet that software systems, validators, code generators, and engineers need in a structured form.

MRD focuses on practical hardware details:

* pins and pads
* pin functions
* registers and fields
* interfaces
* clocks, resets, interrupts, and DMA
* constraints and conflicts
* errata and workarounds

* * *

## 1. Scope

MRD may describe:

* device identity and revisions
* packages, pads, and pins
* pin multiplexing rules
* registers and fields
* peripheral blocks
* clocks, resets, interrupts, DMA
* interface instances
* electrical and functional constraints
* errata and workarounds
* traceability to source documentation

* * *

## 2. Why MRD Matters

Hardware rules are scattered across PDFs, code examples, app notes, and errata. Engineers often have to jump between all of them just to understand what firmware is allowed to do.

MRD gives those rules a reusable structure so that tools and reviewers do not have to rediscover the same details every time.

* * *

## 3. Relationship to Other Repositories

* [EmbeddedX-Specs](https://github.com/telespial/EmbeddedX-Specs): umbrella platform
* [Machine-Readable-Connectivity-Specs](https://github.com/telespial/Machine-Readable-Connectivity-Specs): shows how the schematic, netlist, BOM, and board files connect the device in a real design
* [Model-Definition-Package-Specs](https://github.com/telespial/Model-Definition-Package-Specs): defines model inputs, outputs, and behavior
* [Embedded-Intelligence-Layer-Specs](https://github.com/telespial/Embedded-Intelligence-Layer-Specs): defines runtime intelligence boundaries
* [AI-Integrated-Coding-System-Spec](https://github.com/telespial/AI-Integrated-Coding-System-Spec): controls code generation and validation so generated code does not contradict MRD
* [Embedded-Intelligence-Package-Specs](https://github.com/telespial/Embedded-Intelligence-Package-Specs): may package deployable artifacts that assume MRD-aligned integration

MRD describes what a device or pin can do.
MRC shows what that device or pin is connected to on the board.

* * *

## 4. Core Principle

If firmware depends on a hardware detail, MRD should be able to express it.

* * *

## License

See `license.md`.
