pip install virtualenv
virtualenv comp90089
source comp90089/bin/activate

comp90089/bin/pip install google-cloud-bigquery
pip install jupyter
python -m ipykernel install --user --name=comp90089 --display-name "MLAH"
jupyter notebook

brew install --cask google-cloud-sdk
