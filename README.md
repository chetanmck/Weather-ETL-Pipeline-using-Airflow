# Weather-ETL-Pipeline-using-Airflow

This project is an ETL pipeline that extracts real-time weather data for Overland Park using the Open-Meteo API, transforms it, and loads it into a PostgreSQL database using Apache Airflow. The pipeline is designed to run daily, storing weather information like temperature, windspeed, and direction.

Project Structure

DAG:
•	extract_weather_data(): Fetches real-time weather data for Overland Park.
•	transform_weather_data(): Extracts essential weather details.
•	load_weather_data(): Loads the transformed data into PostgreSQL.

Docker Compose Configuration:The PostgreSQL database is set up using Docker. 



Running Locally
	
1.	Start PostgreSQL: Run docker-compose up to start the PostgreSQL service with persistent storage using the postgres_data volume.
2.	Start Airflow: Run astro dev start to start the Airflow environment.
3.	Access Airflow UI: Go to http://localhost:8080 (Username/Password: admin).
4.	Monitor the DAG: View DAG execution and task logs in the Airflow UI.
5.	Real-Time Data Visualization: Use DBeaver or any SQL client to connect to the PostgreSQL database (localhost:5432) to view and query the real-time weather data stored in the weather_data table.
