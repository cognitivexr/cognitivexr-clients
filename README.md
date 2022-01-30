CognitiveXR Clients
===================

This repository collects links to clients and client SDKs for the [cognitivexr-platform](https://github.com/cognitivexr/cognitivexr-platform).

Unity
-----

TODO: link

* CPOP
* CogStream

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

  Part of the cogstream python framework 
