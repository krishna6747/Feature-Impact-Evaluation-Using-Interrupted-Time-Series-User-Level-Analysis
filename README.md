# Feature-Impact-Evaluation-Using-Interrupted-Time-Series-User-Level-Analysis

This project simulates a real-world product analytics case where no A/B test was available. It demonstrates how causal inference techniques can still be applied to estimate feature impact

**Project Overview**

This project evaluates the business impact of Feature A, launched in July 2022, using observational data (no randomized experiment available).

We investigate whether Feature A improved:

- MAU (Monthly Active Users) – breadth of engagement

- PAU (Primary Account Users) – depth of engagement

The analysis combines macro time-series modeling with user-level behavioral methods to estimate causal impact.

**Business Question**

Did Feature A meaningfully improve user engagement?

If yes:

Did it increase overall activity (MAU)?

Or did it deepen engagement (PAU)?

Is adoption the real bottleneck?

**Methods Used**

**1️. Interrupted Time Series (ITS)**

Used to estimate:

Immediate post-launch level change

Post-launch slope change

Structural pre-trends

Robust standard errors (HAC) were used to handle autocorrelation.


**2️. Event Study Around First Adoption**

Measured user behavior:

6 months before adoption

6 months after adoption

To check:

Pre-trend validity

Timing alignment

Engagement shift at adoption.

**3️. Within-User (Fixed Effects–Style) Regression**

Compared each user to themselves:

PAU_demeaned ~ feature_A_demeaned

Clustered standard errors by user.

This isolates behavioral change rather than cross-user differences.

**4. Cohort & Retention Analysis**

Measured:

Adoption rate

Month-1 retention

12-month retention

Habit formation

**5️. Rolling Engagement Metrics**

Built 3-month rolling MAU to avoid noisy one-month spikes.

**Key Findings**

- Adoption

Stabilized at 5–6%

Limited macro penetration

-  MAU (Breadth)

No statistically significant impact

Pre-existing downward trend continued

- PAU (Depth)

+0.6pp immediate macro uplift (ITS)

+7.7pp within-user uplift

Users 4.4× more likely to become PAU after adopting Feature A.

- Retention

82% Month-1 retention

67% retention after 12+ months

Strong habit formation.

**Interpretation**

Feature A:

Does NOT increase how many people are active

DOES increase how deeply users engage

Is high-quality but under-distributed

The constraint is adoption, not product strength.

**Recommendation**

Shift focus from improving the feature → to increasing adoption.

Given strong retention and engagement uplift, even modest adoption gains could meaningfully improve business health.
