## Ronni Merrill
## 2026-11-26

# Technical Experiment: Reducing the Top Token Output

## 1. Purpose
The purpose of this experiment was to make a small technical modification to the NLP pipeline by reducing the number of most frequently occurring tokens displayed in the analysis output.

## 2. Original Behavior
The original NLP pipeline displayed the top 20 most frequently occurring tokens identified during text analysis.

## 3. Technical Modification
The pipeline was modified to display the top 10 most frequently occurring tokens instead of the top 20.

This modification required changing the number of tokens selected for display while leaving the remaining text-processing and analysis steps unchanged.

## 4. Results
After implementing the modification, the pipeline successfully processed the source text and displayed the 10 most frequently occurring tokens.

The output was shorter and more focused, making the most frequently used words easier to review.

## 5. Conclusion
This experiment demonstrated how a small modification to an NLP pipeline can change the presentation of analytical results without changing the underlying text-processing workflow.

Reducing the token output from 20 to 10 provided a more concise summary of the most frequently occurring words in the source text.
