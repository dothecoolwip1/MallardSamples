# Mallard Environmental Sample Tracker

Standalone repository for the Mallard Environmental sample tracking web app.

## Active application

The production interface is `src/MallardSampleTrackerV3.tsx`.

Current functionality includes automatic classification codes, per-classification sample sequences, reusable sites, separate suspected and confirmed material fields, archive and delete rules, document uploads, layout-aware PDF parsing, OCR fallback, sample history, disposal tracking, and the classification/sample-type catalog.

## Sample numbering

Human-readable sample IDs use `CCC-NNNN`.

Archived samples keep their number reserved. Deleted samples release their sequence for reuse while retaining deletion history.

## Backend

For now this standalone frontend continues to use the existing Supabase project that Mallard previously shared with NorthBorn. All Mallard database migrations are preserved in `supabase/migrations`.

Override the backend with `VITE_SUPABASE_URL` and `VITE_SUPABASE_PUBLISHABLE_KEY`.

## Development

```bash
npm install
npm run dev
npm run test:mallard-documents
npm run build
```

Mallard was separated from the NorthBorn codebase on September 20, 2026.
