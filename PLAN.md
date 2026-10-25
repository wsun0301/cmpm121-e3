# E3: Feature Branches — Portrait Plan

## Starting Point

The starter project contains a neutral SVG face with two eyes, a nose, and a straight mouth. The Spin button rotates the portrait.

The goal is to explore three different visual designs using separate Git branches, then select one to integrate into `main`.

## Initial Plan

### Alternative A — Geometry

**Branch:** `A`

I plan to add at least 100 small geometric shapes to the character's face. My idea is to use 120 small circles as freckles to give the portrait a textured appearance.

This alternative explores how repeated SVG shapes can create visual details without using external images.

### Alternative B — Image Assets

**Branch:** `B`

I plan to use at least two separate image assets to customize the character. My idea is to add a hat and sunglasses.

This alternative explores how external SVG image assets can be combined with an existing portrait to create a different personality.

### Alternative C — Color and Curves

**Branch:** `C`

I plan to replace the original face color with an SVG linear gradient and change the straight mouth into a curved smile using a quadratic Bézier curve.

This alternative explores how color and curves can change the character's expression.

---

## Exploration Status

### Alternative A — Geometry

**Status: Explored**

I implemented 120 SVG circles using nested loops (10 rows and 12 columns). The circles create freckles across the character's face.

This version adds visual texture while keeping the original facial features and Spin functionality.

### Alternative B — Image Assets

**Status: Explored**

I created two separate SVG image assets:

- `hat.svg` — a blue baseball-style hat.
- `sunglasses.svg` — dark sunglasses.

Both assets are displayed using SVG image elements. This version changes the character's personality while preserving the original face and Spin functionality.

### Alternative C — Color and Curves

**Status: Explored**

I implemented a linear gradient transitioning from pink to gold.

I also replaced the straight mouth with a quadratic Bézier curve to create a smiling expression.

This version makes the character look happier while maintaining the original functionality.

---

## Comparison of Alternatives

| Alternative          | Strengths                                  | Limitations                               |
| -------------------- | ------------------------------------------ | ----------------------------------------- |
| A — Geometry         | Adds detail using simple SVG shapes        | The freckles make the face visually busy  |
| B — Image Assets     | Gives the character a distinct personality | Requires additional asset files           |
| C — Color and Curves | Simple, expressive, and visually appealing | Less detailed than the other alternatives |

All three alternatives were developed independently on their own branches.

---

## Refactoring

Before integrating the selected alternative, I refactored the neutral portrait on `main` by extracting the drawing logic into a function called `buildFace()`.

This separated the SVG construction from the application setup and Spin button logic without changing the original portrait's appearance or behavior.

## Final Decision

**Selected Alternative: C — Color and Curves**

I chose Alternative C because the gradient and Bézier smile create a more expressive character while keeping the implementation simple.

Alternative A demonstrated repeated geometry, and Alternative B demonstrated the use of image assets. However, I think Alternative C provides the clearest improvement to the character's appearance without introducing unnecessary complexity.

### Integration Process

I rebased branch `C` onto the updated `main` branch after the `buildFace()` refactoring.

During the rebase, I resolved a conflict in `src/main.ts` by preserving the extracted function and incorporating the gradient and Bézier smile inside it.

After completing the rebase, I fast-forwarded `main` to branch `C`, preserving both the refactoring and the selected visual design.

The final portrait contains the gradient and curved smile, while the Spin button continues to work. Branches `A` and `B` remain available as separate alternatives.
