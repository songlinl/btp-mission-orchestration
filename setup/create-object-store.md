## Set Up Object Store

>📝**Note**: Several object repositories can be used for storing and retrieving data. In this mission, we will use the **Object Store on SAP Business Technology Platform (BTP)** as the primary repository. However, you can also integrate with alternative repositories such as **AWS S3**, **Microsoft SharePoint**, or [other compatible storage solutions](https://help.sap.com/docs/sap-ai-core/sap-ai-core-service-guide/grounding-035c455a5a424697b60f4a24b6d791fe), depending on your system landscape and development preferences. 

1. Navigate to your global account and ensure the **Object Store** with '**standard**' plan is assigned to the subaccount. 

    ![](img/objectstore01.png)

2. Navigate to your subaccount and choose **Instances and Subscriptions** -> **Create**. 

    ![](img/objectstore02.png)

3. Configure the Object Store with the following and choose **Create**. 

    - Service: **Object Store**
    - Plan: **standard**
    - Runtime Environment: **Cloud Foundry**
    - Space: **dev**
    - Instance Name: **object-store** 

    ![](img/objectstore03.png)

4. Once the Object Store is created, choose **Create Service Key**. 

    ![](img/objectstore04.png)

5. Provide a **Service Key Name** and choose **Create**. 

    ![](img/objectstore05.png)

6. Open the service key. 

    ![](img/objectstore06.png)

7. Note down the service key details; they will be required in subsequent steps.

    ![](img/objectstore07.png)

## Upload Grounding Data to Object Store

1. Download and install [**AWS Command Line Interface**](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html). 

2. Download the [**grounding data**](https://d.dam.sap.com/a/iND4HUy?rc=10&doi=SAP1241295) and extract the files into a local directory. 

    ![](img/objectstore09.png)

3. Open the command line interface and configure AWS S3 credentials using the service key details.

    ```
    AWS Configure
    ```
    ![](img/objectstore08.png)

4. Use the `s3 cp` command to copy objects from a local directory. 

    ```
    aws s3 cp <source> <target> [--options]
    ```
    > **s3 cp Example**  
    > The following example copies a local file from your current working directory to the Amazon S3 bucket with the s3 cp command. "your-bucket-name" is the value of "bucket" in the service key. 
    > ```
    > aws s3 cp filename.txt s3://your-bucket-name
    > ```

    ![](img/objectstore10.png)

5. Verify the files uploaded into the S3 bucket using the following command. 
    ```
    aws s3 ls s3://your-bucket-name
    ```