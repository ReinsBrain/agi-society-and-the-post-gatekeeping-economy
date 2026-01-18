<!-- Standalone parity test for break-before: left/right on GitHub Pages -->

<style>
/* Keep the theme wrapper from adding noise */
.markdown-body > h1:first-of-type { display: none !important; }

/* Hide AnchorJS injected links if the theme loads it */
.anchorjs-link { display: none !important; }

/* Make our invisible break markers behave like real block-level breakpoints */
.pb {
  display: block;
  height: 0;
}

@media print {
  /* Make each section consume exactly one printed page (approximately).
     The goal is to force page boundaries so left/right parity is the only variable. */
  .page {
    break-after: page;
    page-break-after: always;
    /* Using a physical unit tends to be more stable than vh in print engines. */
    min-height: 9.5in;
    padding-top: 0.5in;
  }

  .pb-right { break-before: right !important; page-break-before: right !important; }
  .pb-left  { break-before: left  !important; page-break-before: left  !important; }

  /* Visual debugging: keep headings together with the first paragraph */
  h2 { break-after: avoid-page; }
}
</style>

# Parity break test (left/right)

This page is designed to answer one question:

> Does the print engine honor `break-before: left/right` by inserting a *blank page* when needed?

The test uses a sequence where **two consecutive sections request the same side**. If parity is honored, the engine must sometimes insert a blank page to land on the requested side.

Print this page (Chrome print preview is fine) and look at the thumbnails:

- Each “Section N” should start on the requested side (RIGHT/LEFT).
- If you see two consecutive “RIGHT requested” sections starting on opposite sides with **no blank page** inserted between them, parity isn’t being enforced.

---

<a id="s1" class="pb pb-right"></a>

## Section 1 — REQUEST: RIGHT (should be page 1)

If this is not on the first (right/recto) page, something is already off.

<div class="page"></div>

<a id="s2" class="pb pb-right"></a>

## Section 2 — REQUEST: RIGHT again (should force a blank page if parity is enforced)

If the engine is honoring parity, it cannot start this section on the immediately next page (which would normally be LEFT). It must advance to a RIGHT page, usually by inserting a blank.

<div class="page"></div>

<a id="s3" class="pb pb-left"></a>

## Section 3 — REQUEST: LEFT (should naturally follow)

After a RIGHT page, the next page is typically LEFT, so this one may not require any blank insertion.

<div class="page"></div>

<a id="s4" class="pb pb-left"></a>

## Section 4 — REQUEST: LEFT again (should force a blank page if parity is enforced)

If parity is honored, the engine must skip over a RIGHT page to land on LEFT again.

<div class="page"></div>

<a id="s5" class="pb pb-right"></a>

## Section 5 — REQUEST: RIGHT (control)

One more RIGHT request to see if behavior is consistent.

<div class="page"></div>
