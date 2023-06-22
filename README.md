# freelabel-2023-accessories
Notes for running the FreeLabel annotation tool on Ubuntu 18.04 and 20.04.


2023-06-22
Freelabel's repository is: [philadias/freelabel](https://github.com/philadias/freelabel).

Steps for installing FreeLabel, the `venv` method:

1. clone repository. `git clone --branch main --depth 1 https://github.com/philadias/freelabel.git`
2. enter the repository directory, `cd freelabel/`.
3. Create a directory for the python environment, `mkdir python-env`.
4. Create virtual environment: `python -m venv python-env`.
5. Activate virtual environment: `source ./python-env/bin/activate`.
6. Check on pip: `python -m pip install --upgrade pip`.
7. Install requirements: `python -m pip install -r requirements.txt`.
8. Recompile callRGR: 
	- `cd freelabel` (so the path is `freelabel/freelabel`)
	- `python setup.py build_ext --inplace`
	- `cd ..`
9. run Django project: `python manage.py runserver localhost:9000`
10. If problems, migrate before running the project: `python manage.py migrate`
