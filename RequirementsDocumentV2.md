# Requirements Document - future EZElectronics

Date: 04/05/2024

Version: V2 - description of EZElectronics in FUTURE form (as proposed by the team)

| Version number | Change |
| :------------: | :----: |
|       2.1         |   2     |

# Contents

- [Requirements Document - future EZElectronics](#requirements-document---future-ezelectronics)
- [Contents](#contents)
- [Informal description](#informal-description)
- [Stakeholders](#stakeholders)
- [Context Diagram and interfaces](#context-diagram-and-interfaces)
  - [Context Diagram](#context-diagram)
  - [Interfaces](#interfaces)
- [Stories and personas](#stories-and-personas)
- [Functional and non functional requirements](#functional-and-non-functional-requirements)
  - [Functional Requirements](#functional-requirements)
  - [Non Functional Requirements](#non-functional-requirements)
- [Use case diagram and use cases](#use-case-diagram-and-use-cases)
  - [Use case diagram](#use-case-diagram)
    - [Use case 1, Login (UC1)](#use-case-1-login-uc1)
      - [Scenario 1.1](#scenario-11)
      - [Scenario 1.2](#scenario-12)
      - [Scenario 1.3](#scenario-13)
    - [Use case 2, Logout (UC2)](#use-case-2-logout-uc2)
        - [Scenario 2.1](#scenario-21)
    - [Use case 3, Register (UC3)](#use-case-3-register-uc3)
      - [Scenario 3.1](#scenario-31)
      - [Scenario 3.2](#scenario-32)
    - [Use case 4, Search user (UC4)](#use-case-4-search-user-uc4)
      - [Scenario 4.1](#scenario-41)
      - [Scenario 4.2](#scenario-42)
      - [Scenario 4.3](#scenario-43)
    - [Use case 5, Delete user (UC5)](#use-case-5-delete-user-uc5)
      - [Scenario 5.1](#scenario-51)
      - [Scenario 5.2](#scenario-52)
    - [Use case 6, Define privileges (UC6)](#use-case-6-define-privileges-uc6)
      - [Scenario 6.1](#scenario-61)
      - [Scenario 6.2](#scenario-62)
    - [Use case 7, Register product (UC7)](#use-case-7-register-product-uc7)
      - [Scenario 7.1](#scenario-71)
      - [Scenario 7.2](#scenario-72)
    - [Use case 8, Delete product (UC8)](#use-case-8-delete-product-uc8)
      - [Scenario 8.1](#scenario-81)
      - [Scenario 8.2](#scenario-82)
    - [Use case 9, Sell product (UC9)](#use-case-9-sell-product-uc9)
      - [Scenario 9.1](#scenario-91)
      - [Scenario 9.2](#scenario-92)
    - [Use case 10, Edit product (UC10)](#use-case-10-edit-product-uc10)
      - [Scenario 10.1](#scenario-101)
      - [Scenario 10.2](#scenario-102)
    - [Use case 11, Show by category (UC11)](#use-case-11-show-by-category-uc11)
      - [Scenario 11.1](#scenario-111)
      - [Scenario 11.2](#scenario-112)
    - [Use case 12, Show by model (UC12)](#use-case-12-show-by-model-uc12)
      - [Scenario 12.1](#scenario-121)
      - [Scenario 12.2](#scenario-122)
    - [Use case 13, Show by product code (UC13)](#use-case-13-show-by-product-code-uc13)
      - [Scenario 13.1](#scenario-131)
      - [Scenario 13.2](#scenario-132)
    - [Use case 14, Show cart (UC14)](#use-case-14-show-cart-uc14)
      - [Scenario 14.1](#scenario-141)
      - [Scenario 14.2](#scenario-142)
    - [Use case 15, Checkout cart (UC15)](#use-case-15-checkout-cart-uc15)
      - [Scenario 15.1](#scenario-151)
      - [Scenario 15.2](#scenario-152)
    - [Use case 16, Add to cart (UC14)](#use-case-16-add-to-cart-uc16)
      - [Scenario 16.1](#scenario-161)
      - [Scenario 16.2](#scenario-162)
    - [Use case 17, Remove from cart (UC17)](#use-case-17-remove-from-cart-uc17)
      - [Scenario 17.1](#scenario-171)
      - [Scenario 17.2](#scenario-172)
    - [Use case 18, Delete cart (UC18)](#use-case-18-delete-cart-uc18)
      - [Scenario 18.1](#scenario-181)
      - [Scenario 18.2](#scenario-182)
    - [Use case 19, Support inquiries (UC19)](#use-case-19-support-inquiries-uc19)
      - [Scenario 19.1](#scenario-191)
      - [Scenario 19.2](#scenario-192)
    - [Use case 20, Send promotional offers (UC20)](#use-case-20-send-promotional-offers-uc20)
      - [Scenario 20.1](#scenario-201)
      - [Scenario 20.2](#scenario-202)
    - [Use case 21, Analyze sales (UC21)](#use-case-21-analyze-sales-uc21)
      - [Scenario 21.1](#scenario-211)
      - [Scenario 21.2](#scenario-212)
- [Glossary](#glossary)
- [System Design](#system-design)
- [Deployment Diagram](#deployment-diagram)

# Informal description

EZElectronics (read EaSy Electronics) is a software application designed to help managers of electronics stores to manage their products and offer them to customers through a dedicated website. Managers can assess the available products, record new ones, and confirm purchases. Customers can see available products, add them to a cart and see the history of their past purchases.

# Stakeholders

| Stakeholder name | Description |
| :--------------: | :---------: |
| Customer |      Individuals who use the application to browse and purchase electronics products.      |
| Manager |      Individuals who can manage the products and their arrivals.     |
| Start up company  |     Entities that purchase or commission the development of the EZElectronics application for use within their electronic stores or retail chains.       |
| Admin |       Developers responsible for building, maintaining, and updating the EZElectronics application, translating requirements into code and ensuring its functionality, reliability, and scalability.     |
| Analyst |   Professionals who analyze market trends, customer behavior, and sales data to provide insights and recommendations for optimizing the EZElectronics application.        |
| Store Admin  |     Individuals responsible for managing the overall producet and the the properties of the EZElectronics platform.      |
| Payment service |  Payment services facilitate secure and convenient online transactions between buyers and sellers by processing payments through various payment methods, such as credit cards, debit cards, digital wallets, and bank transfers.         |
| Google ads  |  Google Ads serves as an advertising platform that enables businesses to promote their products or services through targeted ads displayed across Google's network of websites and platforms.          |

# Context Diagram and interfaces

## Context Diagram

![](/uploads/6286604e088d4094b3dd2e55b41bb52a/context.png)

## Interfaces

| Actor | Logical Interface | Physical Interface  |
| ------------- |:-------------:| -----:|
| Customer | Graphical User Interface of web application (TBD) | Mouse, keyboard |
| Database | Web services | Internet |

# Stories and personas

<!-- \<A Persona is a realistic impersonation of an actor. Define here a few personas and describe in plain text how a persona interacts with the system> -->

<!-- \<Persona is-an-instance-of actor> -->

<!-- \<stories will be formalized later as scenarios in use cases> -->

## Persona 1: Single male technology enthusiast/developer
- Story: A software developer who enjoys staying updated with the latest tech gadgets. He uses the EZElectronics application to browse, compare, and purchase electronics products quickly. He appreciates the user-friendly interface and actively participates in community discussions to share his expertise and recommendations with others.
## Persona 2: Single female middle age, business owner.
- Story: An entrepreneur who owns multiple electronics stores. She relies on the EZElectronics application to manage her store operations efficiently while on the move. She uses the app to check inventory, update listings, and track orders remotely, allowing her to stay connected to her business at all times.
## Persona 3: Budget shopper, low-income, young.
- Story: A recent college graduate working part-time as a freelance writer. She uses the EZElectronics application to find the best deals and discounts on electronics products within her budget. She takes advantage of special promotions and compares prices to ensure she gets the most value for her money when shopping for electronics.

# Functional and non functional requirements

## Functional Requirements

\<In the form DO SOMETHING, or VERB NOUN, describe high level capabilities of the system>

\<they match to high level use cases>

|  ID   | Description |
| :---: | :---------: |
|FR1  |Manage account|
|FR1.1|Register      |
|FR1.2|Login       |
|FR1.3|Logout      |
|FR2  |Manage user|
|FR2.1|Search user |
|FR2.2|Delete user |
|FR2.3|Define privileges(customer/manager)|
|FR3  |Manage Product|
|FR3.1|Register product|
|FR3.2|Sell product|
|FR3.3|Delete product|
|FR3.4|Edit product|
|FR4  |Search product|
|FR4.1|Show by category|
|FR4.2|Show by model|
|FR4.3|Show by product code|
|FR5  |Manage cart    |
|FR5.1|Show cart    |
|FR5.2|Checkout cart    |
|FR5.3|Add to cart    |
|FR5.4|Remove from cart    |
|FR5.5|Delete cart    |
|FR6  |Engage customer    |
|FR6.1|Support inquiries|
|FR6.2|Send promotional offers|
|FR7  |Track Progress|
|FR7.1|Analyze sales|
## Non Functional Requirements

\<Describe constraints on functional requirements>

|   ID    | Type (efficiency, reliability, ..) | Description | Refers to |
| :-----: | :--------------------------------: | :---------: | :-------: |
|NFR1|Performance|System responses shall not exceed 1 seconds.|All FR |
|NFR2|Performance|Support up to 1,000 concurrent users without performance degradation.|    All FR     |
|NFR3|Security|Use role-based access control (RBAC) to enforce user permissions.|All FR|
|NFR4|Security|Implement SSL/TLS for all transactions.|All FR|
|NFR5|Security|User data and password should be stored as encrypted in the database.|All FR|
|NFR6|Reliability|The system should guarantee 99% uptime outside of scheduled maintenance windows.|All FR|
|NFR7|Usability|The GUI should be intuitive, with support for multiple browsers and responsive design.|All FR|

# Use case diagram and use cases

## Use case diagram

<!--\<define here UML Use case diagram UCD summarizing all use cases, and their relationships> -->

<!-- \<next describe here each use case in the UCD> -->
![Usecase Diagram](/uploads/fbc9f88f52adc2c6bd54fffc532c0471/usecase-v2.png)

### Use case 1, Login (UC1)

| Actors Involved  | Customer, Manager |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | User has a registered account |
|  Post condition  |  User is successfully logged in   |
| Nominal Scenario |   Scenario 1.1|
|     Variants     |  None|
|    Exceptions    |   Scenario 1.2, 1.3  |

##### Scenario 1.1

|  Scenario 1.1  |     Successful Login|
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | Provided email and password matches with system records|
| Post condition |  Successful login   |
|     Step#      |  Description|
|       1 |User provides email and password|
|       2 |System checks user records|
|       3 |System matches provided email and password|
|       4 |User successful logged in|

##### Scenario 1.2

|  Scenario 1.2  |  User is not found|
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | Provided email is not found on system |
| Post condition |  Failed to login   |
|     Step#      |  Description|
|       1 |User provides email and password|
|       2 |System checks user records|
|       3 |System fails to find the provided email on|
|       4 |System provides an error message "User is not found"|

##### Scenario 1.3

|  Scenario 1.3  |  User information   mismatch|
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | Provided password does not match with user record |
| Post condition |  Failed to login   |
|     Step#      |  Description|
|       1 |User provides email and password|
|       2 |System checks user records|
|       3 |System finds the user with provided email|
|       4 |System cannot match provided password with user record|
|       5 |System provides an error message "Wrong password"|

### Use case 2, Logout (UC2)

| Actors Involved  |  Customer, Manager |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | User has already logged in |
|  Post condition  |  User is successfully logged out   |
| Nominal Scenario |   Scenario 2.1|
|     Variants     |  None|
|    Exceptions    |   None  |

##### Scenario 2.1

|  Scenario 2.1  |     Successful Logout|
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |User is already logged in|
| Post condition |  Successful logout   |
|     Step#      |  Description|
|       1 |User asks to logout|
|       2 |System approves|
|       3 |User successful logged out|

### Use case 3, Register (UC3)

| Actors Involved  |  Customer, Manager|
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | User is not registered in the system |
|  Post condition  | User is successfully registered   |
| Nominal Scenario | Scenario 3.1       |
|     Variants     |    None                 |
|    Exceptions    |     Scenario 3.2                   |


##### Scenario 3.1

|  Scenario 3.1  |   System creates a new account for the user                                                                         |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The user doesn't have an account |
| Post condition |  User successfully registered   |
|     Step#      | Description|
|       1|        User opens the registeration page|
|       2        |  User provides necessary registration information|
|      3      |     System validates the information|
|      4      |     System creates a new account for the user|

##### Scenario 3.2

|  Scenario 3.2  |   User already registered to the system                                                                        |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The user has already an account |
| Post condition |  User registration fails   |
|     Step#      | Description|
|       1|        User opens the registeration page|
|       2        |  User provides necessary registration information|
|       3        |  Provided email associated with a registered account|
|      4      |     System fails to validate the registration|
|      5      |     System provides an error message|

### Use case 4, Search user (UC4)

| Actors Involved  | Manager  |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | User is found on user records |
|  Post condition  | User details shown to the manager   |
| Nominal Scenario | Scenario 4.1       |
|     Variants     |    Scenario 4.2                 |
|    Exceptions    |     Scenario 4.3|

##### Scenario 4.1

|  Scenario 4.1  |  User found with given username  |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | Searched user has an account |
| Post condition |  User found  |
|     Step#      | Description|
|       1|       Manager searches for a user with username|
|       2|       System checkes provided username in user records|
|       3|       System finds the user record|
|       4|       System shows the user details to manager|

##### Scenario 4.2

|  Scenario 4.2  | User found with given role  |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | There are user(s) with that role |
| Post condition |  Users found with given role|
|     Step#      | Description|
|       1|       Manager searches for a user with role|
|       2|       System filters users with provided role|
|       3|       System shows the users' details to manager|

##### Scenario 4.3

|  Scenario 4.3  | User not found with provided username  |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The user doesn't have an account |
| Post condition |  User successfully registered   |
|     Step#      | Description|
|       1|       Manager searches for a user with username|
|       2|       System checkes provided username in user records|
|       3|       System cannot find the related user record|
|       4|       System gives an error message "User with _username_ does not exist"|


### Use case 5, Delete user (UC5)

| Actors Involved  | Manager |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | User is found on user records |
|  Post condition  | User details removed from user records|
| Nominal Scenario | Scenario 5.1       |
|     Variants     |    None                 |
|    Exceptions    |     Scenario 5.2                   |

##### Scenario 5.1

|  Scenario 5.1  |  Manager deletes a user|
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |  User to be deleted has a user record |
| Post condition |  Manager successfully delete user record   |
|     Step#      | Description|
|       1|        Manager finds the user to be deleted|
|       2|        Manager asks to delete the user record|
|       3|        System authentificate the manager to delete the user record|
|       4|        User successfully deleted from the user records|

##### Scenario 5.2

|  Scenario 5.2  |  Manager tries to remove itself |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |  User to be deleted is the manager itself |
| Post condition |  Manager cannot delete itself from the system  |
|     Step#      | Description|
|       1|       Manager asks the system for its own user record|
|       2|       System provides the manager with its user record|
|       3|       Manager asks the system to delete the record|
|       4|       System does not authentificate the manager to delete its own user record|
|       5|       System gives an error message "Managers cannot remove their own user record"|

### Use case 6, Define privileges (UC6)

| Actors Involved  |  Manager  |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | User to be defined privileges is found on user records |
|  Post condition  | User privileges defined   |
| Nominal Scenario | Scenario 6.1       |
|     Variants     |    None                 |
|    Exceptions    |     Scenario 6.2                   |

##### Scenario 6.1

|  Scenario 6.1  | Manager defines privileges for a user|
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | User to be defined privileges is found on user records |
| Post condition |  User privileges defined   |
|     Step#      | Description|
|       1|        Manager finds the user to be defined privileges|
|       2|        Manager asks the system to define privileges for the found user|
|       3|        System approves the privileges defined|
|       4|        System updates the user record privileges|

##### Scenario 6.2

|  Scenario 6.2  | Manager tries to update defined privileges of its own |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | User to be defined privileges is manager itself |
| Post condition |  Manager cannot update the defined privileges for itself  |
|     Step#      | Description|
|       1|       Manager asks the system for its own user record|
|       2|       System provides the manager with its user record|
|       3|       Manager asks the system to update defined privileges of its own|
|       4|       System does not authentificate the manager to update its own defined privileges|
|       5|       System gives an error message "Managers cannot update their own defined privileges"|

### Use case 7, Register product (UC7)

| Actors Involved  |     Manager                                                                 |
| :--------------: | :------------------------------------------------------------------: |
|   Pre condition   | The Manager is authenticated and has access to the product registration feature. |
|  Post condition  |  The product is successfully registered in the system.  |
| Nominal Scenario |        Scenario 7.1       |
|     Variants     |                           |
|    Exceptions    |                      Scenario 7.2                    |

##### Scenario 7.1

|  Scenario 7.1  |        Successful Product Registration                                                                    |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Manager is authenticated and has access to the product registration feature. |
| Post condition |  The product is successfully registered in the system.   |
|     Step#      |                                Description                                 |
|       1        |          Manager navigates to the product registration page.                                                                   |
|       2        |            Manager enters the necessary details for the product, including name, description, price, and quantity.                                                                |
|      3     |       Manager submits the product information for registration.                                                                     |
|      4     |        System validates the entered information.                                                                    |
|      5     |     System adds the product to the product catalog.                                                                       |
|      6     |      System confirms successful product registration.                                                                      |

##### Scenario 7.2

|  Scenario 7.2  |       Product Registration with Incomplete Information                                                                     |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Manager is authenticated and has access to the product registration feature. |
| Post condition | The product is not registered in the system due to incomplete information.   |
|     Step#      |                                Description                                 |
|       1        |      Manager navigates to the product registration page.                                                                      |
|       2        |       Manager enters partial details for the product, missing some required fields.                                                                     |
|      3     |       Manager submits the incomplete product information for registration.                                                                     |
|      4     |       System detects missing information and displays an error message.                                                                     |

### Use case 8, Delete product (UC8)

| Actors Involved  |   Manager                                                                   |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Manager is authenticated and has access to the product deletion feature. |
|  Post condition  |  The product is successfully deleted from the system.   |
| Nominal Scenario |      Scenario 8.1     |
|     Variants     |                          |
|    Exceptions    |                      Scenario 8.2                     |

##### Scenario 8.1

|  Scenario 8.1  |          Successful Product Deletion                                                                   |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Manager is authenticated and has access to the product deletion feature. |
| Post condition | The product is successfully deleted from the system.   |
|     Step#      |                                Description                                 |
|       1        |     Manager navigates to the product management section.                                                                     |
|       2        |      Manager selects the product to be deleted from the product catalog.                                                                      |
|      3     |     Manager confirms the deletion action.                                                                       |
|      4     |       System removes the product from the product catalog.                                                                     |
|      5     |       System confirms successful product deletion.                                                                     |


##### Scenario 8.2

|  Scenario 8.2  |      Product Deletion with Existing Orders                                                                      |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Manager is authenticated and has access to the product deletion feature. |
| Post condition |  The product remains in the system due to existing orders associated with it.  |
|     Step#      |                                Description                                 |
|       1        |     Manager navigates to the product management section.                                                                      |
|       2        |       Manager selects a product that has existing orders associated with it.                                                                      |
|      3     |      Manager attempts to delete the product.                                                                     |
|      4     |      System detects existing orders associated with the product and displays a warning message.                                                                      |
|      5     |      Manager cancels the deletion action or chooses not to delete the product.                                                                      |
|      6     |       System does not remove the product from the product catalog.                                                                     |
|      7     |       System maintains the existing orders associated with the product.                                                                     |
|      8     |                                                            System confirms that the product was not deleted from the system.                |

### Use case 9, Sell product (UC9)

| Actors Involved  |     Manager                                                             |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The product is available in the product catalog and has sufficient stock. |
|  Post condition  | The product is successfully sold, and the inventory is updated accordingly.   |
| Nominal Scenario |      Scenario 9.1   |
|     Variants     |                                      |
|    Exceptions    |                      Scenario 9.2                       |

##### Scenario 9.1

|  Scenario 9.1  |             Successful Product Sale                                                               |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The product is available in the product catalog and has sufficient stock. |
| Post condition |  The product is successfully sold, and the inventory is updated accordingly.   |
|     Step#      |                                Description                                 |
|       1        |       System receives a request from a customer to purchase a product.                                                                     |
|       2        |      System checks the availability of the requested product in the inventory.                                                                      |
|      3     |     System confirms the availability of the product and proceeds to process the sale.                                                                       |
|      4     |      System collects payment from the customer and updates the inventory to reflect the sold product.                                                                      |
|      5     |       System provides the customer with an order confirmation.                                                                     |


##### Scenario 9.2

|  Scenario 9.2  |         Product Sale with Payment Processing Error                                                                   |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The product is available in the product catalog and has sufficient stock. |
| Post condition |  The product remains in the inventory due to payment processing errors.   |
|     Step#      |                                Description                                 |
|       1        |       System receives a request from a customer to purchase a product.                                                                     |
|       2        |     System checks the availability of the requested product in the inventory.                                                                       |
|      3     |                                                              System confirms the availability of the product and proceeds to process the sale.              |
|      4     |       Payment processing fails due to errors in the payment information or technical issues.                                                                     |

### Use case 10, Edit product (UC10)

| Actors Involved  |     Manager                                                                 |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Manager is authenticated and has access to the product management system. |
|  Post condition  |  The product information is successfully updated in the system.   |
| Nominal Scenario |       Scenario 10.1          |
|     Variants     |                                        |
|    Exceptions    |                      Scenario 10.2                       |

##### Scenario 10.1

|  Scenario 10.1  |   Successful Product Information Update                                                                         |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Manager is authenticated and has access to the product management system. |
| Post condition |  The product information is successfully updated in the system.   |
|     Step#      |                                Description                                 |
|       1        |     Manager navigates to the product management section.                                                                       |
|       2        |       Manager selects the product whose information needs to be updated from the product catalog.                                                                      |
|      3     |     Manager edits the necessary product information, such as name, description, price, or quantity.                                                                       |
|      4     |     Manager submits the updated product information.                                                                      |
|      5     |      System validates the entered information.                                                                      |
|      6     |       System updates the product information in the system.                                                                     |
|      7     |       System confirms successful update of product information.                                                                     |


##### Scenario 10.2

|  Scenario 10.2  |         Product Information Update with Invalid Data                                                                   |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Manager is authenticated and has access to the product management system. |
| Post condition |  The product information remains unchanged due to invalid data.   |
|     Step#      |                                Description                                 |
|       1        |     Manager navigates to the product management section.                                                                       |
|       2        |     Manager selects the product whose information needs to be updated from the product catalog.                                                                       |
|      3     |    Manager attempts to edit the product information but provides invalid or incomplete data.                                                                        |
|      4     |     Manager submits the updated product information.                                                                       |
|      5     |       System detects invalid data and displays an error message, prompting the Manager to correct the information.                                                                     |


### Use case 11, Show by category (UC11)

| Actors Involved  |     Customer, Manager                                                                 |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer/manager is authenticated and has access to the product search functionality. |
|  Post condition  |  The search results are displayed to the Customer/manager.  |
| Nominal Scenario |      Scenario 11.1       |
|     Variants     |                                       |
|    Exceptions    |                      Scenario 11.2                        |

##### Scenario 11.1

|  Scenario 11.1  |        Successful Product Search                                                                    |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer/manager is authenticated and has access to the product search functionality. |
| Post condition |  The search results are displayed to the Customer/manager.   |
|     Step#      |                                Description                                 |
|       1        |      Customer or Manager navigates to the search bar on the product catalog page.                                                                      |
|       2        |      Customer or Manager enters the filters to search for a specific product category.                                                                      |
|      3     |      System retrieves relevant products based on the search criteria.                                                                      |
|      4     |      System displays the search results to the Customer.                                                                      |

##### Scenario 11.2

|  Scenario 11.2  |     No Results Found                                                                       |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |The Customer/manager is authenticated and has access to the product search functionality. |
| Post condition |  The system displays a message indicating no results found.  |
|     Step#      |                                Description                                 |
|       1        |        Customer or Manager navigates to the search bar on the product catalog page.                                                                    |
|       2        |     Customer or Manager enters filters to search for a specific product category.                                                                       |
|      3     |     System searches for products based on the provided criteria.                                                                       |
|      4     |     System does not find any products in the chosen category.                                                                       |
|      5     |     System displays a message indicating no results found to the Customer or Manager.                                                                       |



### Use case 12, Show by model (UC12)

| Actors Involved  |     Customer, Manager                                                                 |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer/manager is authenticated and has access to the product search functionality. |
|  Post condition  |  The search results are displayed to the Customer/manager.  |
| Nominal Scenario |      Scenario 12.1       |
|     Variants     |                                       |
|    Exceptions    |                      Scenario 12.2                        |

##### Scenario 12.1

|  Scenario 12.1  |        Successful Product Search                                                                    |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer/manager is authenticated and has access to the product search functionality. |
| Post condition |  The search results are displayed to the Customer/manager.   |
|     Step#      |                                Description                                 |
|       1        |      Customer or Manager navigates to the search bar on the product catalog page.                                                                      |
|       2        |      Customer or Manager enters the filters to search for a specific product model.                                                                      |
|      3     |      System retrieves relevant products based on the search criteria.                                                                      |
|      4     |      System displays the search results to the Customer.                                                                      |

##### Scenario 12.2

|  Scenario 12.2  |     No Results Found                                                                       |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |The Customer/manager is authenticated and has access to the product search functionality. |
| Post condition |  The system displays a message indicating no results found.  |
|     Step#      |                                Description                                 |
|       1        |        Customer or Manager navigates to the search bar on the product catalog page.                                                                    |
|       2        |     Customer or Manager enters filters to search for a specific product model.                                                                       |
|      3     |     System searches for products based on the provided criteria.                                                                       |
|      4     |     System does not find any products of the chosen model.                                                                       |
|      5     |     System displays a message indicating no results found to the Customer or Manager.                                                                       |
### Use case 13, Show by product code (UC13)

| Actors Involved  |     Customer, Manager                                                                 |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer/manager is authenticated and has access to the product search functionality. |
|  Post condition  |  The search results are displayed to the Customer/manager.  |
| Nominal Scenario |      Scenario 13.1       |
|     Variants     |                                       |
|    Exceptions    |                      Scenario 13.2                        |

##### Scenario 13.1

|  Scenario 13.1  |        Successful Product Search                                                                    |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer/manager is authenticated and has access to the product search functionality. |
| Post condition |  The search results are displayed to the Customer/manager.   |
|     Step#      |                                Description                                 |
|       1        |      Customer or Manager navigates to the search bar on the product catalog page.                                                                      |
|       2        |      Customer or Manager enters the filters to search for a specific product code.                                                                      |
|      3     |      System retrieves relevant products based on the search criteria.                                                                      |
|      4     |      System displays the search results to the Customer.                                                                      |

##### Scenario 13.2

|  Scenario 13.2  |     No Results Found                                                                       |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |The Customer/manager is authenticated and has access to the product search functionality. |
| Post condition |  The system displays a message indicating no results found.  |
|     Step#      |                                Description                                 |
|       1        |        Customer or Manager navigates to the search bar on the product catalog page.                                                                    |
|       2        |     Customer or Manager enters filters to search for a specific product code.                                                                       |
|      3     |     System searches for products based on the provided criteria.                                                                       |
|      4     |     System does not find any products with the given code.                                                                       |
|      5     |     System displays a message indicating no results found to the Customer or Manager.                                                                       |

### Use case 14, Show cart (UC14)

| Actors Involved  |        Customer                                                              |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer has items in their shopping cart. |
|  Post condition  |  The contents of the shopping cart are displayed to the Customer.   |
| Nominal Scenario |     Scenario 14.1         |
|     Variants     |                                         |
|    Exceptions    |                       Scenario 14.2                       |

##### Scenario 14.1

|  Scenario 14.1  |       View Cart with Items                                                                     |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  |The Customer has items in their shopping cart.|
| Post condition |  The contents of the shopping cart are successfully displayed to the Customer.  |
|     Step#      |                                Description                                 |
|       1        |      Customer navigates to the shopping cart page.                                                                      |
|       2        |    System retrieves the items currently in the Customer's shopping cart.                                                                        |
|      3     |      System displays the contents of the shopping cart to the Customer.                                                                      |
|      4     |    Customer reviews the items in the shopping cart.                                                                        |

##### Scenario 14.2

|  Scenario 14.2  |      View Empty Cart                                                                      |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer's shopping cart is empty. |
| Post condition |  The system displays a message indicating that the cart is empty.   |
|     Step#      |                                Description                                 |
|       1        |      Customer navigates to the shopping cart page.                                                                      |
|       2        |      System detects that the Customer's shopping cart is empty.                                                                      |
|      3     |     System displays a message indicating that the cart is empty to the Customer.                                                                       |                                               |

### Use case 15, Checkout cart (UC15)

| Actors Involved  |       Customer                                                               |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer has items in their shopping cart. |
|  Post condition  |  The System succesfully confirms order.   |
| Nominal Scenario |        Scenario 15.1      |
|     Variants     |                      None                      |
|    Exceptions    |                        None                        |

##### Scenario 15.1

|  Scenario 15.1  |        Proceed to the checkout of the cart            |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer has items in their shopping cart. |
| Post condition |  The System succesfully confirms order.   |
|     Step#      |     Description                                 |
|       1        |       Customer navigates to the shopping cart page.                 |
|       2        |     Customer reviews the items in the shopping cart.                   |
|     3      |           Customer chooses to checkout the cart.               |
|4|System proceeds to checkout the cart |
|5|System displays a message indicating that the Customer can proceed to payment.|

### Use case 16, Add to cart (UC16)

| Actors Involved  |          Customer                                                            |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The product is available in the product catalog and has sufficient stock. |
|  Post condition  |  The product is successfully sold, and the inventory is updated accordingly.   |
| Nominal Scenario |         Scenario 16.1          |
|     Variants     |                      None                      |
|    Exceptions    |                     Scenario 16.2                        |

##### Scenario 16.1

|  Scenario 16.1  |   Adding product to the cart                                             |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The product is available in the product catalog and has sufficient stock. |
| Post condition |  The product is successfully sold, and the inventory is updated accordingly.   |
|     Step#      |                                Description                                 |
|       1        |  System receives a request from a customer to add a product to the cart.                 |
|       2        |  System checks the availability of the requested product in the inventory.              |
|      3       |     System confirms the availability of the product and proceeds to add it to the cart.   |
|4|System provides the customer with a confirmation message.|

##### Scenario 16.2

|  Scenario 16.2  |  Adding to cart with availability error     |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The product is not available in the inventory. |
| Post condition |  The system displays a message indicating that the product is not available.   |
|     Step#      |                                Description                                 |
|       1        | System receives a request from a customer to add a product to the cart.                |
|       2        | System checks the availability of the requested product in the inventory.    |
|     3       | System detects that the product is not available.      |
|4|System displays a message indicating that the product is unavailable to the Customer.|

### Use case 17, Remove from cart (UC17)

| Actors Involved  |                           Customer                                           |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer has items in their shopping cart.                       |
|  Post condition  |  The item is succesfully removed from the shopping cart    |
| Nominal Scenario |         Scenario 17.1         |
|     Variants     |                                          None  |
|    Exceptions    |                        None                     |

##### Scenario 17.1

|  Scenario 17.1  |          Remove element from cart                                                 |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer has items in their shopping cart. |
| Post condition |  The item is succesfully removed from the shopping cart.   |
|     Step#      |                                Description                                 |
|1|Customer navigates to the shopping cart page.|
|       2        |           Customer reviews the items in the shopping cart.                         |
|       3       |          Customer chooses the item to delete.               |
|      4      |             System deletes the chosen item currently in the Customer's shopping cart.       |
|5|System displays the contents of the updated shopping cart to the Customer.|


### Use case 18, Delete cart (UC18)

| Actors Involved  |               Customer                                               |
| :--------------: | :------------------------------------------------------------------: |
|   Precondition   | The Customer has items in their shopping cart.  |
|  Post condition  |  All items are succesfully removed from the shopping cart.   |
| Nominal Scenario |         Scenario 18.1         |
|     Variants     |                      None                      |
|    Exceptions    |                        None                        |

##### Scenario 18.1

|  Scenario 18.1  |      Remove all elements from cart                                                             |
| :------------: | :------------------------------------------------------------------------: |
|  Precondition  | The Customer has items in their shopping cart. |
| Post condition |  All items are succesfully removed from the shopping cart.   |
|     Step#      |                                Description                                 |
|1|Customer navigates to the shopping cart page.|
|       2        |           Customer reviews the items in the shopping cart.                         |
|       3       |          Customer uses the delete all button.               |
|      4      |             System all the items currently in the Customer's shopping cart.       |
|5|System displays a message indicating that all items have succesfully been removed.|



### Use case 19 - Support inquiries (UC19)
| Actors Involved        | Customer, Manager |
| ------------- |:-------------:| 
|  Precondition     | Customer has an issue or question |
|  Post condition     | Customer issue resolved or escalated |
|  Nominal Scenario     | Scenario 19.1 |
|  Variants     | None |
|  Exceptions     | Scenario 19.2 |

##### Scenario 19.1 - Everything is correct
| Scenario 19.1 | |
| ------------- |:-------------:| 
|  Precondition     | Customer has an issue or question |
|  Post condition     | Customer satisfied and issue resolved |
| Step#        | Description  |
|  1     | Customer contacts support via website chat |  
|  2     | Support agent reviews the issue and accesses customer data |
|  3     | Immediate solution provided based on FAQs and knowledge base |
|  4     | Customer confirms resolution and closes the ticket |

##### Scenario 19.2 -  Support system is unavailable
| Scenario 19.2 | |
| ------------- |:-------------:| 
|  Precondition     | Customer has an issue or question |
|  Post condition   | Customer redirected to email support |
| Step#  | Description  |
|  1     | Customer attempts to access online support |  
|  2     | Support system experiences a technical failure |
|  3     | Customer is automatically redirected to submit an email |
|  4     | Issue logged and flagged for follow-up when the system is back online |

### Use case 20 - Send promotional offers (UC20)
| Actors Involved        | Manager |
| ------------- |:-------------:| 
|  Precondition     | Marketing campaign prepared |
|  Post condition     | Promotional offers sent out |
|  Nominal Scenario     | Scenario 20.1 |
|  Variants     | None |
|  Exceptions     | Scenario 20.2 |

##### Scenario 20.1 - Everything is correct
| Scenario 20.1 | |
| ------------- |:-------------:| 
|  Precondition     | Marketing campaign prepared |
|  Post condition     | Emails tracked for effectiveness |
| Step#        | Description  |
|  1     | Marketing team curates a list of products for promotion |  
|  2     | Personalized emails are created and sent to targeted segments |
|  3     | Email engagement monitored and analyzed for conversion rates |
|  4     | Results used to optimize future campaigns |

##### Scenario 20.2 -  Email service provider down
| Scenario 20.2 | |
| ------------- |:-------------:| 
|  Precondition     | Marketing campaign prepared |
|  Post condition   | Campaign launch postponed |
| Step#  | Description  |
|  1     | Marketing team attempts to launch email campaign |  
|  2     | Service provider experiences outage, emails not sent |
|  3     | Marketing team notifies service provider, seeks resolution |
|  4     | Emails rescheduled for a future date post-issue resolution |


### Use case 21 - Analyze sales (UC21)
| Actors Involved        | Manager |
| ------------- |:-------------:| 
|  Precondition     | Sales data is available for analysis |
|  Post condition     | Sales insights are generated and reported |
|  Nominal Scenario     | Scenario 21.1 |
|  Variants     | None |
|  Exceptions     | Scenario 21.2 |

##### Scenario 21.1 - Everything is correct
| Scenario 21.1 | |
| ------------- |:-------------:| 
|  Precondition     | Sales data is available for analysis |
|  Post condition     | Insights reported to management |
| Step#        | Description  |
|  1     | Sales analyst collects and consolidates data from various sales channels |  
|  2     | Data is processed using analytics tools to identify trends and patterns |
|  3     | Analyst prepares a detailed report highlighting key performance indicators |
|  4     | Report is presented to management to inform decision-making |

##### Scenario 21.2 -  Email service provider down
| Scenario 21.2 | |
| ------------- |:-------------:| 
|  Precondition     |Sales data is available for analysis |
|  Post condition   | Analysis delayed, data recovery initiated |
| Step#  | Description  |
|  1     | Sales analyst discovers data inconsistencies during routine analysis |  
|  2     | Attempts to reconcile data fail due to corruption issues |
|  3     | Analyst notifies IT department to investigate and recover data |
|  4     | Analysis is postponed until accurate and complete data is restored |

# Glossary

![](/uploads/c04e2b92899ad6032479596e9da39ef5/glossary__1_.png)

# System Design

![](/uploads/1d61cec025b0b0eb033a8ab82044efcc/Systemdesign.png)

# Deployment Diagram

![](/uploads/e9126f032e580b122c4eaa9fc9e0b58d/deployment__1_.png)
