# Machine Readable Datasheet (MRD)

## Hardware Data Firmware Can Actually Use

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See license.md for more information.

Part of the [EmbeddedX platform](https://github.com/telespial/EmbeddedX-Specs).

* * *

## Abstract

Machine Readable Datasheet (MRD) defines a machine-readable format for the parts of a device description that firmware actually depends on. It pulls together the details engineers usually chase across datasheets, reference manuals, and errata, then puts them in a form that tools and reviewers can reuse.

MRD focuses on firmware-relevant device data: pins, pad functions, registers, fields, interfaces, constraints, conflicts, and errata. It is not trying to replace a vendor datasheet. It is trying to capture the operational details software depends on.

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

The data firmware needs is scattered. Engineers jump between PDFs, code examples, app notes, and errata just to confirm what a device can do and what firmware is allowed to assume.

MRD establishes a reusable hardware contract so that generators and reviewers are not forced to rediscover the same rules every time.

* * *

## 3. Relationship to Other Repositories

* [EmbeddedX-Specs](https://github.com/telespial/EmbeddedX-Specs) establishes the umbrella platform
* [Machine-Readable-Connectivity-Specs](https://github.com/telespial/Machine-Readable-Connectivity-Specs) establishes what that device or pin is actually connected to in a board design
* [Model-Definition-Package-Specs](https://github.com/telespial/Model-Definition-Package-Specs) defines model metadata and runtime assumptions
* [Embedded-Intelligence-Layer-Specs](https://github.com/telespial/Embedded-Intelligence-Layer-Specs) establishes runtime intelligence boundaries
* [AI-Integrated-Coding-System-Spec](https://github.com/telespial/AI-Integrated-Coding-System-Spec) should not generate code that contradicts MRD
* [Embedded-Intelligence-Package-Specs](https://github.com/telespial/Embedded-Intelligence-Package-Specs) may package deployable artifacts that assume MRD-aligned integration

MRD establishes what a device or pin can do.
MRC establishes what that device or pin is actually connected to in a board design.

* * *

## 4. Core Principle

If the firmware depends on it, MRD should be able to express it.

* * *

## License

See `license.md`.
