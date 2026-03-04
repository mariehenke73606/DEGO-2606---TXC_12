# DEGO-2606---TXC_12
DEGO 2606 Group Project – Credit Application Governance Analysis

Contributors:
- Marie Christine Henke (73606)
- Jonas Dittrich (71637)
- Simon Anthofer (71078)

---

## 02 - Bias Analysis: Executive Summary

We analyze algorithmic bias in NovaCred's credit approval system across 496 applications.

**Critical Findings:**

**Gender Discrimination**: Females approved at 50.81% vs males 65.73% (DI = 0.773, p < 0.001) — violates Four-Fifths rule.

**Age Discrimination**: Applicants <30 approved at 41.49% vs 50+ at 57.61% (DI = 0.720, p < 0.001) — severe age penalty.

**Intersectional Effect**: Youngest females (18-30) face the steepest barrier at 33.3% approval (DI = 0.667), with compound gender + age penalties.

**Proxy Variables at Risk**: 
- Credit History (ρ = 0.63 with age): Structurally disadvantages younger applicants BUT bank requires track-record
- Savings Balance (ρ = 0.37 with age, interacts with gender p = 0.038): Legitimate security measure BUT amplifies age bias
- Annual Income (ρ = 0.48 with age): Income threshold may mechanically enforce age discrimination OR reflect legitimate credit risk
- ZIP Code (42 pp gap at similar income): Suggests race/ethnicity proxy BUT low statistical power

**Lower-Risk Variables**: Debt-to-Income (no effect), Loan Purpose (90% missing), Spending Categories (statistically not significant BUT observed differences may emerge with better data).


---



---

