## Diagnostic Questions

#### Q1. The backend of Cymbal Superstore’s e-commerce system consists of managed instance groups. You need to update the operating system of the instances in an automated way using minimal resources. What do you do?

- [ ] Create a new instance template. Click Update VMs. Set the update type to Opportunistic. Click Start.
- [x] Create a new instance template, then click Update VMs. Set the update type to PROACTIVE. Click Start.
- [ ] Abandon each of the instances in the managed instance group. Delete the instance template, replace it with a new one, and recreate the instances in the managed group.
- [ ] Create a new instance template. Click Update VMs. Set max surge to 5. Click Start.

**Explanation:** This institutes a rolling update where the surge is set to 1 automatically, which minimizes resources as requested.


#### Q2. What action does the terraform apply command perform?

- [ ] Downloads the latest version of the terraform provider.
- [x] Sets up resources requested in the terraform config file.
- [ ] Verifies syntax of terraform config file.
- [ ] Shows a preview of resources that will be created.

**Explanation:** Terraform Apply sets up resources specified in the terraform config file.
 
 
#### Q3. You require a Cloud Storage bucket serving users in New York City. There is a need for geo-redundancy. You do not plan on using ACLs. What CLI command do you use?

- [ ] Run a gcloud mb command specifying the name of the bucket and accepting defaults for the other mb settings.
- [ ] Run a gsutil mb command specifying a dual-region bucket and accepting defaults for the other mb settings.
- [ ] Run a gsutil mb command specifying a multi-regional location and an option to turn ACL evaluation off.
- [x] Run a gsutil mb command specifying a dual-region bucket and an option to turn ACL evaluation off.

**Explanation:** NAM4 implements a dual-region bucket with us-east1 and us-central1 as the configured regions.
 
 
 #### Q4. Cymbal Superstore’s sales department has a medium-sized MySQL database. This database includes user-defined functions and is used internally by the marketing department at Cymbal Superstore HQ. The sales department asks you to migrate the database to Google Cloud in the most timely and economical way. What should you do?

- [ ] Find a MySQL machine image in Cloud Marketplace and configure it to meet your needs.
- [ ] Use gcloud to implement a Compute Engine instance with an E2-standard-8 machine type, install, and configure MySQL.
- [ ] Implement a database instance using Cloud SQL, back up your local data, and restore it to the new instance.
- [x] Configure a Compute Engine VM with an N2 machine type, install MySQL, and restore your data to the new instance.

**Explanation:** N2 is a balanced machine type, which is recommended for medium-large databases.


#### Q5. You need to quickly deploy a containerized web application on Google Cloud. You know the services you want to be exposed. You do not want to manage infrastructure. You only want to pay when requests are being handled and need support for custom packages. What technology meets these needs?

- [ ] App Engine flexible environment
- [ ] Cloud Functions
- [ ] App Engine standard environment
- [x] Cloud Run

**Explanation:**  Cloud Run is serverless, exposes your services as an endpoint, and abstracts all infrastructure.
 
 
 #### Q6. Cymbal Superstore’s marketing department needs to load some slowly changing data into BigQuery. The data arrives hourly in a Cloud Storage bucket. You want to minimize cost and implement this in the fewest steps. What should you do?

- [ ] Implement a bq load command in a command line script and schedule it with cron.
- [x] Use the BigQuery data transfer service to schedule a transfer between your bucket and BigQuery.
- [ ] Read the data from your bucket by using the BigQuery streaming API in a program.
- [ ] Create a Cloud Function to push data to BigQuery through a Dataflow pipeline.

**Explanation:**  BigQuery transfer service is the simplest process to set up transfers between Cloud Storage and BigQuery. It is encompassed by one command. It is also free.


#### Q7. Which Virtual Private Cloud (VPC) network type allows you to fully control IP ranges and the definition of regional subnets?

- [ ] Default Project network 
- [ ] An auto mode network converted to a custom network
- [ ] Auto mode network
- [x] Custom mode network

**Explanation:** A custom mode network gives you control over regions that you place your subnets in and lets you specify IP ranges for them as well.
 
 #### Q8. The development team for the supply chain project is ready to start building their new cloud app using a small Kubernetes cluster for the pilot. The cluster should only be available to team members and does not need to be highly available. The developers also need the ability to change the cluster architecture as they deploy new capabilities. How would you implement this?

- [ ] Implement an autopilot cluster in us-central1-a with a default pool and an Ubuntu image.
- [ ] Implement an autopilot cluster in us-central1 with an Ubuntu image type.
- [x] Implement a private standard zonal cluster in us-central1-a with a default pool and an Ubuntu image.
- [ ] Implement a private standard regional cluster in us-central1 with a default pool and container-optimized image type.

**Explanation:**   Correct! Standard clusters can be zonal. The default pool provides nodes
used by the cluster. 


#### Q9. You need to analyze and act on files being added to a Cloud Storage bucket. Your programming team is proficient in Python. The analysis you need to do takes at most 5 minutes. You implement a Cloud Function to accomplish your processing and specify a trigger resource pointing to your bucket. How should you configure the --trigger-event parameter using gcloud?

- [x] --trigger-event google.storage.object.finalize
- [ ] --trigger-event google.storage.object.add
- [ ] --trigger-event google.storage.object.create
- [ ] --trigger-event google.storage.object.change

**Explanation:** Finalize event trigger when a write to Cloud Storage is complete.


#### Q10. Cymbal Superstore asks you to implement Cloud SQL as a database backend to their supply chain application. You want to configure automatic failover in case of a zone outage. You decide to use the gcloud sql instances create command set to accomplish this. Which gcloud command line argument is required to configure the stated failover capability as you create the required instances?

- [x] --availability-type
- [ ] --master-instance-name
- [ ] --replica-type
- [ ] --secondary-zone

**Explanation:** This option allows you to specify zonal or regional availability, with regional providing automatic failover to a standby node in another region.
