# Hades CTF - Infrastructure Setup

Hades CTF was hosted in the cloud, using Amazon Web Services while the challenges were developed locally.

### AWS Setup
First, a t2.2xlarge EC2 instance running Ubuntu was deployed with 25GB of disk storage.
The EC2 instance was configured with a singular security group that:
- Allowed inbound traffic from all IP Addresses on port 443
- Allowed inbound SSH traffic from the residential IPs of the core R&D team ([Devesh](https://github.com/DeveshChande) and [theproton](https://github.com/Parthiv-M))
- Allowed inbound traffic from all IP Addresses for the port range 32600 - 33000 (this was only during the timeframe of the CTF)

### CTFd Setup
The git repository [ctf-framework](https://github.com/DeveshChande/ctf-framework) was cloned on the EC2 instance, following which the setup.sh script was executed, which was responsible for the following activities:
- Installing relevant dependencies
- Cloning the core-ctfd repository
- Fetching plugins to use for the CTF (unique flags, cheating monitoring, docker container deployment)

As detailed in the documentation.md file, the post-script setup involves using a self-signed certificate with CTFd for HTTPS traffic.

Once the certificate is generated, the command `docker compose up` was used to bring up the infrastructure (by navigating to the `ctf-framework` directory). After the infrastructure is online (approximately five minutes), the admin page was navigated to by opening up the public IP of the EC2 instance (e.g. `https://<ec2-instance-public-ip>`). After this, the instructions on the webpage were followed to setup CTFd (restricting team size, setting up the admin user, etc.).

Note: The '[Pixo Theme](https://github.com/hmrserver/CTFd-theme-pixo/tree/67abc2b8a444206061ad6f6070b5e5e17215336b)' was used for sprucing up the aesthetic of the CTF.


Lessons Learned:
- Incorporate brute-force protections for both the instance hosting CTFd and the docker containers.
- Build a custom CTF theme.






