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
| `fesadef`        | async function             |
| `fesbasemodel`   | Pydantic BaseModel         |
| `feserror`       | Custom Error Handling      |
| `fessqldb`       | SQLAlchemy Database        |
| `fesgetdb`       | SessionLocal Dependency    |
| `fesstup`        | Startup Event              |
| `fesshdn`        | Shutdown Event             |


## Usage

### Initiate FastAPI app (*`fes + init`*):

```python
# fesinit :
from fastapi import FastAPI
app = FastAPI()

@app.get("/")
async def index():
    return {"message": "Hello FES APP"}
```

### `async`  [METHOD] path (*`fes + a + [method]`*):
> methods: `GET`, `POST`, `PUT`, `DEL`
```python
# fesaget :
@app.get('/path_name')
async def method_name(args):
    pass
```

### `sync` [METHOD] path (*`fes + [method]`*):
> methods: `GET`, `POST`, `PUT`, `DEL`
```python
# fesget :
@app.get('/path_name')
def method_name(args):
    pass
```

### Pydantic BaseModel (*`fes + basemodel`*):
```python
# fesbasemodel :
class ModelName(BaseModel):
    field_name: str
```

### Custom Error Handling (*`fes + error`*):
```python
# feserror :
class CustomException(Exception):
    def __init__(self):
        pass

@app.exception_handler(CustomException)
async def custom_exception_handler(request: Request, exc: CustomException):
    return JSONResponse(
        status_code=status_code,
        content={'message': 'message'}
    )
```

...


## Contributing
Feel free to [submit a pull request on github](https://github.com/Shekhrozx/fastapies)


## Release Notes
See [changelog](CHANGELOG.md) for releases

## For more information



**Enjoy!**
