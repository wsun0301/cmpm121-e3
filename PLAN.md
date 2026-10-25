## Exploration Status

### Alternative A — Geometry

**Status: Explored**

Implemented 120 SVG circles as freckles on branch `A`. The repeated shapes add texture to the character while preserving the original facial features and Spin interaction.

### Alternative B — Image Assets

**Status: Explored**

Implemented a hat and sunglasses using two separate SVG image assets on branch `B`. This alternative gives the character a different personality while demonstrating how image assets can be incorporated into an SVG portrait.

### Alternative C — Color and Curves

**Status: Explored**

Implemented a colorful linear gradient and a curved smile using a quadratic Bézier path on branch `C`. This alternative creates a happier expression through changes to color and geometry.

## Comparison

- **A:** Adds visual detail using repeated geometric shapes.
- **B:** Changes the character's personality using image assets.
- **C:** Changes the character's expression using gradients and curves.

All three alternatives have been implemented and explored independently. The final selection will be recorded after rebasing the chosen branch onto the updated main branch.

## Final Decision

**Selected Alternative: C — Color and Curves**

I chose Alternative C because the gradient and Bézier smile create a more expressive character while keeping the design simple. Alternative A demonstrated repeated geometry, and Alternative B explored image assets, but C provides the clearest improvement to the character's expression.

I rebased branch C onto main after extracting `buildFace()`. This preserved both the refactoring and the chosen design. I then fast-forwarded main to integrate the alternative without creating a merge commit.
