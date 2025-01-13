# IDS Validation Queries
George Alter

The Access database "IDS_validation_v5.accdb" runs SQL queries that validate an IDS database.  Entries in the Type and Value columns are compared to the Metadata table.  Checks are performed to be sure that entries in the INDIV_INDIV table are reciprocal.    
   
Steps:
1. Use the MS-Access Linked Table Manager (under the External Data tab) to link the IDS files (CONTEXT, CONTEXT_CONTEXT, INDIV_CONTEXT, INDIV_INDIV, INDIVIDUAL) to the data in a separate MS-Access database. Check the "Always prompt for new location" to change to a different database.  Test data have been provided in the Fam_Recon_test_data_v2.accdb file.     
        
2. Use the MS-Access Linked Table Manager to link the metadata tables.     
The "Metadata_standard" table should be linked to the latest version of IDS Metadata.   The "Metadata_local" table can be used for metadata definitions developed locally that are not part of the IDS standard. 
       
3. Run the "Run report" macro.  Executing the macro called "Run report" will run all of the queries and create a report with the results.    
   
4. Select "Print Preview" under the "Views" option on the "Home" tab.  Click "Print" to print the report.   
         
Notes:      
The Linked Table Manager can be used to link to data in other IDS databases in Access or other database systems.   Databases other than Access (MySQL, Posgres, Oracle, etc.) can be linked via ODBC.   
   
The queries given here may require editing before they can be used in other database systems.  While basic SQL keywords are the same in all versions of SQL, functions are often implemented differently.  These queries make extensive use of functions for dates and for parsing text, which may not be compatible with other dialects of SQL.   
   
These queries can be tested using the [Fam_Recon_test_data_v2.accdb](https://github.com/altergc/IDS/blob/main/Tools/IDS_Validation/Fam_Recon_test_data_v2.accdb), which is provided in this repository.  This test should generate the result found in the [Known_errors_IDS_validation_tests--Fam_recon_test.pdf](https://github.com/altergc/IDS/blob/main/Tools/IDS_Validation/Known_errors_IDS_validation_tests--Fam_recon_test.pdf) file.   
   
   
## License    
This work is licensed under the [MIT License](https://opensource.org/licenses/MIT).    
Please see the LICENSE.txt file in this folder.    
    
## Citation	 
Please cite this work as:    
Alter, G. C. (2022). IDS Validation Queries [SQL]. https://github.com/altergc/IDS/tree/main/Tools/IDS_Validation


