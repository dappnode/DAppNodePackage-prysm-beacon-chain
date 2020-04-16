# Prysm beacon-chain DAppNode package

[![DAppNode Available](https://img.shields.io/badge/DAppNode-Available-brightgreen.svg)](http://my.dappnode/#/installer/prysm-beacon-chain.public.dappnode.eth)

[![prysm github](https://img.shields.io/badge/prysm-Github-blue.svg)](https://prylabs.net/)
[![prysm participate](https://img.shields.io/badge/prysm-participate-753a88.svg)](https://prylabs.net/participate?node=dappnode)

# Installation Notes

1. Install the DAppNodePackage: 

[![DAppNode Install](https://img.shields.io/badge/DAppNode-Install-blue.svg)](http://my.dappnode/#/installer/prysm-beacon-chain.public.dappnode.eth)

2. After the installation the beacon-chain and the validator should be running on your DAppNode: http://my.dappnode/#/packages

![](https://i.imgur.com/11y8pgQ.png)

3. Go to [Participate](https://prylabs.net/participate?node=dappnode)

* **Follow** Step 1 "Get GöETH — Test ether", as per Prysm's faucet steps.

* **Follow** Step 2 [Download deposit data](http://my.dappnode/#/packages/prysm-validator.public.dappnode.eth/file-manager?from=%2Fdata%2Fdeposit_data.txt) file and open it, you will get something like this:

        ```
        ========================Deposit Data=======================

        0xbc0000006....

        ===========================================================
        ```

    * Copy the value `0xbc0000006...` from the .txt file.

    * Paste it in the field `your validator deposit data` of the Prysm's website:

        ![](https://i.imgur.com/a29SNWI.png)

* **Follow** step 3 "Send a validator deposit" by clicking `Make deposit`.

    ![](https://i.imgur.com/bEM7vlL.png)


* Wait for your validator assignment (it takes a while)

    ![](https://i.imgur.com/DeZqiNV.png)


**Congratulations! Now you should have a network validator node on testnet!**

You can check it by looking at the validator logs: http://my.dappnode/#/Packages/prysm-validator.public.dappnode.eth

![](https://i.imgur.com/Sfq88es.png)

## Note

This is early stage software and it's just a PoC

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
