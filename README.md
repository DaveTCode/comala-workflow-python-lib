[![Build Status](https://travis-ci.org/DaveTCode/comala-workflow-python-lib.svg?branch=master)](https://travis-ci.org/DaveTCode/comala-workflow-python-lib)

# Comala Workflow Python Library

This is a simple wrapper around the REST API which the Comala Workflow plugin 
for Confluence provides.

## Installation

To install from pypi use:

~~~~
pip install comala-workflows
~~~~

## Usage

```python
from comala.workflows.client import ComalaWorkflowsClient
client = ComalaWorkflowsClient("https://server:port/contextpath", ("user", "pass"))
status = client.status(page_id=1, expand="state,states,approvals,actions,tasks")
print(status.state.name)
print(len(status.tasks))
```

## Development and Deployment

See the [Contribution guidelines for this project](CONTRIBUTING.md) for details on how to make changes to this library.