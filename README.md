# Dynamic Load Balancer with Health Checks

Developed using Node.js and Express, this project acts as a dynamic load balancer for a server cluster. Its goal is to minimize response time, maximize resource use, and prevent server overload by directing client requests to capable servers. It also seamlessly adapts to changes, redirecting traffic during server outages and integrating new servers automatically.

## Project Goals

- Develop a load balancer with the ability to route traffic across two or more servers.
- Integrate ongoing health checks for backend servers.
- Automate the process of handling servers that go offline due to failed health checks.
- Support the smooth reintegration of servers returning online after passing a health check.
  By fulfilling these goals, this load balancer provides a holistic solution for optimizing resource distribution, ensuring high availability, and enhancing resilience in distributed systems.

## Run Locally

Clone the project

```bash
  git clone https://github.com/rudra07-git/Load-Balancer.git
```

Go to the project directory

```bash
  cd my-project
```

Install dependencies

```bash
  npm install
```

Start the server in different terminals.

```bash
  node src/backend-servers/server1.js
```

```bash
  node src/backend-servers/server2.js
```

```bash
  node src/backend-servers/server3.js
```

Run the Load-Balancer server

```bash
  node src/load-balancer/index.js
```

## Running Tests

To validate the load balancer's ability to distribute requests efficiently, you can run multiple concurrent requests using curl.

Execute the following command to initiate the tests:

```bash
  curl --parallel --parallel-max 3 --config test/urls.txt
```

Feel free to adjust the --parallel-max option to control the level of parallelism to suit your testing needs.

## Acknowledgements

- [Coding Challenges By John Crickett](https://codingchallenges.fyi/challenges/challenge-load-balancer)
