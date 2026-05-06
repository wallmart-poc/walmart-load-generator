# walmart-load-generator · Load Generator

Locust-based synthetic traffic generator. Simulates realistic user journeys against the frontend to drive load testing and performance validation.

## Stack
- **Language:** Python 3.11
- **Framework:** [Locust](https://locust.io/)

## Simulated flows
- Browse homepage and product pages
- Add items to cart
- Complete checkout flow
- Currency switching

## Running locally
```bash
pip install -r requirements.txt
locust -f locustfile.py --host=http://<frontend-addr>
```
Open the Locust web UI at `http://localhost:8089` to configure user count and spawn rate.

## Dependencies
Sends HTTP traffic to `walmart-frontend` only — all downstream service calls are made transitively through the frontend.
