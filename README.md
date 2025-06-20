#  Location Recommendation System

This project recommends locations to users based on different criteria, including their check-in-history, social connections, and travel routes. It can suggest nearby unvisited places, locations popular among a user's network, or convenient stops along a planned trip.
Features

![Image](https://github.com/user-attachments/assets/25ff0778-1f84-4a3d-8da5-ae6d7fc82b53)

## This system offers three main functionalities:

  - Personalized Location Recommendations: Recommends a list of 10 unvisited locations for a user based on their last check-in. The system identifies unvisited locations, ranks them by proximity, and uses the Mapbox API to calculate travel times.

  - Social-Based Recommendations: Suggests up to 15 unvisited locations based on the places visited by a user's "2-hop friends" (friends of friends).

  - Travel Plan Recommendations: Generates a travel plan with up to 10 recommended locations that have the shortest travel time along a specified route. It identifies clusters of locations along the route and suggests the fastest places to reach.

## How to Use

The project is run via a command-line interface. Upon starting, you will be prompted to select one of the three problems to solve.
  
  - For Personalized Recommendations:

      Enter 1 when prompted.
  
      Enter the desired user ID.

      The system will output a table of 10 recommended locations, including their distance and estimated travel time.

    Result example:
    
    ![Image](https://github.com/user-attachments/assets/39e38f08-e343-412b-8fad-dae124be4424)

  - For Social-Based Recommendations:

      Enter 2 when prompted.

      Enter the desired user ID.

      A table of recommended locations visited by 2-hop friends will be displayed.

    Result example:

![Image](https://github.com/user-attachments/assets/97dfb23e-edc2-4d75-be04-247c456399b1)

  - For Travel Plan Recommendations:

      Enter 3 when prompted.

      Enter the starting and ending points as latitude, longitude coordinates.

      The system will return a list of recommended locations along the route, optimized for the shortest travel time.

    Result example:

![Image](https://github.com/user-attachments/assets/c6f59f76-1121-4d36-8805-f838d613355e)
![Image](https://github.com/user-attachments/assets/6434d2bb-6f84-4e3b-9905-6c825fc70ee9)


## For each feature, you will be asked if you want to see a map visualization of the results. Answering yes will generate and open an interactive HTML map.
Technology Stack

  Distance Calculation: geopy

  Travel Time and Routing: Mapbox API

  Data Processing and Clustering: The system processes user check-in data, clusters locations, and handles sparse data by regrouping it.

  Map Visualization: Folium

  Spatial Analysis: GeoPandas
