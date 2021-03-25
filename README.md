# ansible-python2

conda env create --file dependencies/bare-metal.yml
conda activate test_purl_obolibrary
conda deactivate
conda env remove test_purl_obolibrary

terraform -chdir=aws init
terraform -chdir=aws apply
terraform -chdir=aws show
terraform -chdir=aws destroy
