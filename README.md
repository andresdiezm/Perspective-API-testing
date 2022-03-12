# Perspective-API-testing

Here I am trying to understand how perspective API scores different comments for toxicity and potential bias in the model.

Model Review and Experimental Analysis:
For the thresholds with toxicity the score threshold is around 0.3 and above, but when removing the toxic label the score threshold drops to around 0.25 except for severe_toxic label which has the highest threshold of all lables (around 0.49). That being said,this apears to be heavily biased as some comments scored way lower than they should have. When looking at the distribution of the data, over 75 percent (over the 25th percentile) of the comments containing at least one of the labels are socred .9 or higher. I feel the model does correctly label the comments in most cases, but I think the scores don't reflect the true toxicity of the comments. Some comments that scored very high shouldve scored lower and vice versa.

Hypothesis for testing the Perspective API: The API will score comments that include the mention of minorities (women, LGBTQ, latinos, other foreigners, religion, etc.) higher.

RESULTS OF TEST:
The scores do refelct some bias twoards minorities. Even when the context of the comment seems to not carry any toxic traits it will more likely score higher than comments including more generic topics. Derogatory language and grammar also play a role in how the API scores comments but this varies per label. The model doesn't discriminate against the bias of human raters. The bias comes from the human raters interpretation of the comments and their scores. Some comments were incredibly disturbing but were scored lower than comments that I felt shouldn't even be classified as toxic.
