# 2021-tokyo-olympic-dataset
# Azure Data Factory Pipeline for Transforming CSV Data

This project demonstrates how to create an Azure Data Factory pipeline to transform CSV data. The pipeline uses the following activities:

* **Copy Data:** Copies data from a source to a sink.
* **Move & Transform Data:** Transforms data using a mapping script.

## Prerequisites

* An Azure subscription
* An Azure Data Factory
* Storage account with containeres for raw and transformed data

## Steps

1. **Create a storage account.**
2. **Create containers for raw and transformed data.**
3. **Create a data factory.**
4. **Launch Data Factory Studio.**
5. **Author a pipeline with the following activities:**
    * **Source:** Set the source type to "HTTP" and paste the URL of the CSV file on GitHub.
    * **Copy Data:** Set the source to the HTTP dataset and the sink to the raw data container.
    * **Move & Transform Data:** Set the source to the raw data container and the sink to the transformed data container.
6. **Validate the pipeline.**
7. **Publish the pipeline.**
8. **Create App Registration:**
   * **Client ID**
   * **Tenant ID**
   * **Secret ID**
9. **Go to Storage Account:**
    * **Storage Account Name | Access Control (IAM)**
    * **Select Storage Blob Data Contributor : Allows for read, write and delete access to Azure Storage blob containers and data**
    * **New member select your app registration name**
10. **Create Data Bricks:**
    * **Create a single node compute cluster**
    * **Select Node Type**
    * **New Notebook**
    * **Use Below suit to connect storage to azure data bricks:**
    * **configs = {"fs.azure.account.auth.type": "OAuth",
                   "fs.azure.account.oauth.provider. type": "org. apache. hadoop. fs. azurebfs.oauth2. ClientCredsTokenProvider",
                   "fs.azure.account.oauth2.client.id": "client_id",
                   "fs.azure. account.oauth2.client.secret": 'secret_id,
                   "fs.azure.account.oauth2.client.endpoint": "https://login.microsoftonline.com/tenant_id/oauth2/token"}**
     * **dbutils.fs.mount(
             source = "abfss://tokyo-olympic-data@tokyoolympicdata.dfs.core.windows.net", # contrainer@storageacc
             mount_point = "/mnt/tokyoolymic",
             extra_configs = configs)**
      * **%fs**
      * **ls "/mnt/tokyoolymic"**
   11. **Now you can perform Data Analysis and get insights about data.**
## Additional Notes

* This is a basic example. You may need to modify the pipeline to meet your specific needs.
* For more information on Azure Data Factory, please see the following resources:
    * Microsoft documentation: https://docs.microsoft.com/en-us/azure/data-factory/
    * Azure Data Factory samples: https://github.com/Azure/azure-samples/tree/master/data-factory

I hope this helps! Let me know if you have any other questions.
