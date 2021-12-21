# <b>INTERNAL TRANSFER OF BALANACES</b>
---
Cheers Friends, 

This guide will teach you how to transfer your funds from our "substrate" side to our Ethereum-Virtual-Machine (EVM).
Remember, the EVM side of our chain allows you to interact with many eth-based smart contracts and projects that eventually will move to Kusari.
Moreover, our cross-chain bridges will be attached to our EVM module, so for you to utilize cross-chain trades you must use the EVM.

That said, let me tell you how we tackle this.
First, I will walk you through the process so that you can get started right away.
Second, I will elablorate a bit more on the concept so that the interested lads can read up.

## <b> PART 1 - WALKTHROUGH </b>
!!! Hint
    You can access the TRANSFER function here: LINK
    You can watch me walking you through the process in this video: LINK

The tansfer is done in four (4) steps:

- Setup 
- Origin and Destination Address
- Amount
- Confirmation

### <b> STEP 01 - Setup </b>

!!! Hint
    Make sure you selected the "Transfers" function of your DApp (see picture below)

![img](assets/Internal-transfer-step-01.png#center)


!!! Hint 
    You can change the transfer direction with the center button.
    Confirm the direction by clicking on next

![img](assets/Internal-transfer-step-011.png#center)

!!! Hint 
    Click on "Connect SwapDex Account" to connect your substrate wallet to the DApp. 
    This substrate address need to hold the funds you wish to transfer.
    If you are using the polkadot.js browser extension to manage your addresses then the DApp will offer you a dropdown menu.

![img](assets/Internal-transfer-step-012.png#center)

!!! Hint
    Click next once you selected your address.
    If you have trouble seeing the dropdown please reaload the page or close your browser and restart the process.

### <b> STEP 02 - Origin and Destination Address </b>

In this step you can choose to either connect to your MetaMask wallet to automatically fetch the correct address or you can paste any eth-based address.

![img](assets/Internal-transfer-step-02.png#center)

!!! Hint
    Once you selected a target address you can confirm by clicking on next.
    You need to confirm the selected accounts and click on "Ok"

![img](assets/Internal-transfer-step-021.png#center)

### <b> STEP 03 - Amount </b>

In this step you need to select the amonut you want to transfer and confirm by clicking on the "Transfer Amount" button.

![img](assets/Internal-transfer-step-03.png#center)

!!! Hint
    Open the substrate or evm explorer to be prepared to check that the tranfer went through successfully
    substrate explorer [Link](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fws.kusari.network#/explorer)
    EVM explorer [Link](https://evm.kusari.network/)


### <b> STEP 04 - Confirmation </b>

Confirm the transfer by hitting the "Sign and Send" button.

![img](assets/Internal-transfer-step-04.png#center)

!!! Hint
    Sign with your substrate account.

![img](assets/Internal-transfer-step-041.png#center)

!!! Hint 
    If everything went fine you will see a success message at the button of the page

![img](assets/Internal-transfer-step-042.png#center)

!!! Hint 
    Now head over to the substrate explorer to check if the transfer was successfully written into a block

![img](assets/Internal-transfer-step-043.png#center)


!!! Success
    Congrats, you successfully swapped KSI from the substrate to the EVM side.
    Feel free to reverse the swap and use the tranfer function to your needs. 


## <b> PART 2 - WHAT HAPPENS IN THE BACKGROUND </b>
---

Many may ask themselves, is Kuari one single chain or how does is work to have and ethereum and substrate side at teh same time?
Well, to make a long story short... Kusari is one single chain BUT it runs a ethereum simulation in parallel.

How does this works?

To answer this question we need to take a look at the node architecture. Nodes are pillars of our distributed network and they run all the neccessary code. 

![img](assets/node-architecture.png#center)

I'd like to direct your focus to the SUBSTRATE RUNTIME module of the Substrate Node. 
The Runtime hosts all the code that makes Kusari unique and it's composed of code pallets. 
As you can see the democracy function of our chain is also a code pallet and allows our community to govern the chain. Likewise, the staking pallet allows our community to run validators and stake as nominators. Similar to those pallets, the EVM is another pallet that allows our community to interact with eth-based smart contracts and the cross-chain bridges.

What we are doing by performing the transfer described in step 01 is that we are transfering coins from the SUBSTRATE RUNTIME ENVIRONMENT into the EVM pallet and visa versa that's it :D.
As briefly touched on earlier, the EVM side opens up many new opportunities to you to utilize your KSI coins.

![img](assets/node-architecture-01.png#center)


<br></br>

<p align=right> Written by Masterdubs & Petar </p>

