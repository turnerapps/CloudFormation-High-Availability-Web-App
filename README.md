# CloudFormation High Availability Web App
This project is part of my coursework under [Udacity's Cloud DevOps Engineer Nanodegree Program](https://www.udacity.com/course/cloud-dev-ops-nanodegree--nd9991). In the "infrastructure as code" course, I designed and built a highly-available web app that will scale to meet demand, and balance the load across available web servers. This project has the following major components:

- Public Subnet: Contains NAT Gateways for private subnets and Load Balancer.
- Private Subnet: Contains Web Servers. Not accessible from the internet.
- Load Balancer: receives requests from the web and distributes to Web Servers.
- AutoScaling Group: Based on incoming requests, spins up and/or kills web servers. Performs health check on web servers and replaces unhealthy servers.
- Launch Configuration: Lists the specifications for the web servers, including a single-run init script that more precisely sets up the software on the web servers.
