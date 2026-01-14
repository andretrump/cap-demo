## Init project
- Explain scenario
- Run `cds init`
- Run `npm i`
- Explain folder structure

## Add domain model
- Create schema.cds
- Copy local part of domain model

## Add order service
- Add order-service.cds with everything except for `submitOrder` and auth checks
- Start app with `cds watch`
- Show running OData service without data

## Add test data
- Add all CSV files
- Delete supplier ID column from books
- Show OData service with test data

## Add custom submit order action
- Explain custom actions
- Add action to cds
- Create service implementation and add handler
- Demonstrate action

## Add admin service
- Explain reasoning (one service per use case, different user groups)
- Create admin-service.cds with auth checks
- Add auth check to `submitOrder`

## Add remote data
- Explain use case (need to integrate business partners as suppliers)
- Open business accelerator hub and show business partner service
- Download definition
- MAKE SURE APP IS NOT RUNNING!
- Copy service definition AND env file with API key
- Run cds import
- Add credentials section to package.json
- Add supplier entity to schema.cds
- Add supply-monitoring-service with handler to forward to business accelerator hub
- Install required dependencies with `npm i @sap-cloud-sdk/http-client @sap-cloud-sdk/resilience`
- Show service with remote data

## Add mashup
- Add associations to Books and Suppliers in schema.cds
- Add handler for mashup to service implementation

## Deployment
- Add configuration using `cds add mta,hana,xsuaa --for production`
- Add flag `"restrict_all_services": false` to auth section
- Build and deploy
- Show additional materials while deployment is running
- Demonstrate running app in BTP cockpit
