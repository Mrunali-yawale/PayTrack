# PayTrack – Phase 1: Acceptance Criteria

## Project Description

PayTrack is an invoice and payment management application designed to help distributors manage invoices, track payments, calculate GST, and automate recurring invoice generation. 
The system focuses on secure tenant isolation, accurate invoice numbering, correct tax calculations, and efficient invoice management.

## Acceptance Criteria

1) Tenant Isolation
- A user belonging to one distributor must not be able to access or view another distributor's invoices.

2) Safe Invoice Numbering
- When 20 invoices are issued simultaneously, they must receive 20 consecutive invoice numbers without gaps or duplicates.

3) Tax Correctness
- GST must be calculated correctly for:
  - Same-state transactions (CGST + SGST).
  - Different-state transactions (IGST).
  - Mixed tax rates.

4) Change Request CR-1 Implementation
- Implement recurring invoices.
- Customers must be able to create a monthly invoice template that automatically generates invoices on a selected day.

5) Client-Specific Requirement – Dental Clinic Chain
- Each invoice must be divided between the insurance company and the patient.
- The system must track invoice amounts, payments, and pending balances separately for both.
- GST must be calculated correctly for each payer's share.
- The combined amounts must match the total invoice amount.


