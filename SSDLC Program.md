Steps:

## Developer Education
The first step in any secure SDLC is training your developers. Developers must be trained on how to write secure code. Developers also need security awareness training to help them be aware of how attackers operate and what they can do to protect their software.

Security training is more than watching a webinar or attending a class once a year. It’s an ongoing task where developers are educated and trained while on the job. When vulnerabilities are discovered in their software, show developers what the vulnerabilities are, how they can be exploited, and how to fix them properly.


## CREATE AN AUTOMATED PATCH MANAGEMENT PROCESS
An ongoing patch management process is required to make sure your software doesn't become out of date.


When you have third-party software covered, don’t ignore your own code. Fix bugs found in your code quickly and build continuous integration, delivery, and deployment into your pipeline to make sure patches are delivered to production quickly.

## SECURE YOUR ENVIRONMENT
If your systems are on-prem, use firewall best practices to stay on top of your firewall configuration. Create a DMZ. Segment your network to reduce the chances of an attacker finding what he wants.

Protect the most sensitive data with extra measures such as database encryption. Use HTTPS to protect sensitive data in transit.

When in a cloud environment, use the security tools given to you to secure your infrastructure. Use VPC in AWS or Security Center in Azure and monitor your network properly. Misconfigurations in cloud environments can allow attackers to get in and get out undetected.

For example, here are some high-level best practices to secure your AWS environment:

Use VPCs
Use Network ACLs, Security Groups and NAT Gateways to control which machines can talk to each other and to the Internet
Never use 0.0.0.0/0 in a Security Group--you’re allowing any computer to connect to your instance!
Follow AWS best practices for VPC management and monitoring
Use a build pipeline to create EC2 instances--never create them manually
Protect private encryption keys and other secrets, never hard-coding them into your code or storing them in version control
Secure your S3 buckets, ensuring they aren’t publicly accessible (hint: use AWS config rules to find violations and fix them)
Create good IAM policies


## AUTOMATE SECURITY TESTING



## PENETRATION TESTING
Despite your efforts to automate security testing, you’ll eventually need to find more complex vulnerabilities that require human intuition to find. Penetration tests allow humans to poke around in your application to find problems.

Many regulations and standards, such as PCI DSS and HIPAA, require penetration tests to occur on a regular basis.

Penetration testing can be done in an agile environment. Your environments should be created automatically by a build pipeline. Create a new environment in the cloud and deploy your latest production build. Have the penetration testers test in that environment, and report their findings. Then tear down the temporary environment when completed.

Another option for ongoing security testing is a bug bounty program. Bug bounties pay ethical hackers to constantly search through your applications to find vulnerabilities. 
Your application will be attacked using real-world attack scenarios and these programs often discover bugs you wouldn’t otherwise find. The testing happens in the background on a continual basis with regular reports coming in.

## VULNERABILITY MANAGEMENT PROCESS

Your secure SDLC needs a strong vulnerability management process. Finding vulnerabilities doesn’t make your software safer; fixing them does.

Establish vulnerability ratings that make sense for you. It could be a rating from 1-5 or Low, Medium, High, Critical. But use caution when creating your ratings.
Too many rating levels create confusion and slow decision-making. What makes critical worse than high? Is there a practical difference between a 4 or a 5?

A better option is to keep things simple. Andrew Dunbar, VP of Security Engineering at Shopify, mentioned in a recent webinar on application security testing that Shopify has two levels: low and high. High risks are fixed right away. Low risks can be fixed in the next sprint or two.

Once you have a rating system, create SLAs based on those ratings. Hold your developers accountable for fixing vulnerabilities promptly. Security is now an intrinsic part of code quality.

Ref:
https://blog.engineroomtech.com/creating-a-secure-sdlc
