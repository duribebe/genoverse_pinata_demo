# GenoVerse_pinata_demo
How to unlock Biosample derived data using Pinata (IPFS) Submarine Function 


The following repository contains helper scripts to allow you to submarine folders and files corresponding to DNA Datasets.

Submarining is the process of obtaining and publishing an IPFS folder without publishing the files contained within the folder. This is useful for, for example, an NFT project using the GenoBank.io's Biosample permission Token  ERC721 contract: https://github.com/Genobank/biosample-permission-token

ifps://<folder CID>/<BioNFT ID>

and the contract deployer only wants to reveal the underlying images over time, rather than all at once.

Some IPFS gateway companies offer this as a paid service, but the following project allows anyone to do this for free.

Overview
The scripts set up two instances of the IPFS, one which is kept private, and one which is a public gateway out to the rest of the IPFS. The image folder is added and pinned in the private IPFS swarm, and then commands are avaialbe for copying parts but not all of the files underlying a folder to the public gateway.

GATEWAY: https://genoverse.mypinata.cloud

To use
Run the IPFS setup script: ./install.sh

This will set up a private IPFS instance which is not running as a background process, but can still be used by the other scripts to submarine and reveal files. It also starts a public IPFS server, the control panel of which is found at http://127.0.0.1/5001.

To submarine a particular DNA dataset, run: ./submarine_DNA.sh <DNA dataset folder>

To reveal a particular DNA dataset from the folder, run: ./reveal_BioNFT.sh <DNA dataset folder>/<DNA_file>

