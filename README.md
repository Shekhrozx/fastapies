# FastAPI Easy Snippets

**FastAPI Easy Snippets** is a Visual Studio Code extension that provides code snippets for FastAPI to make life easier. Inspired by [fastapi-snippets](https://github.com/damildrizzy/fastapi-snippets).

## Features

### Snippets
`fes...` - Easy access to FES (FastAPI Easy Snippets).

| Abbreviation     | Description                |
| ---------------- | -------------------------- |
| `fesinit`        | FastAPI Init               |
|                  |                            |
| `fesaget`        | async GET path             |
| `fesapost`       | async POST path            |
| `fesaput`        | async PUT path             |
| `fesadel`        | async DELETE path          |
|                  |                            |
| `fesget`         | GET path                   |
| `fespost`        | POST path                  |
| `fesput`         | PUT path                   |
| `fesdel`         | DELETE path                |
|                  |                            |
| `fesbasemodel`   | Pydantic BaseModel         |
| `feserror`       | Custom Error Handling      |
| `fessqldb`       | SQLAlchemy Database        |
| `fesgetdb`       | SessionLocal Dependency    |
| `fesstup`        | Startup Event              |
| `fesshdn`        | Shutdown Event             |


## Usage

Initiate FastAPI app
```python
# fesinit :
from fastapi import FastAPI
app = FastAPI()

@app.get("/")
async def index():
    return {"message": "Hello FES APP"}
```

async GET path
```python
# fesaget :
@app.get('/path_name')
async def method_name(args):
    pass
```

GET path
```python
# fesget :
@app.get('/path_name')
def method_name(args):
    pass
```

Pydantic BaseModel
```python
# fesbasemodel :
class ModelName(BaseModel):
    field_name: str
```

...




## Contributing
Feel free to [submit a pull request on github](https://github.com/Shekhrozx/fastapies)


## Release Notes
See [changelog](CHANGELOG.md) for releases

## For more information



**Enjoy!**
