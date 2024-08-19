# Alexa virtual Assistant

This is a freelance project for one of my US Client where the Assistant act like a reminder with a specific voice note.

## Overview

This guide provides detailed steps for hosting an audio file, updating your Alexa skill code to handle audio playback, deploying the skill, and managing session persistence.

## Step 1: Host Your Audio File

1. **Host Your Audio File:**
   - Ensure your audio file is available on a secure (HTTPS) server.
   - The URL should point directly to the audio file and be publicly accessible.

2. **Verify the URL:**
   - Test the URL in a web browser to ensure it correctly loads the audio file.

## Step 2: Update Your Skill Code

1. **Install the Alexa Skills SDK:**
   - If you haven’t already, install the Alexa Skills SDK for Node.js:
     ```bash
     npm install ask-sdk-core
     ```

     ## Step 3: Deploy Your Skill

1. **Zip Your Code:**
   - Compress your code files into a zip file. Ensure that `index.js` (or your main file) is at the root of the zip file.

2. **Upload to AWS Lambda:**
   - Log in to the AWS Management Console.
   - Navigate to AWS Lambda.
   - Create a new Lambda function or select an existing one.
   - Upload the zip file.

3. **Configure Lambda Function:**
   - Set the runtime to Node.js (ensure it matches your development environment).
   - Configure the handler to point to your main file (e.g., `index.handler`).

4. **Set Up Permissions:**
   - Ensure that your Lambda function has the necessary permissions to be invoked by Alexa.

5. **Link Lambda to Alexa Developer Console:**
   - Log in to the Alexa Developer Console.
   - Go to your skill and navigate to the endpoint section.
   - Set the endpoint type to AWS Lambda ARN and enter your Lambda function ARN.

## Step 4: Test Your Skill

1. **Use the Alexa Simulator:**
   - In the Alexa Developer Console, use the Alexa Simulator to test your skill.
   - Ensure that the audio plays correctly when the skill is launched.

2. **Test on an Alexa-enabled Device:**
   - Enable your skill on an Alexa-enabled device.
   - Test the skill to ensure the audio plays 10 minutes after launch as expected.