Challenge Project:

1. Deploy a simple hello world web app to AWS using "eb_deployer"  
	1. The basic instructions for using eb_deployer are in the readme:  
	   https://github.com/ThoughtWorksStudios/eb_deployer/blob/master/README.md  
	2. The "hello world" application can be in any language.  You don't need to write this application, just get it deployed.  You can find sample applications to download here:  
	   https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/GettingStarted.html#GettingStarted.Walkthrough.DeployApp
2. eb_deployer supports the notion of a "resources" stack, which is an additional cloudformation stack to hold supplementary resources, like databases, roles, etc.  Add a resources stack to your configuration, which just includes a custom IAM role and instance profile for your ec2 instances in your web apps.  The policy for the role can be anything, just show that you can add a custom role.  Include a stack output for the instance profile name.  See the following links for a sample of using a resource stack  
	1. https://github.com/ThoughtWorksStudios/eb_deployer/blob/master/samples/multi_components/config/eb_deployer.yml#L99  
	2. https://github.com/ThoughtWorksStudios/eb_deployer/blob/master/samples/multi_components/config/aws_resources.json  
2. Lastly, write a ruby rake task that queries and prints the instance profile name by querying the output of the resources stack.  Use the "EbDeployer.query_resource_output" function to make this query.  
(see https://github.com/ThoughtWorksStudios/eb_deployer/blob/46c7688557221bb86845cb372d7dd75793c7993b/lib/eb_deployer.rb#L45)


