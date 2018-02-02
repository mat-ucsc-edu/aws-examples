# aws-examples::Drupal Demo
These templates demostrate a three teir application that is common in many current applications. There are more mordern designs that are becoming common, however, here we are attempting to demostrate patterns that are seen actual deployments for our institution. It is not intended to specifically demostrate drupal. Rather it is meant to be a fast and low cost demostration that is also has design patterns that would be familar to staff working in AWS for us. 

## Overview
![architecture-overview](images/diag.png)

This is a modified verstion of [Amazon AWS Reference Templates ](https://github.com/awslabs/aws-refarch-drupal). See that code for even more in depth solution with caching and cloudfront.

## Requirements
* AWS Account
  * Admin rights or sufficient to create all resources in template 
  * This will result in charges so must have credits or funding
* EC2 Keypair for instances
* Other 
  * There are many prompts for database name, password and same for drupal
  * IP CIDR block to allow SSH from, at least limit to campus or your own IP

## Sign up for AWS Accounts

Generally ITS teams are provided just an IAM account for access to existing accounts. Courses will likely pre-provision accounts as well. If you are reading this and want to try this on your own--it will cost you--use this link to start an account:
* https://aws.amazon.com

## Running the Stack

A Stack is a term AWS uses in a few services. It is basically everything created in this set of templates. You can log into AWS Console and go to Cloudformation and call the master yaml tempalte from an S3 location. All other templates need to be there and need to update the master to refence the correct https location.

That bucket must be public for references to work (might be able to limit to a VPC S3 endpoint, but that didn't seem to work with the OpsWorks service). For this content a public read bucket is not risk, however, do not use that same bucket for anything private or personal or sensitive--no passwords or credentials either.

Alternately you can click here to open a new tab in Cloudformation with the template launched. This will break if it stops being hosted in the bucket I am calling it from in this link.

 

