FROM arm64v8/python:3.7

RUN apt-get update && apt-get install -y libsndfile1 ffmpeg && \
    git clone --depth 1 --branch v2.3.0 https://github.com/deezer/spleeter.git

COPY poetry.lock pyproject.toml /spleeter

RUN pip install poetry && pip3 install llvmlite==0.38.0 && cd /spleeter && poetry add markdown==3.3.4 && poetry add h5py==3.6.0

RUN cd /spleeter && poetry build && pip install ./dist/spleeter-2.3.0-py3-none-any.whl

