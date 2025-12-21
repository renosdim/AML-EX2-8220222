## **Understanding Age – Gender Distortion**

Please execute code cells with order.

**Code Cell 1** looks at how gender and age dimensions relate to each other in the dataset.  
It calculates a Pearson correlation between the main gender and age scores, including confidence intervals, p-values, Bayes factors, and statistical power.  
Then it builds two correlation matrices—one for gender features and one for age features—and displays them as heatmaps, so you can see how these latent dimensions align with each other.

**Code Cell 2** runs a simple OLS regression predicting age from gender.  
It prints a regression summary and creates two plots:  
a static regression plot with highlighted outliers, and an interactive Plotly plot where you can hover over each point to see the category.  
This gives you a visual sense of whether gender scores push age predictions up or down.

**Code Cell 3** moves into the behavioral dataset.  
Here, for each occupation, it computes the difference between the treatment group’s age estimate and the control group’s average age.  
Then it plots two kernel density curves—one for male images and one for female images—plus vertical lines marking each mean difference.  
That visualization shows how the gender of the image shifts age judgments.

**Code Cell 4** performs three statistical tests.  
First, a t-test comparing raw age estimates for male versus female images in the treatment group.  
Then two one-sample t-tests—one for female-image age differences and one for male-image age differences—testing how much the age approximations of the treatment group differ from reality.  
It outputs the mean differences, t-values, and p-values for all three tests.

**Code Cell 5** fits a full regression model with condition, gender, their interaction, category, and subject.  
This tells you whether the Image condition amplifies gender distortions after controlling for who the participant is and what occupation they're rating.  
It prints a full regression table with model statistics, coefficients, and residual diagnostics in a polished HTML format.

**Code Cell 6** fits a simpler regression using only category and subject to predict age.  
Then it computes predicted ages and residuals for every observation.  
Two plots show how predictions and residuals differ across condition and gender, giving insight into where the treatment shifts people above or below expected baselines.

Finally, **Code Cell 7** runs two ANOVAs using sum coding.  
The first ANOVA examines the effects of condition, gender, and their interaction on age.  
The second adds category and subject to control for those differences.  
Both outputs give you clean tables with sums of squares, F-values, and p-values, showing how much variance each factor explains.
