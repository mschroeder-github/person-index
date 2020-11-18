# The Person Index Challenge: Extraction of Persons from Messy, Short Texts


When persons are mentioned in texts with their first name, last name and/or middle names, there can be a high variation which of their names are used, how their names are ordered and if their names are abbreviated.
If multiple persons are mentioned consecutively in very different ways, especially short texts can be perceived as "messy".
Once ambiguous names occur, associations to persons may not be inferred correctly.
We define a person index as a structured table that distinctly catalogs individuals by their names.
This code (programmed in Java) includes:
* a procedure to generate ground truth data for future evaluations,
* a baseline approach,
* an evaluation strategy to test the performance of the baseline and suggest further improvements.

Executable classes (contain `main` methods):
1. [PersonMessyGenerator](src/main/java/de/dfki/sds/personindex/PersonMessyGenerator.java) generates data in `ground-truth-folder`.
2. [BaselineApproach](src/main/java/de/dfki/sds/personindex/BaselineApproach.java) runs baseline algorithm and creates result folders in `ground-truth-folder`.
3. [Evaluator](src/main/java/de/dfki/sds/personindex/Evaluator.java) evaluates all results and prints a latex table.
4. [Pipeline](src/main/java/de/dfki/sds/personindex/Pipeline.java) runs ground truth generation, baseline approach and evaluation in one pipeline and prints a latex table.

Data classes:
* [Person](src/main/java/de/dfki/sds/personindex/Person.java) represents a person.
* [AmbiguityEntry](src/main/java/de/dfki/sds/personindex/AmbiguityEntry.java) represents an ambiguity entry.

Helper classes:
* [Constants](src/main/java/de/dfki/sds/personindex/Constants.java) for configuration.
* [Utils](src/main/java/de/dfki/sds/personindex/Utils.java) contains utility methods.
* [MinAvgMaxSdDouble](src/main/java/de/dfki/sds/personindex/MinAvgMaxSdDouble.java) for descriptive statistics (evaluation).
* [Histogram](src/main/java/de/dfki/sds/personindex/Histogram.java) for descriptive statistics (evaluation).
