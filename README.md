# Even Split ✂️ — a webxdc cutting puzzle

A daily precision game for [webxdc](https://webxdc.org) (Delta Chat and other webxdc hosts),
inspired by [Cutle](https://ko-fi.com/cutle).

Each day a geometric shape appears. Make **one straight cut** to divide it into two halves
that are as equal in area as possible. The closer to a perfect **50 : 50** split, the better —
**48 : 52 or better counts as a win**.

## How to play

- **Drag** a straight line across the shape.
- The two halves split apart and the live area ratio is shown.
- You get **one official attempt per day**; afterwards you can keep practicing.
- Your result is **shared automatically** — see the **Daily** and **Overall** leaderboards.
- Only **today's** puzzle is playable; the **‹ ›** arrows let you look back at earlier days (view-only) and their results.
- A fresh puzzle drops every day at **midnight in the chat's chosen timezone**, with a
  countdown to the next one.

### Daily shape (deterministic)

The shape is generated from the UTC day number with a seeded PRNG (`mulberry32`), so **every
member of a group gets the same shape** without any coordination — no shared-config handshake
needed. Shapes include regular polygons, irregular blobs, stars, rectangles, arrows, L-shapes
and crosses (concave shapes are handled correctly by half-plane polygon clipping).
