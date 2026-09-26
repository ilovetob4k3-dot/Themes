# Themes

Client-specific repairs and adaptations of themes that do not behave correctly on newer clients.

## Sakura Path Cat

- `Original/Sakura-Path-Cat-Animated-Theme-L.json` — untouched Vendetta/spec-2 source theme.
- `ShiggyCord/Sakura-Path-Cat-Light.json` — converted to ShiggyCord's native color theme spec 3.
- `ShiggyCord/Sakura-Path-Cat-Light-compat.json` — compatibility build based on spec 2, with both light/dark slots populated plus modern Discord semantic aliases. This is the closer-match test build for current ShiggyCord.
- `ShiggyCord/Sakura-Path-Cat-Light-font.json` — the original theme's fonts split into ShiggyCord's separate font spec.

### Why the ShiggyCord version differs

The original spec-2 file stores semantic colors as one-element arrays. ShiggyCord treats spec-2 semantic arrays as dark/light slots, which can make the palette disappear when the light slot is selected. The ShiggyCord copy declares itself as a native light theme and stores each semantic value directly.

The animated background was moved to `main.background` and its old `alpha` value was converted to `opacity`.

The original `plus.iconpack` entry is not copied into the color manifest because ShiggyCord's current color-theme spec does not define an icon-pack field.

### Installation note

ShiggyCord installs themes/fonts by fetching their URLs. A private GitHub repository is not anonymously fetchable, so the raw URLs from this repository will only be usable directly by ShiggyCord if the files are hosted at a publicly accessible URL (for example, if the repository is made public).


### Current ShiggyCord compatibility test

The creator screenshots were made against an older Discord/Revenge-style token set. Current Discord uses newer semantic names for many surfaces, text roles, selected rows, controls, and mobile UI. The compat build keeps the original palette but adds aliases for those newer token names while retaining spec-2 behavior in ShiggyCord.
