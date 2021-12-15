# Overview

This is an example [AWS Systems Manager Runbook](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-automation.html) (formerly called Automation Document). The goal of this runbook is to demonstrate:

- Graceful shutdown of services running on an EC2 instance
- Resizing of an EC2 instance
- Graceful start of services back on the EC2 instance

When resizing the EC2 instance, this automation leverages the [AWS-ResizeInstance](https://docs.aws.amazon.com/systems-manager-automation-runbooks/latest/userguide/automation-aws-resizeinstance.html) runbook.

## Modifying the runbook

In this example runbook, it will gracefully shutdown the Apache web service (httpd) on an RPM-based Linux instance (e.g. Amazon Linux, RHEL, CentOS). You can modify the commands to shutdown your services of choice by editing lines **43** and **61**. Simply provide a list of shell based commands and they will be executed on the instance as a privileged user.
