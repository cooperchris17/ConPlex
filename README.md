# ConstructionComplexityCalculator
This tool calculates the complexity measure described in Nelson (2024). If you use this tool in your research, please cite Nelson's (2024) paper.

The complexity score for one text cna be calculated by pasting a text into the textbox and multiple texts can be analysed by clicking "upload" and selecting the desired number of texts.

Full details about the measure are available in an Open Acess paper:
Nelson, R. (2024). Using constructions to measure developmental language complexity. Cognitive Linguistics. https://doi.org/10.1515/cog-2023-0062

The tool uses Stanza to split texts into sentences and tag the texts with treebank-specific (XPOS) tags. After the texts have been tagged, tokens with the universal POS (UPOS) tag of "PUNCT", meaning all punctuation, are excluded from the analysis. The entropy used in the sentence diversity and sentence productivity calculation (see Nelson (2024) for more details) is calculated using the entropy() function in SciPy. 

The tool outputs the mean complexity score for each text, along with the mean diversity and mean productivity scores. It is expected that most researchers will only use the complexity score.
