# paxmoney-legal
Authentication: Firebase Auth (Email/Password & Google Sign-In). Collects Name, Email, and Photo URL.
Database: Firebase Firestore. Stores financial portfolios, transactions, accounts, and dividends linked to a User ID.
AI & Processing: Google Gemini API (@google/genai). Used to process uploaded images/PDFs for data extraction and generate forecasts. Data is sent to Google's servers for inference.
Financial Data: The app calls multiple third-party APIs (Brapi, CoinGecko, CoinMarketCap, TwelveData, EODHD, Alpha Vantage, Massive). It sends ticker symbols to these services but does not appear to send user PII (Personally Identifiable Information) to them.
Analytics: Firebase configuration includes a measurementId, indicating Google Analytics for Firebase is active.
Local Storage: Used for UI preferences (Theme, Branding, Language).
1. Privacy Policy
Last Updated: [Date]
1. Introduction
PaxMoney ("we," "our," or "us") is committed to protecting your privacy. This Privacy Policy explains how our mobile application collects, uses, and safeguards your information. By using PaxMoney, you agree to the collection and use of information in accordance with this policy.
2. Data We Collect
We collect the following types of data to provide the application's functionality:
Contact Information: When you create an account, we collect your Name, Email Address, and Profile Picture (if signing in via Google).
Financial Information: You voluntarily input data regarding your investment portfolios, including asset tickers, quantities, purchase prices, transaction dates, and dividend history.
User Content: If you use the "Import" feature, you may upload PDF files or images (e.g., brokerage statements). These files are processed to extract transaction data.
Identifiers: We collect a unique User ID and Device ID to manage your account and authentication state.
Usage Data: We collect anonymous data on how you interact with the app (e.g., screens visited, features used) to improve performance.
3. How We Use Your Data
App Functionality: To store your portfolio, calculate performance metrics (Profit/Loss, Yield), and sync data across your devices via Google Firebase.
AI Features: If you upload documents or request forecasts, the specific data required for that task (image data or dividend history) is processed using Google Gemini AI.
Market Data: We use the ticker symbols you add to fetch public market prices from third-party financial data providers. We do not send your personal identity to these providers.
4. Data Sharing and Third Parties
We do not sell your personal data. We share data only with the following service providers essential to the app's operation:
Google Firebase: For authentication, database storage, and hosting.
Google Gemini (AI): For processing text/image recognition and generating financial summaries.
Financial Data APIs: We query APIs (such as CoinGecko, Brapi, TwelveData) to retrieve asset prices. These requests contain asset symbols but are not linked to your user identity.
5. Data Retention and Deletion
Retention: We retain your data as long as your account is active.
Account Deletion: You have the right to delete your account and all associated data at any time directly within the app (Settings > Personal Details > Delete Account). Upon confirmation, your data is permanently removed from our databases.
6. Children’s Privacy
Our Service does not address anyone under the age of 13. We do not knowingly collect personally identifiable information from anyone under the age of 13.
7. Changes to This Policy
We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page.
8. Contact Us
If you have any questions about this Privacy Policy, please contact us at: [Your Support Email]
2. Terms and Conditions
Last Updated: [Date]
1. Acceptance of Terms
By downloading or using the PaxMoney app, these terms will automatically apply to you. You should make sure therefore that you read them carefully before using the app.
2. Nature of Service (Not Financial Advice)
PaxMoney is a portfolio tracking and visualization tool only.
No Advice: The content, calculations, AI-generated forecasts, and data provided by the app are for informational purposes only and do not constitute financial, investment, legal, or tax advice.
Accuracy: While we strive to provide accurate market data via third-party APIs, we cannot guarantee the accuracy, completeness, or timeliness of asset prices, dividend data, or AI interpretations.
Risk: You are solely responsible for your investment decisions. We are not liable for any financial losses or damages arising from your use of the app or reliance on its data.
3. User Accounts
You are responsible for maintaining the confidentiality of your login credentials (email/password).
You accept responsibility for all activities that occur under your account.
We reserve the right to terminate accounts that violate these terms or engage in illegal activity.
4. Artificial Intelligence (AI) Features
The app utilizes Artificial Intelligence (Google Gemini) to extract data from files and generate summaries. AI can make mistakes ("hallucinations"). You agree to verify all data extracted or generated by the AI against your original documents before relying on it.
5. API Usage
PaxMoney uses public and private APIs to fetch market data.
If you input your own personal API keys into the app settings, you are responsible for adhering to the terms of service of those specific providers (e.g., Alpha Vantage, Twelve Data) and for any usage costs incurred.
6. Intellectual Property
The PaxMoney app, including its original content, features, and functionality, is owned by [Your Name/Company Name] and is protected by international copyright and trademark laws.
7. Limitation of Liability
In no event shall [Your Name/Company Name] be liable for any indirect, incidental, special, consequential, or punitive damages, including without limitation, loss of profits, data, use, goodwill, or other intangible losses, resulting from your access to or use of or inability to access or use the Service.
8. Governing Law
These Terms shall be governed and construed in accordance with the laws of [Your Country/State], without regard to its conflict of law provisions.
3. Data & Security Policy
1. Data Minimization
We only collect data necessary to provide the portfolio tracking service. We do not collect physical addresses, phone numbers, or credit card numbers directly within the app.
2. Encryption
In Transit: All data transmitted between the App, Firebase, and third-party APIs is encrypted using Transport Layer Security (TLS/SSL).
At Rest: User data stored in Google Firestore is encrypted at rest by our cloud provider (Google Cloud Platform).
3. Access Control
Authentication: Access to user data is strictly gated by Firebase Authentication.
Database Rules: We utilize Firestore Security Rules to ensure that users can only read and write data belonging to their own User ID (UID), or data explicitly shared via the "Joint Dashboard" feature.
4. Third-Party API Keys
If you choose to save custom API keys (e.g., for Alpha Vantage or OpenAI) within the app settings, these keys are stored in your private user document in the database. We do not use your personal keys for other users.
5. Incident Response
In the unlikely event of a data breach, we will notify affected users via their registered email address within 72 hours of becoming aware of the breach, in accordance with applicable laws.
Apple App Store: App Privacy Details Summary
When submitting to the App Store, you will need to fill out the "App Privacy" section. Based on your code, here is the mapping:
1. Data Linked to You
The following data may be collected and linked to the user's identity:
Contact Info: Email Address, Name.
User Content: Other User Content (Financial Holdings, Transactions, Uploaded Files).
Identifiers: User ID, Device ID.
2. Data Not Linked to You
The following data may be collected but is not linked to the user's identity (if anonymized correctly):
Usage Data: Product Interaction (via Firebase Analytics).
Diagnostics: Crash Data (via Firebase Crashlytics).
3. Tracking
No: Based on the code, you do not appear to use IDFA (Identifier for Advertisers) or third-party advertising SDKs (like AdMob or Facebook Ads) to track users across other companies' apps and websites. Answer No to Tracking.
Submission Warnings
Account Deletion (Guideline 5.1.1(v)):
Status: ok Compliant. Your code contains UserProfileModal.tsx which includes a handleDeleteAccount function calling user.delete(). This is a strict requirement for Apple and you have it implemented.
API Key Usage:
Observation: Your config.ts contains hardcoded "Default" API keys (DEFAULT_BRAPI_API_KEY, etc.).
Warning: While not strictly an App Store rejection reason, if these keys have usage limits or billing attached to you, releasing them in a public app can lead to them being scraped or your quotas being exhausted immediately. It is highly recommended to use a proxy backend or force users to enter their own keys to avoid service disruption.
Finance Category:
Since this is a Finance app, Apple Reviewers are stricter. Ensure the "Not Financial Advice" disclaimer is visible in the app (e.g., on the login screen footer or settings menu), not just in the Terms document.
