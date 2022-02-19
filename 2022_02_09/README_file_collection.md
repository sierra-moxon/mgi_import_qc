https://docs.google.com/spreadsheets/d/1W31XELOzjLobxE8kGh-BIM5AxJCf2S4SB7IAIKhs7GI/edit#gid=0

 1102  mv noctua_mgi_file_2\ \(1\).gpad 2_mgi.gpad
 1103  grep -e "^\!" 2_mgi.gpad > 2_merged.gpad
 1104  awk FNR!=1 2* >> 2_merged.gpad


python ./differ.py -file1 ~/Documents/src/mgi_import_qc/02_09_2022/1_go_cam_mgi.gpad -file2 ~/Documents/src/mgi_import_qc/02_09_2022/2_merged.gpad -o 02092022_file1_to_file2_mgi -gb evidence_code -gb subject -gb object -rtd True
python ./differ.py -file1 ~/Documents/src/mgi_import_qc/02_09_2022/3_mgi.gpad -file2 ~/Documents/src/mgi_import_qc/02_09_2022/4_merged.gpad -o 02092022_file3_to_file4_mgi -gb evidence_code -gb subject -gb object -rtd True
python ./differ.py -file1 ~/Documents/src/mgi_import_qc/02_09_2022/2_merged.gpad -file2 ~/Documents/src/mgi_import_qc/02_09_2022/4_merged.gpad -o 02092022_file2_to_file4_mgi -gb evidence_code -gb subject -gb object -rtd True

