Audit of Racial Bias in the COMPAS Recidivism Dataset Using AIF360

This practical audit examines the fairness of the COMPAS recidivism dataset using the AI Fairness 360 (AIF360) toolkit, focusing on potential racial bias between African-American defendants (unprivileged group) and Caucasian defendants (privileged group). The objective was to compute key fairness metrics, visualize disparities, and apply a mitigation technique to reduce observed bias.

To begin, the dataset was preprocessed by selecting relevant variables such as age, sex, priors count, and charge degree. Race was encoded so that African-American individuals formed the protected class. The audit computed two key fairness metrics: Disparate Impact (DI) and Statistical Parity Difference (SPD). DI values below 0.8 typically indicate bias against the protected group, while SPD values significantly below zero show reduced opportunity for the unprivileged group.

The initial analysis revealed substantial racial disparity. African-American defendants exhibited a less favorable distribution of predicted outcomes, reflected by low DI and significantly negative SPD values. This indicates that African-Americans were more likely to be classified as high risk compared to their White counterparts.

To address this, the Reweighing algorithm in AIF360 was applied. This technique adjusts sample weights to reduce the correlation between protected attributes and outcomes. After mitigation, both DI and SPD moved closer to fairness thresholds. DI increased toward 1, while SPD shifted toward 0, demonstrating measurable improvement in fairness. A bar chart visualization further highlights the reduction in bias across both metrics.

In conclusion, the audit confirms that the COMPAS dataset contains racial disparities that disadvantage African-American defendants. However, bias mitigation through Reweighing significantly improved fairness metrics. This demonstrates the importance of ethical oversight and the application of fairness-enhancing algorithms when deploying machine learning systems in high-stakes domains such as criminal justice.
