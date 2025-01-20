# www.east5th.co

## Initial Deploy

Run `yarn deploy-east5th --profile ${AWS_PROFILE}` from the base of the project. This will deploy a CloudFormation stack that creates a Code Pipeline that triggers on a push to `main` in the `east5th` Github repo.

Then, approve the pending Github connection in AWS CodePipeline in the associated AWS account. Also, add www records to Route 53 from Certificate Manager.

To test, push to `main` and validate that the CodePipeline successfully triggers.
