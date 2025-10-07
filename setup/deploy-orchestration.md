### Deploy Orchestration Service 

1. Expand the ML Operations menu on the left and choose **Configurations**. 
    
    You need to create a configuration of the orchestration service. Choose **Create**.

    ![config orchestration start](img/orch-02-create-config-start.png)

2. Provide the following information and choose **Next**.

    - Configuration Name: **my-first-orchestration**
    - Scenario: **orchestration**
    - Version: **0.0.1**
    - Executable: **orchestration**

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

    > 📝**Note**: The deployment process usually takes between a few minutes, depending on the server's status, network, the number of parallel jobs, etc. You can refresh the status by clicking the refresh icon on the top right of the screen. In the meantime, you can proceed with the following steps.
    > ![refresh deployment](img/orch-10-refresh-deploy.png)


10. After some time, you should see the orchestration deployed and running. 

    ![deployment running](img/orch-12-deploy-running.png)
