# Beginners Guide to Deployment Manager

## How to deploy using Deployment-Manager
Deployment-manager can only be trigger via the CLI As of 9-Mar-2018

Commands : To Create a new Deployment
```
gcloud deployment-manager deployments create two-vms-deployment --config examples/v2/step_by_step_guide/step2_create_a_configuration/two-vms.yaml
```
Example Outputs

```
API [deploymentmanager.googleapis.com] not enabled on project
[XXXXXXXXXX]. Would you like to enable and retry?  (y/N)?  y

Enabling service deploymentmanager.googleapis.com on project XXXXXXXX...
Waiting for async operation operations/tmo-acf.XXXXXXX-XYYYY-4046-a314-e123214 to complete...
Operation finished successfully. The following command can describe the Operation details:
 gcloud services operations describe operations/tmo-acf.e7XXXXXX-XYYYY-4046-a314-e123214
The fingerprint of the deployment is 2ccccc-xxxx-ffff==
done.
Create operation operation-xxxx-yyyy-zzzz-wwww completed successfully.
NAME           TYPE                 STATE      ERRORS  INTENT
the-first-vm   compute.v1.instance  COMPLETED  []
the-second-vm  compute.v1.instance  COMPLETED  []


```
Commands : To Delete a Deployment
```
gcloud deployment-manager deployments delete two-vms-deployment
```
