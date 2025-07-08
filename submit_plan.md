# ✅ 1. Use Python 3.11

Make sure Python 3.11 is installed and available in your PATH. You can download it from [python.org](https://www.python.org/downloads/release/python-3110/).

Check your Python version:

```sh
python --version
```

## 🧱 2. Project Structure

Your bot folder should look like this:

```text
stuxbot/
├── run.py
├── ladder.py
├── stuxbot/
│   ├── __init__.py
│   └── my_bot.py
├── cython_extensions/
│   └── *.so  (from cython-extensions-sc2)
├── requirements.txt
└── README.md
```

---

## 📥 3. Get Precompiled Cython Extensions

1. Download from: [AresSC2/cython-extensions-sc2 Releases](https://github.com/AresSC2/cython-extensions-sc2/releases)
2. In the list of assets, look for and download `ubuntu-latest_python3.11.zip` (if available for your release).
3. Extract the `cython_extensions/` folder into your bot root.

---

## 🧪 4. Test Locally

Run these commands to test your bot locally:

```sh
python run.py         # For local testing
python ladder.py      # Simulates AI Arena ladder environment
```

---

## 📄 5. Create requirements.txt

Export your dependencies with:

```sh
poetry export --without-hashes --only main -f requirements.txt > requirements.txt
```

Ensure `requirements.txt` includes:

- python-sc2
- cython-extensions-sc2
- numpy

---

## 🗜️ 6. Zip Your Bot

From the parent directory, run:

```sh
cd ..
zip -r MyAresBot.zip MyAresBot
```