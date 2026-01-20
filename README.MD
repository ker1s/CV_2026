```bash
# 1. Установи Jupyter глобально (один раз для всей системы)
pip install jupyterlab notebook

# 2. Для КАЖДОГО проекта создай venv
cd labX
python -m venv .venv
.venv\Scripts\activate

# 3. В КАЖДОМ venv установи ipykernel
pip install ipykernel numpy matplotlib opencv-python  # и другие зависимости проекта
# или 
pip install -r requirements.txt


# 4. Добавь ядро этого venv в глобальный Jupyter
python -m ipykernel install --user --name=.venv --display-name="labX"

# 5. Если добавил зависимости не забудь
pip freeze > requirements.txt

# 6. Удалить ядро
jupyter kernelspec uninstall .venv
```