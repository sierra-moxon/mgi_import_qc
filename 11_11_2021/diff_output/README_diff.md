# diff command:

```
# from ontobio/ontobio/io

python diff.py -file1 ../../../mgi_import_qc/11_11_2021/go_cam_mgi_file1.gpad -file2 ../../../mgi_import_qc/11_11_2021/noctua_merged_file2.gpad -gb subject -gb evidence_code -gb object -rtd True -o diffs 

```

## output:

```


## COLUMN COUNT SUMMARY 

This report generated on 2021-11-11

  * Compared Files: ../../../mgi_import_qc/11_11_2021/go_cam_mgi_file1.gpad, ../../../mgi_import_qc/11_11_2021/noctua_merged_file2.gpad
  * See Report File: diffs_counts_per_column_report


               ../../../mgi_import_qc/11_11_2021/go_cam_mgi_file1.gpad  ../../../mgi_import_qc/11_11_2021/noctua_merged_file2.gpad
subject                                                  25891.0                                                  14420.0         
relation                                                    10.0                                                      NaN         
object                                                    9138.0                                                   9577.0         
evidence_code                                               33.0                                                     72.0         
reference                                                18351.0                                                  19230.0         
qualifiers                                                   NaN                                                     16.0         


## DIFF SUMMARY

This report generated on 2021-11-11

  * Total Unmatched Associations: 10000
  * Total Associations Compared: 130251
  * See report: diffs_compare_report



## GROUP BY SUMMARY 

This report generated on 2021-11-11

  * Group By Columns: ('subject', 'object', 'evidence_code')
  * Compared Files: ../../../mgi_import_qc/11_11_2021/go_cam_mgi_file1.gpad, ../../../mgi_import_qc/11_11_2021/noctua_merged_file2.gpad
  * Number of unqiue subjects that show differences: 12560
  * See output file diffs_subject_counts_per_column_report






## GROUP BY SUMMARY 

This report generated on 2021-11-11

  * Group By Columns: ('subject', 'object', 'evidence_code')
  * Compared Files: ../../../mgi_import_qc/11_11_2021/go_cam_mgi_file1.gpad, ../../../mgi_import_qc/11_11_2021/noctua_merged_file2.gpad
  * Number of unqiue subjects that show differences: 12560
  * See output file diffs_subject_counts_per_column_report
  * Number of unqiue objects that show differences: 481
  * See output file diffs_object_counts_per_column_report






## GROUP BY SUMMARY 

This report generated on 2021-11-11

  * Group By Columns: ('subject', 'object', 'evidence_code')
  * Compared Files: ../../../mgi_import_qc/11_11_2021/go_cam_mgi_file1.gpad, ../../../mgi_import_qc/11_11_2021/noctua_merged_file2.gpad
  * Number of unqiue subjects that show differences: 12560
  * See output file diffs_subject_counts_per_column_report
  * Number of unqiue objects that show differences: 481
  * See output file diffs_object_counts_per_column_report
  * Number of unqiue evidence_codes that show differences: 6
  * See output file diffs_evidence_code_counts_per_column_report


```

# file output :

## diffs_compare_report:
- Produces a report in the familiar ontobio report format that shows each row in file1 that isn't found in file2
- Uses GoAssociation objects for the diff.

## diffs_counts_per_column_report

- General counts of unique values per column in each file.

## diffs_subject_counts_per_column_report

- Counts per subject of the number of annotations per file
- because `-rtd True` was included in the diff command, the only reported rows are those in which the count of 
annotations per subject reported in file2, were lower than those counted for the subject in file1

## diffs_evidence_code_counts_per_column_report

- Counts per evidence_code of the number of annotations per file
- because `-rtd True` was included in the diff command, the only reported rows are those in which the count of 
annotations per evidence_code reported in file2, were lower than those counted for the evidence_code in file1

## diffs_object_counts_per_column_report

- Counts per subject of the number of annotations per file
- because `-rtd True` was included in the diff command, the only reported rows are those in which the count of 
annotations per object reported in file2, were lower than those counted for the object in file1
