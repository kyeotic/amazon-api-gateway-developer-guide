# Build an API Gateway API with Lambda Integration<a name="getting-started-with-lambda-integration"></a>

 To build an API with Lambda integrations, you can use either the Lambda proxy integration or the Lambda custom integration\. In general, you should use the Lambda proxy integration for a nimble and streamlined API set up while providing versatile and powerful features\. The custom integration may be a better value proposition if it is necessary for API Gateway to pre\-process incoming request data before it reaches to the backend Lambda function\. However, it is a legacy technology\. Setting up a Lambda custom integration is more involved than setting up the Lambda proxy integration and the existing setup is likely to be inoperable when the backend Lambda function requires changes in its input or output\. 

 With the Lambda proxy integration, the input to the integrated Lambda function can be expressed as any combination of request headers, path variables, query string parameters, and body\. In addition, the Lambda function can use the API configuration settings to influence its execution logic\. For an API developer, setting up a Lambda proxy integration is simple\. Other than choosing a particular Lambda function in a given region, you have little else to do\. API Gateway configures the integration request and integration response for you\. Once set up, the integrated API method can evolve with the backend without modifying the existing settings\. This is possible because the backend Lambda function developer parses the incoming request data and responds with desired results to the client when nothing goes wrong or responds with error messages when anything goes wrong\. 

 With the Lambda custom integration, you must ensure that the input to the Lambda function is supplied as the integration request payload\. This implies that you, as an API developer, must map any input data the client supplied as request parameters into the proper integration request body\. You may also need to translate the client\-supplied request body into a format recognized by the Lambda function\. 

**Topics**
+ [Build an API Gateway API with Lambda Proxy Integration](api-gateway-create-api-as-simple-proxy-for-lambda.md)
+ [Build an API Gateway API with Cross\-Account Lambda Proxy Integration](apigateway-cross-account-lambda-integrations.md)
+ [Build an API Gateway API with Custom Lambda Integration](getting-started-lambda-non-proxy-integration.md)