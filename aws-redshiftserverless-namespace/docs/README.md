# AWS::RedshiftServerless::Namespace

Definition of AWS::RedshiftServerless::Namespace Resource Type

## Syntax

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON

<pre>
{
    "Type" : "AWS::RedshiftServerless::Namespace",
    "Properties" : {
        "<a href="#adminpasswordsecretkmskeyid" title="AdminPasswordSecretKmsKeyId">AdminPasswordSecretKmsKeyId</a>" : <i>String</i>,
        "<a href="#adminuserpassword" title="AdminUserPassword">AdminUserPassword</a>" : <i>String</i>,
        "<a href="#adminusername" title="AdminUsername">AdminUsername</a>" : <i>String</i>,
        "<a href="#dbname" title="DbName">DbName</a>" : <i>String</i>,
        "<a href="#defaultiamrolearn" title="DefaultIamRoleArn">DefaultIamRoleArn</a>" : <i>String</i>,
        "<a href="#iamroles" title="IamRoles">IamRoles</a>" : <i>[ String, ... ]</i>,
        "<a href="#kmskeyid" title="KmsKeyId">KmsKeyId</a>" : <i>String</i>,
        "<a href="#logexports" title="LogExports">LogExports</a>" : <i>[ String, ... ]</i>,
        "<a href="#manageadminpassword" title="ManageAdminPassword">ManageAdminPassword</a>" : <i>Boolean</i>,
        "<a href="#adminpasswordsecretarn" title="AdminPasswordSecretArn">AdminPasswordSecretArn</a>" : <i>String</i>,
        "<a href="#namespacename" title="NamespaceName">NamespaceName</a>" : <i>String</i>,
        "<a href="#tags" title="Tags">Tags</a>" : <i>[ <a href="tag.md">Tag</a>, ... ]</i>,
        "<a href="#finalsnapshotname" title="FinalSnapshotName">FinalSnapshotName</a>" : <i>String</i>,
        "<a href="#finalsnapshotretentionperiod" title="FinalSnapshotRetentionPeriod">FinalSnapshotRetentionPeriod</a>" : <i>Integer</i>,
        "<a href="#namespaceresourcepolicy" title="NamespaceResourcePolicy">NamespaceResourcePolicy</a>" : <i>Map</i>
    }
}
</pre>

### YAML

<pre>
Type: AWS::RedshiftServerless::Namespace
Properties:
    <a href="#adminpasswordsecretkmskeyid" title="AdminPasswordSecretKmsKeyId">AdminPasswordSecretKmsKeyId</a>: <i>String</i>
    <a href="#adminuserpassword" title="AdminUserPassword">AdminUserPassword</a>: <i>String</i>
    <a href="#adminusername" title="AdminUsername">AdminUsername</a>: <i>String</i>
    <a href="#dbname" title="DbName">DbName</a>: <i>String</i>
    <a href="#defaultiamrolearn" title="DefaultIamRoleArn">DefaultIamRoleArn</a>: <i>String</i>
    <a href="#iamroles" title="IamRoles">IamRoles</a>: <i>
      - String</i>
    <a href="#kmskeyid" title="KmsKeyId">KmsKeyId</a>: <i>String</i>
    <a href="#logexports" title="LogExports">LogExports</a>: <i>
      - String</i>
    <a href="#manageadminpassword" title="ManageAdminPassword">ManageAdminPassword</a>: <i>Boolean</i>
    <a href="#adminpasswordsecretarn" title="AdminPasswordSecretArn">AdminPasswordSecretArn</a>: <i>String</i>
    <a href="#namespacename" title="NamespaceName">NamespaceName</a>: <i>String</i>
    <a href="#tags" title="Tags">Tags</a>: <i>
      - <a href="tag.md">Tag</a></i>
    <a href="#finalsnapshotname" title="FinalSnapshotName">FinalSnapshotName</a>: <i>String</i>
    <a href="#finalsnapshotretentionperiod" title="FinalSnapshotRetentionPeriod">FinalSnapshotRetentionPeriod</a>: <i>Integer</i>
    <a href="#namespaceresourcepolicy" title="NamespaceResourcePolicy">NamespaceResourcePolicy</a>: <i>Map</i>
</pre>

## Properties

#### AdminPasswordSecretKmsKeyId

The ID of the AWS Key Management Service (KMS) key used to encrypt and store the namespace's admin credentials secret. You can only use this parameter if manageAdminPassword is true.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AdminUserPassword

The password associated with the admin user for the namespace that is being created. Password must be at least 8 characters in length, should be any printable ASCII character. Must contain at least one lowercase letter, one uppercase letter and one decimal digit.

_Required_: No

_Type_: String

_Minimum Length_: <code>8</code>

_Maximum Length_: <code>64</code>

_Pattern_: <code>^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[^\x00-\x20\x22\x27\x2f\x40\x5c\x7f-\uffff]+</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AdminUsername

The user name associated with the admin user for the namespace that is being created. Only alphanumeric characters and underscores are allowed. It should start with an alphabet.

_Required_: No

_Type_: String

_Pattern_: <code>[a-zA-Z][a-zA-Z_0-9+.@-]*</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### DbName

The database name associated for the namespace that is being created. Only alphanumeric characters and underscores are allowed. It should start with an alphabet.

_Required_: No

_Type_: String

_Maximum Length_: <code>127</code>

_Pattern_: <code>[a-zA-Z][a-zA-Z_0-9+.@-]*</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### DefaultIamRoleArn

The default IAM role ARN for the namespace that is being created.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### IamRoles

A list of AWS Identity and Access Management (IAM) roles that can be used by the namespace to access other AWS services. You must supply the IAM roles in their Amazon Resource Name (ARN) format. The Default role limit for each request is 10.

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### KmsKeyId

The AWS Key Management Service (KMS) key ID of the encryption key that you want to use to encrypt data in the namespace.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### LogExports

The collection of log types to be exported provided by the customer. Should only be one of the three supported log types: userlog, useractivitylog and connectionlog

_Required_: No

_Type_: List of String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### ManageAdminPassword

If true, Amazon Redshift uses AWS Secrets Manager to manage the namespace's admin credentials. You can't use adminUserPassword if manageAdminPassword is true. If manageAdminPassword is false or not set, Amazon Redshift uses adminUserPassword for the admin user account's password.

_Required_: No

_Type_: Boolean

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### AdminPasswordSecretArn

The Amazon Resource Name (ARN) for the namespace's admin user credentials secret.

_Required_: No

_Type_: String

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### NamespaceName

A unique identifier for the namespace. You use this identifier to refer to the namespace for any subsequent namespace operations such as deleting or modifying. All alphabetical characters must be lower case. Namespace name should be unique for all namespaces within an AWS account.

_Required_: Yes

_Type_: String

_Minimum Length_: <code>3</code>

_Maximum Length_: <code>64</code>

_Pattern_: <code>^[a-z0-9-]+$</code>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### Tags

The list of tags for the namespace.

_Required_: No

_Type_: List of <a href="tag.md">Tag</a>

_Update requires_: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

#### FinalSnapshotName

The name of the namespace the source snapshot was created from. Please specify the name if needed before deleting namespace

_Required_: No

_Type_: String

_Maximum Length_: <code>255</code>

_Pattern_: <code>[a-z][a-z0-9]*(-[a-z0-9]+)*</code>

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### FinalSnapshotRetentionPeriod

The number of days to retain automated snapshot in the destination region after they are copied from the source region. If the value is -1, the manual snapshot is retained indefinitely. The value must be either -1 or an integer between 1 and 3,653.

_Required_: No

_Type_: Integer

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

#### NamespaceResourcePolicy

The resource policy document that will be attached to the namespace.

_Required_: No

_Type_: Map

_Update requires_: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values

### Ref

When you pass the logical ID of this resource to the intrinsic `Ref` function, Ref returns the NamespaceName.

### Fn::GetAtt

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html).

#### Namespace

Returns the <code>Namespace</code> value.

#### NamespaceArn

Returns the <code>NamespaceArn</code> value.

#### NamespaceId

Returns the <code>NamespaceId</code> value.

#### NamespaceName

Returns the <code>NamespaceName</code> value.

#### AdminUsername

Returns the <code>AdminUsername</code> value.

#### DbName

Returns the <code>DbName</code> value.

#### KmsKeyId

Returns the <code>KmsKeyId</code> value.

#### DefaultIamRoleArn

Returns the <code>DefaultIamRoleArn</code> value.

#### IamRoles

Returns the <code>IamRoles</code> value.

#### LogExports

Returns the <code>LogExports</code> value.

#### Status

Returns the <code>Status</code> value.

#### CreationDate

Returns the <code>CreationDate</code> value.

#### AdminPasswordSecretArn

Returns the <code>AdminPasswordSecretArn</code> value.

#### AdminPasswordSecretKmsKeyId

Returns the <code>AdminPasswordSecretKmsKeyId</code> value.
