# College Income Predictor

This project delivers an end-to-end machine learning pipeline to predict whether a student will earn above a target income threshold based on their chosen college and major. By modeling historical outcomes using Random Forests and engineered features like target encoding and frequency counts, the framework identifies institution-program combinations most likely to lead to financial stability by earning above an income threshold.

Dataset available [here](https://collegescorecard.ed.gov/data/).

***

# Motivation

Choosing a college and major may be one of the most important financial decisions a student can make, yet guidance is often anecdotal or incomplete. This project aims to provide a data-driven approach to help prospective students (like my sister-in-law) identify schools, programs, and level of degree that align with their income goals.

Specifically, my sister-in-law is interested in a program aligned with the liberal arts (specifically **English**, **history**, **policital science**, **psychology**, and **sociology**) at a short list of a few schools (**James Madison University**, **Towson University**, **University of Maryland College Park**, and **West Virginia University**). She has a financial goal of earning at least **$50,000 within a year of completing her Bachelor's degree**.

***

# Predictive Modeling Conclusions

<div style="display:flex; justify-content:center; width:100%;">
  <img
    src="https://github.com/michael-whiteman/college-income-predictor/blob/main/results/cross_validated_roc_curves.png"
    style="width:48%; margin-right:2%;"
  />
  <img
    src="https://github.com/michael-whiteman/college-income-predictor/blob/main/results/feature_importance_plot.png"
    style="width:48%;"
  />
</div>

The machine learning pipeline achieved strong cross-validated performance, particularly in precision (0.902) and average precision score (0.941), making it well-suited for identifying high-confidence institution-program combinations which satisfy income requirements. Random Forest was selected for its balance of accuracy and interpretability, and the final model revealed that the **choice of major** has the highest predictive power by far, with over **four times (4.26)** the predictive power of the choice of institution or any non-program related feature in determining whether an institution-program leads to above-threshold income.  The **institution itself** and **credential level** also contribute significant predictive power.

When considering only Bachelor's degrees, none of the institution-program pairs in my sister-in-law's areas of interest surpassed the income threshold of $50,000. However, the **Clinical, Counseling, and Applied Psychology** program at **James Madison University** and **University of Maryland College Park** came the closest, suggesting that with a Bachelor’s-level credential, certain applied fields within the liberal arts may be acceptable. Reevaluating the same programs under the assumption that she earns a **Master’s Degree** changes the outlook considerably. With this higher credential level, **multiple graduate programs in Psychology at the University of Maryland College Park** and the **Clinical, Counseling and Applied Psychology** program at **Towson University** are predicted to exceed the income threshold, indicating that continued education may substantially improve her earning potential - especially within the field of psychology.

Overall my recommendations to my sister-in-law will be:  
1. Broaden school options and explore other majors if only interested in pursuing a Bachelor's while keeping the income requirement.
2. Consider a Master's to meet income requirements if keeping current schools and majors.  
3. Prioritize University of Maryland College Park and Towson University (if pursuing a Master's) among current choices.
4. Use the predicted results as a decision support tool, not a final answer.

Thanks for following along, and I hope that you learned something!

***
