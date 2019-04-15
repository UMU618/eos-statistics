# EOS Statistics Tools

## 0. [Optional] Preparation

You may need to install/update nodejs.

**Ubuntu** reference: <https://github.com/nodesource/distributions/blob/master/README.md>

```
curl -sL https://deb.nodesource.com/setup_11.x | sudo -E bash -
sudo apt-get install -y nodejs
```

You may need to install/update yarn.

**Ubuntu** reference: <https://yarnpkg.com/en/docs/install#debian-stable>

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt-get update && sudo apt-get install --no-install-recommends yarn
```

## 1. Install required nodejs modules

```
yarn install
```

## 2. Run statistics scripts

### Export all accounts of mainnet

```
node 1-export-accounts.js -m
```

### Get accounts info

```
node 2-get-accounts-info.js -m mainnet-1-all-accounts.txt
```

### Calculate total staked EOS for NET and CPU

```
node 3-calc-total-staked-eos.js mainnet-2-info.txt
```
