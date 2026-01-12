# How to set up Genlayer studio to write intelligent smart contracts and become your own validator

<img width="1537" height="893" alt="chrome_Jk7SBwDBZA" src="https://github.com/user-attachments/assets/8c7c07c8-2dcd-488a-8626-c60aaab4ef9d" />

This guide will show you how to set up Genlayer Studio, write intelligent smart contracts, and become your own validator.
# First, understand what Genlayer is 
Genlayer is the first Intelligent Blockchain that enables smart contracts to natively access the Internet and go beyond deterministic logic, to make subjective decisions.
It is also the first AI-native blockchain built for AI-powered smart contracts, called Intelligent Contracts, capable of reasoning and adapting to real-world data. Its foundation is the Optimistic Democracy consensus mechanism, an enhanced Delegated Proof of Stake (dPoS) model that allows validators to connect directly to Large Language Models (LLMs). 
This setup allows for non-deterministic operations such as processing text prompts, fetching live web data, and executing AI-based decision-making while preserving the reliability and security of a traditional blockchain.
# Secondly, what are Intelligent Smart Contracts
They are smart contracts in GenLayer that gain reasoning abilities, allowing them to understand natural language, process real-world data, and adapt to evolving conditions.
To integrate AI seamlessly with the blockchain, GenLayer employs a distributed neural consensus network, wherein validators run specialised software connected via API to advanced AI models. 
This approach unifies:
- Delegated Proof of Stake (dPoS) for efficient block production and governance.
- Neural Consensus for non-deterministic transactions requiring advanced AI reasoning.
# Key Features of Genlayer
- AI-powered
- Web Data Access
- Secure and Reliable
- Interoperability
- Python-Based SDK
# Use Cases of Genlayer
- Prediction Markets
- Performance-Based Contracting
- Network States
- Dispute Resolution
- AI-Driven DAOs
# Setting up your own Genlayer Studio
We will be setting up our own Genlayer studio for deploying contracts, writing contracts and also with our own validators
# NT: This guide is strictly for Windows users
# Requirements
Docker Desktop
Node.js
WSL
Python
# 1 First lets install window sub system for Linux 
Open Terminal as administrator and enter the code 
```
wsl --install
```
<img width="1122" height="1065" alt="image" src="https://github.com/user-attachments/assets/92205cc6-1b1c-4302-bc38-10d45fdae307" />
<img width="2074" height="1174" alt="image" src="https://github.com/user-attachments/assets/6049428f-aaed-4db6-add5-a8d63b6d1a4b" />

It will require you to restart your pc, ensure to do so, some systems do not restart. Just move to the next step
- Enter a username and password ( ensure you do not forget the password)
- Done, WSL has been installed successfully
# To always go back to WSL, always enter the code, and you will return to WSL
```
wsl
```
# 2. Install Docker
Visit [DOCKER](https://docs.docker.com/desktop/setup/install/windows-install)

-Download the version for your required system

<img width="1537" height="893" alt="chrome_btigiWHBYb" src="https://github.com/user-attachments/assets/d125442c-8176-449e-96bf-9cf54563a2c0" />

# Lets setup Docker
- Install the Docker Desktop
- Select the wsl integration
- Launch Docker
- Head to Docker Settings
- Select Resource
- Select WSL INTEGRATION
- Enable both that you see there

<img width="1742" height="1054" alt="Docker_Desktop_RG2OzfxPpg" src="https://github.com/user-attachments/assets/74937b81-9376-4932-9c44-948481dec9d5" />

# Lets test to see if Docker is running
- Head to WSL/Ubuntu/Terminal
- Enter the code
  ```
  docker --version
  ```
  <img width="1389" height="563" alt="WindowsTerminal_PgLfA2GU2w" src="https://github.com/user-attachments/assets/c847e7ae-3501-488d-83fc-3e17feca52cb" />
  You should see a version come up. If you do not, try to install Docker again and try again
# 3. Let's install Node.js
Install nvm
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```
in lieu of restarting the shell
```
\. "$HOME/.nvm/nvm.sh"
```
Download and install Node.js
```
nvm install 24
```
Verify the Node.js version
```
node -v
```
Should print "v24.12.0".

<img width="1249" height="505" alt="WindowsTerminal_EvxojbzRN5" src="https://github.com/user-attachments/assets/bcb3ad82-450a-44b7-bbfa-b497a48412eb" />

# 4. Lets install Python

```
sudo apt install python3
```

Check Python version
```
python3 --version
```

You should see a 3.12.3

<img width="1596" height="401" alt="WindowsTerminal_lOBEmdornN" src="https://github.com/user-attachments/assets/f8758e6a-f3f3-4ff1-a492-d7160854e220" />

Add Pip to Python
```
sudo apt install python3-pip
```
Done
# Now we have all our 3 requirements ready

<img width="1242" height="741" alt="WindowsTerminal_YhbnbxFYfl" src="https://github.com/user-attachments/assets/1a719a0e-d4f6-4f5b-951f-80ba8de4df0b" />

# 5. Let's install the Genlayer CLI
- Open Docker Desktop in background
- Install Genlayer CLI
```
npm install -g genlayer
```
 <img width="1405" height="736" alt="WindowsTerminal_MSuJ46sY4X" src="https://github.com/user-attachments/assets/29a86cc2-acd0-41bc-be32-00908921617e" />

  What we are doing here is basically enabling the CLI to work as a blockchain simulator for us in our terminal
  It may take some time to load, but it should come up
# 6. Create a workspace for your project
```
mkdir my-project
```
```
cd my-project
```

<img width="1449" height="718" alt="WindowsTerminal_Krs7FL0APr" src="https://github.com/user-attachments/assets/31192e1b-9afd-4ca9-ac99-16c4242e0bca" />

mkdir helps in creating a folder; it stands for markdown directory, while cd helps to go back to that file directory
# You can name it anything you choose 
# 7. Initialise Genlayer Studio 
```
genlayer init
```

<img width="1744" height="663" alt="WindowsTerminal_JzJ0huhpfi" src="https://github.com/user-attachments/assets/444d8746-89db-46f5-9c14-baa64d0f8da0" />

We want to initialise 5 validators, and we will need API keys for this 
# To get our API keys
- Select HEURIST
- Select with Spacebar Key
- Enter API keys

<img width="1751" height="594" alt="WindowsTerminal_XXR45fDsJJ" src="https://github.com/user-attachments/assets/7d2256ba-aac3-4c0b-a289-b7f541ec08d6" />

# Let us get our API keys
- Head to [HEURIST](https://dev-api-form.heurist.ai)
- Click on Let's begin
- Select Project Types
- Describe your use case
- Enter your email address
- Enter your project URL ( you can enter the GitHub website here )
- Connect social media handles
- Enter Referral Code: ENTER genlayer
- Enter your wallet address
- All Done
- Next, head to [HEURIST CREDITS](https://www.heurist.ai/credits)
- Connect Wallet
- Click on Add New Api Key
- Copy the Api Key you have added

<img width="1113" height="1066" alt="chrome_FtzRjx9Zz7" src="https://github.com/user-attachments/assets/aeaf7069-cf61-48b8-b211-57085027ba76" />

<img width="1113" height="1066" alt="chrome_ZEdur8zVq5" src="https://github.com/user-attachments/assets/a05c088e-18b4-4aad-9fdb-ddb9447661bc" />

<img width="1113" height="1066" alt="chrome_OzjXEd8y6y" src="https://github.com/user-attachments/assets/ca75f370-e201-4b13-8583-621218ec2098" />

<img width="1113" height="1066" alt="chrome_dApHagZfYY" src="https://github.com/user-attachments/assets/be9ae613-22eb-43bd-8c44-117536370a37" />

<img width="1113" height="1066" alt="chrome_jfY3XxByHK" src="https://github.com/user-attachments/assets/7d6be85d-808f-47b4-b38f-a4b2dce4255f" />

<img width="1113" height="1066" alt="chrome_fZTEZ1uvZb" src="https://github.com/user-attachments/assets/6f22a2e2-db16-44e2-b630-66aac9d078a3" />

<img width="1113" height="1066" alt="chrome_tYfTV34Zzs" src="https://github.com/user-attachments/assets/d8c77aeb-d30b-4eec-884b-8b72c9c9e3c6" />

<img width="1113" height="1066" alt="chrome_2SXDsfm4O1" src="https://github.com/user-attachments/assets/b138342e-2f11-47c9-b938-23f0cce7ab0d" />

<img width="1113" height="1066" alt="chrome_yU75ENLpbJ" src="https://github.com/user-attachments/assets/32825fd4-d5e1-49be-b639-0db4c37631a3" />

<img width="2074" height="1066" alt="image" src="https://github.com/user-attachments/assets/fa294f3d-65ac-4db0-ae1d-301eacfa6b35" />

<img width="2074" height="1066" alt="image" src="https://github.com/user-attachments/assets/26912cef-5f84-4114-bf18-e0f217358d24" />

- Next Paste the copied API key in your terminal and press ENTER

<img width="1738" height="682" alt="qYfCbB3PXG" src="https://github.com/user-attachments/assets/8dee2d6f-2ff0-4dca-8aba-2e0e84a6c636" />

# 8. Start up the Node
```
genlayer up
```
You should see a localhost open directly in your browser, and click on it 
# http://localhost:8080

<img width="1765" height="295" alt="image" src="https://github.com/user-attachments/assets/b7120c72-bb74-4318-9e5e-177f1d8ee060" />

You will be welcome to the Genlayer Studio
# 9. The Genlayer Studio
- Open Localhost
- Watch the tutorial on how to navigate the studio

<img width="1537" height="893" alt="chrome_zq41DKb9wx" src="https://github.com/user-attachments/assets/a2686f58-27c9-41a8-bd5f-f4a718291cae" />

- Click on your validators to check

<img width="1537" height="893" alt="chrome_LUmjDH5pHp" src="https://github.com/user-attachments/assets/9e337820-520d-402c-ba25-72d105e1bb9b" />

# 10. Writing your first smart contract
- Select contracts
- Connect wallet
- Connect Metamask wallet
- Switch to the Genlayer Test Network
- Click on _hello_world.py
- You will have a bunch of codes already
- Click on Run and Debug
- Click on Deploy _hello_world.py
- Confirm and Approve in wallet
- Done, your contract will be deployed successfully

<img width="1537" height="893" alt="chrome_BgaAP7AR0E" src="https://github.com/user-attachments/assets/ba1864eb-3426-4def-99af-d4b995c70ec8" />

<img width="1537" height="893" alt="chrome_QNe4dL0F9U" src="https://github.com/user-attachments/assets/d5a51bbb-e011-41f8-ac70-8e5cb09eee5a" />

<img width="1537" height="893" alt="chrome_lDQu5wSM7V" src="https://github.com/user-attachments/assets/0e21c283-d17a-470c-8b52-bda44b6989d5" />

<img width="1537" height="893" alt="chrome_s9Od32Ju0D" src="https://github.com/user-attachments/assets/aa37e177-d386-4def-a455-a98ae2fc5eaa" />

# 11. [Get Started with Genlayer Incentived Builder Point Program](https://x.com/MystiqueMide/status/2006223513930080342)
- Follow all the steps below above the link to get started

# We have successfully learnt how to create and run our own genlayer CLI using our own terminal

# TROUBLESHOOT 
### ⚠️ 1. Error: stderr maxBuffer length exceeded
This occurs during `genlayer init` when the terminal output is too large for the Node.js buffer.

**The Manual Workaround:**
If the automatic initialisation fails, run the Docker commands manually:
1. `cd` into your GenLayer node_modules directory.
2. Run `docker compose build`.
3. Run `docker compose -p genlayer --profile frontend up -d`
### 2. Error: connection reset by peer
This happens if your internet connection drops while Docker is pulling the GenLayer images. 

**Solution:**
1. Check your internet connection.
2. Run
    ```
   docker system prune -f
   ```
   to clear partial downloads.
5. Re-run
```
genlayer init.
```
Docker will resume from where it left off.
### 3. Resolving the "Unmatched" Error
I noticed an error: `(eval):1: unmatched '`. 
 **The Cause:** This happens if you accidentally paste a command that has a single quote `'` that isn't closed.
 **The Fix:** If you see this, press **`Ctrl + C`** to cancel the line and try typing the command again.
### 4. Linux/WSL Troubleshooting

#### a). Permission Denied (docker.sock)
If you get a "permission denied" error when running `genlayer init`, add your user to the docker group:
```bash
sudo usermod -aG docker $USER
newgrp docker
```
### b) "genlayer init" Fails

<img width="2025" height="1013" alt="WindowsTerminal_z3umh1XaVn" src="https://github.com/user-attachments/assets/f9cc265c-f0e3-43eb-9170-caf46d252af5" />

1. Restart Docker Desktop
2. Run `genlayer init` again

### 5. Network/Download Errors
1. Add DNS to Docker Desktop: Settings → Docker Engine
```json
   "dns": ["8.8.8.8", "8.8.4.4"]
```
2. Check Windows Firewall for Docker Desktop

<img width="854" height="465" alt="explorer_elwL7Zy61e" src="https://github.com/user-attachments/assets/64ac0598-7d9c-46dc-acd7-0528de8dcb14" />


### 6. Out of Space
```bash
docker system prune -a --volumes
```
### 7. Ensure Docker Images pulled successfully

<img width="1567" height="1085" alt="vySM1zY4D2" src="https://github.com/user-attachments/assets/3895a9b0-286d-4699-8bfd-7be8b3dda8e1" />

### Made with 🫶🏻❤️ by [MYSTIQUEMIDE](https://x.com/MystiqueMide)
