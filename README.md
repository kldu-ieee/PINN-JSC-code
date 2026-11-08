Journal: Journal of Scientific Computing
Article: A Critical Review of Numerical Evidence for Neural PDE Methods
Authors: Lixia Jin, Longsheng Lu, Jiabin Lu, M. N. S. Swamy, Ke-Lin Du
Corresponding author: Ke-Lin Du
Affiliation: Multimodal Intelligent Transportation Laboratory, Guangzhou Digital Technology Group, Guangzhou 510656, China
Email: kldu@ieee.org
Supplementary material: Online Resource 1 (PINN-JSC-code.zip)

Journal: Journal of Scientific Computing
Article: A Critical Review of Numerical Evidence for Neural PDE Methods
Authors: Lixia Jin, Longsheng Lu, Jiabin Lu, M. N. S. Swamy, Ke-Lin Du
Corresponding author: Ke-Lin Du
Affiliation: Multimodal Intelligent Transportation Laboratory, Guangzhou Digital Technology Group, Guangzhou 510656, China
Email: kldu@ieee.org
Supplementary material: Online Resource 1 (PINN-JSC-code.zip)

# Reproducibility code for PINN_JSC.tex

Associated manuscript: *A Critical Review of Numerical Evidence for Neural PDE Methods*
Supplementary archive: `PINN-JSC-code.zip`

The six numerical scripts (01–06) generate the numerical calculations behind Figs. 1–5,
including the 32-sensor operator model and the eight-sensor retraining study.
Script 07 generates the publication figures from the saved JSON outputs.

Dependencies: Python 3, NumPy, Matplotlib, and PyTorch (see `requirements.txt`).
For consistent EPS output, install `pdftocairo` from Poppler when available.

    python -m pip install -r requirements.txt
    python run_all.py

Regenerate only figures from archived numerical results:

    python scripts/07_publication_figures.py

The source and numerical records are unchanged from the v112 audited calculation.
In the v112 audit, scripts 01–06 were rerun and the resulting values were compared
with the archived numerical outputs; this final editorial revision does not rerun
these simulations or change their results.

The conditional Gaussian reconstruction uses the assumed known Gaussian prior
and noiseless eight-sensor observations; its optimality refers to expected
squared *absolute* field error, not the reported median relative error.

The manuscript's LaTeX source and original artwork are supplied separately.
