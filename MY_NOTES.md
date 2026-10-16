# Notes made during project implementation
**During every tutorial project, I make notes on what differed from the tutorial set. These notes are stored here.**

1) The default metrics set for CLoudWatch already has the "memory used %" metrics; it does not need to be customized manually.
2) An SSM agent now needs to be set up before CloudWatch can be setup.
3) The "architecture shown above"(VPC Deployment-1) is missing from both the GitHub Readme and the website. I eventually found it in one of the non-main stale branches(one public net for bastion and two private, two public nets for the application)
4) A NAT gateway cannot be attached before the Internet gateway.
5) There is a new option for creating a NAT gateway for the whole VPC and all the AZs, which I went for.
6) Log streams are created automatically on flow logs creation
7) The script.sh copies only the index page and not the whole website data.
8) Launch configurations have been replaced with launch templates. Also, t2.micro instance type is no longer available.
9) I need a domain for a Route53 hosted zone and this is not supported by AWS free tier, so I had to skip step 15. Validation step 3 is also impossible. I had to check the website functionality through the NLB's DNS name.

