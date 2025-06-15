## Basic load testing demo with JMeter

This demo includes a screen recording of the load test.

Purpose: load test 'my-jmeter-site.ddev.site' with 102 virtual users

Test cases: 6 scenarios identified which resembles common day to day activities 


Acceptance Criteria:  
* Response Time          "Avg. response time < 500msec for 95% of requests"
* Throughput	          "≥ 20 requests/second"
* Error Rate	          "Error rate < 1%"
* Resource Utilization	"CPU < 60%, Memory < 20%"

Other notes:
* This is a fictitious load testing project with the above conditions for demo purposes.
* my-jmeter-site.ddev.site is a custom drupal site running locally in my local machine.
* JMeter script is organized using logic controllers for script reusability.
* Test Case 1 to 6 are basic user activities which will ran simulatenously.
* Each test case runs 17 virtual users (16.67% throughput) during the load test.
* This load test simulates 102 virtual users running in 5 minutes.
* Load test follows a trapezoidal load with 10% ramp up, 80% sustained load, and 10% ramp down

Listeners are set to capture reporting/results:

* 'PerfMon Metrics Collector' listener collects server side resource utilization (ServerAgent.sh should be running in the server so that 'PerfMon Metrics Collector' can collect data)
* 'Aggregate Report' listner captures the following results: Response Time, Throughput, Error Rate

