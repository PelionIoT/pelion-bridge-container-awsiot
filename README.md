arm PELION Device Shadow bridge for Amazon AWS IoT 
 
01/04/2019: Happy New Year! minor update to mbed-properties-editor

11/26/2018: updated bridge - removed outdated scripts - no longer needed

11/07/2018: updated bridge - new Google CloudIoT HTTP-based implementation (optional) in leu of MQTT

11/04/2018: updated bridge - reoganized for future AWS and Google HTTP implementations

11/03/2018: updated bridge - new IoTHub HTTP-based implementation (optional) in leu of MQTT

Container Bridge Instance Installation:

1). Clone this repo into a Linux instance that supports docker images

2). cd into the cloned repo and run: ./run-reload-bridge.sh

Once the container instance is live, you must configure the bridge and bind it between your mbed Pelion account and your IoT Account in AWS

1). Create your IAM Access Key ID and Secret Access Key to enable the AWS CLI in your container. Record those values
    You will also need to record the region of your service (i.e. us-east-1, us-west-2, etc...). Please record that as well. 
    For more information on creating the KeyID and Access Key see: https://aws.amazon.com/cli/

2). Next go to https://os.mbed.com and create your mbed Account. You can then request a Pelion developer account using the same credentials at https://portal.us-east-1.mbedcloud.com

3). Once your Pelion account is created, you need to "Access Keys" to create a Pelion API Key/Token. Record the Token Value

Now that you have your:

    - AWS Region (i.e. us-east-1)
    
    - AWS Access Key ID for the AWS IoT CLI

    - AWS Secret Access Key for the AWS IoT CLI

    - Pelion API Key/Token generated

Go to:  https://[[your containers public IP address]]:8234

    - username: "admin" (no quotes)

    - password: "admin" (no quotes)

Enter each of Key ID, Access Key, and Pelion API Token

    - Please press "SAVE" after *each* is entered... 

    - After all 4 are entered and saved, press "RESTART"

Your Pelion bridge should now be configured and operational. 

Bridge source (Apache 2.0 licensed - Enjoy!): https://github.com/ARMmbed/pelion-bridge.git

Copyright 2018. ARM Ltd. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License. 
