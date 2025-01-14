---
subcategory: "Transit Gateway"
layout: "aws"
page_title: "AWS: aws_ec2_transit_gateway_vpc_attachment"
description: |-
  Get information on an EC2 Transit Gateway VPC Attachment
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_ec2_transit_gateway_vpc_attachment

Get information on an EC2 Transit Gateway VPC Attachment.

## Example Usage

### By Filter

```python
# Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_ec2_transit_gateway_vpc_attachment import DataAwsEc2TransitGatewayVpcAttachment
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsEc2TransitGatewayVpcAttachment(self, "example",
            filter=[DataAwsEc2TransitGatewayVpcAttachmentFilter(
                name="vpc-id",
                values=["vpc-12345678"]
            )
            ]
        )
```

### By Identifier

```python
# Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_ec2_transit_gateway_vpc_attachment import DataAwsEc2TransitGatewayVpcAttachment
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsEc2TransitGatewayVpcAttachment(self, "example",
            id="tgw-attach-12345678"
        )
```

## Argument Reference

The following arguments are supported:

* `filter` - (Optional) One or more configuration blocks containing name-values filters. Detailed below.
* `id` - (Optional) Identifier of the EC2 Transit Gateway VPC Attachment.

### filter Argument Reference

* `name` - (Required) Name of the filter.
* `values` - (Required) List of one or more values for the filter.

## Attribute Reference

In addition to all arguments above, the following attributes are exported:

* `appliance_mode_support` - Whether Appliance Mode support is enabled.
* `dns_support` - Whether DNS support is enabled.
* `id` - EC2 Transit Gateway VPC Attachment identifier
* `ipv6_support` - Whether IPv6 support is enabled.
* `subnet_ids` - Identifiers of EC2 Subnets.
* `transit_gateway_id` - EC2 Transit Gateway identifier
* `tags` - Key-value tags for the EC2 Transit Gateway VPC Attachment
* `vpc_id` - Identifier of EC2 VPC.
* `vpc_owner_id` - Identifier of the AWS account that owns the EC2 VPC.

## Timeouts

[Configuration options](https://developer.hashicorp.com/terraform/language/resources/syntax#operation-timeouts):

- `read` - (Default `20m`)

<!-- cache-key: cdktf-0.17.1 input-d9a7b3de207778ae6262226683d82d8cf55a2755353a69faa2211b11f09ae695 -->