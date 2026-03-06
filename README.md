# DEGO-2606---TXC_12
DEGO 2606 Group Project – Credit Application Governance Analysis

Contributors:
- Marie Christine Henke (73606)
- Jonas Dittrich (71637)
- Simon Anthofer (71078)

---

## 01 - Data Engineer:

**Critical findings:**

**Consistency:**
Income - 488 correct values, 8 as stings, 1 as float and 5 values had been stored in a variable called annaul_salary. All have been correctly transformend and safed as annual income.

Gender - 388 correctly labled values, 111 labeld as "M" or "F" and 3 missing values. All existing values have been transformed into the right format.

Date of Birth - 340 correctly formated values, 157 incorrect formats that hav been corrected, with 57 of these being flaged as ambigouos based on month and date.

**Completness:**
There were 5 missing dates of birth. 3 missing genders, 2 of which have been allocated bast on their first names. 5 instances of missing income, which have been deleted from the dataset in order not to bias the dataset. 5 missing SSN and IPs.

**Validity:**
Income - One isntance of an income equal to zero, which has been set to None, as the value is impossible.

Credit history - Two negative values set to None, as they are also impossible.

Debt to Income ratio - One suspicious outlier of 1.85 set to None.

Saving balance - One negative values has been set to None, as negative values are  impossible in a standard savings account.

Emails - 4 invalid emails recognissed.

**Uniqueness:**

Name & SSN - Two cases of duplicate people. One case has been deleted (app_001) and the other kept, because it was a resubmission.

SSN - Two cases of duplicate SSNs.


## 02 - Bias Analysis:

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

