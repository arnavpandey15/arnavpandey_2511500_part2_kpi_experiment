# Subscription Onboarding Experiment Analysis

## 1. Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and early engagement.

To evaluate the effectiveness of the new experience, users were randomly assigned to one of two groups:

- **Control Group:** Existing onboarding experience
- **Treatment Group:** New onboarding and activation campaign

The objective of this experiment was to determine whether the new onboarding experience should be rolled out to all users while maintaining a positive user experience and business performance.

---

# 2. Dataset Description

The dataset contains user-level experiment data collected during the A/B test.

### Dataset Size

- Total Users: 1,408
- Control Group: 693 users
- Treatment Group: 715 users

### Key Variables

| Variable | Description |
|----------|-------------|
| user_id | Unique user identifier |
| experiment_group | Control or Treatment |
| region | User geographic region |
| device_type | Desktop, Mobile, Tablet |
| traffic_source | Acquisition channel |
| plan_type | Subscription plan |
| visited_landing_page | User visited landing page |
| started_trial | User started trial |
| completed_onboarding | User completed onboarding |
| converted_to_paid | User converted to paid subscription |
| revenue_30d | Revenue generated within 30 days |
| support_tickets_30d | Support tickets raised |
| refund_requested | Refund request indicator |
| days_to_convert | Days taken to convert |
| engagement_score | User engagement score |

---

# 3. North Star Metric Selected

## Paid Conversion Rate

### Definition

Paid Conversion Rate = Number of Users Converted to Paid ÷ Total Users

### Reason for Selection

Paid Conversion Rate was selected because:

- It directly measures the success of the onboarding campaign.
- It is closely tied to revenue growth.
- It aligns with the primary business objective.
- It serves as the most important indicator for rollout decisions.

---

# 4. KPI Tree Summary

The KPI framework was built around Paid Conversion Rate.

## North Star Metric

**Paid Conversion Rate**

### Activation Drivers

- Landing Page Visit Rate
- Trial Start Rate
- Onboarding Completion Rate

### Engagement Drivers

- Engagement Score
- Product Usage Frequency
- Feature Adoption

### Monetization Drivers

- Revenue per User
- Premium Plan Adoption
- Upgrade Rate

### Guardrail Metrics

- Refund Rate
- Support Ticket Rate
- Days to Convert
- Engagement Score

The KPI tree helps connect operational metrics to business outcomes and ensures decisions are not based on conversion alone.

---

# 5. Experiment Analysis Approach

The analysis followed the following process:

### Data Validation

- Checked for missing values
- Verified experiment group counts
- Identified duplicate user IDs
- Validated binary fields
- Evaluated revenue outliers
- Reviewed segment distributions

### Metric Comparison

Control and Treatment groups were compared across:

- Landing Page Visit Rate
- Trial Start Rate
- Onboarding Completion Rate
- Paid Conversion Rate
- Revenue Metrics
- Engagement Metrics
- Guardrail Metrics

### Segment Analysis

Performance was evaluated across:

- Region
- Device Type
- Traffic Source

---

# 6. Hypothesis Test Summary

## Objective

Determine whether the Treatment onboarding experience improves Paid Conversion Rate.

### Null Hypothesis (H₀)

The Treatment experience does not improve Paid Conversion Rate.

H₀: p(Treatment) ≤ p(Control)

### Alternative Hypothesis (H₁)

The Treatment experience improves Paid Conversion Rate.

H₁: p(Treatment) > p(Control)

### Test Used

Two-Proportion Z-Test

### Significance Level

α = 0.05

### Results

| Metric | Value |
|----------|----------|
| Control Conversion Rate | 3.17% |
| Treatment Conversion Rate | 6.99% |
| Z-Statistic | 3.252 |
| P-Value | 0.00057 |

### Decision

Since:

0.00057 < 0.05

Reject the Null Hypothesis.

### Interpretation

The Treatment onboarding experience produces a statistically significant improvement in Paid Conversion Rate.

---

# 7. Guardrail Metrics Considered

To ensure business quality was maintained, the following guardrail metrics were evaluated.

## Refund Rate

| Group | Refund Rate |
|---------|---------|
| Control | 0.00% |
| Treatment | 0.42% |

### Assessment

Slight increase observed.

---

## Support Ticket Rate

| Group | Average Support Tickets |
|---------|---------|
| Control | 0.22 |
| Treatment | 0.37 |

### Assessment

Support requests increased under Treatment.

---

## Days to Convert

| Group | Average Days |
|---------|---------|
| Control | 8.86 |
| Treatment | 6.40 |

### Assessment

Treatment users converted faster.

---

## Engagement Score

| Group | Score |
|---------|---------|
| Control | 57.03 |
| Treatment | 62.93 |

### Assessment

Treatment users demonstrated stronger engagement.

---

# 8. Final Recommendation

## Recommendation: Launch (Phased Rollout)

The Treatment onboarding experience should be rolled out gradually.

### Supporting Evidence

- Paid Conversion Rate increased from 3.17% to 6.99%.
- Conversion improvement is statistically significant.
- Engagement Score improved.
- Users converted more quickly.
- Positive performance was observed across major segments.
- Guardrail risks remain manageable.

### Expected Business Impact

- Increased subscription revenue
- Improved onboarding effectiveness
- Higher user engagement
- Faster customer activation

---

# 9. Assumptions and Limitations

## Assumptions

- Random assignment produced comparable groups.
- User behavior during the experiment is representative of future users.
- Revenue and engagement metrics were measured consistently.

## Limitations

- Analysis only covers the first 30 days after signup.
- Long-term retention was not measured.
- Revenue quality beyond the experiment window was not evaluated.
- Additional monitoring is required after rollout.

---

# 10. Screenshots Included

The following screenshots are included in the repository:

### KPI Tree

Location:

screenshots/kpi_tree_preview.png

Purpose:

Visual representation of the KPI hierarchy and business metric framework.

### Hypothesis Test Output

Location:

screenshots/hypothesis_test_output.png

Purpose:

Evidence of statistical testing, including conversion rates, test statistic, p-value, and decision outcome.

---

# Repository Deliverables

## Analysis

- analysis/experiment_analysis.xlsx
- analysis/hypothesis_test_notes.md

## Outputs

- outputs/experiment_summary.xlsx
- outputs/kpi_tree.png
- outputs/recommendation_memo.md

## Screenshots

- screenshots/kpi_tree_preview.png
- screenshots/hypothesis_test_output.png

## Documentation

- README.md

---

# Final Conclusion

The Treatment onboarding campaign delivered a statistically significant increase in Paid Conversion Rate while also improving engagement and reducing time to conversion. Although support ticket volume and refund requests increased slightly, the overall business impact is positive. A phased rollout is recommended with continued monitoring of guardrail metrics.