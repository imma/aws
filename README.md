Setup
=====

For bash, source `script/profile` to expose the `aws` command.  Requires the
`defn/app` project installed and sourced.

Maintenance
===========

To get the latest Ubuntu Trusty ami for each region:

    aws runmany 5 'echo local $1=$(aws with $1 aws ami)' | sort > script/aws_ami
