# SkillLab CSS NC II — Acceptance Test Checklist

Use a disposable Test / Sample student account where possible.

## A. Student account and class entry
- [ ] Student sign-in loads without console/page error.
- [ ] Valid class code joins the correct class.
- [ ] Invalid/paused class gives a clear error.
- [ ] Existing simulator progress is still visible.

## B. COC unlock chain
- [ ] COC 1 is initially available.
- [ ] COC 2 stays locked until COC 1 Learn + passing Practice + Procedure Drill are complete.
- [ ] COC 3 stays locked until COC 2 is complete.
- [ ] COC 4 stays locked until COC 3 is complete.
- [ ] Mock Assessment stays locked until 4/4 digital preparation AND 10/10 simulator bank are complete.

## C. COC 1
- [ ] Learn displays all five COC 1 elements.
- [ ] Practice questions and choices are randomized.
- [ ] Practice below class pass score does not unlock Procedure Drill.
- [ ] Procedure Drill resets after an incorrect sequence.
- [ ] Completion syncs to Teacher Dashboard within about 5 seconds.

## D. COC 2
- [ ] Learn content loads.
- [ ] Practice target works.
- [ ] T568A/T568B standard is randomized.
- [ ] Wrong cable pin resets the cable drill.
- [ ] IP configuration accepts the intended /24 configuration only.
- [ ] Connectivity validation sequence resets on wrong order.
- [ ] Mobile cable grid remains usable in portrait view.

## E. COC 3
- [ ] User Access Drill uses least-privilege decisions.
- [ ] Wrong access policy restarts the drill.
- [ ] Server-service role matching works.
- [ ] Pre-deployment workflow resets on wrong order.
- [ ] COC 3 completion syncs to Teacher Dashboard.

## F. COC 4
- [ ] Maintenance scenarios use service-order / preventive-maintenance logic.
- [ ] Fault Isolation uses evidence before diagnosis.
- [ ] Wrong unrelated diagnosis/correction restarts the case set.
- [ ] Existing No Display / No Boot / Overheating / Slow Storage simulations remain usable.

## G. Simulator anti-gaming
- [ ] Diagnosis/repair cannot be submitted without the minimum evidence requirement.
- [ ] Rapid-guess behavior is flagged when applicable.
- [ ] Unnecessary checks reduce efficiency.
- [ ] Evidence score is stored on attempts.
- [ ] Passing score still follows the selected class setting.

## H. Mock Assessment
- [ ] Unlock rule requires 4/4 digital prep + 10/10 simulators.
- [ ] Oral/knowledge stage gives no answer explanation while running.
- [ ] Procedure stage gives no hint while running.
- [ ] At least one procedure item from each COC is included.
- [ ] Overall score uses 40% oral + 60% procedure.
- [ ] Oral and procedure percentages can save values up to 100.
- [ ] Per-COC breakdown is stored.
- [ ] Result appears in Teacher Dashboard within about 5 seconds.
- [ ] Mock history is visible in Student and Teacher views.

## I. Cross-device / network behavior
- [ ] Complete one NC II stage on Device A.
- [ ] Sign in on Device B and confirm Supabase-restored progress.
- [ ] Turn internet off, complete a readiness stage, then reconnect and confirm sync.
- [ ] If feasible, finish a mock during a forced save failure and confirm it retries after reconnection.
- [ ] Teacher dashboard displays Offline when disconnected and resumes live refresh after reconnect.

## J. Teacher dashboard
- [ ] COC 1–4 readiness percentages match Student progress.
- [ ] Student with readiness progress but zero simulator attempts still appears correctly.
- [ ] Mock summary shows best/latest/oral/procedure/attempt count.
- [ ] Remediation Intelligence gives an evidence-based priority.
- [ ] Class Intervention Groups group students by current top weakness.
- [ ] Clicking View Profile opens the correct student.
- [ ] Student Intervention Profile shows readiness, simulator history, anti-guess data, mock history and top interventions.
- [ ] Manage Student from the profile opens that same student.

## K. Reports / exports
- [ ] Main CSV includes NC II readiness + mock + remediation columns.
- [ ] Intervention Group CSV downloads correctly.
- [ ] Student Intervention CSV downloads correctly.
- [ ] Printable Class Report includes readiness, intervention groups, remediation and mock summary.
- [ ] Print / Save PDF layout is readable.

## L. Reset / delete
- [ ] Reset one simulator removes only that simulator’s attempts/sessions/feedback.
- [ ] Resetting one simulator does not erase COC readiness unless intentionally designed to do so.
- [ ] Delete Test / Sample Data removes simulator data, readiness rows, mock attempts and class membership.
- [ ] Deleting a class cascades its NC II readiness/mock data.
- [ ] Login account is retained after Test / Sample data deletion.

## M. Final release gate
- [ ] No blocker bugs.
- [ ] No blank/frozen screens.
- [ ] No unintended data loss.
- [ ] Student and Teacher pages work on mobile.
- [ ] Existing live 10-simulator behavior remains compatible.
- [ ] Both PRs remain mergeable.
- [ ] Production rollback SHAs are recorded before merge.

Record every failure as: **screen / action / expected / actual / screenshot if possible**.
