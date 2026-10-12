<img width="1450" height="310" alt="image" src="https://github.com/user-attachments/assets/fea11098-c5fb-4219-89d4-acbc2e359e67" />

<img width="1156" height="738" alt="image" src="https://github.com/user-attachments/assets/8b6d0594-18b9-4046-988d-965851311f17" />

<img width="1150" height="721" alt="image" src="https://github.com/user-attachments/assets/22eba3d4-7866-4023-81af-b9304cd33182" />

<img width="1136" height="708" alt="image" src="https://github.com/user-attachments/assets/2d3b860c-65c7-4c81-83ba-5eb3794d0a69" />

# 1 single framework = Decision Stack
    read cloud brief
    find the real problem
    choose the right aws services
    explain the trade-offs

    from these we will know
    when to use them
    why they fit
    what trade-offs you are making

# decision Stack
    1- Traffic
    2- Compute
    3- Data
    4- Security
    5- Cost
    6- Monitor

<img width="977" height="859" alt="image" src="https://github.com/user-attachments/assets/14a44239-3665-4fa6-a239-b85d45aa45d2" />

<img width="1056" height="664" alt="image" src="https://github.com/user-attachments/assets/9c6bf1f0-319e-4d76-a992-f69174a049d7" />

<img width="870" height="673" alt="image" src="https://github.com/user-attachments/assets/402d5f8b-51cb-4b05-b5fa-c1abfa38d43a" />

<img width="720" height="404" alt="image" src="https://github.com/user-attachments/assets/5a380758-d905-4655-ae00-322b579cb005" />

# 1-TRAFFIC

<img width="1804" height="1012" alt="image" src="https://github.com/user-attachments/assets/36f0a508-0f5d-459b-a579-7ba0ca68131c" />

# 2-COMPUTE
<img width="1725" height="949" alt="image" src="https://github.com/user-attachments/assets/f0c153e1-25bb-4893-b64d-4dbe2090e399" />

# 3-DATA
<img width="1830" height="1023" alt="image" src="https://github.com/user-attachments/assets/28ea37e7-47e8-460e-a53f-3bc0c81bce4c" />

# 4-SECURITY

# 5-COST

# 6-MONITOR

# FINAL
        -1-customer type the url and its device does a DNS LOOKUP free resolves the domain
        and points them to cloudfront. this happens once
        after this its device knows where to go
        2-the request arrives at cloudfront , it checks if it is a real user or maliciious
        cloudfront looks for the app files in a nearest edge location.if they are cached there
        it serves them instantly.if not , it pulls them fresh from S3 and serves them to the user.
        and caches a copy for the next person.
        the app loads on the screen , the user fills in the email and password and sign up
        3- the device sends request to API GATEWAY, WHICH IS PART OF THE BACKEND THAT HAS public@
        API gateway identity that as a signal request and triggers the right lambda function
        4- Lambda runs a signup code .it validates the infos , creates the account,saves user data to dynamoDB.
        Lmabda's IM key card only allows it to write to dynamodb.It can't touch S3, and cant access anything else.
        5- dynamodb confirms that data is saved, lamdba sends confirmation response back through the API gateway
        to the user device, account created, signed up across the bottom.
        6- CloudWatch has been collecting data from every service
        
        it scales automatically
        it costs almost nothing at low traffic
        if something change easy to swap out one layer without rebuilding anything else
<img width="1577" height="974" alt="image" src="https://github.com/user-attachments/assets/c521a6d6-147f-4c4a-b1d4-59d5fb46ee02" />
