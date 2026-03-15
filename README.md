# Molecule visualiser!
<img src="example/paracetamol.jpeg" width=300 height=300>
Generate nice icons of molecules from SMILES.

This program follows the topology of SMILES chemical structures and creates an icon.
The atoms' colours are inspired by the [CPK colouring convention](https://sciencenotes.org/molecule-atom-colors-cpk-colors/)

## Try the web app:

[Molecule-visualiser](https://atoms-molecule-visualiser.streamlit.app/) powered by streamlit

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://atoms-molecule-visualiser.streamlit.app/)

## Cite this work:

If you use the icons please cite this project:

```
Lucandia. Lucandia/Molecule-Icon-Generator; Zenodo, 2022. https://doi.org/10.5281/ZENODO.7388429.
```
[![DOI](https://zenodo.org/badge/530035520.svg)](https://zenodo.org/badge/latestdoi/530035520)

## Run it on local:

### Step 1: clone the repository

```
git clone https://github.com/anshk1234/molecule-visualiser.git
```

### Step 2: install packages and requirements

For Linux:

```
xargs -a packages.txt sudo apt-get install 
pip install -r requirements.txt
```

### Step 3: Have Fun

- Run the code from the command line:

 ```
  python molecule_icon_generator.py "CC(=O)Nc1ccc(cc1)O" --name paracetamol --rdkit_svg
 ```

- Or from the python interpreter:

 ```
 import molecule_icon_generator as mig 
 molecule = mig.parse_structure("CC(=O)Nc1ccc(cc1)O", remove_H=False)
 mig.icon_print(molecule, name = 'paracetamol', rdkit_svg = True, single_bonds = False, remove_H = False, verbose=False)
 ```

- Or use the Streamlit functionalities! From the terminal run:

 ```
python -m streamlit run streamlit_app.py
 ```
 


## License

Code is licensed under the MIT License 

[![License: GPL-3.0](https://img.shields.io/badge/License-MIT%20-lightgrey.svg)](https://github.com/anshk1234/molecule-visualiser/blob/main/LICENSE)

---


