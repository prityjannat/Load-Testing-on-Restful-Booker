# Load-Testing-on-Restful-Booker
I performed load testing and stress testing on the Restful-Booker website using Apache JMeter. The test scenario included:
- Login Test: I created a login request using valid credentials and retrieved an authentication token.
- Create Booking: Used the token to create bookings with random values.
- Search Booking: Fetched booking IDs and viewed the details using those IDs.

## Load Testing:
- Duration: 7 minutes (420 seconds)
- Users: 1116
- Throughput: 2.7 requests/sec
- Observation: The server could serve 2–3 users per second.

## Stress Testing:
- Duration: 7 minutes (420 seconds)
- Users: 1170
- Throughput: 2.8 requests/sec
- Peak Load: The server could handle up to 54 users concurrently before errors started.
- Error Threshold: At 1200 users, an error rate of 0.03% occurred at the 7-minute mark.

## Prerequisites
- Install Apache JMeter (v5.5 or later recommended)
- Ensure Java (JDK) is installed and configured in system path
- Stable internet connection
- Access to the Restful-Booker API

## Instructions on How to Run the Tests
- Open JMeter and load the Booking.jmx file.
- Review the test flow: login → create booking → search booking.
- Run the test in stages:
- Start with 60 seconds and 166 users.
- Gradually increase the number of users over time.
- Monitor response time, error rate, and throughput.

### For load testing:
- Simulate gradual user growth until performance levels off.

### For stress testing:
- Continue increasing users until the system breaks or errors occur.
- Record the exact time and user count when the server begins to fail.

## Request summary and statistics report
![Load_Test_Report](https://github.com/user-attachments/assets/d4c14e6e-26e1-423e-92a2-7c95da7324a2)

## Load Test Report
![load_test_excel](https://github.com/user-attachments/assets/c2c34ff8-e53c-4a42-8113-7caea7c5441a)

## Stress Test Report
![strees_test_excel](https://github.com/user-attachments/assets/a36ad82e-02a9-45c7-bba0-664e680f6a5c)



