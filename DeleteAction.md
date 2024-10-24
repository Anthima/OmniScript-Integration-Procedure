# Delete Action in OmniStudio Integration Procedure

The Delete Action in OmniStudio’s Integration Procedure allows you to efficiently delete sObject records from Salesforce using a declarative approach. This feature is particularly useful for managing your Salesforce records without writing code.

## Steps to Configure the Delete Action

### 1. Create a New Integration Procedure
- **Navigate to OmniStudio:** Start by going to the OmniStudio section in Salesforce and selecting Integration Procedures.
- **Create a New Integration Procedure:** Click on New, fill in the Type and Subtype fields, and save your Integration Procedure.

### 2. Add the Delete Action
- **Drag and Drop the Delete Action:** From the Available Components panel, find the Delete Action and drag it into your Integration Procedure structure. This action allows you to specify the records you wish to delete.
- **Name Your Delete Action:** Give your Delete Action a recognizable name for easy identification.
- **Add sObject to Delete:** Click on the Add sObject to Delete option. In the Type column, select the Salesforce object whose records you want to delete (e.g., Contact).
  ![image](https://github.com/user-attachments/assets/da370eca-6535-4239-91e8-5a08341d577a)

### 3. Specify the Path to Record IDs
![image](https://github.com/user-attachments/assets/da216f7f-09bd-47d8-96c0-80bffc97f2bd)
- **Define the Path to Id:** In the Path to Id field, input the JSON path that corresponds to the record IDs you want to delete.
For example, if your data JSON is structured like this:

json:
{
    "MyObj": {
        "ContactIds": [
            "0037800000LyxyxAAB",
            "0037800000J2ZovAAF"
        ]
    }
}



The **Path to Id** would be%MyObj:ContactIds%
### 3. Execute the Integration Procedure
![image](https://github.com/user-attachments/assets/672f7375-7537-40af-b3b0-80ad9714b5bd)
- **Debugging: :** To test your Delete Action, go to the Debug Log Panel and select your Delete Action (for instance, DeleteAction1). This will execute the procedure and initiate the deletion process.
- **Verify Deletion:** After execution, you can check the records to confirm that they have been successfully deleted from Salesforce.
  
By following these steps, you can effectively set up a Delete Action in OmniStudio’s Integration Procedure to manage your Salesforce records. This capability enhances your ability to maintain data integrity and streamline record management within your organization.
