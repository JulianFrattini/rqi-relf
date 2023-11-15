# Data Description

This document describes the [interview](#interview-data) and [issue](#issue-data) data to make them easier to understand and reuse it. None of the two data sources published here contain any verbatim data from interview transcripts or issue trackers, as this data is confidential.

## Interview Data

The interview data (`interview-data.xlsx`) contains the codes applied to the statements extracted from the interview transcripts. 

### Sheets

The file contains the following sheets:

- *Data*: Codes applied to the interview statements by the author
- *Overlap*: Codes applied to a sample of the interview statements by an independent, senior researcher
- *Codes \<concept\>*: Codes available for a specific concept
- *Statistic Quality Factors*: Number of codes per quality factor category
- *Matrix Activities x Attributes*: Co-occurrence of activity and attribute codes

### Columns

The *Data* sheet (and the *Overlap* sheet for the most part) contains the following columns:

| Column | Description |
|---|---|
| ID | unique identifier of a statement |
| P | unique identifier of an interview participant |
| Section | interview section in which the participant issued the respective statement |
| M | `FALSE` if the participant claimed that they did not perceive any issues in the regard of this section, `TRUE` otherwise |
| Quality Factor Mention | Extraction from the interview transcript that describes the properties of the requirements entity |
| Quality Factor 1/2 | Quality factor code (available codes are listed in the sheet *Codes Quality Factors*) |
| Entity-Fact 1/2 | Entity-fact codes (available codes are listed in the sheet *Codes Quality Factors* in the "Entity-Fact (Values)" column) |
| Frequency Mention | Extraction from the interview transcript that describes how often the quality factor occurs (not used during the analysis)
| Frequency | Frequency code |
| Context Mention | Extraction from the interview transcript that describes the context of the statement, i.e., context factors that impact the influence of the quality factors on the activities |
| Context Factor 1/2/3 | Context factor code (available codes are listed in the sheet *Codes Context Factors*) |
| Activity Mention | Extraction from the interview transcript that describes the impact on the activities |
| Impact Mention | Extraction from the interview transcript that describes the magnitude of the impact on the activities (in the manuscript, this is merged with the Activity Mention) |
| Activity 1/2 | Activity code (available codes are listed in the sheet *Codes Activities*)|
| Attribute 1/2 | Attribute code (available codes are listed in the sheet *Codes Attributes*) |
| Impact 1/2 | Impact code (available codes are listed in the sheet *Codes Impact*)|

## Issue Data

The issue data (`issue-data.xlsx`) contains the codes applied to the statements extracted from the issues. The file contains the following sheets:

- *Data*: Codes applied to the issue statements by the author
- *Statistics*: Number of applied quality factor codes
- *Impact*: Number of cooccurrences between quality factor codes and activity/attribute code pairs

The columns of the Data sheet resemble the ones presented in the [interview data section](#columns).