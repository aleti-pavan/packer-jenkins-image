# packer-jenkins-image

This is Packer Example to build AWS AMI ID made for Wiseup Wednesday on 25/08/2020


## Pre-requisites

1. Have `AWS CLI Installed and configured` on your machine.
2. `Packer Installed`

## Validation

1. `packer validate ansible-ubuntu18.04.json`

## Build AMI

1. `packer build ansible-ubuntu18.04.json` -> builds and spits an AMI Id.

## Verify AMI

1. `aws ec2 describe-images --image-ids <ami-id> --region <region>`
             
                      (or)

      __Validate within the AWS Console__

## Delete the AMI

### de-register ami

1. `aws ec2 deregister-image --image-id <ami-id> --region <region>`

### delete-snapshot

1. `aws ec2 delete-snapshot --snapshot-id <snapshot-id> --region <region>`