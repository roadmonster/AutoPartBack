# AutoPartBack

This is a backend software for a online AutoParts Store.
To run it
  1. start service registry
  2. start config server
  3. start gateway server
  4. start order-service3
  5. start payment-service
  6. start demo (This is the inventory service)

Once all the service up running, go to localhost:8761 to check out the eureka portal if all the service up.
Then you are good to go verify the service availability on PostMan.

The inventory service is designed to be load balanced and cached. All the incoming request were diverted to
gateway server on port 8989 which will load balance between different services, and for same services will load
balance between different instances.

The config server is configured to pull configurations from git and each service will go to config server to pull
the latest changes. 
