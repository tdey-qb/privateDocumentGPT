# Environment Setup
In order to set your environment up to run the code here, first install all requirements:

```shell
pip3 install -r requirements.txt
```

### Running the FastAPI Backend

To run the FastAPI backend, execute the following command:
```
gunicorn app:app -k uvicorn.workers.UvicornWorker --timeout 1500
```
This command starts the backend server and automatically handles the necessary downloads for the language model and the embedding models. The `--timeout 500` option ensures that sufficient time is allowed for proper model downloading.

### Running the Streamlit App

Please update the `API_BASE_URL` to appropriate FastAPI url 

To run the Streamlit app, use the following command:
```
streamlit run streamlit_app.py --server.address localhost
```
This command launches the Streamlit app and connects it to the backend server running at `localhost`.