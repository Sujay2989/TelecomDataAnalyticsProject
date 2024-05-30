# Telecom Analytics Dashboard

## Overview
The Telecom Analytics Dashboard is a comprehensive web application designed to manage and analyze call records. Users can add new call records through a form and view various analytics through visual charts. The project is divided into two main parts: the frontend, built with React and Material-UI, and the backend, which includes two Spring Boot-based microservices: Call Record Service and Analytics Service.

## Table of Contents
1. [Frontend](#frontend)
   - [Overview](#overview-1)
   - [Components](#components)
   - [API Interaction](#api-interaction)
   - [Styling](#styling)
2. [Backend](#backend)
   - [Call Record Service](#call-record-service)
     - [Overview](#overview-2)
     - [Endpoints](#endpoints)
     - [Database](#database)
     - [Business Logic](#business-logic)
   - [Analytics Service](#analytics-service)
     - [Overview](#overview-3)
     - [Endpoints](#endpoints-1)
     - [Database](#database-1)
     - [Business Logic](#business-logic-1)

## Frontend
### Overview
The frontend of the Telecom Analytics Dashboard is built using React and Material-UI. It allows users to interact with the application through forms and visual charts. The frontend communicates with the backend services to fetch and display data.

### Components
1. **CallRecordForm**
   - A form to input new call records.
   - Fields: Caller, Callee, Duration, Call Type.
   - Validates inputs and sends a POST request to the Call Record Service.
2. **TotalCallsChart**
   - Displays the total number of calls using a Pie Chart.
3. **TotalDurationChart**
   - Displays the duration of each call using a Bar Chart.
4. **CallTypesChart**
   - Displays the distribution of call types using a Pie Chart.

### API Interaction
The frontend interacts with the backend using Axios for HTTP requests. It communicates with various endpoints to submit call records and fetch analytics data.

### Styling
Material-UI is used for styling the components. The `CssBaseline` component is used to provide a consistent baseline for styling across the application. A background image is applied to the entire application to enhance visual appeal.

## Backend
### Call Record Service
#### Overview
The Call Record Service is a Spring Boot application responsible for managing call records. It provides endpoints to add and retrieve call records.

#### Endpoints
1. **POST /call-records**: Add a new call record.

#### Database
- **MySQL Database**: Stores call records for demonstration purposes.

#### Business Logic
- Manages CRUD operations for call records.
- Validates and processes incoming data before storing it in the database.

### Analytics Service
#### Overview
The Analytics Service is a Spring Boot application responsible for computing and serving analytics based on the call records.

#### Endpoints
1. **GET /analytics/total-calls**: Fetch total number of calls.
2. **GET /analytics/total-duration**: Fetch total duration of all calls.
3. **GET /analytics/call-types**: Fetch count of each call type.
4. **GET /analytics/durations**: Fetch durations of all calls.

#### Database
- **MySQL Database**: Stores analytics data for demonstration purposes.

#### Business Logic
- Computes analytics based on data retrieved from the Call Record Service.
- Aggregates and processes data to provide meaningful insights.
