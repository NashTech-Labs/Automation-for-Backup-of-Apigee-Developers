# Developers in Apigee

In Apigee, "developers" refer to individuals or entities who interact with and consume APIs managed on the Apigee API management platform. Developers play a significant role in the API ecosystem, and Apigee provides tools and features to manage developer accounts, monitor their API usage, and engage with them effectively.

## Taking Backup of developer from Apigee to Github Repository using Jenkins

This repository contains Jenkinsfile which has script for taking Backup of developer from Apigee to Github Repository using Jenkins.

For using this template we have to update following values in  jenkinsfile:

`<GCP_CREDENTIAL_ID>`

`<GITHUB_CREDS_ID>`

`<GITHUB_USER_NAME>`

`<GITHUB_USER_EMAIL>`

`<APIGEE_ORG_NAME>`
            
1. Create a Jenkins pipeline using this repository. Configure your jenkins pipeline to use this github repository accordingly.

2. This jenkins pipeline contains a scheduled cronjob (weekly basis) which will run to automate the backup process at regular intervals. This ensures that backups are performed consistently without manual intervention.

3. Jenkins pipeline for backup is utilizing the Apigee Command Line Interface (Apigeecli) to export the identified Apigee resources. Apigeecli allows to interact with the Apigee API and export configurations and definitions.

4. When this pipeline will run and then it will create a following type of directory structure here in this repository and will store backup data in this:

`<APIGEE_ORG_NAME> > <DATE_OF_BACKUP> > developers.json`

![jenkins_pipeline](https://i.postimg.cc/xCMqCc2H/download-3.png)


6. `developers.json` file will contain all the developers configurations.

7. To verify this move to:

   GCP > Apigee > developers

