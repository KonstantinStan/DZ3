# Счетчик - бэкэнд

Бэкэнд счетчика.

## Установка

Выполните следующие команды

```sh
mkdir -p dist
poetry export --without-hashes --format constraints.txt --output dist/constraints.txt
poetry run python -m pip wheel --isolated --requirement dist/constraints.txt --wheel-dir dist/vendor
poetry build --format wheel
```

Или запустите `make build`.

## Развертывание

* Запакуйте собранный сервер командой `make package` в архив `server.tar.gz`;
* Скопируйте на сервер;
* Распакуйте и уставновите скриптом `install.sh`;

<img width="1260" height="624" alt="image" src="https://github.com/user-attachments/assets/d5e50b3d-ca97-44dd-90fa-ffecfe61c5e5" />

<img width="1263" height="420" alt="image" src="https://github.com/user-attachments/assets/5054f0b2-e2d8-432b-9f55-e04ebb927fee" />
