.PHONY: env install lint test notebook train evaluate

# Создать окружение и установить зависимости через Poetry
install:
	poetry install

# Проверка стиля кода
lint:
	poetry run black src tests && poetry run flake8 src tests

# Прогон тестов
test:
	poetry run pytest -q

# Запуск Jupyter Notebook
notebook:
	poetry run jupyter notebook notebooks/01-exploration.ipynb

# Обучение модели
train:
	poetry run python -m src.{{cookiecutter.package_name}}.model --train

# Оценка модели
evaluate:
	poetry run python -m src.{{cookiecutter.package_name}}.model --evaluate
