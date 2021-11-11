# MGI File #1: 
Contains all annotations made by MGI curators that are in the MGI production database

source location: https://github.com/geneontology/mgi-go-cams/blob/mgi-imports-20211104/source/go_cam_mgi.gpad
  

# MGI File #2: 
Contains everything exported from GOC/Nocuta: Resident annotations (SynGO and MGI and others), imported from MGI using file #1. 
Skyhook: 2 Files; MGI and PRO

source location: http://skyhook.berkeleybop.org/issue-237-mgi-test-pipeline/products/annotations/noctua_mgi.gpad.gz
            http://skyhook.berkeleybop.org/issue-237-mgi-test-pipeline/products/annotations/noctua_pr.gpad.gz

have to concantenate these two files in order to have a proper comparison
```
% grep -e "^\!" noctua_mgi.gpad > noctua_merged_file2.gpad
% awk FNR!=1 noctua_* >> noctua_merged_file2.gpad
```
# MGI File #3: 
Contains all MGI annotations imported into GOC from file #2

source location: emailed from David H and Lori, stored here for reference
go_cam_mgi.gpad.gz
  
have to eliminate non-MGI annotations to avoid SynGO filtered annotations in diff
```
% grep -e "^\!" go_cam_mgi.gpad > go_cam_mgi_import_only.gpad
% grep "noctua-model-id=gomodel:MGI_MGI_" go_cam_mgi.gpad >> go_cam_mgi_import_only.gpad
```  
  
# MGI File #4: 
Contains all annotations from file #3 that have run through GOC

source location: TBD from Dustin
  
  
  
