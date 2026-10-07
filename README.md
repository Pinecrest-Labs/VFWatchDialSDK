# VFWatchDialSDK

VFWatchDialSDK is a pre-compiled SDK full of development tools for watch face preview generation and compiling watch faces for smartwatches that use the VeryFit app.

This cross-platform toolchain provides the underlying binary assets, configuration utilities, and native runtime libraries required to build, validate, and serialize factory-compliant `.iwf` container payloads entirely offline.

## Core Component Modules

The SDK packages pre-compiled, optimized tool components to streamline asset building pipelines:

* **Watch Face Compiler Engine:** Native layout assembler designed to ingest structured asset coordinates and compile hardware-ready container blobs.
* **JSON Schema Tool:** Local structural validator that enforces strict compliance with the IDO Watch Face framework property keys and calculates required x+1, y+1 compound component offsets.
* **Native Runtime Libraries:** Cross-platform pre-compiled binaries (`.dll` for Windows environments and `.so` for Linux systems; Mach-O configurations for macOS environments to be added in a future release cycle) to handle automated asset quantization and raw stream packing.

## SDK Directory Tree (Directory structure may vary)

```text
VFWatchDialSDK/
├── win32_bin/                       # Pre-compiled Application Binaries for Windows
│   ├── compile_dial.zip             # Core local compiler executable
│   └── json_schema_tool.zip         # Native manifest schema layout auditor
├── lib/                             # Cross-Platform Native Runtime Libraries
│   ├── win32_x64/                   # Windows 64-bit platform targets (.dll)
│   └── linux_x64/                   # Linux 64-bit platform targets (.so)
├── include/                         # Header files for custom compiler hooks
└── LICENSE                          # License File
```
More tools will be added later.

---

## Operational Sideload Deployment

Once the compiler output structures your localized watch face package, the compiled container file can be deployed directly over-the-air (OTA) utilizing any standard Bluetooth Low Energy (BLE) sideloading client tool directed at the hardware's native storage partition directory.

---

Built for developers.
