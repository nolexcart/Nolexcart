# Nolexcart Architecture Overview

Nolexcart is an online shopping platform designed to provide a seamless e-commerce experience. This document outlines the high-level architecture of the system.

## System Architecture

```mermaid
graph TB
    subgraph Client["Client Layer"]
        WEB["Web Application"]
        MOBILE["Mobile Application"]
    end

    subgraph Frontend["Frontend Services"]
        UI["User Interface"]
        CART["Shopping Cart"]
        SEARCH["Product Search"]
        AUTH_FE["Authentication UI"]
    end

    subgraph Gateway["API Gateway Layer"]
        APIGW["API Gateway"]
    end

    subgraph Backend["Backend Services"]
        AUTH["Authentication Service"]
        PRODUCT["Product Service"]
        ORDER["Order Service"]
        PAYMENT["Payment Service"]
        USER["User Service"]
        CART_SVC["Cart Service"]
    end

    subgraph Database["Data Layer"]
        PRODUCT_DB["Product Database"]
        USER_DB["User Database"]
        ORDER_DB["Order Database"]
        CACHE["Cache Layer"]
    end

    subgraph External["External Services"]
        PAYMENT_GW["Payment Gateway"]
        EMAIL["Email Service"]
        NOTIFICATION["Notification Service"]
    end

    subgraph Features["Key Features"]
        CATEGORIES["Categories"]
        HOME["Home & Kitchen"]
        GADGETS["Gadgets"]
        BEAUTY["Beauty"]
        FITNESS["Fitness"]
        LIFESTYLE["Lifestyle"]
    end

    %% Client connections
    WEB --> UI
    MOBILE --> UI
    
    %% Frontend to Gateway
    UI --> APIGW
    CART --> APIGW
    SEARCH --> APIGW
    AUTH_FE --> APIGW

    %% Gateway to Services
    APIGW --> AUTH
    APIGW --> PRODUCT
    APIGW --> ORDER
    APIGW --> USER
    APIGW --> CART_SVC

    %% Services to Database
    AUTH --> USER_DB
    USER --> USER_DB
    PRODUCT --> PRODUCT_DB
    ORDER --> ORDER_DB
    CART_SVC --> CACHE

    %% Services to External
    ORDER --> PAYMENT_GW
    PAYMENT --> PAYMENT_GW
    ORDER --> EMAIL
    PAYMENT --> EMAIL
    ORDER --> NOTIFICATION

    %% Product categories
    PRODUCT --> CATEGORIES
    CATEGORIES --> HOME
    CATEGORIES --> GADGETS
    CATEGORIES --> BEAUTY
    CATEGORIES --> FITNESS
    CATEGORIES --> LIFESTYLE

    %% Styling
    classDef clientStyle fill:#e1f5ff,stroke:#01579b,stroke-width:2px
    classDef serviceStyle fill:#f3e5f5,stroke:#4a148c,stroke-width:2px
    classDef dataStyle fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px
    classDef externalStyle fill:#fff3e0,stroke:#e65100,stroke-width:2px
    classDef featureStyle fill:#fce4ec,stroke:#880e4f,stroke-width:2px

    class WEB,MOBILE clientStyle
    class AUTH,PRODUCT,ORDER,PAYMENT,USER,CART_SVC serviceStyle
    class PRODUCT_DB,USER_DB,ORDER_DB,CACHE dataStyle
    class PAYMENT_GW,EMAIL,NOTIFICATION externalStyle
    class HOME,GADGETS,BEAUTY,FITNESS,LIFESTYLE featureStyle
```

## Architecture Components

### Client Layer
- **Web Application**: Desktop and web browser interface for customers
- **Mobile Application**: Native or cross-platform mobile shopping app

### Frontend Services
- **User Interface**: Main product browsing and display
- **Shopping Cart**: Cart management and checkout flow
- **Product Search**: Search and filtering capabilities
- **Authentication UI**: Login and registration interface

### API Gateway Layer
- **API Gateway**: Central entry point for all frontend requests, handling routing, rate limiting, and authentication

### Backend Services
- **Authentication Service**: User login, registration, and session management
- **Product Service**: Product catalog, details, and inventory management
- **Order Service**: Order creation, tracking, and management
- **Payment Service**: Payment processing and transaction management
- **User Service**: User profile and account management
- **Cart Service**: Shopping cart operations and persistence

### Data Layer
- **Product Database**: Product information, pricing, and inventory
- **User Database**: User profiles, credentials, and preferences
- **Order Database**: Order history and transaction details
- **Cache Layer**: High-performance caching for frequently accessed data

### External Services
- **Payment Gateway**: Third-party payment processing (Stripe, PayPal, etc.)
- **Email Service**: Transactional emails (order confirmations, receipts)
- **Notification Service**: Real-time notifications and alerts

### Product Categories
Nolexcart offers diverse product categories including:
- Home & Kitchen
- Gadgets
- Beauty
- Fitness
- Lifestyle

## Key Features
✅ Trending and affordable products  
✅ Secure shopping experience  
✅ Quality product curation  
✅ Smooth user experience  
✅ Multiple product categories  
✅ Great deals and discounts  

---

*Last Updated: August 10, 2026*
