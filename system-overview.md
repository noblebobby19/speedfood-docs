SpeedFood - System Overview
1. Project Overview
SpeedFood is a multi-platform food ordering and delivery system designed to help users conveniently order food through web and mobile applications without needing to physically visit restaurants or food stores.
The platform acts as an intermediary service between customers and delivery drivers. Customers can browse food items, place orders, and track delivery progress in real time. Delivery staffs receive order notifications, accept available orders, purchase the requested food, and deliver it directly to customers.
The system supports both web and mobile platforms to increase accessibility for customers and delivery drivers.

2. System Objectives
The main objectives of SpeedFood are:
-Help users save time and effort when ordering food.
-Provide a convenient food ordering experience through web and mobile applications.
-Support realtime order processing and delivery updates.
-Allow delivery drivers to receive and manage orders efficiently.
Build a scalable food delivery platform architecture using modern technologies.

3. System Actors
3.1 Guest
Guests can:
-Browse food items
-Search foods
-View categories
-View food details
Guests are not allowed to place orders until they create an account and log in.


3.2 Customer
Customers can:
-Register and log in
-Browse foods
-Search foods by category or keyword
-Add foods to cart
-Place orders
-Select payment methods
-Track order status in realtime
-View order history

3.3 Delivery
Delivery drivers are responsible for handling delivery operations.
Delivery drivers can:
-Receive realtime order notifications
-Accept available orders
-View assigned orders
-Update delivery status
-Deliver food to customers
Delivery drivers can access the platform using mobile applications.

3.4 Admin
Admins manage the overall system.
Admins can:
-Manage users
-Manage staffs
-Manage foods
-Manage categories
-Monitor orders
-Update system information



4. Main Features
Authentication System
-JWT-based authentication
-Role-based authorization
-Secure login and registration

Food Browsing System
-Browse food items
-Search foods
-Filter by categories
-View food details

Cart System
-Add foods to cart
-Update quantities
-Remove items from cart
-Calculate total price

Order System
-Create orders
-Realtime order processing
-Staff assignment
-Order status tracking

Delivery Management
-Broadcast new orders to available staffs
-Staff order acceptance system
-Delivery status updates



Payment System
Supported payment methods:
-Cash on Delivery (COD)
-Bank Transfer

5. Architecture Overview
SpeedFood follows a multi-platform client-server architecture.

The system consists of:
-React Admin Web Application
-Flutter Mobile Application
-REST API Backend Server
-Realtime Communication Server
-MongoDB Database
-Cloudinary Image Storage

The backend server acts as the central system that handles:
-Authentication
-Business logic
-Order processing
-Delivery assignment
-Payment processing
-Realtime communication

6. Platforms
React Web Application
The web application is designed specifically for administrators.
Main functionalities include:
-User management
-Delivery driver management
-Food management
-Category management
-Order monitoring
-System administration

Flutter Mobile Application
The mobile application supports:
-Guest browsing
-Customer food ordering
-Delivery driver order management
-Realtime order updates

7. Order Workflow
The main workflow of the system is:
1.Customer places an order.
2.The system creates a new order with pending status.
3.Available staffs receive realtime order notifications.
4.One staff accepts the order.
5.The system assigns the order to the selected staff.
6.Staff purchases the requested food.
7.Staff delivers the food to the customer.
8.Customer receives the order and completes payment if using COD.
9.The order status becomes completed.

8. Delivery Fee Strategy
SpeedFood uses a distance-based delivery fee model.
The delivery fee is calculated based on the distance between the customer location and the food store location.
Example delivery fee ranges:
Distance	Delivery Fee
0 - 2 km	10,000 VND
2 - 5 km	15,000 VND
5 - 8 km	20,000 VND
More than 8 km	25,000 VND
The total order price is calculated using:
Total Price = Food Total + Delivery Fee
This pricing strategy helps balance delivery costs while maintaining a reasonable customer experience.




9. Realtime Features
SpeedFood uses Socket.IO for realtime communication.
Realtime features include:
-New order notifications
-Order acceptance updates
-Delivery status updates
-Customer order tracking

10. Food Categories
The platform supports multiple food categories such as:
-Rice
-Pho
-Noodles
-Drinks
-Fast Food
Additional categories can be added by administrators.

11. Technology Overview
Frontend
-React.js
-Flutter

Backend
-Node.js
-Express.js

Database
-MongoDB Atlas

Realtime Communication
-Socket.IO

Image Storage
-Cloudinary

12. Future Improvements
Possible future enhancements include:
-Online payment gateway integration
-GPS tracking system
-Push notifications
-AI-based food recommendations
-Dedicated delivery application for staffs
-Restaurant partner management