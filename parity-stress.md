<!-- Stress test: many consecutive RIGHT requests to see if Chrome suppresses parity blank insertion in long documents -->

<style>
.markdown-body > h1:first-of-type { display: none !important; }
.anchorjs-link { display: none !important; }

.pb { display: block; height: 0; }

@media print {
  /* Force a predictable baseline: each section consumes ~one page. */
  .page {
    break-after: page;
    page-break-after: always;
    min-height: 9.5in;
    padding-top: 0.5in;
  }

  .pb-right { break-before: right !important; page-break-before: right !important; }
  /* (Optional) if you want to compare, swap some to left later. */

  /* Keep headings with the first paragraph */
  h2 { break-after: avoid-page; }
}
</style>

# Parity stress test (RIGHT, repeated)

Goal: detect whether Chrome *eventually stops* inserting blank pages to satisfy `break-before: right` when it would otherwise create lots of blanks.

Expected outcomes:

- **If parity is enforced consistently:** sections land on pages 2,4,6,… and the odd pages between are blank.
- **If Chrome suppresses parity in long docs:** at some point sections will start appearing on consecutive pages (or the blank pages stop).

---

<a id="s01" class="pb pb-right"></a>

## Section 01 — REQUEST: RIGHT

<div class="page"></div>

<a id="s02" class="pb pb-right"></a>

## Section 02 — REQUEST: RIGHT

<div class="page"></div>

<a id="s03" class="pb pb-right"></a>

## Section 03 — REQUEST: RIGHT

<div class="page"></div>

<a id="s04" class="pb pb-right"></a>

## Section 04 — REQUEST: RIGHT

<div class="page"></div>

<a id="s05" class="pb pb-right"></a>

## Section 05 — REQUEST: RIGHT

<div class="page"></div>

<a id="s06" class="pb pb-right"></a>

## Section 06 — REQUEST: RIGHT

<div class="page"></div>

<a id="s07" class="pb pb-right"></a>

## Section 07 — REQUEST: RIGHT

<div class="page"></div>

<a id="s08" class="pb pb-right"></a>

## Section 08 — REQUEST: RIGHT

<div class="page"></div>

<a id="s09" class="pb pb-right"></a>

## Section 09 — REQUEST: RIGHT

<div class="page"></div>

<a id="s10" class="pb pb-right"></a>

## Section 10 — REQUEST: RIGHT

<div class="page"></div>

<a id="s11" class="pb pb-right"></a>

## Section 11 — REQUEST: RIGHT

<div class="page"></div>

<a id="s12" class="pb pb-right"></a>

## Section 12 — REQUEST: RIGHT

<div class="page"></div>

<a id="s13" class="pb pb-right"></a>

## Section 13 — REQUEST: RIGHT

<div class="page"></div>

<a id="s14" class="pb pb-right"></a>

## Section 14 — REQUEST: RIGHT

<div class="page"></div>

<a id="s15" class="pb pb-right"></a>

## Section 15 — REQUEST: RIGHT

<div class="page"></div>

<a id="s16" class="pb pb-right"></a>

## Section 16 — REQUEST: RIGHT

<div class="page"></div>

<a id="s17" class="pb pb-right"></a>

## Section 17 — REQUEST: RIGHT

<div class="page"></div>

<a id="s18" class="pb pb-right"></a>

## Section 18 — REQUEST: RIGHT

<div class="page"></div>

<a id="s19" class="pb pb-right"></a>

## Section 19 — REQUEST: RIGHT

<div class="page"></div>

<a id="s20" class="pb pb-right"></a>

## Section 20 — REQUEST: RIGHT

<div class="page"></div>

<a id="s21" class="pb pb-right"></a>

## Section 21 — REQUEST: RIGHT

<div class="page"></div>

<a id="s22" class="pb pb-right"></a>

## Section 22 — REQUEST: RIGHT

<div class="page"></div>

<a id="s23" class="pb pb-right"></a>

## Section 23 — REQUEST: RIGHT

<div class="page"></div>

<a id="s24" class="pb pb-right"></a>

## Section 24 — REQUEST: RIGHT

<div class="page"></div>

<a id="s25" class="pb pb-right"></a>

## Section 25 — REQUEST: RIGHT

<div class="page"></div>

<a id="s26" class="pb pb-right"></a>

## Section 26 — REQUEST: RIGHT

<div class="page"></div>

<a id="s27" class="pb pb-right"></a>

## Section 27 — REQUEST: RIGHT

<div class="page"></div>

<a id="s28" class="pb pb-right"></a>

## Section 28 — REQUEST: RIGHT

<div class="page"></div>

<a id="s29" class="pb pb-right"></a>

## Section 29 — REQUEST: RIGHT

<div class="page"></div>

<a id="s30" class="pb pb-right"></a>

## Section 30 — REQUEST: RIGHT

<div class="page"></div>

<a id="s31" class="pb pb-right"></a>

## Section 31 — REQUEST: RIGHT

<div class="page"></div>

<a id="s32" class="pb pb-right"></a>

## Section 32 — REQUEST: RIGHT

<div class="page"></div>

<a id="s33" class="pb pb-right"></a>

## Section 33 — REQUEST: RIGHT

<div class="page"></div>

<a id="s34" class="pb pb-right"></a>

## Section 34 — REQUEST: RIGHT

<div class="page"></div>

<a id="s35" class="pb pb-right"></a>

## Section 35 — REQUEST: RIGHT

<div class="page"></div>

<a id="s36" class="pb pb-right"></a>

## Section 36 — REQUEST: RIGHT

<div class="page"></div>

<a id="s37" class="pb pb-right"></a>

## Section 37 — REQUEST: RIGHT

<div class="page"></div>

<a id="s38" class="pb pb-right"></a>

## Section 38 — REQUEST: RIGHT

<div class="page"></div>

<a id="s39" class="pb pb-right"></a>

## Section 39 — REQUEST: RIGHT

<div class="page"></div>

<a id="s40" class="pb pb-right"></a>

## Section 40 — REQUEST: RIGHT

<div class="page"></div>
