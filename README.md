# Mac Launcher Template

README ja: [README_ja.md](README_ja.md)

## What is this?

This is a template for making a launcher that can start your application by just "right-clicking -> open" with only binaries and assets in a folder when providing a self-made application on Mac.

The following is what `launcher` does.

- Set the directory where `launcher` is located as the working directory (`cd "$(dirname "$0")"`)
- Make downloaded assets available (`xattr -cr .`)
- Determine whether it is M1/M2/M3 or Intel and start the appropriate binary.
  - For Intel, start `binary_x64`
  - For M1/M2/M3, start `binary_arm64`

## How to use

- Place the Intel binary `binary_x64` and the M1/M2/M3 binary `binary_arm64` in the folder.
  - If you don't need to separate Intel/ARM, place the same content in two binaries.
  - The same applies if you only have the Intel version.
- Place assets and other necessary files in the folder as needed.
- Rename `launcher` to your favorite.
- Compress the folder and provide it.