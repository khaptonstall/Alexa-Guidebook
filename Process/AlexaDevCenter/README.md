# Developing An Alexa Skill

The following guide will step you through Alexa Developer Portal portion of creating an Alexa Skill.

## Alexa Developer Portal

The [Alexa Developer Portal](https://developer.amazon.com/alexa) is where you'll manage everything about your Skill except the actual code (which lives in Lambda). This includes the customer facing details about your Skill, the intents, and steps for certification.

Click on the link above and sign in with your Amazon account. When you first create an account on the Alexa Developer Portal, you will need to fill out the registration details. Afterwards you can begin creating a new skill by:

1. Clicking on the Alexa tab
2. Click "Get Started" on the Alexa Skills Kit
3. Click "Add a New Skill"

## Creating A New Skill

The following steps will guide you through the sections for creating a new Skill via the Alexa Developer Console. You will still need to follow the instructions in the sections after this in order to actually upload and test your code before final submission.

- [Skill Information](#1-skill-information)
- [Interaction Model](#2-interaction-model)
- [Configuration](#3-configuration)
- [SSL Certificate](#4-ssl-certificate)
- [Test](#5-test)
- [Publishing Information](#6-publishing-information)
- [Privacy and Compliance](#7-privacy-and-compliance)

### 1. Skill Information

#### Skill Type

This should be defaulted to "Custom Interaction Model" as this is probably want you want and gives you the most freedom.

The "Smart Home Skill API" gives you less freedom but an easy to use API for interfacing with smart home objects.

The "Flash Briefing Skill API" is for developing Skills which deliver quick bites of up-to-date information. User's can invoke your Skill directly, but more importantly a Flash Briefing Skill will be included in the user's daily overview if they ask something like, "Alexa, what's going on today?".

For more information, check out [Amazon's Documentation](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/understanding-the-different-types-of-skills).

#### Name

This is the consumer facing name of your Skill.

Note: Say your skill reads New York Times articles, so to be clear to your audience you want to name it "New York Times Reader". In order to pass certification you will need to disassociate yourself with any brand by including the word "Unofficial" or "Fan" into your Skill's name. i.e. "Unofficial New York Times Reader"

#### Invocation Name

This is the name that your user is going to be saying every single time they want to use your Skill. It is important to be something that is easier to remember and say.

A bad invocation name would be: "Unofficial New York Times Reader".
i.e. "Alexa, ask Unofficial New York Times Reader for today's headlines."

A good invocation name would be "Times Reader".
i.e. "Alexa, ask Times Reader for today's headlines."

### 2. Interaction Model

TODO

### 3. Configuration

#### Service Endpoint Type

AWS Lambda is selected by default and will be the easiest to configure. Of course, you will then be using AWS as your service for all your customers API calls so you will need to ensure Amazon's price model is right for you.

After selecting AWS Lambda ARN and your region, be sure to grab the ARN from your Lambda function and paste it in the box below your region name. The ARN will be found in the top right corner of the page when viewing your function.

See [here](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/developing-an-alexa-skill-as-a-web-service) for more information on using HTTPS instead of AWS.

### 4. SSL Certificate

This section will only apply to you if you chose HTTPS in the previous step. See the link on using HTTPS in the Service Endpoint Type section.

### 5. Test

This is where you can test your Skill in the browser. Testing your skill here accesses Lambda to run your code and will show the JSON response here.

Enter what you'd expect the user to say in the "Enter Utterance" section and click "Ask".

The Lambda Request section will show you what is being sent to your Alexa Skill, and the Lambda Response will show you your Skills output. Click "Listen" to hear how Alexa will speak your response. (This is often useful for catching punctuation errors).

### 6. Publishing Information

While most of the information on this page is pretty straightforward, the Example Phrases can often be a part of certification failure. The Example Phrases you enter here should correspond to your Sample Utterances (found in the Interaction Model section).

From the Sample Utterances:
>Up to 3 of these will be used as Example Phrases, which are hints to users.

As an example, say I have the following Sample Utterances defined for a Mario Kart Skill:

```
GetRace a random race
GetRace a random course
GetGrandPrix a random grand prix
```

My Example Phrases would be:

```
Alexa ask <Invocation Name> for a random race
Alexa ask <Invocation Name> for a random course
Alexa ask <Invocation Name> for a random grand prix
```

### 7. Privacy and Compliance

Simply check fields that align with the nature of your Skill and Submit For Certification.
