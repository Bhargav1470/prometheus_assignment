# prometheus_assignment
    1.Export the metrics (like request per second, memory usage, cpu usage etc) in the existing mini project given to Interns

    2.Install Prometheus and Grafana using Docker (with docker-compose)

    3.Configure prometheus (scrape configs) such way that it can scrape the metrics from default metric path of the application job

    4.Validate the entire configuration to check if the data is coming or not in Prometheus UI

    5.Create the Dashboards in Grafana on top of the metrics exported by adding the Prometheus as a Datasource.

# Steps <br>
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
<h3>Step 5: Start Containers<br></h3>

`$docker-compose up -d`
<h3>Step 6: Validate Configuration<br></h3>
Access Prometheus UI:<br>
&nbsp &nbsp 1. Go to http://localhost:9090 to access the Prometheus UI.<br>
&nbsp &nbsp 2. Check the Status > Targets section to verify if your application's target is up and scraped successfully.<br>
<h3>Step 7: Set up Grafana Dashboard<br></h3>
Access Grafana UI:<br>
&nbsp &nbsp Visit http://localhost:3000 to access the Grafana UI.<br>
Add Prometheus as a Datasource:<br>
&nbsp &nbsp       Go to Configuration > Data Sources > Add Data Source.<br>
&nbsp &nbsp       Choose Prometheus and configure the URL (http://localhost:9090)<br>
Create Dashboards:<br>
&nbsp &nbsp  Go to Create > Dashboard.<br>
&nbsp &nbsp  Add a new panel and select the Prometheus data source.<br>
&nbsp &nbsp  Use queries to visualize the metrics exported by your application.<br>
<h3>Step 8: Select and Run Queries<br></h3>
Query for CPU Usage<br>
&nbsp &nbsp Under the "Metric" field, select 'flask_cpu_usage_percent'.<br>
&nbsp &nbsp Click "Run queries" to see the visualization on the dashboard.<br>
<h3>Screenshots<br></h3>
Prometheus Targets Page<br>

![image](https://github.com/Bhargav1470/prometheus_assignment/assets/90518660/623d187e-f982-4e5f-b08d-cded3e32f313)

Dashboard in Grafana: Visualizing Flask Application Metrics<br>
![image](https://github.com/Bhargav1470/prometheus_assignment/assets/90518660/0ab2aa10-a378-4e3b-847a-cf1aeb4d1047)

![image](https://github.com/Bhargav1470/prometheus_assignment/assets/90518660/346dfa0d-697a-43a0-bec5-1bb97ced9f1a)


Metrics
![image](https://github.com/Bhargav1470/prometheus_assignment/assets/90518660/ce92425a-c10e-4703-b80a-495339aa2f8f)

        
        
