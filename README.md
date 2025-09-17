# aws-websocket-api

Build a real-time chat app using AWS WebSocket API + DynamoDB + Python Lambdas:--



Architecture AWS WebSocket API:

1.API Gateway WebSocket API routes: $connect, $disconnect, sendMessage

2.Each route → Python Lambda

3.Lambdas store connection IDs in DynamoDB and broadcast with ApiGatewayManagementApi.post_to_connection

4.Client connects to wss://<api-id>.execute-api.<region>.amazonaws.com/<stage>
