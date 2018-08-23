# AzureBotClientSample
Interacting with Azure BOT Service through DirectLine / Mock Channel for validating BOT deployments. 
# Direct Line
Directline client library is provided by Microsoft for connecting to BOT Service. The solution utilizes it for communicating with BOT. This approach however is slower and is less preferred than using the Mock Channel approach. The solution has example code for DirectLine as well just as a reference. It is suitable for use in Functional testing to run short tests to validate few inputs to BOT. Remember, this approach is slower and not suitable when we want to run a test which contains hundreds of input values to the BOT, which is the case most of the time as we have to validate several thousand inputs that the user can provide to the BOT 

# MockChannel 
This approach uses an intermediate service which can be called by the BOT service. This we call it as the CallBackService as we provide the endpoint of this service to BOT when sending a message, the BOT then calls this CallBackService with its response to be processed by the same. This approach is faster and is suitable for use in functional / load & performance testing scenarios. 
