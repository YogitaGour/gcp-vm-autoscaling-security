# gcp-vm-autoscaling-security
GCP VM Auto-Scaling and Security Implementation
Objective:
Set up a virtual machine in Google Cloud Platform, implement auto-scaling based on CPU utilization, and configure security measures including IAM and firewall rules.

            gcloud compute instances create ...
            gcloud compute instance-groups managed create ...
            gcloud compute instance-groups managed set-autoscaling ...

1. VM Creation

  1. Created VM instance using Compute Engine.
  2. Installed Apache web server.
  3. Verified via external IP.

2. Managed Instance Group & Auto-Scaling

  1. Created Instance Template.
  2. Created Managed Instance Group.
  3. Configured auto-scaling based on CPU utilization (e.g., 60% threshold).
  4. Verified scaling policy from Compute Engine console.

3. Security Implementation
  1. IAM Configuration
  2. Applied restricted IAM roles.
  3. Tested access control.
  4. Enabled OS Login via project metadata.

4. Firewall Configuration

  1. Restricted SSH access to specific IP: 49.36.66.209/32.
  2. Enabled firewall logging.
  3. Created test DENY rule to validate logging.
  4.Verified denied traffic in Logs Explorer using:

      jsonPayload.disposition="DENIED"

5. 4. Logging Verification

  1. Firewall logs confirmed blocked SSH attempts with:
  2. Disposition: DENIED
  3. Destination port: 22
