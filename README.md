CognitiveXR Clients
===================

This repository collects links to clients and client SDKs for the [cognitivexr-platform](https://github.com/cognitivexr/cognitivexr-platform).

Unity
-----

[Unity Package](https://github.com/cognitivexr/cognitivexr-unity-client)
  
  Is a package that can be included into a Unity project via its package manager

* [CPOP](https://github.com/cognitivexr/cognitivexr-unity-client/blob/main/Runtime/Cpop)
  
  The Unity CPOP client connects to a CPOP stream and listens for updates

* [CogStream](https://github.com/cognitivexr/cognitivexr-unity-client/tree/main/Runtime/cogstream)
  
  Contains the MediatorClient and EngineClient. 
  The [MediatorClient](https://github.com/cognitivexr/cognitivexr-unity-client/blob/main/Runtime/cogstream/MediatorClient.cs) establishes a connection to the mediator, returns a list of available engines and facilitates the launch and connection to the engine. Once an engine is launched, the address, returned by the mediator client, can be passed to an EngineClient.
  The [EngineClient](https://github.com/cognitivexr/cognitivexr-unity-client/blob/main/Runtime/cogstream/EngineClient.cs) connects to an engine and supports a send and a receive channel.
  
  [Example Project](https://github.com/cognitivexr/unity-demo-app)

Python
------

* [Interactive CogStream desktop client](https://github.com/cognitivexr/CogStream/tree/main/clients/python)

  Client to interact with the mediator to start engines and stream the connected camera.
  Useful for debugging and developing.
  Navigate into `cogstream/clients/python`, create a virtual environment and install the requirements.
  With the mediator running you can then run `python -m interactive.main` and you should see something like this:
  ```
  % python -m interactive.main
  0: EngineSpec(name='debug', attributes={'format.colorMode': ['0'], 'format.height': ['0'], 'format.width': ['0']})
  1: EngineSpec(name='fermx', attributes={'format.colorMode': ['0'], 'format.height': ['0'], 'format.width': ['0']})
  2: EngineSpec(name='yolov5', attributes={'format.colorMode': ['0'], 'format.height': ['0'], 'format.width': ['0']})
  which engine do you want to use?: 
  ```
  Once an engine is selected, the client will attempt to stream the currently connected camera to the engine.
  

* [CogStream engine client library](https://github.com/cognitivexr/CogStream/blob/main/cogstream-py/cogstream/engine/client.py)

  Part of the cogstream python framework.
  Some of the python engines also come with an engine client for debugging, that demonstrates how the engine client library can be used.
  Here is one example: https://github.com/cognitivexr/CogStream/blob/main/engines/engines-py/fermx/fermx/client.py
