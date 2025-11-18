# Yarg Lang

Host of Yarg, a dynamic language for Microcontroller firmware development.

![Picture of three development boards and slice of Cornish Yarg cheese](boards-and-cheesex320.jpeg)

  * Homepage: [yarg-lang.dev][homepage]
  * Code: [github.com/yarg-lang/yarg-lang][repo]
  * Test Hardware: [github.com/yarg-lang/test-hardware][hardware]

##  Places to get Updates
  * Blog: [posts tagged yarg-lang][blog].
  * John's Newsletter: [yarg-lang.dev/notes][newsletter].

## Why Yarg

Microcontrollers (such as the $4 Raspberry Pi Pico, or the ESP32 family) are powerful computers. They containmultiple cores, many peripherals and a rich interface of memory mapped registers and interrupts. We commonly develop software for them with languages like C or Python. C offers complete access to the system, but was designed when resources were very scarce, and it leaves a lot of work to the developer. Languages like Python offer more to the developer, but were designed with a general purpose computer in mind, and make access to hardware awkward (often they require a C driver). Yarg aims to provide the conveniences of languages like Python, alongside features that allow full access to hardware, so that C is not required to complete a project.

Of course, if you want to use modern language features, many general purpose languages are available in 'Micro', 'Tiny' or other cut-down versions of their implementation for microcontroller use. These implementations are faced with choices when the resources available do not support the same implementation possible in their original form. Do they try to be compatible (at what cost, if that is even possible?), or do they document a limitation compared to the original language? Yarg always prioritises microcontroller development, so all of the implementation choices suit production use for firmware.

Without clear multiprocessing support, language samples for starting projects must include polling, ("while true { sleep(x); do-stuff(); }"), which is wasteful of energy. How long is x? How often is do-stuff() actually needed? Modern microcontrollers are designed to be normally off, and to wake when something interesting is happening. Yarg is a language designed to eliminate wasteful polling like this from the start.

[blog]: https://transmissionbegins.com/ToT/tag/yarg-lang/
[homepage]: https://yarg-lang.dev/
[newsletter]: https://yarg-lang.dev/notes
[repo]: https://github.com/yarg-lang/yarg-lang
[hardware]: https://github.com/yarg-lang/test-hardware
