# Diagrams

Diagram as Code

## How to Run

### Create Virtualenv

`virtualenv venv`

### Activate Virtualenv

`source venv/bin/activate`

### Install Requirements

`pip install -r requirements.txt`

### Render Diagrams

`python [file.py]`


```python
from diagrams import Diagram
from diagrams.aws.compute import EC2
from diagrams.aws.database import RDS
from diagrams.aws.network import ELB

with Diagram("Web Service", show=True, graph_attr={"bgcolor": "white"}):
    ELB("lb") >> EC2("web") >> RDS("userdb")
```

![diagram](./.github/web_service.png)
