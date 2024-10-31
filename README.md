# UrbanSync

UrbanSync is a smart contract designed to facilitate efficient management of various city resources, including parking, waste management, and energy allocation. Built in Clarity, UrbanSync provides a structured, secure, and automated framework for municipalities and authorized entities to control and monitor resource usage across urban areas, with integrated IoT device support for real-time updates.

## Features

- **Parking Management**: Reserve parking spots, manage parking fees, and monitor availability.
- **Waste Management**: Track waste bin fill levels and trigger service notifications when needed.
- **Energy Allocation**: Allocate and monitor energy usage for various city resources.
- **IoT Device Integration**: Register and monitor IoT devices, enabling automation and real-time data collection.
- **Admin Controls**: Designed with admin-level control to ensure authorized access and resource configuration.

## Contract Structure

### Constants
- **Error Codes**: Standardized error codes for managing authorization, parameter validation, and resource availability.
- **Resource Types**: Defined constants for resource types, including parking, waste, and energy.

### Data Variables
- **Admin**: Stores the contract administrator's principal for authorized actions.
- **Resource Count**: Tracks the total number of registered resources.
- **Parking Fee & Energy Rate**: Configurable rates for parking and energy allocation.

### Maps
- **Resources**: Stores data on registered resources with information on type, location, capacity, and pricing.
- **Parking Spots**: Tracks each parking spot's status, occupancy, and reservation details.
- **Waste Bins**: Manages fill levels, collection times, and service needs.
- **Energy Consumption**: Allocates and monitors energy usage for resources by user.
- **IoT Devices**: Stores information on IoT devices, including their association with resources and activity status.

## Functions

### Public Functions

- **register-resource**: Allows the admin to add new resources such as parking spots, waste bins, or energy stations to the contract.
- **reserve-parking**: Facilitates parking reservations by deducting the parking fee and updating resource availability.
- **update-waste-level**: Updates the fill level of waste bins and triggers service notifications as required.
- **allocate-energy**: Allocates energy to a specific resource and charges users based on consumption.
- **register-iot-device**: Enables admins to register IoT devices, linking them with resources for real-time data integration.

### Read-only Functions

- **get-resource-details**: Retrieves details for a specified resource by ID.
- **get-parking-status**: Provides information on the status of a parking spot.
- **get-waste-bin-status**: Displays the current fill level and service status of a waste bin.
- **get-energy-usage**: Fetches energy allocation and usage details for a specific user and resource.
- **get-device-status**: Returns the current status of a registered IoT device.

## Authorization

Only the admin, assigned at contract deployment, can register resources and IoT devices. Public functions for parking reservation, waste level updates, and energy allocation are accessible to any user, while automated payment deductions ensure seamless usage.

## Installation

1. Clone this repository.
2. Deploy the `UrbanSync` contract in a Clarity-compatible blockchain environment (e.g., Stacks blockchain).
3. Configure the initial admin principal and variable values as needed.

## Usage

1. **Admin Registration**: Set the admin upon contract deployment.
2. **Resource Registration**: Register parking, waste, and energy resources using `register-resource`.
3. **IoT Device Registration**: Link IoT devices with city resources via `register-iot-device`.
4. **Resource Usage**:
   - Reserve parking and manage availability.
   - Track and update waste bin levels.
   - Allocate energy to specific resources, with payments processed automatically.

## Error Handling

Standard error codes handle:
- Unauthorized access
- Invalid resource types or parameters
- Resource unavailability
- Insufficient payments

## License

This project is open-source.