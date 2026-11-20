# AI Quoting Assistant for CNC & Sheet-Metal Manufacturing

> **Showcase repository.** The product is commercial and the source code is private. This page describes what the system does. Happy to give a live demo on request.

Small and mid-sized machining and sheet-metal shops spend hours per day on the work *around* a quotation: reading e-mails, checking drawings, chasing missing information, typing data into tools and writing the offer. This assistant takes a customer enquiry from the incoming e-mail all the way to a finished, editable quotation.

**Role:** sole developer, designed and built the complete technical product. Business development is handled by a co-founder.
**Status:** working prototype, demonstrated end to end with real enquiries from turning and sheet-metal shops, preparing the first pilot.

## How it works

| Step | What happens |
|---|---|
| 1. Intake | Enquiries arrive by e-mail (IMAP/SMTP, Microsoft Graph, Gmail) |
| 2. Understanding | Reads the request and the attached technical drawings: PDF, scan or photo, DXF (2D), STEP (3D), Excel bills of materials |
| 3. Extraction | Material, dimensions, tolerances, fits, threads, bends, weld seams, plus sheet-metal unfolding for blank size and cut length |
| 4. Gap check | Detects missing information and drafts a follow-up e-mail to the customer |
| 5. Costing | Deterministic costing for turning, milling, laser cutting, bending, welding and punching, with feasibility checks and quantity-scale pricing |
| 6. Output | Quotation as PDF and Excel plus a reply e-mail, sent only after human approval |
| 7. Learning | An experience database calibrates future prices from approved quotations |

## Design principles

**Human-in-the-loop.** Nothing leaves the system without explicit approval, and every value stays editable and traceable.

**Deterministic pricing.** The language model only reads the drawing. All pricing logic runs locally and deterministically, so identical inputs always produce identical quotations.

**Built for trust.** EU hosting, automatic HTTPS, GDPR-compliant data export and deletion, and automatic redaction of drawings before they go to subcontractors.

**Tested.** 826+ automated tests, including determinism and invariant checks.

## Tech stack

Python · FastAPI · React · Anthropic Claude API (vision) · Docker · Caddy · DXF/STEP parsing

## Contact

Interested in a demo or in something similar for your own workflow? Reach me on [LinkedIn](https://www.linkedin.com/in/abdullah-talal-lmu/) or at talalabdullah377@gmail.com.
