# GraphQL Java Test Runner

Discuss and ask questions in our Discussions: https://github.com/graphql-java/graphql-java/discussions

This is a test runner application to measure the performance of [GraphQL](https://github.com/graphql/graphql-spec) Java implementation.

### Terraform and GCP project Setup

In order to orchestrate all gcp infrastructure we have used terraform, an open source infrastructure as code software tool that enables you to safely and predictably create, change, and improve infrastructure.
Infrastructure used by our test-runner on GCP are:
1. Cloud Tasks Queue.
2. Workflow.
3. Compute Engine.
4. Firestore.

Installation: 
1. Install terraform from [Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)
2. Verify terraform is working locally.
3. Create a new gcp project.
4. Create service account on IAM & Admin->Service Account-> Create Service Account.
5. Give the role as Basic->Owner.
6. Select the service account created above, then go to Actions->Manage keys->Add key->Create new key->JSON.
7. Download the key from above step and paste it in the terraform directory. Rename it as **cred.json** .
8. Open terminal in **terraform** directory.
9. Run **terraform init** 
10. Run **terraform apply -var project_id**=your project id present in **cred.json**.

Terraform will take care of all the infrastructure required by the test runner.

FYI: Firestore can be enabled only once per project and it can never be destroyed.

### Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md).
By contributing to this project (commenting or opening PR/Issues etc) you are agreeing to follow this conduct, so please
take the time to read it. 

### License

Copyright (c) 2015, Andreas Marek and [Contributors](https://github.com/graphql-java/graphql-java/graphs/contributors)

### Supported by

![YourKit](https://www.yourkit.com/images/yklogo.png)

[YourKit](https://www.yourkit.com/) supports this project by providing the YourKit Java Profiler.


