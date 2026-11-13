# **PulseWatch: API monitoring Platform**

## *Project Overview:*
## API monitoring platform

### Project Description:
PulseWatch is a web-based application that allows users to register and monitor API endpoints. The application automatically sends periodic HTTP requests to registered endpoints, records their availability and performance, detects failures, and tracks incidents.

### Problem it solves:
Developers need to know when their APIs become unavailable or start responding slowly. Without monitoring, they might not discover a problem until customers report it.

My application will help developers identify these problems sooner.

### Target Users: 
 - Software Developers
 - Small Development Teams
 - Students

### Objectives:
1. Allow users to register and manage API endpoints.
2. Automatically monitor registered endpoints.
3. Record response times and HTTP status codes.
4. Detect API failures and recoveries.
5. Track uptime and historical performance.
6. Display monitoring information through a dashboard.

### Core Features:
* #### User accounts and authentication
    Users should be able to:
  * Create an account
  * Log in and Log out
  * Manage their account
  * Access only their monitoring and configurations
* #### API endpoint management
    Users should be able to:
  * Register an API endpoint using its URL
  * Give the endpoint a name
  * Edit endpoint information
  * Pause and resume monitoring
  * Delete an endpoint
  * View all registered endpoints
* #### Automated endpoint monitoring
    The application will:
  * Retrieve a registered endpoint
  * Send an HTTP request
  * Measure how long the request takes
  * Capture the HTTP response code
  * Determine whether the endpoint is healthy
  * Save the monitoring result in the database
  * Repeat according to the configured monitoring interval
* #### Incident detection
  The application should:
  * Detect when an endpoint fails
  * Create an incident
  * Record when the incident started
  * Track repeated failures
  * Detect when the endpoint recovers
  * Record the recovery time
  * Calculate incident duration
* #### Performance Tracking
  * Average response time
  * Fastest response time
  * Slowest response time
  * Uptime Percentage
  * Number of successful checks
  * Number of failed checks
* #### Dashboard
  The dashboard should display:
  * Total monitored endpoints
  * Currently operational endpoints
  * Currently failing endpoints
  * Overall uptime percentage
  * Response-time graphs
  * Recent endpoint health
  
### Functional Requirements:
    Category      |      Requirement
    ----------------------------------------------------------------
    Accounts      |      Register, authenticate, and authorize users
    Endpoints     |      Create, edit, pause, resume, and delete monitors
    Monitoring    |      Automatically execute HTTP checks
    Results       |      Store status codes, timestamps, and response times
    Incidents     |      Create, update, and resolve incidents
    Analytics     |      Calculate uptime and performance statistics
    Dashboard     |      Display endpoint health and historical information

### Non-functional Requirements:
    Category        |      Requirement
    ----------------------------------------------------------------
    Performance     |      Monitoring requests should have configureable timeouts
    Reliability     |      A failed monitoring check should not crash the app
    Security        |      Users must not acces others monitors
    Maintainability |      Separate controllers, services, and repositories       
    Scalability     |      Design monitoring so additional endpints can be handled
    Data integrity  |      Monitoring results and incidents should remain consistent
    Testing         |      Core business logic must have automated tests
