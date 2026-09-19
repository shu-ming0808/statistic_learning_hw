此作業為中央統計研究所(NCU STAT) 碩二上學期開的統計學習課程作業

參考用書：An Introduction to Statistical Learning with application in python
書本連結：https://www.statlearning.com/

## Python 環境

使用 Python 3.10，虛擬環境放在 `.venv`。

在此資料夾開啟 PowerShell，首次建立環境：

```powershell
uv venv --python 3.10 .venv
uv pip sync --python .venv/Scripts/python.exe requirements-lock.txt
.\.venv\Scripts\python.exe -m ipykernel install --user --name ncu-stat-learning --display-name "Python (NCU Statistical Learning)"
```

啟用環境：

```powershell
.\.venv\Scripts\Activate.ps1
```

若 PowerShell 不允許執行啟用腳本，可以直接使用環境中的 Python，不需修改執行原則：

```powershell
.\.venv\Scripts\python.exe -m jupyterlab
```

開啟 `1.ipynb` 後，選擇核心 `Python (NCU Statistical Learning)`；在 VS Code 也可直接選擇 `.venv\Scripts\python.exe`。套件已預先安裝，可略過 Notebook 第一格的 `pip install`。

`requirements.txt` 列出直接依賴，`requirements-lock.txt` 固定完整套件版本。新增套件後可用以下指令重新產生版本清單並安裝：

```powershell
uv pip compile --python .venv/Scripts/python.exe requirements.txt -o requirements-lock.txt
uv pip sync --python .venv/Scripts/python.exe requirements-lock.txt
```
