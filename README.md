# ACME Serverless Fitness Shop

> Serverless and Fitness, because combining two amazing things can only lead to more amazing things

## Getting Started

These instructions will allow you to run entire ACME Serverless Fitness Shop

The ACME Serverless Fitness Shop contains six different domains of service:

* [Shipment](https://github.com/retgits/acme-serverless-shipment)
* [Payment](https://github.com/retgits/acme-serverless-payment)
* [Order](https://github.com/retgits/acme-serverless-order)
* [Cart](https://github.com/retgits/acme-serverless-cart)
* [Catalog](https://github.com/retgits/acme-serverless-catalog)
* [User](https://github.com/retgits/acme-serverless-user)

To get started you'll need:

* [Go (at least Go 1.12)](https://golang.org/dl/);
* [An AWS Account](https://portal.aws.amazon.com/billing/signup);
* The _vuln_ targets for Make and Mage rely on the [Snyk](http://snyk.io/) CLI.

Each of the repositories contains the source code, data structures (if needed), and deployment scripts to deploy the different domains to AWS.

## Supported AWS Services

### Data Store

* [Amazon DynamoDB](https://aws.amazon.com/dynamodb/): Each of the domains has a [Makefile.dynamodb](./deploy/cloudformation), which you can use to run `make -f Makefile.dynamodb deploy` to create the DynamoDB table.

### Eventing

* [Amazon EventBridge](https://aws.amazon.com/eventbridge/): Each of the domains that supports Amazon EventBridge will have instructions and sources how to run the ACME Serverless Fitness Shop using Amazon EventBridge;
* [Amazon Simple Queue Service](https://aws.amazon.com/sqs/): Each of the domains that supports Amazon Simple Queue Service will have instructions and sources how to run the ACME Serverless Fitness Shop using Amazon Simple Queue Service;
* [Amazon API Gateway](https://aws.amazon.com/api-gateway/) _(only when there are public APIs available)_

## Overview

![architecture](./overview-sqs.png)

The diagram shows how the services in the different domains work together. The architecture above shows the Amazon Simple Queue Service deployment option

## Contributing

Pull requests are welcome in their individual repositories. For major changes or questions, please open [an issue](https://github.com/retgits/acme-serverless/issues) first to discuss what you would like to change.

## License

See the [LICENSE](./LICENSE) file in the repository.