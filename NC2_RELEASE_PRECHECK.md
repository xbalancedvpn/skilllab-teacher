# SkillLab CSS NC II Readiness — Release Precheck

Date: 2026-09-29

## Scope
Student branch: `nc2-readiness-v1`
Teacher branch: `nc2-readiness-v1`

## Rollback anchors
- Student main before NC II merge: `b8c19f39e2c23464c32a89e36a01e811a1ffc602`
- Teacher main before NC II merge: `0c87f2f405fc66a46d22a8525859e6990722cd9d`
- Student NC II head: `77c7fd6a82df8125482f10433e36e230a663b8f9`
- Teacher NC II head at initial precheck: `9fb4741a2fdba9d2ce911ad74c882ce16d446255`

## Backend changes
- `nc2_readiness_progress`: RLS enabled; student self select/insert/update; teacher owner select.
- `nc2_mock_attempts`: RLS enabled; student self select/insert; teacher owner select.
- Anonymous access to both NC II tables is blocked.
- Class and user foreign keys use ON DELETE CASCADE.
- Mock component score constraints corrected to 0–100 for both oral and procedure percentage fields.
- `skilllab-teacher-manage` Edge Function: version 6; test-data purge includes readiness + mock rows.

## Preflight results
### Code integrity
- Student JavaScript syntax: PASS
- Teacher JavaScript syntax: PASS
- PR mergeability: PASS for both draft PRs
- Static selector audit: no missing queried static IDs
- Existing 10-simulator bank retained

### Mobile / responsive
- COC cards collapse responsively.
- Training stages use auto-fit responsive layout.
- Cable drill: 8 → 4 → 2 column adaptation.
- IP configuration collapses to single column.
- Drill action grid collapses to one column on narrow screens.
- Tables remain horizontally scrollable.

### Failure handling
- Student startup recovery screen added.
- Student online/offline indicator added.
- Readiness progress remains in localStorage and retries Supabase sync when connectivity returns.
- Mock result receives a client-generated UUID, is kept locally on failed save, and retries after reconnection.
- Teacher online/offline indicator added and live dashboard refresh resumes when connectivity returns.

## Known platform advisory
Supabase Auth leaked-password protection is currently disabled. This is a security hardening recommendation and not a blocker for NC II readiness functionality.

## Environment validation status
The existing Vercel `skilllab-ph` preview deployments contain the older Cloud MVP, not the NC II Student/Teacher branch builds.

The current connected deployment tools do not expose a safe file-to-preview deployment action for these two branch-only single-file apps. Therefore visual browser validation of the actual NC II branch build remains pending until a real staging URL is available.

Do not merge to production solely to obtain a staging URL.
