# PythonChatbot
based around:
https://developer.webex.com/blog/blog-details-8110.html


Start ngrok within the venv directory with:

ngrok http -host-header=rewrite localhost:10010

Enable webex webhook through the following:
https://developer.webex.com/endpoint-webhooks-post.html
("secret" is "Bot ID")
Should follow this format:

{
"id": "Y2lz111111112222222233333333",
"name": "BotDemo Project ROOMNAME",
"targetUrl": "http://ec2-10-20-30-40.us-west-2.compute.amazonaws.com:10010",
"resource": "messages",
"event": "created",
"filter": "roomId=Y2lz12345678901234567890"
}


Will only work in the roomid used. Find roomId using:

https://developer.webex.com/endpoint-rooms-get.html
