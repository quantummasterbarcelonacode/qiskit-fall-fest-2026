# Simulating a quantum computer on your laptop

MQST Qiskit Fall Fest 2026 challenge (Qiskit + Tensor Networks).

Everything you need is in this folder:

`challenge_statement.md` is the challenge itself, in two pages. Read it first.
`tn_qiskit_challenge.ipynb` is the notebook you will work in.
`requirements.txt` lists the Python dependencies.
`../lanyon2011.pdf` is the paper the challenge reproduces.

## Setup

You need Python 3.10 or newer, 3.12 recommended. Then:

```bash
python3 -m venv .venv
source .venv/bin/activate            # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab tn_qiskit_challenge.ipynb
```

This must print both version numbers without errors:

```bash
python -c "import qiskit, qiskit_aer; print(qiskit.__version__, qiskit_aer.__version__)"
```

## How the challenge works

The notebook is divided into two parts: a main track (parts 1 to 5), and a second part with a set of additional work (part 6). 

Do the main track in order to be able to answer the main question.
The additional work is a pure bonus, so start them only once you finish the main part.

Code cells marked `# Your code goes here:` are for you to fill in with your code.

Some sections end with questions and a `> Your answer:` slot. Answer them with the results you measure on your own computer. The notebook with those answers will serve as the final report to be graded, together with a live defence. The code is an instrument, while answering the main question is what will weigh more. During the live defence, demonstrating clear conceptual understanding will be especially valued.

Part 1 builds a state vector simulator and finds your machine's memory wall. Part 2 adds a
sparse matrix and Krylov solver, still exact but much cheaper, and asks whether it moved that
wall. Part 3 reproduces the trapped-ion experiment and compares first and second order Trotter
steps. Part 4 builds a matrix product state simulator with SVD truncation and entanglement
entropy. Part 5 is the experiment: push everything until it breaks, across system size and
interaction range, and then write your verdict.

Work at your own pace.

Good luck.
