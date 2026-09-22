# Mavlanov — MiniTorch Module 0

Первая часть домашнего задания по DL2. Основа — шаблон
[minitorch/Module-0](https://github.com/minitorch/Module-0).

Выполнены задания 0.1–0.4:

- базовые операции и их производные;
- проверки математических свойств через hypothesis;
- функции для обработки списков;
- режимы обучения и сбор параметров вложенных модулей.

Визуализация из задания 0.5 пропущена по разрешению преподавателя.

## Запуск

Используется Python 3.11, numpy 1.26.4 и numba 0.58.1 — сочетание из
уточнения преподавателя. Зависимости для визуализации не нужны.

```bash
python3.11 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip install --no-deps -e .
python -m pip check
python -m pytest -v
```

В `.github/workflows/minitorch.yml` настроен запуск всех тестов при загрузке
коммитов, создании pull request и ручном запуске. Проверка flake8 не включена
по уточнению преподавателя. В исходном шаблоне есть один тест с `xfail`:
вызов базового модуля без реализации `forward` должен завершаться ошибкой.

Для сдачи нужны ссылка на этот репозиторий и скриншот успешного GitHub Actions.
Локальный запуск тестов не заменяет Actions.

Локальная проверка на macOS, Python 3.11.16: `57 passed, 1 xfailed`.
Проверка `pip check` не обнаружила конфликтов зависимостей.

## Источники

- [Условие домашнего задания](https://github.com/thecrazymage/DL2_HSE/tree/main/homeworks/homework_01).
- [Условия модуля 0](https://minitorch.github.io/module0/module0/).
- Пояснения преподавателя, приложенные к заданию.
