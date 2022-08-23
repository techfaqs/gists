# Installing python packages on Mac M1

If you are here, you are already on **python3**, first set up a [venv](https://docs.python.org/3/tutorial/venv.html#creating-virtual-environments)
or a different python from the system python (which comes with the OS),
_this is so that you don't mess that in any case!_

Now run,

```
pip install --upgrade pip
```

### Numpy And Pandas

```
pip install cython

pip install --no-binary :all: --no-use-pep517 numpy

pip install pandas
```

### Scipy

```
pip install cython pybind11
pip install pythran

brew install openblas gfortran
export OPENBLAS=/opt/homebrew/opt/openblas/lib/

pip install --no-binary :all: --no-use-pep517 scipy
```

Reference: [(SO)Install SciPy on Apple Silicon (ARM / M1)](https://stackoverflow.com/a/66536896/2142994)

### SkLearn

```
pip3 install -U --no-use-pep517 scikit-learn
```

### PyTorch

```
pip install torch
```

### PySpark

```
PYSPARK_HADOOP_VERSION=3 pip install pyspark
```

### PyArrow

```
brew install apache-arrow
pip install pyarrow
```
