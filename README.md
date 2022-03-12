# Perspective-API-testing

Here I am trying to understand how perspective API scores different comments for toxicity and potential bias in the model.

Model Review and Analysis:
For the thresholds with toxicity the score threshold is around 0.3 and above, but when removing the toxic label the score threshold drops to around 0.25 except for severe_toxic label which has the highest threshold of all lables (around 0.49).

Hypothesis for testing the Perspective API: The API will score comments that include the mention of minorities (women,gays, latinos, other foreigners, religion, etc.) higher.

RESULTS OF TEST:
The scores do refelct some bias twoards minorities. Even when the context of the comment seems to not carry any toxic traits it will more likely score higher than comments including more generic topics. Derogatory language and grammar also play a role in how the API scores comments. The model doesn't discriminate against the bias of human raters and does not consider the words within the text like other machine learning models. The bias comes from the human raters interpretation of the comments.
