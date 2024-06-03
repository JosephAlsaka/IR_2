# Search_Engine
To run the program, you first need to download the NLTK library.

Datasets:
Antique/train (https://ir-datasets.com/antique.html#antique/train)
Lotte/science/dev/forum (https://ir-datasets.com/lotte.html#lotte/science/dev/forum)


To run the offline section, you need to run these two files (one for Antique and one for Lotte): `final_lotte.ipynb`, `final_antique.ipynb`.

To run the online section, you need to run each service on a different port:

1. `python -m uvicorn FastApi:app_main --reload --port 8000`
2. `python -m uvicorn FastApi:app_processing --reload --port 8001`
3. `python -m uvicorn FastApi:app_vectorization --reload --port 8002`
4. `python -m uvicorn FastApi:app_ranking --reload --port 8003`

swagger: [Localhost:8000/docs](http://127.0.0.1:8000/docs)
