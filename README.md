# EGA_dataset
Setting up the EGA dataset and download
https://github.com/EGA-archive/ega-download-client
## Steps
1. Get the access by email and create the ega account
2. Download the pyega3 client in a _new conda envrionment_ by
```
conda install pyega3
```
3. Check if the client is installed successfully
```
pyega3 --help
```
4. Create a credential file in .json format in your directory

ega-download-client/pyega3/config/
```
{
    "username": "ega-test-data@ebi.ac.uk",
    "password": "egarocks"
}
```
5. Check the dataset available under your account
```
pyega3 -cf credential.json dataset
```
6. Check the files available in certain dataset
```
pyega3 -cf credential.json files EGAD0000100xxxx
```
7. Download a certain file in to the local directory
```
pyega3 -cf credential.json fetch EGAF0000xxxxxxx
```
