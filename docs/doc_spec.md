# Relay: Product Spec v0.1 (Draft)

## Target first user
Organizers of recurring student-organization events/workshops, subject to user discovery.

## Problem hypothesis
Organizers coordinate task staffing via spreadsheets and chat. Preference-based assignment and replacement when participants fail to acknowledge a task may require manual follow-ups.

## Proposed workflow
1. Organizer creates an event with tasks, staffing capacity, and qualification constraints.
2. Members submit availability and ranked task preferences.
3. Organizer previews allocation and approves it.
4. Assigned members acknowledge or decline by a specified deadline.
5. Unacknowledged tasks surface for reassignment, using eligible backups or organizer intervention.
6. Audit log explains changes; no automatic punitive score in MVP.

## MVP non-goals
- Automatic performance scoring / penalties
- Payroll, legal shift scheduling, workforce compliance
- ML prediction of no-shows
- Multi-region distributed deployment

## Key invariants to design and test
- Assignment count cannot exceed task capacity.
- No member receives overlapping assignments without explicit allowance.
- An assignment cannot be simultaneously accepted and reassigned.
- A retry of the same confirmed action does not create duplicate assignments.
- Every reassignment has a traceable reason.

## Validation questions
- What was the last event where reassignment happened? How was it handled?
- How are preferences collected today? What breaks in the current workflow?
- Do coordinators want auto-assignment, or preview/approval first?
- Are deadlines about task completion or confirming ownership?
- How much time would a better process actually save?
