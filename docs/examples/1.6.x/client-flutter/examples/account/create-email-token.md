import 'package:appwrite/appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

Account account = Account(client);

Token result = await account.createEmailToken(
    userId: '<USER_ID>',
    email: 'email@example.com',
    phrase: false, // optional
);