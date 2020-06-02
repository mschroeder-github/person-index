# The Person Index Challenge: Extraction of Persons from Messy, Short Texts

The project is programmed in Java.

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
