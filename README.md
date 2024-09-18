# WebAPI Starter Code

This repository provides an introduction to the WebAPI for generating and analyzing human flow data. The WebAPI offers two major services: spatiotemporal data interpolation and spatiotemporal data provision, allowing users to retrieve or estimate geographic information based on specified conditions.

For actual code implementation and examples, please refer to the `StarterCode.ipynb` file included in this repository.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [API Functions](#api-functions)
- [Starter Code](#starter-code)
- [License](#license)

## Overview

The WebAPI provides services using HTTP communication to return results based on specified conditions. It is broadly categorized into two services:

1. **Spatiotporal Data Interpolation Service**:  
   This service allows users to match and estimate routes using road or railway networks and timetables, enabling the retrieval of location information (longitude and latitude) for a specified location.

2. **Spatiotemporal Data Provision Service**:  
   Users can specify arbitrary spatiotemporal ranges or attributes (e.g., gender, occupation) to search for human location data. The results can be provided in CSV format (longitude and latitude) or as images with background maps.

**Note**: To use this API, an account from the University of Tokyo Center for Spatial Information Science's JoRAS collaborative research system is required.

## Features

- **Session Management**: Create and manage sessions for interacting with the WebAPI.
- **Data Retrieval**: Retrieve interpolated spatiotemporal points based on geographic and temporal inputs.
- **Response Processing**: Parse and process JSON responses to extract relevant mobility data.

## API Functions

The WebAPI includes several functions that enable users to interact with spatial and temporal data:

- **CreateSession**: Perform JoRAS authentication and obtain a session.
- **DestroySession**: Destroy the session and log out.
- **GetNearestRoadPoint**: Retrieve the nearest road point for a specified geographic coordinate.
- **GetRoadRoute**: Retrieve road routes based on specified points (start, end, and waypoints).
- **GetRailRoute**: Retrieve railway routes based on specified station coordinates (start, end, and waypoints).
- **GetMixedRoute**: Retrieve both road and railway routes based on specified points (start, end, and waypoints). Mainly uses railways and other public transportation.
- **GetSTInterpolatedPoints**: Retrieve interpolated spatiotemporal points based on start and end coordinates, and time range.

## Starter Code

For detailed setup instructions and code examples, please refer to the `StarterCode.ipynb` file included in this repository. The notebook provides step-by-step guidance on how to authenticate, interact with the WebAPI, and process the results.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
