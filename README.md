# Arena

A small C memory arena library.

This library provides a simple virtual-memory-backed arena allocator. It reserves a large block of address space up front and commits memory as needed. Allocations are fast, linear, and can be cleared or popped in bulk.

## Features

- Simple arena allocator API
- Linear allocation
- Bulk clear/reset support
- Pop support
- Platform memory reservation/commit/decommit helpers
- Linux support using `mmap`, `mprotect`, `madvise`, and `munmap`
- Windows support using `VirtualAlloc` and `VirtualFree`
- Depends on the external `base` header-only library for common typedefs and macros

## Dependencies

This library depends on `base`.

The `base` library should provide types and macros such as:

```c
u8
u32
u64
i32
b32
MiB
GiB
MIN
MAX
