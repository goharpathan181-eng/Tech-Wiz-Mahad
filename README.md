After extracting it, run these exact commands:

cd /d "C:\Users\Students\Downloads\DineIQ-Fully-Integrated-Production"

python -m venv .venv

.venv\Scripts\activate

python -m pip install -r requirements.txt

python scripts\check_environment.py

Then:

python spark\00_smoke_test.py

Then:

python scripts\run_pipeline.py --schema-mode explicit

For FastAPI:

python scripts\run_backend.py

Do not run python -m uvicorn app.main:app from the root anymore.
