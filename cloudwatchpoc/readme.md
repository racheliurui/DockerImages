https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/install-CloudWatch-Agent-on-first-onprem.html

Step 1, set up a redhat docker image
Step 2, install cloudwatch agent on it
   Config cloudwatch agent by use default. Prepare
Step 3, try push logs into AWS cloudwatch agent and monitor



sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m onPremise -c file:~/.aws/agentconfig.json -s



```shell
docker build -t liuruibnu/cloudwatchpoc:v1 .
docker run -it liuruibnu/cloudwatchpoc:v1
docker run --tmpfs /tmp --tmpfs /run -v /sys/fs/cgroup:/sys/fs/cgroup:ro liuruibnu/cloudwatchpoc:v1 \
/opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m onPremise -c file:/home/ec2-user/.aws/agentconfig.json -s
```


Run system service in docker is hard.
