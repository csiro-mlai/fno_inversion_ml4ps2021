# 🎰🎰🎰 hackfest-ppl 🎰🎰🎰


## Install dependencies

This step should work for everyone:

```bash
git clone https://github.com/csiro-mlai/fno_inversion_ml4ps2021.git
cd fno_inversion_ml4ps2021
```

Now, install the requirements.
Local desktop, bash shell:

```bash
python3 -m venv --prompt fno_inversion_ml4ps2021 ./venv
source ./venv/bin/activate
pip install -r requirements.txt
jupyter lab operator_inversion.ipynb
```

This should work for Linux, macos, or Windows Susbystem for Linux. 
For windows native, you are on your own, good luck.

### Choosing regularisation

To experiment with selecting the regularisation parameter you will need a large validation data set.
Here is one.

```bash
wget https://cloudstor.aarnet.edu.au/plus/s/FblQ6LxQtCosPkq/download -O ./data/grf_forcing_mini_1.h5
```

### Graphical models

If you wish to additionally visualize graphical models, you need graphviz.
Depending on your platform this will be something like

```bash
brew install graphviz       # MacOS with homebrew
conda install graphviz      # anaconda
sudo apt install graphviz   # Debian/ubuntu/WSL default
# etc
```

[Graphviz on Windows is complicated](https://forum.graphviz.org/t/new-simplified-installation-procedure-on-windows/224) so once again, use WSL.

### Developer setup

If you want to contribute back to this repository, please do.
To keep the storage small(er) we strip out all the notebooks using [nbstripout](https://github.com/kynan/nbstripout):

```bash
nbstripout --install --attributes .gitattributes
```

## Authors

- [Dan MacKinlay](http://danmackinlay.name)

With input from

- Alasdair Tran
