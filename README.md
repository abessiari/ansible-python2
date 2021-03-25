## Install using miniconda

To install miniconda go to [url](https://docs.conda.io/en/latest/miniconda.html)

This will install ansible, python and terraform.

conda env create --file dependencies/bare-metal.yml

conda activate test_purl_obolibrary

conda deactivate

conda env remove -n test_purl_obolibrary

terraform -chdir=aws init

terraform -chdir=aws apply

terraform -chdir=aws show

terraform -chdir=aws destroy
