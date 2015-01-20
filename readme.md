Example usage for the CordovaService plugin (https://github.com/Khopa/CordovaService)

##Installing examples :##

- Install this folder as a plugin (This will also install CordovaService)

```
cordova plugin add https://github.com/Khopa/CordovaService-Examples
```

##Running the example services :##

Call the following Javascript code in your Cordova app after the ready event to start the example services :


```javascript
service.startService("com.alu.service.example.ExampleServiceA",
                function(result){
                    console.log(result);
                },
                function(error){
                    console.log(error);
                });
                
service.startService("com.alu.service.example.ExampleServiceB",
                function(result){
                    console.log(result);
                },
                function(error){
                    console.log(error);
                });
```


The services are registered in the manifest. If you want to start your own service, you'll need to register them in the manifest too.

##Checking the log messages##

Run the following command in the terminal

```
adb logcat ServicePlugin:d *:S
```

*Example trace after calling some methods :*

```
D/ServicePlugin(16664): Starting service : com.alu.service.example.ExampleServiceA
D/ServicePlugin(16664): Service ExampleServiceA is starting
D/ServicePlugin(16664): Hello from Service ExampleServiceA
D/ServicePlugin(16664): Hello from Service ExampleServiceA
D/ServicePlugin(16664): Hello from Service ExampleServiceA
D/ServicePlugin(16664): Starting service : com.alu.service.example.ExampleServiceB
D/ServicePlugin(16664): Service ExampleServiceB is starting
D/ServicePlugin(16664): Hello from Service ExampleServiceB
D/ServicePlugin(16664): Hello from Service ExampleServiceA
D/ServicePlugin(16664): Hello from Service ExampleServiceB
D/ServicePlugin(16664): Hello from Service ExampleServiceA
D/ServicePlugin(16664): Hello from Service ExampleServiceB
D/ServicePlugin(16664): Stopping service : com.alu.service.example.ExampleServiceA
D/ServicePlugin(16664): Service ExampleServiceA is being destroyed
D/ServicePlugin(16664): Service ExampleServiceA thread is dead
D/ServicePlugin(16664): Hello from Service ExampleServiceB
D/ServicePlugin(16664): Stopping service : com.alu.service.example.ExampleServiceB
D/ServicePlugin(16664): Service ExampleServiceB is being destroyed
D/ServicePlugin(16664): Service ExampleServiceB thread is dead
```

See the full doc for the javascript interface here : https://github.com/Khopa/CordovaService
