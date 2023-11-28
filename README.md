# prometheus_assignment
    1.Export the metrics (like request per second, memory usage, cpu usage etc) in the existing mini project given to Interns

    2.Install Prometheus and Grafana using Docker (with docker-compose)

    3.Configure prometheus (scrape configs) such way that it can scrape the metrics from default metric path of the application job

    4.Validate the entire configuration to check if the data is coming or not in Prometheus UI

    5.Create the Dashboards in Grafana on top of the metrics exported by adding the Prometheus as a Datasource.

# Steps To do assignment. <br>
<h3>Step 1: Set up Docker Environment <br></h3>
Install Docker and Docker Compose if you haven't already. <br>
<h3>Step 2: Create Application<br></h3>
Create a Flask application with metrics instrumentation. Create app.py file and add the python code into that file.<br> 
<h3>Step 3: Create Docker Compose File. <br></h3>
Create a docker-compose.yml file in a directory for your project.<br>
<h3>Step 3: Configure Prometheus <br></h3>
Add Prometheus Service:<br>
&nbsp &nbsp 1. Define the Prometheus service in the docker-compose.yml file.<br>
&nbsp &nbsp 2. Specify the image (prom/prometheus).<br>
&nbsp &nbsp 3. Mount the Prometheus configuration file (prometheus.yml) as a volume.<br>
Create prometheus.yml Configuration:<br></h5>
&nbsp &nbsp 1. Configure prometheus.yml to define jobs that scrape metrics from your application.<br>
&nbsp &nbsp 2. Define the scrape_configs for your application's metrics endpoint.<br>
<h3>Step 4: Configure Grafana <br></h3>
Add Grafana Service:<br>
&nbsp &nbsp 1. Define the Grafana service in the docker-compose.yml file.<br>
&nbsp &nbsp 2. Specify the image (grafana/grafana)<br>
&nbsp &nbsp 3. Mount Grafana data as volumes for persistence.<br>
<h3>Step 5: Start Services<br></h3>
Run docker-compose up -d to start all services defined in the docker-compose.yml file.<br>



        
        
