
# Queue Service

Create a simple backend queue service. Queue consumers should be able to create a queue, send a message to the queue, receive a message to the queue and tell the queue it’s done processing and to delete the message. Unlike a pub/sub model, end users of this queue should be responsible for receiving and deleting messages, using polling or another alternative.

This should be a web server that exposes the following 4 methods:

| URL | Request Params | Return |
| ------------- | ------------- | ------------- |
| /CreateQueue  | queueName | created |
| /SendMessage  | queueName, delayInMS, message | messageId |
| /ReceiveMessage | queueName  | messageId,message |
| /DeleteMessage  | queueName, messageId | wasDeleted |


Use any languages, libraries, or frameworks, except for the queue itself which should be mostly your own invention.

Please additionally include in your submission:
* Readme, including what you would have done if you had more time.
* Unit tests.
