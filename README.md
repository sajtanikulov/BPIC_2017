# BPIC 2017 – Event Log Analysis Repository

This repository contains resources for analysing the **BPI Challenge 2017 (BPIC 2017)** event log as part of a process-mining and data-science workflow.  
It includes:

- The **large BPIC-17 XES log** (stored via Git LFS)  
- A **BPMN model**  
- A **PDF document**  
- A **Jupyter Notebook** used for exploring and analysing the dataset

The repository is fully Git-LFS-enabled so you can clone it safely, even though one file exceeds 500 MB.

---

## 📦 Repository Contents

```

BPIC_2017/
│
├── BPI_Challenge_2017.xes        # ~550 MB event log (Git LFS)
├── BPIC_2017.pdf                 # Project-related PDF file
├── BPIC_2017 (2).bpmn            # BPMN diagram of the loan process
├── BRIC17 (12).ipynb             # Jupyter Notebook for analysis
└── .gitattributes                # Git LFS tracking configuration

````

---

## ⚙️ Requirements

To properly work with this repository, you need:

- **Git**
- **Git LFS** (required for downloading the large XES file)
- **Python 3.7+** (if you want to run the notebook)
- **Jupyter Notebook** or JupyterLab
- Common data-science libraries (`pandas`, `numpy`, `pm4py`, etc.)

---

## 🚀 Cloning the Repository (IMPORTANT)

This repository contains a **large XES file tracked by Git LFS**.  
If Git LFS is not installed, you will only download a pointer file instead of the dataset.

### 1. Install Git LFS

Download from:  
https://git-lfs.github.com

Or install via terminal:

```bash
git lfs install
````

### 2. Clone the repository

```bash
git clone https://github.com/sajtanikulov/BPIC_2017.git
cd BPIC_2017
```

### 3. Ensure LFS files are downloaded

Normally this happens automatically.
To force it:

```bash
git lfs pull
```

### 4. Verify LFS files

```bash
git lfs ls-files
```

You should see:

```
<sha> * BPI_Challenge_2017.xes
```

---

## 🧠 About the BPIC 2017 Dataset

The BPIC 2017 event log originates from a financial institution’s **loan application process**.
It contains:

* **31,509 cases**
* **More than 1.2M events**
* **Highly variable case durations**
* **15,000+ unique process variants**
* Rich attributes for advanced process analysis (timestamps, activities, resources, outcomes)

This dataset is widely used for:

* Process discovery (e.g., Inductive Miner, Heuristics Miner)
* Conformance checking
* Performance analysis
* Time prediction
* Simulation and optimisation

---

## 📘 Using the Notebook

To run the analysis notebook:

1. Create a Python virtual environment (optional):

   ```bash
   python -m venv venv
   ```

   Activate it:

   * Windows: `venv\Scripts\activate`
   * Mac/Linux: `source venv/bin/activate`

2. Install required libraries:

   ```bash
   pip install pandas numpy pm4py jupyter
   ```

3. Launch Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open:

   ```
   BRIC17 (12).ipynb
   ```

---

## 🔧 Git LFS Notes

This repository uses `.gitattributes` to track XES files via LFS:

```
*.xes filter=lfs diff=lfs merge=lfs -text
```

This ensures:

* The large event log does **not** bloat the repository
* Clones remain fast and safe
* The dataset is downloaded only when needed

To check which files are under LFS:

```bash
git lfs ls-files
```

---

## 📄 License

This repository is intended for **educational and research purposes**.
Please comply with any usage restrictions associated with the original BPIC 2017 dataset.

---

## 🤝 Contributions

Pull requests and issue reports are welcome — whether improving the notebook, adding new process-mining analyses, or extending documentation.

---

Happy exploring and analysing the BPIC 2017 event log!
