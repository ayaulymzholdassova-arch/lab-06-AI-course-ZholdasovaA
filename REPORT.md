# REPORT — what the measurement showed, who it affects, and whose responsibility it is
# REPORT

## 1. What I measured

I tested the AI agent using different control mechanisms. I compared its performance before and after applying the controls. I measured correct answers, incorrect answers, refusals, and the agent's ability to handle risky requests.

## 2. Who is affected

The system can affect users who rely on AI-generated information and people whose data may be processed by the agent. Incorrect answers or unsafe decisions can negatively affect users. Therefore, the system must be reliable, transparent, and safe.

## 3. What I am responsible for

I am responsible for testing the system, checking its outputs, identifying possible risks, and applying appropriate safety controls. I must ensure that the agent refuses unsafe requests and protects user information.

## 1. Measurement read-out

(Dimension: Evidence of Specific Impact.)

Guiding questions:

- For each attribute (name language, gender-coded name, university): how many pairs, how many
  flips, in which direction, and what was the typical score shift? Are these counts and magnitudes,
  or a description of them?
- Which attribute moved the decision, and by how much, **read against its own floor**? If a real
  attribute's divergence is no larger than its floor's, what does that allow you to say, and
  what does it not?
- How much of the divergence could be noise? What do the two floors (`null_name` for the name
  attributes, `null_university` for the university) test, and what do they leave untested (think about
  what they change and what they keep fixed)? What would a stronger estimate require?
- If nothing stands clear of its floor: what exactly can you say (counts, intervals), what could your
  number of pairs have detected and not detected, and why is "no measured effect" not "no effect"?
- Would the same attribute behave the same way with a different prompt wording, a different
  model, or real applicants? Say what your run can and cannot support.

## 2. Who is affected

(Dimension: Affected Parties and the Consequences They Bear.)

Guiding questions:

- On each side of a **wrong** decision, who is it? Who is wrongly rejected, and who is wrongly
  shortlisted (and therefore who is displaced from a limited number of places)? Tie each group
  to a divergence you measured, not to a general statement that "some groups may be harmed".
- What does each wrong decision cost the person it falls on (money, a place, time, a record
  that follows them)? Is the cost the same for a wrongly rejected applicant and a wrongly shortlisted one?
- Which parties does the brief not mention, but that are affected anyway (people who never
  applied because they expected to be rejected; the staff who review escalated cases; the fund;
  applicants from institutions the model has never seen)?
- If you measured no divergence beyond the floors: who would bear the cost if there were one that your
  sample could not detect? Tie that to what your number of pairs could and could not see.
- Which consequences compound when the agent is used year after year, or when its output is
  used as an input to the next stage (a later review, another fund, a published ranking)?

## 3. Professional responsibility

(Dimension: Recognition of Professional Responsibility.)

Guiding questions:

- Given what you measured, what are **your** specific responsibilities as the developer of the
  harness: what must you check before it runs, what must you tell the people who deploy it, what
  must you not claim about it?
- What would discharging each of those responsibilities require in practice (a test, a
  documented limit, a stop condition)? What have you actually done in this lab, and what is left?
- Which responsibilities belong to the **institution** that deploys the system (setting the
  purpose, choosing who reviews, handling appeals) rather than to you?
- Where do the two conflict? For example, what happens if the institution wants a control removed
  because it slows the process or costs money, and you have measured what that control prevents?
