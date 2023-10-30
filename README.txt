
===Canvas Add-on for Splunk===
>Splunk Add-on for Canvas API. 

#############################################################
This add-on was developed with Splunk Add-on Builder.
To develop further please install Splunk Add-on Builder.
Import the Canvas Add-on for Splunk to Splunk Add-on Builder.

For more information please visit the site below.
https://docs.splunk.com/Documentation/AddonBuilder
Add-on Builder: https://splunkbase.splunk.com/app/2962
#############################################################

_____________________________________________________________________________________________________________________
-Defined the properties of the data input-
_____________________________________________________________________________________________________________________
# Published Courses #: Gets only new courses added with details and gets total courses periodically from the account.
# Total Teachers #:    Gets total teachers periodically from the account.
# Total Students #:    Gets total students periodically from the account.
# Total Users #:       Gets only new users added with details.
# File Uploaded #:     Gets file details per course periodically.
# File Storage #:      Gets file details per course periodically.
# Media Uploaded #:    Gets total media periodically from the account.
# Media Storage #:     Gets only new media added with details.
_____________________________________________________________________________________________________________________



=====================================================================================================================
-Endpoints-> (Please check https://canvas.instructure.com/doc/api/ for more details.)
_____________________________________________________________________________________________________________________
# Published Courses #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/courses.html]
 https://{subdomain}.instructure.com/api/v1/courses" (To get new course details)
 

[More details about the endpoint below: https://canvas.instructure.com/doc/api/analytics.html]
 https://{subdomain}.instructure.com/api/v1/accounts/{account_id}/analytics/current/statistics"

 https://{subdomain}.instructure.com/api/v1/accounts" (To get the account_id)

---------------------------------------------------------------------------------------------------------------------
# Total Teachers #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/analytics.html] 
 https://{subdomain}.instructure.com/api/v1/accounts/{account_id}/analytics/current/statistics"
    
 https://{subdomain}.instructure.com/api/v1/accounts" (To get the account_id)
    
---------------------------------------------------------------------------------------------------------------------
# Total Students #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/analytics.html]
 https://{subdomain}.instructure.com/api/v1/accounts/{account_id}/analytics/current/statistics"

 https://{subdomain}.instructure.com/api/v1/accounts" (To get the account_id)

---------------------------------------------------------------------------------------------------------------------
# Total Users #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/accounts.html]
 https://{subdomain}.instructure.com/api/v1/accounts"

---------------------------------------------------------------------------------------------------------------------
# File Uploaded #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/files.html]
 https://{subdomain}.instructure.com/api/v1/courses/{course_id}/files"

 https://{subdomain}.instructure.com/api/v1/courses" (To get the course_id)

---------------------------------------------------------------------------------------------------------------------
# File Storage #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/files.html]
 https://{subdomain}.instructure.com/api/v1/courses/{course_id}/files"

 https://{subdomain}.instructure.com/api/v1/courses" (To get the course_id)
---------------------------------------------------------------------------------------------------------------------
# Media Uploaded #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/analytics.html]
 https://{subdomain}.instructure.com/api/v1/accounts/{account_id}/analytics/current/statistics"

 https://{subdomain}.instructure.com/api/v1/accounts" (To get the account_id)

---------------------------------------------------------------------------------------------------------------------
# Media Storage #

[More details about the endpoint below: https://canvas.instructure.com/doc/api/media_objects.html]
 https://{subdomain}.instructure.com/api/v1/media_objects"
_____________________________________________________________________________________________________________________

-How to use-

1.) Go to the Configuration tab. Select Add-on Settings. Please define the subdomain and access token for data input. Click on the save button.
Maximum of 4 settings are allowed. (Use a custom Subdomain and Access Token or Reach out to fdse@splunk.com for an enhancement.)

2.) Go to the Inputs tab. Click Create New Input button. Define the parameters that are required for your data input.
Please use your subdomain to create the base URL to collect data with REST API requests. (https://<VALUE>.instructure.com/api/v1/...)
Please manage API access tokens from your Canvas User Settings in Canvas. Access tokens provide access to Canvas resources through the Canvas API.
Select the Add-on Setup Parameter that you've configured in the first step.

Note: To override the Add-on Setup Parameter Setting with Subdomain 0(custom) and Access Token 0(custom) value. (Add-on Setup Parameter Settings will be set as a Subdomain and Access token if not selected.
So, only click to Override checkbox to use Subdomain 0 and Access Token 0 settings. In case you need more than 4 subdomains.)

Alert: Only GET requests are used in this add-on. The Add-on is not going to change your data in your Canvas account. 
Alert: Please protect your Access Tokens. Don't share them with anyone. Set an expiration date for your access tokens.

------------------------------------------------------------------------
Please reach out to FSDE@splunk.com for further development.
https://gitlab.com/splunk-fdse/modular-inputs/canvas-add-on-for-splunk
The project is still going on. (ggokdemir@splunk.com || fdse@splunk.com)

