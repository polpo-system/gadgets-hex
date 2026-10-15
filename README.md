# gadgets-hex

Hex for the gadgets of [polpo](https://github.com/polpo-system/polpo): a hex dump viewer and
editor for any file. A Hex document shows the position of each byte, its value in hexadecimal and
as ASCII; you can edit both columns, and a middle click on a byte shows the bytes from there
interpreted as numbers, reals and so on in the System.Log.

```
portia.Install gadgets-hex
```

## Using

    Hex.Open file          the file in a new Hex document (Store keeps the changes)
    Hex.Search ^           look for a pattern in the marked document
    Hex.Locate ^           set the caret in the marked document

`tools/Hex.Tool` (from Linux Oberon) has these commands and the keys of the editor.

## What is here

    src/Hex.Mod            the editor
    tools/Hex.Tool
    test/HexTest.Mod

Hex is by Patrick Saladin. The source comes from ETH Linux Oberon (OLR, 2017-06-18), converted from an Oberon text to plain
text; the first commit has it unchanged. It compiles unchanged with all five of polpo's compilers
(x86, ARM, ARMv7, RISC-V, MIPS).

## Tests

    HexTest.Run      2 checks: a Hex gadget made, a Hex document of a file loaded; it needs the
                     desktop's display

The license is GPL-3 (`LICENSE`); the code comes from ETH Oberon, whose license (`LICENSE.ETH`)
asks to keep its copyright notice and conditions, which `LICENSE.ETH` does.
