with-aws-mfa: Run command with temporary credentials
=================================================================================================

**with-aws-mfa** obtains temporary AWS credentials that use Multi-Factor Authentication.  The reason to use temporary credentials is to not force a command line user to use Multi-Factor Authentication and not to have long live credentials live on the system.  This tool sets the environment variables **AWS_ACCESS_KEY_ID**, **AWS_SECRET_ACCESS_KEY** and **AWS_SESSION_TOKEN**.

If you haven't yet enabled multi-factor authentication for AWS API access, check out the [AWS article](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_configure-api-require.html) on doing so.


Installation:
-------------
Option 1
```sh
$ pip install with-aws-mfa
```

Option 2
```sh
1. Clone this repo
2. $ python setup.py install
```

To use:
------

```sh
with-aws-mfa [--profile profile] subcommand
```

By default this uses the default AWS long lived credentials to identify the user.  To use a specific profile, pass the **--profile** flag.
