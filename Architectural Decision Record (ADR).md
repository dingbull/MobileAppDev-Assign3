Architectural Decision Record (ADR)

**Student Name: Rolan Ho**

**Student ID: 000888473**

**Architectural Decision Record (ADR) for Scenario 1**

1. Title: New Mobile App for a Retail Company

2. Status: Proposed

3. Context: We are developing a new mobile app for a retail company with features such as product browsing, order tracking, loyalty programs, push notifications, payment gateways, user behavior tracking, image optimization, and multilingual support.

4. Decision:

a. Native, web, or hybrid app: We will develop a native app to leverage platform-specific advantages like better performance, access to device-specific functionalities, and enhanced user experience.

b. UI Framework: React Native – this will allow us to develop for both iOS and Android platforms simultaneously, yet achieve near-native performance.

c. Backend language: Node.js with Express.js framework. It's lightweight, fast, and can handle multiple simultaneous connections.

d. Permissions:

1. Internet Access for syncing data.
2. Push Notifications to send order updates, offers, etc.
3. Access to storage for caching product images for offline use.

e. Data Storage:

1. Local SQLite database for offline mode to store product details and order history.
2. Cloud Firestore for cloud storage, given its offline capabilities and real-time sync.

f. Additional frameworks or technology stacks:

1. Firebase Cloud Messaging for push notifications.
2. Stripe and PayPal for payment gateway integrations.
3. Google Analytics for tracking user behavior.
4. Cloudinary for image optimization and storage.
5. Flutter's intl package for multilingual support.

5. Rationale:

a. A native app provides the performance and usability required for the app's complex features and regular usage.

b. React Native allows code reuse between iOS and Android, reducing development time and ensuring consistent behavior across platforms.

c. Node.js is asynchronous, making it perfect for handling multiple payment gateway interactions and database operations.

d. Permissions have been chosen considering the app's features and user privacy.

e. SQLite is lightweight and perfect for offline storage. Firestore allows for real-time sync, scalability, and offline capabilities.

f. The selected frameworks and stacks are industry leaders in their respective domains, ensuring reliability and performance.

6. Consequences: Using the above architectures and decisions will enable faster development with efficient performance. Regular updates and maintenance would be required to keep up with platform and third-party service changes.
