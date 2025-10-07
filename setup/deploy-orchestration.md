### Deploy Orchestration Service 

1. Choose **ML Operations** -> **Configurations** -> **Create**.

    ![config orchestration start](img/orch-02-create-config-start.png)

2. Configure your orchestration with the following:

    - Configuration Name: **my-first-orchestration**
    - Scenario: **orchestration**
    - Version: **0.0.1**
    - Executable: **orchestration**
    - Choose **Next**.

    ![enter name](img/orch-03-enter-name.png)

3. Choose **Next**.

    ![enter parameter](img/orch-04-next.png)

5. Choose **Review**. 

    ![review configuration](img/orch-05-review.png)

6. Review the properties of your orchestraion and choose **Create**. 

    ![create configuration](img/orch-06-create-button.png)

7. Choose **Create Deployment**.

    ![create deployment start](img/orch-07-create-deploy-start.png)


8. Choose the duration as **Standard** and choose **Review**. 

    ![select duration](img/orch-08-deploy-review.png)

9. Review the details and choose **Create**. 

    ![select review](img/orch-09-create-deploy-button.png)

    **Now the deployment has started.** Monitor the status changes here. 
    On the deployment screen, you can see the Target Status is **RUNNING** and in the beginning, the Current Status is **UNKNOWN**.  Also, the deployment URL shows *URL isn't available* until the orchestration is deployed.  

    > 📝**Note**: The deployment could take a few minutes depending on the server's status, network, the number of parallel jobs, etc. You can refresh the status by clicking the refresh icon on the top right of the screen. 
    > ![refresh deployment](img/orch-10-refresh-deploy.png)


10. Finally, you will see the orchestration is deployed. 

    ![deployment running](img/orch-12-deploy-running.png)
