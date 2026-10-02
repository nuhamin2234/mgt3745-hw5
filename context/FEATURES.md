# FEATURES.md

The living feature table and the verification record. Copy in from HW3 and extend.

## Features

| Feature | Kano | Status |
| Edit a note | Performance | Delegated to bolt.new (HW5) |


## Acceptance criteria (EARS)

- E1: WHEN the user saves an edited note, THE SYSTEM SHALL update the stored text and show the new text on the page.
- E2: IF the edited text is empty, THEN THE SYSTEM SHALL reject it with a reason and keep the old text.
- E3: IF the note does not exist, THEN THE SYSTEM SHALL respond 404 with a reason.
- E4: IF the server cannot be reached while saving an edit, THEN THE SYSTEM SHALL show an error on the page and keep the original text.
- E5: THE SYSTEM SHALL return the edited text from GET /entries on any device.

## Verification

Walk every statement against the deployed page. PASS, FAIL, CANNOT TEST YET, or DEFERRED, with a reason.

| Statement | HW3 verdict | HW4 verdict | Reason |
|---|---|---|---|
| Return entries in order | PASS | *?* | |
| Store valid entry | PASS | *?* | |
| Reject missing text | *?* | *?* | |
| Survive cleared cache | CANNOT TEST YET | *?* | *now testable* |
| Server unreachable | | *?* | *how would you simulate an outage?* |
| Server returns 500 | | *?* | |
| Second client writes to the same table | | *?* | *DEFERRED if ADR-002 says so* |
