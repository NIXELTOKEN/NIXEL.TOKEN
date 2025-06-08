<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NIXEL Token | BSC</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link rel="icon" href="favicon.ico" type="image/x-icon">
  <script src="https://cdn.jsdelivr.net/npm/web3@1.8.2/dist/web3.min.js"></script>
</head>
<body class="bg-gray-900 text-white font-sans">

  <!-- Hero Section -->
  <section class="text-center py-20 px-5">
    <h1 class="text-4xl md:text-6xl font-bold text-blue-400">NIXEL Token</h1>
    <p class="mt-4 text-lg md:text-xl text-gray-300 max-w-xl mx-auto">
      The next big utility token on Binance Smart Chain with dynamic stage-based sales and zero taxes.
    </p>
    <div class="mt-8">
      <button id="connectWallet" class="bg-green-500 hover:bg-green-600 text-white font-bold py-3 px-6 rounded-full transition">Connect Wallet</button>
      <button id="buyButton" class="ml-4 bg-blue-500 hover:bg-blue-600 text-white font-bold py-3 px-6 rounded-full transition">Buy Now</button>
    </div>
  </section>

  <!-- باقي الأقسام بدون تغيير -->

  <!-- Live Stats Section -->
  <section class="bg-gray-800 py-16 px-6">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-8 text-blue-300">Live Stats</h2>
      <div id="stats" class="text-lg space-y-4">
        <p id="stage">Loading current stage...</p>
        <p id="price">Loading current price...</p>
        <p id="sold">Loading total sold tokens...</p>
        <p id="left">Loading remaining tokens in this stage...</p>
        <p id="bnb">Loading total BNB received...</p>
        <p id="usd">Loading USD value of BNB received...</p>
      </div>
    </div>
  </section>

  <footer class="bg-gray-800 py-10 text-center">
    <p class="mb-4">Smart Contract Address:</p>
    <code class="bg-gray-700 p-2 rounded">0x9EB6c8C1877BF58BCd8680E057C3780B14749625</code>
    <div class="mt-6 space-x-4">
      <a href="https://t.me/nixelcommunity" target="_blank" class="text-blue-400 hover:underline">Telegram</a>
      <a href="https://bscscan.com/address/0x9EB6c8C1877BF58BCd8680E057C3780B14749625" target="_blank" class="text-blue-400 hover:underline">View on BscScan</a>
    </div>
    <p class="mt-6 text-sm text-gray-400">© 2025 NIXEL Token. All rights reserved.</p>
  </footer>

  <script>
    let web3;
    let userAccount;

    async function connectWallet() {
      if (window.ethereum) {
        web3 = new Web3(window.ethereum);
        try {
          const accounts = await ethereum.request({ method: 'eth_requestAccounts' });
          userAccount = accounts[0];
          document.getElementById('connectWallet').textContent = 'Connected';
          console.log("Wallet connected:", userAccount);
        } catch (error) {
          alert('Wallet connection denied');
        }
      } else {
        alert('Please install MetaMask');
      }
    }

    document.getElementById('connectWallet').addEventListener('click', connectWallet);

    async function buyToken() {
      if (!web3 || !userAccount) {
        alert('Please connect your wallet first.');
        return;
      }
      const contractAddress = '0x9EB6c8C1877BF58BCd8680E057C3780B14749625';
      const amountInBNB = '0.01';

      try {
        const tx = await web3.eth.sendTransaction({
          from: userAccount,
          to: contractAddress,
          value: web3.utils.toWei(amountInBNB, 'ether')
        });
        console.log("Transaction sent:", tx);
        alert("Purchase successful!");
      } catch (error) {
        console.error(error);
        alert("Transaction failed.");
      }
    }

    document.getElementById('buyButton').addEventListener('click', buyToken);

    const stage1Cap = 2000000000;
    const stage2Cap = 1500000000;
    const stage3Cap = 500000000;
    const totalSold = 650000000;
    const bnbReceived = 61750;
    const bnbPriceUSD = 650; // تم التعديل هنا حسب طلبك

    let stage, price, remaining;

    if (totalSold < stage1Cap) {
      stage = 'Stage 1';
      price = '$0.000095';
      remaining = stage1Cap - totalSold;
    } else if (totalSold < stage1Cap + stage2Cap) {
      stage = 'Stage 2';
      price = '$0.0005';
      remaining = stage1Cap + stage2Cap - totalSold;
    } else {
      stage = 'Stage 3';
      price = '$0.00085';
      remaining = stage1Cap + stage2Cap + stage3Cap - totalSold;
    }

    document.getElementById('stage').textContent = `Current Stage: ${stage}`;
    document.getElementById('price').textContent = `Current Price: ${price}`;
    document.getElementById('sold').textContent = `Total Sold Tokens: ${totalSold.toLocaleString()} NIX`;
    document.getElementById('left').textContent = `Remaining in This Stage: ${remaining.toLocaleString()} NIX`;
    document.getElementById('bnb').textContent = `Total BNB Received: ${bnbReceived.toLocaleString()} BNB`;
    document.getElementById('usd').textContent = `USD Equivalent: ~$${(bnbReceived * bnbPriceUSD).toLocaleString()}`;
  </script>
</body>
</html>
