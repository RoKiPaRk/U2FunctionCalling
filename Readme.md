## Sample AI chatbot for Multivalue
This project is based on Python, Chainlit, UOFast, and the U2 Unidata database. It provides a RESTful service using UOFast and integrates with Chainlit for conversational AI capabilities.

### Table of Contents

#### Installation
##### Download Anaconda:
Go to the Anaconda website and download the installer for your operating system.
##### Install Anaconda:
Follow the instructions provided by the installer.

Here are the docs -> https://docs.anaconda.com/anaconda/install/windows/

##### Setting Up the Conda Environment

Create a new Conda environment:
```
conda create -n myenv python=3.9
conda activate myenv  ( this is to activate the environment)
```

##### Install required packages:

```pip install chainlit uofast langchain llm-axe langchain_experimental```

#### Usage
#### Starting UOFast 
#### Edit UOFast.cfg:
Configure the necessary settings in the UOFast.cfg file located in the 
your project installation directory. 

```Below is an example configuration:
[UOConnectionSettings]
UOhost = <Server name or IP Address>
UOaccount = <Account path e.g. C:\U2\UD82\DEMO\>
UOservice = <udcs for Unidata>
UOport = <UniRPC port in UniObjects e.g. 31438>
UOuser = <Unidata user id>
UOpassword = <Unidata password>

[ApplicationSettings]
Mainlogname = UOFastMainAPI.log
UOConnectionLogs = UOConnectionProcesses.log

[PoolSettings]
Initial_connections = 2
max_connections = 2
session_timeout = 600
reap_interval = 180
```

##### Starting UOFast
##### Run the UOFast server:

```uvicorn UOFast.main:server.app --port=8200```

#### Running OllamaLLMAxe.py in Chainlit
Run the OllamaLLMAxe.py python file in ChainLit

```chainlit run OllamaLLMAxe.py ```

