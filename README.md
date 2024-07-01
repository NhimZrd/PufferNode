## Puffer Finance Project Overview:

**Puffer Finance is a liquid restacking protocol built on top of EigenLayer. Within its framework, users deposit stETH or wstETH and receive pufETH in return. In order to return the original investment along with the profit, the issued asset must be returned.**

The functionality of the liquid token is not limited to this. It can be used in DeFi applications similarly to the assets "frozen" in Puffer Finance.

Nevertheless, the main mission of the protocol is to decentralize the Ethereum network by attracting more solo-stakers, as well as providing AVS operators on EigenLayer. This is precisely what user funds are needed for this purpose, and users are financially rewarded for providing them.

The full-fledged version of Puffer Finance launched on February 1, 2024. It is being developed by Puffer Labs, a company founded by Amir Forouzani and Jason Vranek. The former has a background in NASA and the latter was briefly a member of the Chainlink Labs team.

According to DeFiLlama, at the time of writing, the project's blockchain blockchain funds in smart contracts (TVL) stands at $1.317 billion, second only to ether.fi and Renzo. The protocol also has backing from over twenty investors who have invested over $18 million in its development. 

**Most notable -- Jump Crypto, Animoca Brands and Ethereum Foundation. It is worth noting that on January 30, 2024, Binance Labs joined this list, but the amount of the deal is not disclosed.**

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/ff49f7db-36ff-4574-8937-f4b245adadd8)

- Website : [go](https://www.puffer.fi/)
- Twitter : [go](https://twitter.com/puffer_finance)
- Discord : [go](https://discord.gg/pufferfi)
- GitHub : [go](https://github.com/PufferFinance)

### Server System Requirements(official):

- **CPU : 4 cores;**
- **RAM : 16 GB;**
- **Disk : 2 TB SSD(NVMe recommended) + 14 TB SSD for Ethereum archive;**
- **OS : Ubuntu 20.04**

### Specifications on which the node can also run:

- **CPU : 4 cores;**
- **RAM : 16 GB;**
- **Disk : 1 TB SSD (SATA or NVMe).
- **OS : Ubuntu 20.04**

## Instructions for installing the Puffer node:

**1. Set up a separate Ethereum wallet for the node. You can do it via Metamask.**

**2. Connect to the server and update the packets:**

```bash

sudo apt update && sudo apt upgrade -y

```

**3. Install the necessary software for the node to work:**
```bash

apt update && sudo apt upgrade -y

```

```bash

sudo apt install build-essential curl

```

**4. Run the installation script. Just press Enter and wait for additional packages to be installed:**

```bash

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/b9f6036b-42bf-4571-be80-0d106f2345c9)


**5. Next, execute the command:**

```bash

source $HOME/.cargo/env

```

**6. Then insert this code:**

```bash

echo "export PATH=\"$HOME/.cargo/bin:$PATH\"" >> ~/.bashrc
source ~/.bashrc

```

**7. Check the installation of the required software. The terminal should display the version of the package:**

```bash

rustc --version
```
![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/595a8bfc-46b9-47ec-be66-3cf78011febb)

*Your version may be different from the one in the screenshot. Don't worry, it's normal)*

**8. Once again, let's update the packages. Let's execute the commands:**

```bash

sudo apt update

```

```bash

sudo apt install libssl-dev pkg-config

```

**If you get a pink window, just press Enter.**

**9. Run the following commands one by one:**

```bash

export OPENSSL_DIR=/usr/include/openssl

```

```bash

echo 'export OPENSSL_DIR=/usr/include/openssl' >> ~/.bashrc
source ~/.bashrc

```

```bash

export OPENSSL_LIB_DIR=/usr/lib/x86_64-linux-gnu

```

```bash

export OPENSSL_INCLUDE_DIR=/usr/include/openssl

```

```bash

echo 'export OPENSSL_LIB_DIR=/usr/lib/x86_64-linux-gnu' >> ~/.bashrc
echo 'export OPENSSL_INCLUDE_DIR=/usr/include/openssl' >> ~/.bashrc
source ~/.bashrc

```

**10. Let's check the version of the packages. Execute the following commands one by one:**

```bash

pkg-config --version

```

```bash

pkg-config --libs openssl

```

*In the terminal it will show*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/1929d0ae-fa06-4a99-a4b7-b16e8ff37897)

*If you got this output, everything installed without errors. Your versions may differ from the versions on the screen, it's normal.*
*11. Go to the installation of the Puffer-Coral-Cli client. Create directory:**

```bash

mkdir puffer

```

**12. Go to the folder:**

```bash

cd puffer

```

**13. Download the node software**

```bash

git clone https://github.com/PufferFinance/coral

```

**14. Go to the installed directory:**

```bash

cd coral

```

**15. Execute the command:**

```bash

cargo build --release

```

*After the command is executed, the logs will appear as on the screen. Wait for the inscription "Finished" and only after that go to the next step:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/16b358ea-af49-415a-8fa4-5ac82b223e8e)

**16. If the previous command was executed with errors, execute the following command:**

```bash

cargo clean

```

**17. Proceed to edit the node password file. Make sure you are in /puffer/coral/ and run the command:**

```bash

nano

```

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/b34f9c3f-8f03-4ccc-a9d2-8ad41db9f592)

**18. Create a password to the node. After that save the file with CTRL + X and name the file "password.txt" (without quotes!)**

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/a82ca444-8306-4017-8245-33d2f82d30c6)

**19. Let's check if the file is in the directory:**

```bash

ls

```

*Should be like the picture below*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/68307ca3-a73d-412e-8086-1887eefb4697)

**20. Proceed to create the registration file. Go to [site](https://launchpad.puffer.fi/Setup) of the Puffer lunchpad. Connect the wallet created specifically for the noda. If you have not added Holesky network to your wallet before, Metamask will automatically prompt you to do so.**

**21. We get to the page as on the screenshot below. Disable Enclave if it was enabled. Open Notepad or any other editor on your local computer and copy the command:**

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/d3adac13-77d1-41bc-8cb0-bc29e77b2e1b)

**22. In the command you will have two empty values, which you should replace with your own:**

```

<PATH_TO_A_KEYSTORE_PASSWORD_FILE> <--- "password.txt".
<PATH_TO_REGISTRATION_JSON> <--- "registration.json".

```

**23. After you have edited the command, copy it from notepad and paste it into the server command line and press Enter. If you have specified everything correctly, the installation will go:**

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/f443312f-7891-4d11-817d-ebbaa550e0e8)

*When the installation is finished, you will see the same thing as in the screenshot below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/63998cd4-c8fb-41b4-bb2a-c02800995314)

**24. Let's move on to configuring the consensus client. Let's run the command:**

```bash

cd

```

**25. Execute the following command. During installation, press Enter:**

```bash

sudo apt-get install build-essential git-lfs cmake

```

26.

```bash

openssl rand -hex 32 | tr -d "\n" > "/tmp/jwtsecret".

```

**27. Go to the specified folder:**

```bash

cd /tmp/

```

**28. Edit the file "jwtsecret". In it you need to specify your private key from the wallet:**

```bash

nano jwtsecret

```

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/e1326eed-f389-4761-b3d4-c2952f3bd3a3)

*After inserting the private key, save the file by CTRL + X*.

29.

```bash

cd

```

**30. Let's perform a consensus client installation:**

```bash

git clone https://github.com/status-im/nimbus-eth2

```

**31. Let's go to the folder with the client:**

```bash

cd nimbus-eth2

```

**32. Run the following command. Replace the "X" with the amount of RAM you are willing to allocate to the consensus client. On my system 16 GB RAM, I replaced the "X" with "8":**

```bash

make -jX nimbus_beacon_node

```

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/1a501200-5aa0-499b-8fd6-5e11a9174405)

*The process may take some time. Wait for the moment as in the screenshot below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/43874920-3a46-4bb2-a9b8-53e73aa1f985)

**33. Let's specify that we want to work in the Holesky network. To do this, run the command:**

```bash

build/nimbus_beacon_node trustedNodeSync \.
  --network:holesky \
  --data-dir=build/data/shared_holesky_0 \.
  --trusted-node-url=https://holesky-checkpoint-sync.stakely.io/

```

*The process will start and will also take a while to complete.*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/bacb3750-fc38-4276-bfa8-ef0ea89ecf34)

*Wait for the moment as in the screenshot below.*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/1214a0c5-32b5-4e74-a8ba-ca5583cc3753)

**34. Let's go to the folder with Puffer validator keys:**

```bash

cd ~/puffer/coral/etc/keys/bls_keys

```

**35. Browse the contents of the folder:**

```bash

ls

```

*You should only see one file named with a sequence of numbers and letters.*

**36. Carefully run the following command:**

```bash

cp -v ~/puffer/coral/etc/keys/bls_keys/REPLACE ~/nimbus-eth2/build/data/shared_holesky_0/validators/
```

Replace "REPLACE" with the file name from the past folder. You can copy the file name completely by highlighting it and pressing CTRL + C, then transfer the name to Notepad on your local computer.

EXAMPLE:

My file: 7742nh471h20471h2409127943h021947h012947h0129834b8213g0d2jds0921dhn721908ed721dd021987h21dhd0

My command would look like this:
```bash
cp -v ~/puffer/coral/etc/keys/bls_keys/7742nh471h20471h2409127943h021947h012947h0129834b8213g0d2jds0921dhn721908ed721dd021987h21dhd0 ~/nimbus-eth2/build/data/shared_holesky_0/validators/

```

**37. Copy the file again to another directory:**

```bash

cp -v ~/puffer/coral/etc/keys/bls_keys/7742nh471h20471h2409127943h021947h012947h0129834b8213g0d2jds0921dhn721908ed721dd021987h21dhd0 ~/nimbus-eth2/build/data/shared_holesky_0/validators/
```
*NOTE: Replace "7742nh471h20471h2409127943h021947h012947h0129834b8213g0d2jds0921dhn721908ed721dd021987h21dhd0" with your own file name!*
**38. Let's go to the directory:**

```bash

cd ~/nimbus-eth2/

```

**39. Execute the command. During execution, the server will ask you to enter the password you created earlier:**

```bash

build/nimbus_beacon_node deposits import --data-dir=build/data/shared_holesky_0

```

**40. Carefully execute the following command:**

```bash

./run-holesky-beacon-node.sh --web3-url=http://127.0.0.1:8551 --suggested-fee-recipient=WALLET_ADDRESS --jwt-secret=/tmp/jwtsecret
```
!WALLET_ADDRESS replace with your wallet address!

EXAMPLE:

My wallet address is: 0xB0551d678a6746F2Cf300CF698d314EA1e74e3c7

My command would look like this:
```
./run-holesky-beacon-node.sh --web3-url=http://127.0.0.1:8551 --suggested-fee-recipient=0xB0551d678a6746F2Cf300CF698d314EA1e74e3c7 --jwt-secret=/tmp/jwtsecret

```

*If you have done everything correctly, you will see the process as in the screenshot below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/0572deef-55ed-4e65-8fa9-aee078d5564c)

*Wait for the logs as in the screenshot below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/94c69f65-f104-449f-be0d-f3e2c2fa30b6)

*Synchronization will start, you can check on the white lines there is a parameter that says "sync: - h - m (0.00%)" which shows the synchronization progress of your node. Once it is fully synchronized, it should say "synced/opt".*

**41. Let's move on to configuring the Execution client. Execute the commands one by one:**

```bash

wget https://packages.microsoft.com/config/ubuntu/$(lsb_release -rs)/packages-microsoft-prod.deb -O packages-microsoft-prod.deb

```

```bash

sudo dpkg -i packages-microsoft-prod.deb

```

```bash

sudo apt-get update

```

```bash

sudo apt-get install dotnet-sdk-8.0 dotnet-runtime-8.0

```

*The installation process will proceed as shown in the screenshot below.

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/c6a20a13-445f-484e-96bb-a42c832dd6ea)

**42. Let's check the installation:**

```bash

dotnet --list-sdks

```

```bash

dotnet --list-runtimes

```

```Bash 
dotnet --list-runtimes
```

*Should appear as in the screen below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/0ff2122f-7d9d-43ad-bfc6-67ea3c9bc1da)

**43. Execute the command:**

```bash

git clone https://github.com/NethermindEth/nethermind.git

```

**Wait for the installation to complete **

44.

```bash

cd nethermind/src/Nethermind/

```

**45. Run the following command:**

```bash

dotnet build Nethermind.sln -c Release

```

*File creation will begin:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/074918e8-671d-4452-940c-e4976c5db1b7)

*Wait for the moment as on the screen below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/6ed5bf72-b52b-4cba-9458-f20007548471)

**46. It is necessary to get Ethereum Holesky test tokens. To do this, go to [faucet](https://www.holeskyfaucet.io/), brand 2 to 3 tokens.**

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/48642295-2cd1-4762-9237-8698fb8e5b06)

**47. After branding Holesky ETH, execute the following commands:**

```bash

sudo apt update

```

```bash

sudo apt install screen

```

**48. Verify that the screen utility is installed correctly with the command:**

```bash

screen --version
```

**49. Create a screen session with the command:**

```bash

screen -S consensus

```

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/486c9140-2d51-4c48-a04a-9d58a1aac39f)

**50. Let's go to the folder:**

```bash

cd ~/nimbus-eth2. 

```

**51. Execute the command:**

```bash

./run-holesky-beacon-node.sh --web3-url=http://127.0.0.1:8551 --suggested-fee-recipient=WALLET --jwt-secret=/tmp/jwtsecret
```
Replace "WALLET" with your wallet address

EXAMPLE:
```
./run-holesky-beacon-node.sh --web3-url=http://127.0.0.1:8551 --suggested-fee-recipient=0xB0551d678a6746F2Cf300CF698d314EA1e74e3c7 --jwt-secret=/tmp/jwtsecret

```
*Logs like the one on the screenshot below will go like this:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/3a6509d2-77de-4ca4-8274-9557ddb075bf)

*Full synchronization will take from 2 to 4 hours.*

**52. Open a new window in SSH client and reconnect to the server. Once connected, run the command:**

```bash

screen -S execution

```

**53. Go to the folder:**

```bash

cd ~/nethermind/src/Nethermind/Nethermind.Runner

```

**54. Execute the command:**

```bash

dotnet run -c Release -- --config=holesky --datadir="../../../../nethermind-datadir" --JsonRpc.Host=0.0.0.0.0 --JsonRpc.JwtSecretFile=/tmp/jwtsecret

```

*Client consensus synchronization will begin:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/cbe7e267-5e0a-4574-8bca-9312b60d70ab)

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/2adbb2d3-6bbf-429a-a06d-249193796f80)

*Wait for synchronization to finish. It's not a quick process.*

**55. Complete the Puffer Dashboard registration. Go to [link](https://launchpad.puffer.fi/Setup)**

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/9e2ae8a7-ba79-497b-820b-29d63be3101f)

**Click "Continue." You will be taken to the page as shown in the screenshot below:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/2dd28d05-9722-440f-9def-f4b3a1740194)

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/8251be4b-3ecd-4239-bc38-408dcba0bb2b)

*In my case, I have set the value to 3. You can specify another value, the main thing is that it should be more than 2 ETH:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/c3f9e2be-37c6-4c6a-a3d4-62c8fed68dd9)

*And then minitimize tickets. 1 ticket = 1 day of node work:*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/70c04ebf-206d-4d0f-8e14-3f7e0f05a0c3)

*Addresses of pufETH and Puffer Validator Tickets contracts on the Ethereum Holesky network. Add them to Metamask:*
```

Holesky pufETH Contract: 0x98408eadD0C7cC9AebbFB2AD2787c7473Db7A1fa

Holesky Puffer Validator Ticket Contract: 0xA143c6bFAff0B25B485454a9a8DB94dC469F8c3b

```

*Press "Continue"*

![image](https://github.com/Mozgiii9/PufferSetupTheNode/assets/74683169/74f8da2a-a203-49bf-8bc9-d9adbb1ee837)

**56. Final step. It is necessary to load the file "registartion.json" into the browser window. You can do it using FileZilla.**

**Open the FileZilla application on your local computer and connect to the server.**

*Then go to the directory "/root/puffer/coral". Transfer the "registration.json" file to your PC. Just highlight it and move it to the left side of the window to any convenient folder on your computer*

*After transferring the file to your PC, load it into your browser window and click "Finish". You will need to sign any necessary transactions in the Metamask window that opens up*

**The node synchronization will start. It may take a long time up to several days. You can monitor your validator in this [explorer](https://holesky.beaconcha.in/validator/)**.
