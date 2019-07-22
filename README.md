
# Beagle Security Plugin for CODESHIP

This plugin can be used to trigger beagle penetration testing from Codeship

### Prerequisites

* Obtain Application Token and Access Token from Beagle Dashboard
* Add the Environment variables "ACCESS_TOKEN" and "APPLICATION_TOKEN" to Codeship.


### Generate your Access Token From Beagle User Settings:
  Settings -> Access token -> Generate your new personal access token

![Generate user token](https://beagle-assets.s3.ca-central-1.amazonaws.com/share/usertoken.png)

### Generate your Application Token From Beagle<br></h3>
  Home -> Applications -> Select your application -> Settings -> Application token

![Get application token](https://beagle-assets.s3.ca-central-1.amazonaws.com/share/apptoken.png)


## What is Beagle?

Beagle is an intelligent and holistic platform to make your applications hack-proof. The platform provides continuous and automated Penetration Testing (under human supervision) for organizations, so that they can always stay on top of the cyber threats.

In short, Beagle finds out how deep your system can be penetrated. Know it before the hackers do! 

* [Beagle Security](https://beaglesecurity.com/) - Visit for more Details!

## Deployment

Following steps will help you to configure beagle penetration testing in your project

#### Creating Environment Variables
In-order to trigger beagle penetration testing you need to create two environment variables. 

1. Login to CODESHIP
2. Select your project
3. Go to project settings 
	![Project Settings](/images/env1.png)
5. Navigate to Environment
	![Environment](/images/env2.png)
6. Add tokens, make sure you use environment variable names as follows:
	* For Access Token -> ACCESS_TOKEN
	* For Application Token -> APPLICATION_TOKEN
	* Final View 
	![Step 3](/images/env3.png)
	* Save Configuration

#### Setup Deployment Script
In-order to trigger beagle penetration testing you need to setup deploy script. 

1. Go to project settings 
	![Project Settings](/images/env1.png)
2. Navigate to Deploy
3. Select your branch to deploy
	![Deploy Home](/images/deploy1.png)
4. After selecting branch scroll down to Add Deployment and select Script
	![Add Deployment](/images/deploy2.png)
5. Add the following snippet to Deployment Commands
	```
	curl --silent -L https://git.io/fjXpj | bash -s
	```
	![Set Custom Command](/images/deploy3.png)
	* click on Create Deployment

6. Build the project! 
 
## Authors

* **Beagle Security**

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details