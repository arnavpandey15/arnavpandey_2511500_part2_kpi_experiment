# Hypothesis Test Notes

## Experiment Objective

The objective of this experiment is to determine whether the new onboarding and activation campaign (Treatment) improves business performance compared to the existing onboarding experience (Control).

The business decision is whether the Treatment experience should be rolled out to all users.

---

## Primary Metric Being Tested

**Paid Conversion Rate**

Paid Conversion Rate = Number of Users Converted to Paid ÷ Total Users

This metric is selected because the primary goal of the onboarding campaign is to increase the number of users who become paying subscribers.

---

## Null Hypothesis (H₀)

The new onboarding campaign does not improve paid conversion rate.

**H₀:** p(Treatment) ≤ p(Control)

Where:

- p(Treatment) = Paid conversion rate in the Treatment group
- p(Control) = Paid conversion rate in the Control group

---

## Alternative Hypothesis (H₁)

The new onboarding campaign increases paid conversion rate.

**H₁:** p(Treatment) > p(Control)

---

## Test Type

### One-Tailed Hypothesis Test

A one-tailed test is appropriate because the business objective is specifically to determine whether the Treatment performs better than the Control, not merely whether it performs differently.

---

## Significance Level

### α = 0.05 (5%)

Decision Rule:

- If p-value < 0.05 → Reject H₀
- If p-value ≥ 0.05 → Fail to Reject H₀

A 5% significance level is commonly used in business experimentation and provides a balance between false positives and false negatives.

---

## Reason for Choosing Paid Conversion Rate

Paid Conversion Rate was selected because:

1. It directly measures the campaign's primary business objective.
2. It has a direct impact on subscription revenue.
3. It is the company's North Star Metric for this experiment.
4. Improvements in conversion directly contribute to business growth.
5. Leadership's rollout decision is primarily based on whether more users become paying customers.

Supporting metrics such as engagement score, trial start rate, onboarding completion rate, revenue per user, and refund rate provide additional context but are not the primary decision metric.

---

## Interpretation Logic

### Scenario 1: Reject H₀

If:

- Treatment conversion rate > Control conversion rate
- p-value < 0.05

Then:

- There is statistically significant evidence that the new onboarding campaign improves paid conversion.
- The business should consider rolling out the Treatment experience, subject to guardrail metric review.

### Scenario 2: Fail to Reject H₀

If:

- p-value ≥ 0.05

Then:

- There is insufficient evidence that the Treatment improves conversion.
- The business should retain the existing onboarding experience or conduct further testing.

---

## Guardrail Considerations

Even if the primary hypothesis is successful, the rollout decision should also consider:

- Refund Rate
- Support Ticket Rate
- Customer Complaints
- Engagement Score
- Revenue per User

A statistically significant increase in conversion should not be accepted if it creates unacceptable negative impacts on user experience or operational costs.

---

## Business Decision Framework

The Treatment should be recommended for rollout if:

1. Paid Conversion Rate shows a statistically significant improvement.
2. Revenue metrics improve or remain stable.
3. Guardrail metrics remain within acceptable limits.
4. Results are consistent across major user segments (Region, Device Type, and Traffic Source).

Otherwise, additional experimentation or campaign refinement should be performed before full deployment.


---


# Task 7: A/B Test Analysis

## Test Objective

Determine whether the Treatment onboarding experience produces a statistically significant improvement in Paid Conversion Rate compared to the Control experience.

---

## Test Inputs

### Control Group

- Users: 693
- Paid Conversions: 22
- Conversion Rate: 3.17%

### Treatment Group

- Users: 715
- Paid Conversions: 50
- Conversion Rate: 6.99%

### Absolute Lift

6.99% - 3.17% = 3.82 percentage points

### Relative Lift

(6.99% - 3.17%) / 3.17% = 120.5%

The Treatment group achieved approximately 121% higher conversion than the Control group.

---

## Statistical Test Used

### Two-Proportion Z-Test

This test is appropriate because:

- The primary metric (Paid Conversion Rate) is binary.
- Users either convert (1) or do not convert (0).
- The goal is to compare conversion rates between two independent groups.

---

## Hypotheses

### Null Hypothesis (H₀)

The Treatment onboarding experience does not improve Paid Conversion Rate.

H₀: p(Treatment) ≤ p(Control)

### Alternative Hypothesis (H₁)

The Treatment onboarding experience improves Paid Conversion Rate.

H₁: p(Treatment) > p(Control)

---

## Significance Level

α = 0.05

Decision Rule:

- If p-value < 0.05 → Reject H₀
- If p-value ≥ 0.05 → Fail to Reject H₀

---

## Test Output

| Metric | Value |
|----------|----------|
| Z-Statistic | 3.252 |
| P-Value | 0.00057 |
| Significance Level | 0.05 |

---

## Decision

Since:

0.00057 < 0.05

Reject the Null Hypothesis.

---

## Business Interpretation

There is strong statistical evidence that the new onboarding campaign improves Paid Conversion Rate.

The observed increase from 3.17% to 6.99% is unlikely to be caused by random chance.

Therefore, the Treatment experience demonstrates a statistically significant improvement in the experiment's primary business metric.

---

# Task 8: Guardrail Metric Evaluation

A rollout decision should not rely solely on conversion improvement.

Several guardrail metrics were reviewed to identify potential risks.

---

## Guardrail Metric 1: Refund Rate

| Group | Refund Rate |
|---------|---------|
| Control | 0.00% |
| Treatment | 0.42% |

### Assessment

The Treatment group generated a small number of refund requests while the Control group generated none.

### Risk

This may indicate:

- Misaligned expectations
- Lower quality conversions
- Users purchasing before fully understanding the product

### Severity

Low to Moderate

Further monitoring is recommended.

---

## Guardrail Metric 2: Support Ticket Rate

| Group | Average Support Tickets |
|---------|---------|
| Control | 0.22 |
| Treatment | 0.37 |

### Assessment

Support requests increased substantially in the Treatment group.

### Risk

Higher support volume may create:

- Increased operating costs
- Longer response times
- Lower customer satisfaction

### Severity

Moderate

Root-cause analysis should be performed before full rollout.

---

## Guardrail Metric 3: Days to Convert

| Group | Average Days to Convert |
|---------|---------|
| Control | 8.86 |
| Treatment | 6.40 |

### Assessment

Treatment users converted faster.

### Risk

No immediate risk identified.

### Business Impact

Positive.

Faster conversion generally improves cash flow and customer acquisition efficiency.

---

## Guardrail Metric 4: Engagement Score

| Group | Average Engagement Score |
|---------|---------|
| Control | 57.03 |
| Treatment | 62.93 |

### Assessment

Engagement increased significantly under the Treatment experience.

### Risk

No significant risk identified.

### Business Impact

Positive.

Higher engagement often correlates with stronger retention and long-term customer value.

---

## Overall Guardrail Assessment

### Positive Findings

- Higher Paid Conversion Rate
- Higher Engagement Score
- Faster Conversion Time

### Risks Identified

- Increased Support Ticket Volume
- Small Increase in Refund Requests

The risks appear manageable but should be monitored during rollout.

---

## Final Recommendation

Recommend a phased rollout of the Treatment onboarding experience.

Justification:

1. Paid Conversion Rate improved significantly.
2. Statistical testing confirms the improvement is significant (p-value = 0.00057).
3. Engagement improved.
4. Users converted faster.
5. Guardrail risks exist but do not currently outweigh the business benefits.

Recommended Actions:

- Launch Treatment gradually.
- Monitor refund rate weekly.
- Monitor support ticket volume weekly.
- Review customer feedback during rollout.
- Reassess performance after additional data is collected.