This article describes how to create users in Omics Data Manager using the python script.
# Requirements
* Python 3
* pip
* Genestack Python client installed and setup with a user account/token. 
  See [how to setup Genestack Python client](../../00_Packages_to_install/1_Genestack_python_client)
* Auxiliary scripts installed.
  See [how to install Genestack auxiliary scripts](../../00_Packages_to_install/2_Genestack_auxiliary_scripts)
* A users.tsv file, for example: [users.tsv](users.tsv)
# Instructions
1. Edit [users.tsv](users.tsv) file in the text editor and replace the example users with your own users - one line per user, detailing email and name, separated by a tab.
2. Run the script below and follow its login instructions, replacing the host name with the address of the instance the script will apply:

    ```$ odm-create-users -H localhost:8080```\
    or use the -u parameter and the user alias created when setting up the Genestack client

    ```$ odm-create-users -u your_alias```
3. The script will create new users and print out their passwords, for example:

    ```
      alice@alphacorp.com    uNgp4F6C    Alice
      bob@alphacorp.com      xI3AOf2h    Bob
    ```
