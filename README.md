<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NIXEL Token | BSC</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
<body class="bg-gray-900 text-white font-sans">

  <!-- Hero Section -->
  <section class="text-center py-20 px-5">
    <h1 class="text-4xl md:text-6xl font-bold text-blue-400">NIXEL Token</h1>
    <p class="mt-4 text-lg md:text-xl text-gray-300 max-w-xl mx-auto">
      The next big utility token on Binance Smart Chain with dynamic stage-based sales and zero taxes.
    </p>
    <a href="#how-to-buy" class="mt-8 inline-block bg-blue-500 hover:bg-blue-600 text-white font-bold py-3 px-6 rounded-full transition">Buy Now with Web3 Wallet</a>
  </section>

  <!-- Tokenomics -->
  <section class="bg-gray-800 py-16 px-6">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-6 text-blue-300">Tokenomics</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="bg-gray-700 p-6 rounded-xl">
          <h3 class="text-xl font-semibold mb-2">Total Supply</h3>
          <p>5 Billion NIX Tokens</p>
        </div>
        <div class="bg-gray-700 p-6 rounded-xl">
          <h3 class="text-xl font-semibold mb-2">Tax</h3>
          <p>No buy or sell taxes</p>
        </div>
        <div class="bg-gray-700 p-6 rounded-xl">
          <h3 class="text-xl font-semibold mb-2">Sale Stages</h3>
          <p>
            - Stage 1: 2B @ $0.000095<br>
            - Stage 2: 1.5B @ $0.0005<br>
            - Stage 3: 0.5B @ $0.00085
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- How to Buy -->
  <section id="how-to-buy" class="py-16 px-6">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-8 text-blue-300">How to Buy</h2>
      <p class="text-lg mb-6">You can buy NIXEL tokens directly from the smart contract using any Web3 wallet such as MetaMask or Trust Wallet. Payment is accepted in <strong>BNB only</strong>.</p>
      <ol class="list-decimal text-left text-lg space-y-4">
        <li>Open your Web3 wallet (MetaMask, Trust Wallet...)</li>
        <li>Connect to Binance Smart Chain (BSC)</li>
        <li>Go to the contract page on BscScan</li>
        <li>Click "Write Contract" → Connect Wallet</li>
        <li>Use the buy function and send the BNB amount</li>
      </ol>
    </div>
  </section>

  <!-- Roadmap -->
  <section class="py-16 px-6">
    <div class="max-w-4xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-8 text-blue-300">Roadmap</h2>
      <ol class="list-decimal text-left text-lg space-y-4">
        <li>Launch the official website</li>
        <li>Deploy and verify the smart contract</li>
        <li>Start dynamic token sales through contract</li>
        <li>Community building on Telegram, Twitter</li>
        <li>Auto-listing on PancakeSwap</li>
        <li>Apply for CoinMarketCap and CoinGecko listings</li>
        <li>Launch NFT Marketplace and staking</li>
        <li>Introduce NIXEL Wallet App</li>
        <li>List on Tier-2 exchanges</li>
        <li>Expand to multi-chain support</li>
      </ol>
    </div>
  </section>

  <!-- Live Stats Section -->
  <section class="bg-gray-800 py-16 px-6">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl font-bold mb-8 text-blue-300">Live Stats</h2>
      <div id="stats" class="text-lg space-y-4">
        <p id="stage">Loading current stage...</p>
        <p id="price">Loading current price...</p>
        <p id="sold">Loading total sold tokens...</p>
        <p id="left">Loading remaining tokens in this stage...</p>
      </div>
    </div>
  </section>

  <!-- Contact & Footer -->
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
    // تحديث بيانات المراحل حسب التوكنات المباعة يدويًا
    const stage1Cap = 2000000000;
    const stage2Cap = 1500000000;
    const stage3Cap = 500000000;
    const totalSold = 650000000; // <-- القيمة الحالية من البوت

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
  </script>

</body>
</html>
