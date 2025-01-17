Media Mart – Our One-Stop E-Commerce Store
Our Goals & Business Focus:
Media Mart, developed by GIAIC and powered by our team of 18 professionals, is a 
modern e-commerce platform specializing in:
• Home Decor
• Kitchen Gadgets
• Electronic Gadgets
• Perfumes
• Health and Beauty Products
Our primary goal is to provide a user-friendly, efficient, and modern shopping 
experience. Key features include:
• Real-time product updates.
• Seamless cart and checkout processes.
• A responsive interface designed for both desktop and mobile users.
Technical Planning for Media Mart
1. System Architecture Overview
Frontend (Next.js)
• A responsive and user-friendly interface.
• Essential pages:
o Home: Overview of categories, featured products, and promotions.
o Product Listing: Display products in each category.
o Product Details: Detailed product descriptions and features.
o Cart: Manage selected items before checkout.
o Order Confirmation: Confirm and review order details after purchase.
Sanity CMS (Backend)
• Centralized system for managing product data, customer information, and order 
records.
• Acts as the primary database for the e-commerce store.
Third-Party APIs
• APIs for payment gateways, shipment tracking, and backend services to 
ensure real-time updates.
Data Flow
• Frontend interacts with Sanity CMS through Product Data APIs.
• Third-party APIs manage payments and shipment tracking.
2. Key Workflows
Browsing Products
1. Users visit Media Mart’s website to browse available products.
2. The frontend fetches product details via the Product Data API from Sanity CMS.
Adding Products to Cart
1. Users select items and add them to the cart.
2. Cart data is managed via Sanity CMS.
Placing Orders
1. Users confirm orders and make payments through third-party payment gateway 
APIs.
2. Order details are stored in Sanity CMS, while shipment details are managed via 
shipment tracking APIs.
3. API Endpoints
Product Data API
• Endpoint: /products
• Method: GET
• Description: Fetch all available products from Sanity CMS.
• Response: Returns product details (ID, Name, Price, Stock, Image).
Order API
• Endpoint: /orders
• Method: POST
• Description: Create a new order.
• Payload: Includes customer info, product details, and payment status.
Shipment API
• Endpoint: /shipment
• Method: GET
• Description: Track order shipment status via a third-party API.
• Response: Includes Shipment ID, Order ID, Status, and Expected Delivery Date.
4. Sanity CMS Schema Examples
Product Schema
• Fields:
o id: Unique product identifier.
o name: Product name.
o price: Product price.
o stock: Available stock quantity.
o image: Product image URL.
o description: Product description.
Order Schema
• Fields:
o orderId: Unique order identifier.
o customerId: Customer ID.
o orderDetails: List of products in the order.
o status: Order status (e.g., Pending, Shipped, Delivered).
o paymentInfo: Payment method and status.
Features for Local Drop shipping in Pakistan
1. Localized Focus: Products tailored to Pakistani customers’ needs and 
preferences.
2. Efficient Payment Options: Integration with local payment gateways such as 
Easypaisa and Jazz Cash.
3. Real-Time Updates: Immediate inventory and order status updates.
4. Customer Support: Accessible support for queries and assistance in Urdu and 
English.
By focusing on these features and workflows, Media Mart aims to establish itself as a 
leading local e-commerce platform, delivering quality products and a hassle-free 
shopping experience
API Endpoints:
API name Endpoint Method Description Request 
Payload Response
Product 
Data API /products GET
Fetch all 
available 
products 
from sanity 
CMS
N/A
Product 
details(ID,n
ame,price,s
tock,image)
Order API /orders POST Create a 
new order.
Customer 
info, 
product 
details, 
payment 
status.
Order 
confirmatio
n or error 
message
Shipment 
API /shipment GET
Track order 
status via a 
third-party 
API.
N/A
Shipment 
ID, Order 
ID, Status, 
Expected 
Delivery 
Date.
Rental 
Manageme
nt API
/rentalduration POST
Add rental 
details for a 
specific 
product
{ "productid
": 456, 
"duration": 
"7 days", 
"deposit": 
500 }
Confirmatio
n or 
validation 
error.
Product Schema:
Field Name Type Description
id string Unique identifier for the 
product.
name string Name of the product.
price number Price of the product.
stock number Number of units in stock.
image image Product image.
description text
Detailed product 
description.
Order Schema:
Field Name Type Description
orderId string Unique identifier for the 
order.
customerId string Unique identifier for the 
customer.
orderDetails array
List of products in the 
order.
status string Status of the order (e.g., 
pending, completed)
paymentInfo object
Payment-related 
information (e.g., method, 
status).
Rental Schema:
Field Name Type Description
productId string Identifier for the rented 
product.
rentalDescription string Duration of the rental 
period.
depositeAmount number Amount of deposit for the 
rental
conditionStatus string Condition of the product 
post-rental.
Technical Roadmap
• Design Sanity CMS schemas aligned with categories and products specific to 
Media Mart.
• Implement API endpoints for real-time product data retrieval and order 
management.
• Develop a responsive frontend using Next.js with dynamic rendering of 
product data.
• Integrate third-party APIs for secure payments and shipment tracking to ensure 
a seamless customer experience.
• Test all workflows thoroughly, including browsing, cart management, checkout, 
and order tracking.
Proposed Design and Architecture
Frontend Development
• Framework: Next.js for server-side rendering, enhanced SEO, and better 
performance.
• Styling: Tailwind CSS to ensure a modern and responsive UI.
• Features:
o Mobile-first design to enhance usability across devices.
o Dynamic content rendering powered by TypeScript for robust and 
efficient data handling.
Backend Development
• Framework: Node.js with Express.js for managing scalable and efficient APIs.
• Content Management: Sanity CMS for:
o Storing product details (e.g., name, price, categories, tags, and media).
o Managing real-time updates (e.g., pricing or stock levels).
Third-Party API Integrations
• Payment Gateway: Integration with Stripe and Razor pay for secure online 
transactions.
• Shipment Tracking: Integration with FedEx and DHL APIs for real-time tracking 
updates.
• Tax and Currency Conversion APIs: To enable localized pricing for Pakistani 
customers.
Key Features and Workflows
User Registration and Login
• Secure registration and login functionality with encrypted user data storage.
Product Browsing
• Products categorized under Home Decor, Kitchen Gadgets, Electronic 
Gadgets, Perfumes, Health & Beauty for easy navigation.
• Real-time updates through Sanity CMS to display fresh and accurate product 
information.
Cart and Order Placement
• Users can add items to their cart, view their cart, and proceed to a secure 
checkout process.
• Checkout includes multiple payment options and shipping methods tailored to 
local needs.
Shipment Tracking
• Real-time tracking of orders via shipment APIs integrated with FedEx and DHL.
API Design:
API Name Endpoint Method Description Request 
Payload
Authentication 
API /Api/auth/login POST User login
{ "email": 
"user@exampl
e.com", 
"password": 
"*******" }
/Api/auth/regis
ter
POST User 
registration
{ "name": "John 
Doe", "email": 
"user@exampl
e.com", 
"password": 
"*******" }
Cart and 
Checkout API /Api/cart/add POST Add items to 
the cart
{ "productId": 
"123", 
"quantity": 2 }
/Api/cart GET View cart 
items N/A
/Api/orders/ch
eckout POST Checkout and 
create an order
{ "customer 
Info": {...}, 
"payment 
Details": {...}, 
"items": [...] }
Shipping API
/Api/shipp
ing/track/
{id}
GET
Track order 
shipment 
status
N/A
Visual Structure (UI/UX Design)
Homepage
• Hero Section: Highlight top categories (Home Décor, Kitchen Gadgets, Health 
& Beauty, Perfumes, Electronic Gadgets).
• Featured Products: Showcase current offers and trending items.
Product Page
• High-quality product images with zoom-in functionality.
• Dynamic details such as name, price, stock, description, and variants.
Cart and Checkout
• A clean cart view with a detailed price breakdown, including taxes and shipping 
fees.
• Secure checkout with options like COD (Cash on Delivery) and online 
payments.
Order Tracking
• A dedicated tracking page with shipment updates, order status, and delivery 
timelines.
Sketch 01(Center part)
Sketch 02 (Right Part)
Sketch 03 (Left Part)
Our Teams:
⦁ Mohsin Raza: Director of Agency
⦁ Afsheen: CEO & Director of Agency
⦁ Abu Bakar: Senior Coordinator & Full Stack Developer
⦁ Saad: Managing Head & Web Developer
⦁ Rahat Bano: Designing Head & Web Developer
⦁ Haroon: Marketing Manager & Web Developer
⦁ Yusra Waheed: Senior Web Developer
⦁ Hamza Bhatti: Marketing Manager & Senior Developer
⦁ Nida: Senior Developer & Marketing Executive
⦁ Saima Waheed: Senior Developer & AI Specialist
⦁ Farrukh: Senior Developer
⦁ Saira Nadeem: Social Media Marketer & Senior Developer
⦁ Amna Imad: Web Developer
⦁ Qaim Uddin Khawaja: Web Developer
⦁ Dua Ali Khan: Web Developer
⦁ Faizan: Expert Video Editor
⦁ Yusra Khan Zai: Senior Developer
⦁ Abdul Salam: Senior Developer & Marketing Executive
Conclusion:
This e-commerce architecture seamlessly integrates a responsive frontend, robust 
CMS, and efficient APIs to deliver smooth shopping experiences, from browsing to 
order fulfilment.
Best Regards: 
WEB & MEDIA TEAMS
