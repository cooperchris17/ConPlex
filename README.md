# ConPlex (CONstruction ComPLEXity Calculator)

Read about the tool in more detail here:

Cooper C. R. (2025). The Construction Complexity Calculator (ConPlex): A tool for calculating Nelson’s (2024) construction-based complexity measure. <i>Research in Corpus Linguistics 13</i>(2), 124-143. https://ricl.aelinco.es/first-view/RiCL_447_13_02_05.pdf

The Construction Complexity Calculator is a GUI tool that calculates the complexity measure described in Nelson (2024), which uses constructions as the unit of language with which the measure is calculated. Full details about the complexity measure are available in an Open Access paper (Nelson, R. (2024). Using constructions to measure developmental language complexity. Cognitive Linguistics. https://doi.org/10.1515/cog-2023-0062). If you use this tool in your research, please cite Nelson's (2024) paper.

Download the tool for Windows <a href="https://drive.google.com/file/d/1PljHorFOaXYTIar527GMaDibNAzk6Coo/view?usp=sharing">here</a>  (Mac and Linux versions to be added later)

<img src="https://github.com/cooperchris17/ConstructionComplexityCalculator/blob/main/supplementary/gui_screenshot.png?raw=true" width="674" height="481">

The complexity score for one text can be calculated by pasting a text into the textbox and clicking "Process Text Input". Multiple texts can be analysed by clicking "Upload and Process Files" and selecting the desired number of texts. For multiple files, the processing will begin immediately.

The tool uses Stanza to split texts into sentences and tag the texts with treebank-specific (XPOS) tags. After the texts have been tagged, tokens with the universal POS (UPOS) tag of "PUNCT", meaning all punctuation, are excluded from the analysis. The entropy used in the sentence diversity and sentence productivity calculation (see Nelson (2024) for more details) is calculated using the entropy() function in SciPy. 

The tool outputs the mean complexity score for each text, along with the mean diversity and mean productivity scores. It is expected that most researchers will only use the complexity scores.

While it is assumed that most researchers will use the downloadable tool, a notebook with the Python code behind the tool is also available in this GitHub repository <a href="https://github.com/cooperchris17/ConstructionComplexityCalculator/blob/main/python_notebooks/construction_complexity.ipynb">(python_notebooks/construction_complexity.ipynb)</a>. Widgets have been added to the notebook so the functionality is the same as the downloadable tool, although it looks a little different. If "run all" is selected, users can input or upload files. The main reason that the notebook has been shared is in case researchers would like to adapt the code for reasons such as trying the complexity measure with other languages, or needing to change the tagger to one that is more appropriate for the users' texts. For using the code with other languages, an easily editable notebook is available with instructions <a href="https://github.com/cooperchris17/ConstructionComplexityCalculator/blob/main/python_notebooks/construction_complexity_other_languages.ipynb">(python_notebooks/construction_complexity_other_languages.ipynb)</a>.

The complexity scores that were calculated for the paper: Construction Complexity Calculator: A tool for calculating Nelson’s (2024) construction-based complexity measure (under review) are available in the <a href="https://github.com/cooperchris17/ConstructionComplexityCalculator/tree/main/supplementary">supplementary</a> folder

This tool was developed in October 2024 by Christopher Cooper.
