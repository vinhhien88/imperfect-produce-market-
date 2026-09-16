# 🥦 Imperfect Produce Market System

A digital agriculture marketplace that connects farmers, buyers, staff, and shippers in one end-to-end commerce and fulfillment platform.

## Overview

CapNong is designed to solve the fragmented workflow of local agricultural commerce by bringing product listing, cart, checkout, payment, delivery coordination, review, and order management into a single system. It targets multi-role stakeholders in a fresh-food supply chain: buyers who want to purchase quality produce, farmers who sell and manage inventory, staff/admin who oversee operations, and shippers who handle delivery.

## Tech Stack

### Backend
- Java 21
- Spring Boot 3.5.6
- Spring Web / REST APIs
- Spring Data JPA
- Spring Security
- JWT + OAuth2 login
- Spring WebSocket
- Springdoc OpenAPI / Swagger
- Lombok + MapStruct
- Google GenAI
- PayOS payment integration
- Apache POI for Excel export
- OpenPDF for PDF export

### Frontend
- React 19
- TypeScript
- Vite
- React Router
- Recharts
- Leaflet
- Tiptap
- SockJS / STOMP

### Mobile
- React Native
- Expo
- Google Sign-In
- Expo Location
- Expo Image Picker
- NativeWind

### Database
- MySQL (primary runtime database used by the project configuration and schema)
- Microsoft SQL Server JDBC driver is present in the backend build configuration as well

### DevOps / Infra
- Docker
- Docker Compose
- NGINX
- Cloudinary for media storage

## Key Features

- Multi-role marketplace with dedicated flows for buyers, farmers/shop owners, staff/admin, and shippers. The frontend route structure is split into role-based sections, and the backend exposes role-aware APIs.
- Full order lifecycle management, including cart and checkout, order creation, shipping-fee preview, paged order queries, batch checkout, and staff dashboards. The codebase includes 37 controllers and 52 entity models, with the order system as one of the core business domains.
- Integrated payment flow with PayOS, COD support, pending-payment recovery, and payment-status confirmation. Payment handling is implemented through dedicated REST endpoints and webhook validation logic.
- Real-time communication for chat, delivery updates, and notifications using WebSocket. This includes chat rooms, unread-message handling, and shipment-related messaging channels.
- AI-assisted commerce and support features through Google GenAI integration, including AI chat and product/decision support flows.
- Quality assurance and operational tools such as review management, return requests, warehouse stock handling, mystery boxes, build-combo plans, and export/report generation.

## Architecture

The project follows a standard layered Spring Boot architecture:

- Controller layer exposes REST and WebSocket endpoints
- Service layer contains business logic and workflow orchestration
- Repository layer handles persistence with Spring Data JPA
- Entity / DTO / Mapper layers separate persistence models from API contracts
- Security configuration protects endpoints with JWT and OAuth2 rules

On the web side, the frontend is a role-based React application using route groups and feature modules, while the mobile app is an Expo-based client consuming the same backend API surface.

## My Role

I was the core backend engineer across both project phases and took ownership of the product’s critical flows from business logic to integration. In the earlier phase, I built and maintained the main backend foundation for authentication, user management, product catalog, orders, payments, and seller operations; in the current CapNong project, I continued to drive the most important technical work, especially around checkout/payment reliability, stock/order flow, and cross-client integration for web and mobile.

Key features I contributed to and/or led in the project history include:
- Real-time chat and notification flows using WebSocket, including conversation-based messaging and unread-state handling.
- Shipper GPS/location tracking and delivery coordination, including the backend adjustments for GPS-based shipper workflows and delivery notification updates.
- Map integration for shipping and delivery operations with Goong map APIs for address suggestions and shipping-fee calculations.
- Payment and checkout improvements, including PayOS integration, COD and batch order handling, pending-payment recovery, and status reconciliation.
- Google login across web and mobile clients, along with security and token flow refinements.
- Business features such as discounts, combo/planning modules, product image management, and reporting/export capabilities that supported the marketplace operations.

## Links

- Source code (Backend): https://github.com/nongsanxauma-vn/FoodMarket_BE
- Source code (Frontend): https://github.com/nongsanxauma-vn/FoodMarket-FE
- Source code (Mobile App): https://github.com/nongsanxauma-exe201/App_CapNong_exe2/tree/develop
## 📸 Demo

### Web App
[▶️ Xem video demo](https://youtu.be/7f_GAWL3h9k)

### Mobile App — Shipper Tracking
[▶️ Xem video demo](https://youtube.com/shorts/7RLE5IRt17w)

## Project Scale

The backend implementation is substantial and production-oriented, with:

- 37 controller classes
- 52 entity classes
- 109 service classes
- 242 API mapping annotations across backend controllers
- Additional real-time WebSocket endpoints for chat, notifications, and shipper tracking

This indicates a broad platform scope spanning commerce, operations, logistics, payments, review, AI-assisted support, and real-time delivery coordination.
