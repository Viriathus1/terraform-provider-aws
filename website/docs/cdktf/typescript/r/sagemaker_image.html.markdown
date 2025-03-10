---
subcategory: "SageMaker AI"
layout: "aws"
page_title: "AWS: aws_sagemaker_image"
description: |-
  Provides a SageMaker Image resource.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_sagemaker_image

Provides a SageMaker Image resource.

## Example Usage

### Basic usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { SagemakerImage } from "./.gen/providers/aws/sagemaker-image";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new SagemakerImage(this, "example", {
      imageName: "example",
      roleArn: test.arn,
    });
  }
}

```

## Argument Reference

This resource supports the following arguments:

* `imageName` - (Required) The name of the image. Must be unique to your account.
* `roleArn` - (Required) The Amazon Resource Name (ARN) of an IAM role that enables Amazon SageMaker to perform tasks on your behalf.
* `displayName` - (Optional) The display name of the image. When the image is added to a domain (must be unique to the domain).
* `description` - (Optional) The description of the image.
* `tags` - (Optional) A map of tags to assign to the resource. If configured with a provider [`defaultTags` configuration block](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#default_tags-configuration-block) present, tags with matching keys will overwrite those defined at the provider-level.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `id` - The name of the Image.
* `arn` - The Amazon Resource Name (ARN) assigned by AWS to this Image.
* `tagsAll` - A map of tags assigned to the resource, including those inherited from the provider [`defaultTags` configuration block](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#default_tags-configuration-block).

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import SageMaker Code Images using the `name`. For example:

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { SagemakerImage } from "./.gen/providers/aws/sagemaker-image";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    SagemakerImage.generateConfigForImport(this, "testImage", "my-code-repo");
  }
}

```

Using `terraform import`, import SageMaker Code Images using the `name`. For example:

```console
% terraform import aws_sagemaker_image.test_image my-code-repo
```

<!-- cache-key: cdktf-0.20.8 input-472a9b03f1ba8f793494df35ff1917699a39c258036a86d840cd026d9a0bfc60 -->