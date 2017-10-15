# Developing An Alexa Skill - Lambda

The following guide will step you through the AWS Console and Lambda portion of creating an Alexa Skill.

## AWS Lambda

AWS Lambda is a serverless compute service that runs your code in response to events and only bills you based only on the time that your code is actually running.

### Signing Up

Since Lambda is a part of AWS, you will need to setup an AWS account [here](https://aws.amazon.com/).

Note: You will need to enter your credit card information. This is because Lambda is setup in order to scale, so billing must be in place if and when that happens. But be aware, at least in testing, you should be fine with the Lambda free tier because the first one million requests each month are free.

After you have completed the sign up flow, you will be taken back to main AWS page. Press the button in the top right which now says "Complete Sign In".

## Getting Started With Lambda

First thing you need to do is switch your AWS region. Currently Alexa Skills support is only available in the US East (N. Virginia) or EU (Ireland) regions, so for US based user bases, select US East.

Once in the AWS console, you can get to Lambda by either typing "Lambda" in the AWS Services search box, or click on the "Services" tab and do the same.

Once you are on the Lambda page, click "Get Started Now".

Now you'll want to start off with a Blueprint. You can select which language/runtime you want to program with by selecting the "Select Runtime" dropdown. After you've selected the runtime you wish to use, select a blueprint that starts off with `alexa-skill-kit-sdk`. This README will focus on `alexa-skill-kit-sdk-color-expect` on the `nodejs6.10` runtime.

The next step will be to Configure Triggers. Select the empty box and select Alexa Skills Kit from the dropdown. Then hit "Next".

Now you can configure your function. What you need to do to continue is fill out the "Name" and "Role" portions. "Name" will simply be an internal name for your Lambda function, not displayed anywhere to the end user of your Alexa Skill. For "Role" you can find detailed information [here](https://docs.aws.amazon.com/lambda/latest/dg/intro-permission-model.html#lambda-intro-execution-role). For basic Alexa Skill setup that doesn't rely on additional AWS services, you can select "Create a custom role" from the Role dropdown and on the following page select `lambda_basic_execution` and then press "Allow".

After these steps, you can press "Review" and then "Create Function".
