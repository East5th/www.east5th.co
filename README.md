## Initial Deploy

Install the East5th tool found [here](https://github.com/East5th/scripts).

Run `east5th aws login` and log in to the `east5th` AWS account.

Run `east5th aws create-stack` and select the `east5th` AWS account, set the stack name to `east5th` and select the `east5th.template` file for the template. This will deploy a CloudFormation stack that creates a Code Pipeline that triggers on a push to `main` in the `www.east5th.co` Github repo.

Then, approve the pending Github connection in AWS CodePipeline and add www records to Route 53 from Certificate Manager.

To test, push to `main` and validate that the CodePipeline successfully triggers.

If template changes are needed, update the template file and run `east5th aws update-stack`. Select the `east5th` AWS account, the `east5th` stack and select the `east5th.template` file for the template.
