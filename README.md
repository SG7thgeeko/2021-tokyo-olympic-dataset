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
    * **Move & Transform Data:** Set the source to the raw data container and the sink to the transformed data container. Use a mapping script to transform the data.
6. **Validate the pipeline.**
7. **Publish the pipeline.**

## Additional Notes

* This is a basic example. You may need to modify the pipeline to meet your specific needs.
* For more information on Azure Data Factory, please see the following resources:
    * Microsoft documentation: https://docs.microsoft.com/en-us/azure/data-factory/
    * Azure Data Factory samples: https://github.com/Azure/azure-samples/tree/master/data-factory

I hope this helps! Let me know if you have any other questions.
