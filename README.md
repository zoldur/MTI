# MTI-Coin
Shell script to install a [MTI Coin Masternode](http://mticoin.io/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
Login to your Linux VPS and run (copy & paste) the following 2 lines:
```
wget -q https://raw.githubusercontent.com/zoldur/MTI/master/MTI_install.sh  
bash MTI_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the MTI Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **15000** MTI to **MN1**. You need to send all 15000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**
11. Login to your VPS and check your masternode status by running the following command. If you get **Status 9**, it means your masternode is active.
```
MTId masternode status
```
***

## Usage:
```
MTId masternode status  
MTId getinfo
```
Also, if you want to check/start/stop **MTI**, run one of the following commands as **root**:

```
systemctl status MTI #To check if MTI service is running  
systemctl start MTI #To start MTI service  
systemctl stop MTI #To stop MTI service  
systemctl is-enabled MTI #To check if MTI service is enabled on boot  
```  
***

## Donations

Any donation is highly appreciated  

**MTI**: MLoVKL9KnXwoF37YDdxFYfHbjCQRSeVMem  
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E  
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB  
