### REST API (Representational State Transfer Application Programming Interface)
**REST API**
  - It's a way for **two systems to talk to each other** over the internet.
  - one system (website/app) can **ask for data or send data** to another system(database/backend)
  - It uses standard web methods like:
    - GET (to read data)
    - POST (to create data)
    - PUT (to update data)
    - DELETE (to remove data)
  - think of it like placing an order at a restaurant:
      - Customer(client) ask for food(data)
      - The waiter(API) takes customer request to the kitchen(server)
      - the kitchen prepares the food and sends it back to customer
        
**REST API in PIM**
  - 1) The **REST API** allows external applications(websites/mobile apps/other systems) to access product data stored in Product 360.
  - 2) Actual APIs we can use to interact with Product 360:
      - **List API:** Get lists of products or other data.
          - allowed REST API methods: **GET, POST, DELETE**
          - Used to read, write and delete data from Product 360
          - to make data selection quicker: **Reports**
          - to further filter report results: **Search query language**
      - **Management API:** Create, update, or delete product data.
          - allowed REST API methods: GET, POST
          - Used to interact with P360 functions such as tasks, merges, exports and data quality.
      - **Meta API:** Get metadata(like structure or configuration info)
          - allowed REST API methods: **GET**
          - Meta API provides **Product 360 repository** information including entity(main object type: article), field(attributes inside an entity: id, supplierID) and enumerations(predefined lists of values for a field: auditflag->approved/pending/rejected) details
          - Useful for finding field identifies, qualifiers(Extra conditions or rules for fields) and enumeration values
          - **Real world example**
              - Suppose you want to build a product upload tool for your e-commerce site:
                  - First, call Meta API to get the structure of Article entity.
                  - We learn that Article has fields like Id, Name, Price, and AuditFlag.
                  - We also learn that AuditFlag can only be Approved or Pending
                  - Now our tool can validate data before sending it to Product 360.

      - **Media API:** Access product images, videos, or other media files.
          - allowed REST API methods: GET
          - Used to access all kinds of Media Asset
  - 3) These are features or data sets that we can access through those APIs. They describe what you can get or do:
      - **Reports** → Predefined reports (e.g., top-selling products).
      - **Search Query Language** → Advanced search for products (e.g., “all laptops under ₹50,000”).
      - **Data Model Info** → Details about entities, fields, properties (helps you understand the structure).
      - **Media Files** → Actual product images or videos.


  - 4) **Scenario**
      - Our company sells clothes online. All product information (like names, sizes, colors, prices, and images) is stored in **Informatica Product 360**
      - Now, our team is building a **mobile app** and wants to show product listings to customers. Instead of manually copying product data, we want the app to **automatically fetch product info** from Product 360.
----------------------------------------------------------------------------------   
