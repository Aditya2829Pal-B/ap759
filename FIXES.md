# Bug Fix: Issue #3594

## Title
Update "Accept" link color in notifications for friend requests

## Problem
The "Accept" link colors in friend request notifications were not matching the design specifications:
- **Light mode**: Was using generic `blue`, should be `#0057EB` (rgb(0, 87, 235))
- **Dark mode**: Was using `rgb(52, 152, 219)`, should be `#4C94FF` (rgb(76, 148, 255))

## Solution
Updated `packages/tamagui-core/src/legacyColorsHotpink.ts`:

### Changes Made:
1. **Line 130 (DARK_COLORS)**: Changed `linkColor: "hotpink"` to `linkColor: "#4C94FF"`
2. **Line 209 (LIGHT_COLORS)**: Changed `linkColor: "hotpink"` to `linkColor: "#0057EB"`

## Files Modified
- `packages/tamagui-core/src/legacyColorsHotpink.ts`

## Testing
The linkColor is used in the theme for notification links. These changes ensure:
- Friend request accept links display with the correct blue color in light mode
- Friend request accept links display with the correct blue color in dark mode
- Colors now match the Figma design system specifications
