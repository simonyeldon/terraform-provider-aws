---
subcategory: "Transit Gateway"
layout: "aws"
page_title: "AWS: aws_ec2_transit_gateway_route_table_propagation"
description: |-
  Manages an EC2 Transit Gateway Route Table propagation
---

# Resource: aws_ec2_transit_gateway_route_table_propagation

Manages an EC2 Transit Gateway Route Table propagation.

## Example Usage

```terraform
resource "aws_ec2_transit_gateway_route_table_propagation" "example" {
  transit_gateway_attachment_id  = aws_ec2_transit_gateway_vpc_attachment.example.id
  transit_gateway_route_table_id = aws_ec2_transit_gateway_route_table.example.id
}
```

## Argument Reference

This resource supports the following arguments:

* `transit_gateway_attachment_id` - (Required) Identifier of EC2 Transit Gateway Attachment.
* `transit_gateway_route_table_id` - (Required) Identifier of EC2 Transit Gateway Route Table.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `id` - EC2 Transit Gateway Route Table identifier combined with EC2 Transit Gateway Attachment identifier
* `resource_id` - Identifier of the resource
* `resource_type` - Type of the resource

## Import

Import `aws_ec2_transit_gateway_route_table_propagation` using the EC2 Transit Gateway Route Table identifier, an underscore, and the EC2 Transit Gateway Attachment identifier. For example:

```
$ terraform import aws_ec2_transit_gateway_route_table_propagation.example tgw-rtb-12345678_tgw-attach-87654321
```
