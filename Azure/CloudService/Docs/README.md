# Alarm Service

Azure Worker Role are waiting for alerts from Azure Event Hub (ehalers) and if there is an overfit of temperature limits send beep command to device.

You have to add Worker policy with Listen rights for ehalerts.

## app.config 

Before run and build application configure the app.config in the project folder.

*Microsoft.ServiceBus.ConnectionStringAlerts* connection string to `ehalerts` event hub with Worker policy.

*Microsoft.ServiceBus.ConnectionStringDevicesService* connection string to Topic with WebService policy.

*Microsoft.Storage.ConnectionString* data storage parameters for IEventProcessor of Event Hubs SDK. 