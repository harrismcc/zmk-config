# ZMK Firmware Configuration

## Build Commands
- **Build firmware**: `west build` (from config directory)
- **Build specific board/shield**: `west build -b nice_nano_v2 -- -DSHIELD=sofle_left`
- **Clean build**: `west build -b nice_nano_v2 -- -DSHIELD=sofle_left -pristine`
- **Flash firmware**: `west flash` (after build)
- **GitHub Actions**: Uses ZMK's build-user-config workflow

## Code Style Guidelines
- **File format**: Devicetree (.dts/.dtsi) for keymaps, .conf for config
- **Naming**: Use snake_case for defines (BASE, LOWER, RAISE, ADJUST)
- **Keymap structure**: Layer-based with descriptive display-name comments
- **Bindings**: Use `&kp` for key presses, `&mo` for momentary layers, `&bt` for Bluetooth
- **Comments**: ASCII art layout diagrams above each layer definition
- **License**: MIT SPDX header in all keymap files
- **Imports**: Standard ZMK behaviors and dt-bindings at top of keymap files
- **Conditional layers**: Use `conditional_layers` for complex layer combinations