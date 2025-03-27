# WeightTracker App Product Roadmap

## Product Vision
The WeightTracker app is a simple, user-friendly mobile application that helps users track their daily weight, view historical averages, and share their progress as PDF reports. It prioritizes ease of use with a clean UI, secure authentication, and seamless data management, targeting individuals focused on fitness, health monitoring, or weight management.

## Current State (March 2025)
- **Frontend**: React Native with Expo (SDK 51), basic navigation (Login, Signup, OTPScreen, HomeScreen, LogsScreen).
- **Backend**: Likely a PostgreSQL database (based on prior context with a `weight_logs` table).
- **Features Implemented**:
  - User authentication (login, signup, OTP verification).
  - Weight entry screen with a number pad (0-9, decimal point, backspace button).
  - Display of historical averages (today, yesterday, last week).
  - UI refinements in progress (e.g., aligning labels to the left, and values to the right).
- **Challenges**:
  - SDK compatibility issues (previously attempted upgrade to SDK 52).
  - UI adjustments (e.g., number pad layout, icon integration).
  - Missing features like PDF sharing.

---

## Phase 1: MVP Development (4-6 Weeks, March 11, 2025 - April 22, 2025)
**Goal**: Build a functional MVP that allows users to log in, enter their weight, view historical data, and share a basic PDF report.

### Milestone 1: Finalize Core UI and Weight Entry (1 Week, March 11 - March 18, 2025)
- **Tasks**:
  - Complete the HomeScreen UI:
    - Ensure labels ("Today:", "Yesterday:", "Last Week:") are left-aligned and values are right-aligned.
    - Style the current weight input ("0") with a proper input field (e.g., `TextInput`).
    - Polish the number pad (ensure circular buttons and backspace functionality work smoothly).
  - Test on both iOS simulator and Android device to confirm consistency.
- **Priority**: High
- **Dependencies**: React Native, Expo, `react-native-heroicons` for backspace icons.
- **Deliverable**: A polished HomeScreen with functional weight entry.

### Milestone 2: Backend Integration for Weight Entry (1 Week, March 18 - March 25, 2025)
- **Tasks**:
  - Set up API endpoints to save weight entries (e.g., `POST /weight_logs` to insert into `weight_logs` table).
  - Integrate API calls in HomeScreen to save weights when the user presses a "Save" button (replace the AM/PM buttons with a single "Save" button).
  - Fetch and display actual averages for "Today:", "Yesterday:", and "Last Week:" from the database.
- **Priority**: High
- **Dependencies**: Backend server (Node.js/Express assumed), PostgreSQL, `axios` for API calls.
- **Deliverable**: Users can save weight entries and see updated averages.

### Milestone 3: Implement PDF Sharing (2 Weeks, March 25 - April 8, 2025)
- **Tasks**:
  - Add a "Share as PDF" button on LogsScreen.
  - Use `expo-print` to generate a PDF of weight logs (e.g., a table with dates and weights).
  - Use `expo-sharing` to share the PDF via email, messaging, etc.
  - Test PDF generation and sharing on both iOS and Android.
- **Priority**: Medium-High
- **Dependencies**: `expo-print`, `expo-sharing`, backend API to fetch weight logs.
- **Deliverable**: Users can generate and share a PDF of their weight history.

### Milestone 4: Testing and Bug Fixes (1-2 Weeks, April 8 - April 22, 2025)
- **Tasks**:
  - Test the entire user flow: login → weight entry → view logs → share PDF.
  - Fix bugs (e.g., UI glitches, API errors, platform-specific issues).
  - Ensure data consistency (e.g., averages update correctly, no duplicate entries).
- **Priority**: High
- **Dependencies**: Testing tools (e.g., Jest for unit tests if applicable), emulator/simulator.
- **Deliverable**: A stable MVP ready for user feedback.

---

## Phase 2: Enhancements (4-6 Weeks, April 22, 2025 - June 3, 2025)
**Goal**: Enhance the app with additional features and polish based on initial feedback.

### Milestone 5: Add Trends and Visualizations (2 Weeks, April 22 - May 6, 2025)
- **Tasks**:
  - Add a "Trends" tab with a line graph showing weight over time (e.g., last 30 days).
  - Use `react-native-chart-kit` or `victory-native` for charting.
  - Allow users to toggle between daily, weekly, and monthly views.
- **Priority**: Medium
- **Dependencies**: Charting library, backend API for historical data.
- **Deliverable**: Users can visualize their weight trends.

### Milestone 6: Improve UI/UX (1-2 Weeks, May 6 - May 20, 2025)
- **Tasks**:
  - Add animations for button presses (e.g., using `react-native-reanimated`).
  - Enhance the LogsScreen with sorting/filtering options (e.g., by date range).
  - Refine typography and spacing for a professional look.
- **Priority**: Medium
- **Dependencies**: `react-native-reanimated`, UI design feedback.
- **Deliverable**: A more polished and interactive UI.

### Milestone 7: Upgrade Expo SDK (1-2 Weeks, May 20 - June 3, 2025)
- **Tasks**:
  - Upgrade from Expo SDK 51 to SDK 52 (or the latest stable version).
  - Resolve any compatibility issues (e.g., update `@react-navigation` dependencies).
  - Test thoroughly to ensure no regressions.
- **Priority**: Medium
- **Dependencies**: Expo documentation, updated libraries.
- **Deliverable**: The app runs on the latest SDK for better performance and features.

---

## Phase 3: Future Growth (3+ Months, June 3, 2025 - September 2025)
**Goal**: Scale the app with advanced features and prepare for a broader release.

### Milestone 8: Add Goal Setting and Reminders (1 Month, June 3 - July 1, 2025)
- **Tasks**:
  - Allow users to set a target weight and track progress.
  - Add daily reminders to log weight using `expo-notifications`.
  - Display motivational messages based on progress.
- **Priority**: Medium
- **Dependencies**: `expo-notifications`, backend support for goals.
- **Deliverable**: Users can set goals and receive reminders.

### Milestone 9: Social Sharing and Cloud Sync (1 Month, July 1 - August 1, 2025)
- **Tasks**:
  - Add options to share progress on social media (e.g., Instagram, Twitter).
  - Implement cloud sync for weight data across devices using a service like Firebase or AWS.
- **Priority**: Low-Medium
- **Dependencies**: Social sharing APIs, cloud backend.
- **Deliverable**: Users can sync data and share progress socially.

### Milestone 10: App Store Launch and Analytics (1 Month, August 1 - September 1, 2025)
- **Tasks**:
  - Prepare the app for App Store and Play Store submission (e.g., icons, descriptions).
  - Add analytics to track usage (e.g., `expo-analytics` or Firebase Analytics).
  - Gather initial user feedback and iterate.
- **Priority**: High
- **Dependencies**: App Store/Play Store accounts, analytics SDK.
- **Deliverable**: The app is live, with insights into user behavior.

---

## Roadmap Visualization
