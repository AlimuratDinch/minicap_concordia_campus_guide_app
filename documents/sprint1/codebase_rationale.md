# Campus Guide Mobile App: External Libraries, Frameworks, and APIs

This document provides a detailed analysis of external libraries, frameworks, and APIs utilized in the development of our Campus Guide mobile app. The app is being developed using React Native for the frontend and Django for the backend. Each tool is evaluated based on its relevance to the project features, along with its pros and cons.

## 1. APIs

### 1.1 Concordia Open Data API
**Use Cases:**
- Easily fetch campus building locations and details.
- Retrieve class schedules based on the user’s calendar.
- Provide information and list nearby amenities like washrooms, coffee shops, or other facilities on campus.

**Pros:**
- Easy access to Concordia-specific data.
- Reduces the load and need for a custom database.
- Free and open source.
- Potential for seamless integration with other features such as maps.

**Cons:**
- Limited data coverage (some information might be missing).
- Dependency on one data source from this API is risky.

---

### 1.2 Google Maps API
**Use Cases:**
- Outdoor directions between buildings and facilities.
- Visualization of campus routes and facilities.
- Integration with Concordia Shuttle directions.

**Pros:**
- Rich feature set with real-time traffic and route information.
- Widely used and has extensive documentation available online.
- Highly customizable.

**Cons:**
- Requires an API key and may incur charges with heavy usage.

---

### 1.3 Google Calendar API
**Use Cases:**
- Potential alternative to the Concordia Open Data API.
- Retrieve information on the user’s calendar.
- Sync users’ calendars with their school schedules.
- Set reminders for users’ classes in their Google Calendar.

**Pros:**
- Well-supported with abundant online documentation.

**Cons:**
- Requires OAuth2 authentication setup.
- Potential complexity in handling multiple calendars simultaneously.

---

## 2. React Native

React Native was chosen for its ability to create a cross-platform application with a single codebase, significantly reducing development time. Additionally, React Native is well-established with a large and active community.

### 2.1 React Native Maps
**Use Cases:**
- Display interactive maps for campus navigation.
- Highlight nearby buildings and facilities.

**Pros:**
- Easy to use.
- Supports both Android and iOS platforms.
- Actively maintained.

**Cons:**
- Limited advanced mapping features may require additional APIs to close the gap.

---

### 2.2 React Native Geolocation Service
**Use Cases:**
- Track the user’s current location.
- Determine proximity to amenities.

**Pros:**
- Free and lightweight alternative to Google’s geolocation API.
- Easy integration.
- Supports background location tracking.

**Cons:**
- Battery-intensive if used for prolonged periods.

---

### 2.3 React Native Navigation
**Use Case:**
React Native Navigation is used for managing navigation and transitions between screens in a React Native application. For the Campus Guide App, it enables smooth transitions between different views of the app (e.g., Loyola campus, main campus, street view, building view).

**Pros:**
- Flexible and integrates well with React Native.

**Cons:**
- Initial setup can be time-consuming for complex navigation.

---

## 3. Django

Django was chosen because it is well-suited for managing complex datasets and user interactions, which are core to our project. It enables rapid development of a robust backend to handle features like fetching real-time campus information, class schedules, and facility data.

### 3.1 Django REST Framework (DRF)
**Use Cases:**
- Develop RESTful APIs.
- Enable communication between the frontend and backend.

**Pros:**
- Easy to use.
- Team familiarity with the framework.
- Robust authentication features.
- Extensive online documentation.

**Cons:**
- Not as lightweight as frameworks like Flask.

---
