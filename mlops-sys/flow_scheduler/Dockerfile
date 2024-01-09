FROM prefecthq/prefect:2.11.0-python3.10

WORKDIR /root/flows

COPY requirements_sys.txt .
RUN pip3 install -r requirements_sys.txt

COPY --from=flow_dir requirements.txt .
RUN pip3 install -r requirements.txt

COPY --from=flow_dir . .

COPY setup.py .