## Run project locally with docker-compose

* copy .env.example to .env
```bash
cp app/.env.example app/.env
```

run with docker-compose

```bash
docker-compose -d --build
```


## Links
* [FastAPI with Async SQLAlchemy, SQLModel, and Alembic](https://testdriven.io/blog/fastapi-sqlmodel/)

## Pre commit Hooks

```bash
pip install pre-commit
```
create a sample pre-commits file
```bash
pre-commit sample-config > .pre-commit-config.yaml
```
edit this file to add hooks
install hooks
```bash
pre-commit install --install-hooks
```

## Container registry



Links
* [pre-commit: A framework for managing and maintaining multi-language pre-commit hooks.](https://pre-commit.com/)
* [Github: Working with the Container registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry)


# Tests

run
```bash
pytest
```

Links
* [tavern-testing](https://tavern.readthedocs.io/en/latest/examples.html)