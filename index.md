# Janus Declarative Specification Measurements - Journal
Static Repository for results and tests used in the journal article relative to the Janus declarative specifications measurement component. This archive contains the additional material to the paper "Measuring Rule-based LTLf Process Specifications: A Probabilistic Data-driven Approach". The use-case study material can be found in this additional repository: [https://github.com/l2brb/Measurement-change-point-evaluation](https://github.com/l2brb/Measurement-change-point-evaluation). 
 
 * web page [https://oneiroe.github.io/DeclarativeSpecificationMeasurements-Journal-static/](https://oneiroe.github.io/DeclarativeSpecificationMeasurements-Journal-static/)
 * static GitHub page to just download the files [https://github.com/Oneiroe/DeclarativeSpecificationMeasurements-Journal-static](https://github.com/Oneiroe/DeclarativeSpecificationMeasurements-Journal-static)

Find the active development in the main [Janus repository](https://github.com/Oneiroe/Janus).

Janus How-to
=========================
Janus is a tool-set for the evaluation of declarative process mining specifications ([LICENSE](https://github.com/Oneiroe/MINERful/blob/master/LICENSE) here).

It is based on Linear Temporal Logic over finite traces with past operators (LTLp~f~) and specifically on the concept  of reactive constraints: formulae with an explicit distinction between the activator and consequent factors of the formula itself.

For details on the usage of the software consult the [wiki page](https://github.com/Oneiroe/Janus/wiki)

Index
=========================

[LICENSE](.\LICENSE)

* **tool-executable**: java executable of our tool. It requires Java version 8-11 to be executed;
  * [tool-executable.zip.001](.\tool-executable.zip.001)
  * [tool-executable.zip.002](.\tool-executable.zip.002)
  * [tool-executable.zip.003](.\tool-executable.zip.003)
* **example** ([example.zip](.\example.zip)): Contains the complete and precise data used for the trailing example in the paper (Table.1):
  * **log.txt** event log from the example
  * **output[eventsEvaluation].csv**: events evaluation for each rule and specification. 
  * **output[logMeasures].csv** : measures for the log for a specification and all its rules.
  * **output[tracesMeasures].csv** : measures for each trace of the log for a specification and all its rules.
  * **output[tracesMeasuresStats].csv** : statistics fo the distribution of trace measures for the specification and its rules.
  * **specification.json** : set of rules of the specification.
* **experiment-1** (folder): scripts required to reproduce the experiment-1:
    * **executables**: contains the executables of the declarative miners used for the experiment (Janus, MINERful, Perracotta).
    * **LOGS**: folder where to place the XES event log to be used for the experiment; 
    	* [LOGS.zip](.\experiment-1\LOGS.zip): contains the logs used in the experiments reported in the paper.
    	* **dataset-references.txt**: contains the references to the logs. 
    * **RESULTS**: folder where to find the results of the experiment.
    	* **plots-generator.py**: utility python script to plot the graphs used in the paper.
    * **peracotta-log-converter.py**: utility python script to convert a xes log into one readable by Perracotta.
    * **peracotta-model-converter.py**: utility python script to convert the specification discovered by Perracotta into DECLARE notation.
    * **REAL-LIFE-MINERS-COMPARISON.sh**: BASH script to launch the experiment (UNIX only). It is required Java 8-11 and Python3 with pm4py package installed.
* **experiment-1-results** ([experiment-1-results.zip](.\experiment-1-results.zip)): results for experiment 1 used in the paper (sepsis) and left out due to space (others).
  * **X-results**: measures for each specification discovered
  * **X-times**: for each specification discovered was saved the number of rules and the time required to compute its measures

* **experiment-2** ([experiment-2.zip](.\experiment-2.zip)): results for experiment 2
	* results for experiment 2 (the model was mined with Janus miner with a Confidence threshold of 1 and Support threshold of 0)

General remarks
=========================
- the event evaluations files (e.g., output[eventsEvaluation].csv) use a byte-schema to encode the results:  0=00 (activation and target violated), 1=01 (activation violated and target satisfied), 2=10(activation satisfied and target violate), 3=11 (activation and target satisfied). The mapping with the paper event-evaluation is 3->1, 2->-1, 0,1->0
- the specifications are called MODEL in the results files for legacy reasons
- the specifications are described using the DECLARE language

Files
=========================
<!-- filetree -->

 - [LICENSE](.\LICENSE)
 - [README.md](.\README.md)
 - [example.zip](.\example.zip)
 - [experiment-1-results.zip](.\experiment-1-results.zip)
 - experiment-1
 	- [LOGS.zip](.\experiment-1\LOGS.zip)
 	- [experiment-1.zip.001](.\experiment-1\experiment-1.zip.001)
 	- [experiment-1.zip.002](.\experiment-1\experiment-1.zip.002)
 	- [experiment-1.zip.003](.\experiment-1\experiment-1.zip.003)
 	- [experiment-1.zip.004](.\experiment-1\experiment-1.zip.004)
 	- [experiment-1.zip.005](.\experiment-1\experiment-1.zip.005)
 	- [experiment-1.zip.006](.\experiment-1\experiment-1.zip.006)
 	- [experiment-1.zip.007](.\experiment-1\experiment-1.zip.007)
 	- [experiment-1.zip.008](.\experiment-1\experiment-1.zip.008)
 	- [experiment-1.zip.009](.\experiment-1\experiment-1.zip.009)
 	- [experiment-1.zip.010](.\experiment-1\experiment-1.zip.010)
 	- [experiment-1.zip.011](.\experiment-1\experiment-1.zip.011)
 	- [experiment-1.zip.012](.\experiment-1\experiment-1.zip.012)
 	- [experiment-1.zip.013](.\experiment-1\experiment-1.zip.013)
 	- [experiment-1.zip.014](.\experiment-1\experiment-1.zip.014)
 - [experiment-2.zip](.\experiment-2.zip)
 - [tool-executable.zip.001](.\tool-executable.zip.001)
 - [tool-executable.zip.002](.\tool-executable.zip.002)
 - [tool-executable.zip.003](.\tool-executable.zip.003)

<!-- filetreestop -->
