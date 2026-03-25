# CompAI — Demo Script

**Duration:** ~5–6 minutes  
**Presenter:** Jane Smith, PAS Manager  
**Date:** March 25, 2026

---

## Opening (30 seconds)

> "Good [morning/afternoon], everyone. Today I'm going to walk you through **CompAI** — our AI-powered compensation processing platform built to eliminate the manual effort, errors, and delays that come with processing global compensation data.
>
> CompAI takes raw compensation files in any format, any language — and turns them into validated, payroll-ready outputs using AI. Let me show you how."

---

## Screen 1 — Dashboard (45 seconds)

**[You land here automatically on load]**

> "This is the CompAI dashboard — the manager's single pane of glass."

**Point out as numbers animate in:**

- **Status Cards (top row):** "At a glance, I can see 5 datasets received today, 3 currently in AI review, 2 with missing information the AI needs help with, 8 ready for payroll, and 42 finalized this month."

- **My Pending Actions:** "This section tells me exactly what needs my attention — 3 batches to review, 7 missing-info questions, and 2 pending approvals."

- **Recent Activity Feed:** "A real-time timeline of everything happening — files being uploaded, batches finalized, and SLA warnings."

- **Processing Metrics:** "Down here — 42 batches processed this month, average cycle time is just 2.1 hours versus what used to take days, 98.2% accuracy, and over 16,400 hours saved year-to-date."

> "Let's walk through the full workflow. It starts with uploading data."

**Click "Upload" in the sidebar.**

---

## Screen 2 — Upload (60 seconds)

> "CompAI uses a simple 3-step wizard to ingest compensation data."

### Step 1 — Client & Period

> "First, I select the client — Acme Corporation — and the compensation period, March 2026. The country is auto-detected from the client profile. The system knows this is a German entity, so it will automatically handle German-language headers and formats."

**Click "Continue."**

### Step 2 — Upload Files

> "Next, I upload files. CompAI accepts Excel, CSV, and even PDF. You can see we already have three files here — an Excel workbook with compensation data, a CSV with equity vesting details, and a PDF vendor report."

**[The PDF auto-completes its upload progress bar after ~2.5 seconds]**

> "Notice the PDF upload just completed. CompAI uses AI to extract structured data from PDFs — no manual copy-paste."

**Click "Continue."**

### Step 3 — Confirm & Submit

> "Finally, a confirmation summary. I tick the checkbox and submit."

**Check the checkbox, then click "Submit for Processing."**

**[The modal opens showing each file being processed one by one — the Excel file is parsed and validated, then the CSV is cross-referenced for employee IDs, then the PDF is extracted — a progress bar fills across the bottom. After all 3 files complete, the modal transitions to the success screen with Batch #1044.]**

> "Watch what happens — the AI is processing each file in real time. It reads the Excel compensation data, cross-references employee IDs in the CSV, and extracts structured data from the PDF. All three files validated and mapped."

**Click "Go to Data Review."**

---

## Screen 3 — Data Review & Exceptions (90 seconds)

> "This is where the magic happens. The AI has processed Batch #1041 for Acme Corp."

### Header + AI Confidence Ring

> "Right away, you see the AI Confidence score — 94.2% — shown as a visual ring. This tells me the AI is highly confident in its mapping and validation of this data."

### Stats Row

> "Below that: 847 total records ingested, 824 validated clean, and 23 flagged as exceptions for human review."

### Exception Summary

> "The exception summary breaks these down: 5 critical issues like missing employee IDs and duplicates, 12 warnings for things like an amount that's 34% higher than last month, and 6 informational flags for new employees."

**Click "Exceptions Only" button to filter the table.**

> "I can filter to show just the exceptions."

### Data Table — Walk Through Exceptions

**Scroll through the table and point out:**

1. **Missing Employee ID (Bob Mueller):** "Here's a critical one — Bob Mueller has no Employee ID. The AI couldn't match this record to our master data. Notice the inline link — 'View generated question.' The AI has automatically generated a clarification question, which we'll see in a moment."

2. **Amount Variance (Clara Diaz):** "This is a warning — Clara's salary jumped 34% versus last month. The AI shows me the historical average. I can accept it, edit, or escalate."

   **Click "Accept" to resolve the exception.**

   > "Done — resolved with one click."

3. **Duplicate Record (Alice Weber):** "The AI detected a potential duplicate — same employee, same comp type, same amount."

4. **New Employee (Eva Schneider):** "And informational flags for new employees the AI hasn't seen before."

### AI Schema Mapping Log

**Scroll down to the mapping log.**

> "This is one of the most powerful features. The source file was in **German**. The AI automatically mapped German column headers to our standard schema:
> - 'Brutto Gehalt' → Base Salary (97% confidence)
> - 'Mitarbeiter Nr' → Employee ID (94% confidence)
> - 'Währung' → Currency (99% confidence)
>
> No configuration, no mapping templates. The AI understands the context."

**Click "Mark as Reviewed."**

**[Spinner appears → Toast: "Batch #1041 reviewed — reports generated" → Auto-navigates to Reports]**

---

## Screen 4 — Missing Info Q&A (60 seconds)

> "Before we look at the reports, let me show you how CompAI handles missing information."

**Click "Missing Info" in the sidebar.**

> "Remember Bob Mueller with the missing Employee ID? The AI has automatically generated a question — and it didn't just ask blindly. It searched prior month data and found a 92% name match: 'B. Mueller' from February was in the Finance department, same compensation type and amount."

**Point out the side-by-side comparison table.**

> "The AI is suggesting these are the same person and recommends assigning Employee ID EMP-4525. I simply confirm."

**The first radio option is already selected ("Yes, confirm EMP-4525").**

> "I can also attach supporting documents if needed. And notice the SLA timer counting down — 18 hours remaining. CompAI tracks SLA compliance automatically."

**Point out the progress dots at the bottom: 3 of 7 answered.**

### Send Clarification to HR

> "Now here's the key — once I've worked through the questions, I don't send them one at a time. I click **Send Clarification to HR**."

**Click "Send Clarification to HR" at the bottom.**

**[Summary modal opens with two clear sections:]**
- **Top (green): "Resolved"** — 4 items auto-applied to the batch (3 AI suggestions accepted + 1 manual fix)
- **Bottom (yellow): "Pending"** — 3 questions that only HR can answer

> "CompAI splits this into two groups. The top section — these 4 are already resolved. I confirmed the AI's suggestions and made one manual fix. These get applied to the batch immediately, they don't go to HR. The bottom section — these 3 questions I can't answer myself. Missing department codes, a new hire confirmation, a bonus verification. Only these 3 get sent to HR."

**Point out the button says "Send 3 Questions to HR" — not all 7.**

**Click "Send 3 Questions to HR."**

**[Animated sending sequence: applying 4 resolved items → generating email for 3 pending → sending to HR → Success: "Sent to HR!" with hr-team@acmecorp.com and 24hr SLA]**

> "Done. Four items applied instantly to the batch. Three questions sent to Acme Corp HR with a 24-hour response SLA. When HR responds, CompAI auto-matches their answers back to the batch."

**Click "Back to Data Review."**

---

## Screen 5 — Reports (45 seconds)

**Click "Reports" in the sidebar.**

> "After review, CompAI auto-generates the output reports."

### Control Report

> "The **Control Report** is our internal QA document — total records, validation rate, exceptions resolved, AI confidence score, processing time. This is the audit trail."

### Payroll Instruction Report

> "The **Payroll Instruction Report** is the deliverable to the client's HR team — 847 records, total value €2.85 million, broken down by comp type, payment method, and GL codes. Available as PDF, Excel, or CSV."

### Year-End Report

> "And the Year-End Report is locked until December — it aggregates all monthly data into an annual summary for tax and compliance."

### Submit for Approval

**Click "Submit for Approval."**

**[Spinner → Approval modal: sent to M. Director, PAS Director, 4-hour SLA]**

> "The reports are now with the approver. Once signed off, the batch is finalized and the payroll instructions are ready for delivery."

**Click "Go to Dashboard."**

---

## Closing (30 seconds)

> "So let's recap what CompAI just did:
> 1. **Ingested** raw files in multiple formats, including German-language Excel and PDF
> 2. **Mapped** foreign-language headers to our schema using AI — no manual configuration
> 3. **Validated** 847 records and flagged 23 exceptions with severity and context
> 4. **Generated** smart clarification questions with AI suggestions from historical data
> 5. **Packaged** resolved items and sent remaining questions to the client's HR — one click
> 6. **Produced** payroll-ready reports in under 2 hours — a process that used to take days
>
> This is CompAI — AI-powered compensation processing. Faster, more accurate, and built for global complexity."

---

## Interactive Tips for the Demo

| Action | What Happens |
|---|---|
| Click sidebar nav items | Smooth screen transitions |
| Bell icon (top right) | Opens notification panel — click "Mark all read" to clear |
| Collapse sidebar (☰ hamburger icon) | Sidebar collapses to icon-only mode |
| Drag & drop a file onto Step 2 | Live upload progress bar with animation |
| Click "Exceptions Only" | Table filters to show only flagged rows |
| Click "Accept" on a variance | Row resolves inline with toast notification |
| Check confirm checkbox → Submit | File-by-file processing animation in modal → success screen |
| "Mark as Reviewed" button | Spinner → auto-navigates to Reports |
| "Send Clarification to HR" | Summary modal → animated sending → success with HR email |
| "Save as Draft" on Missing Info | Toast confirming draft saved |
| "Submit for Approval" button | Spinner → approval modal with SLA info |
| Press Escape | Closes any open modal or panel |

---

## Backup Talking Points (if Q&A comes up)

- **"How does the AI handle different languages?"** — It uses contextual NLP to understand column headers, value formats, and currency codes in any language. The schema mapping log shows its reasoning.

- **"What about data security?"** — All processing happens within EY's secure infrastructure. No data leaves the platform. Full audit trail of every AI decision.

- **"How accurate is it?"** — 98.2% accuracy rate across 42 batches this month. Every AI decision has a confidence score and human review is built into the workflow.

- **"Can it handle other countries?"** — Yes. The system supports multi-country, multi-currency, multi-language processing out of the box.

- **"What happens when the AI is wrong?"** — The exception workflow is designed exactly for that. Low-confidence mappings get flagged, humans review and correct, and the AI learns from those corrections over time.
