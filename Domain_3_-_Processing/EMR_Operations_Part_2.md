## EMR Operations Part 2

* [EMR Best Practices Document](https://d0.awsstatic.com/whitepapers/aws-amazon-emr-best-practices.pdf)

### Long Running Clusters

* Keep HDFS on Core nodes

* Auto-termination is disabled (by default)

* Termination protection is enabled

### Transient Clusters

* Batch jobs, only when needed

* Input and output data and code stored in S3

* A one-node cluster considers the Master node to also be the Core node

## Resources
[EMR Best Practices Whitepaper](https://d0.awsstatic.com/whitepapers/aws-amazon-emr-best-practices.pdf)
