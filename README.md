# CryptoTill
Accept cryptocurrencies just like cash.
Try the [live demo](http://khybertandoori.com/cryptotill/CryptoTill.html); donations welcome using it. :)

![AcceptCryptos](https://github.com/EMRahman/CryptoTill/blob/master/Images/AcceptCryptos.jpeg)

Introduction
============
Simple webpage for accepting Bitcoin and Altcoin payments (Dash, Ethereum & Litecoin). Used live at
[khybertandoori.com](https://khybertandoori.com).

Before Taking Payment
===========================================================
Update file named publicAddresses.js before taking payments. i.e. set the addresses to the public addresses that you own and know the private key to. In this basic version; we are reusing the same public keys provided for all transactions (as opposed to a new public key for each transaction). This should give customers confidence others are using cryptocurrency as payment.

General Usage (Brief)
=========================
1. Enter the amount to charge a customer.
2. Select the coin amount of the preferred cryptocurrency.
3. Ask the customer to scan the QR code using a wallet, such as (e.g. [jaxx.io](http://jaxx.io)).
4. Ask the customer to confirm details: coin type, amount, address & send the required amount.
5. Once the customer has sent the amount; check the blockchain for unconfirmed amount.

General Usage (Detail)
=========================
After entering an amount to charge a customer; the various cryptocurrency amounts are determined using a live FX rate (via [CoinMarketCap.com](http://CoinMarketCap.com)). The FX rate and [estimated transaction fee](https://bitinfocharts.com/comparison/transactionfees-btc-eth-ltc-dash.html#1y) is displayed. Fee's are based on [jaxx.io](http://jaxx.io)'s static rates.

You must then select the desired amount of the crypto the customer wishes to pay in. A QR code will be displayed containing the crypto type, address and amount.

Once the customer has scanned the QR code using their wallet app (e.g. [jaxx.io](http://jaxx.io)), we can check for payments using the "Check Blockchain For Payment" button, this is provided by [blockcypher.com](http://blockcypher.com) and by default they have a 200 requests per hour limit at the time of writing. 

The payment should appear within 1 second in the "Unconfirmed" list. Depending on the [confirmation time](https://bitinfocharts.com/comparison/confirmationtime-btc-eth-ltc-dash.html#1y) (Bitcoin 10 min, Ethereum 15 seconds, Dash/Litecoin 2-2.5 minutes at the time of writing); the payment will later appear in the "Confirmed" list once it has entered a block.

If a customer is sending money to an already known address; the buttons "View Payments" can be used to see such recent payments. No more of a customer having to divulge long credit/debit card numbers and 3 digit pins over the phone begrudgingly!

To convert the crypto to a fiat currency bank account, one option is to transfer the amount via a reputable exchange such as [coinbase](https://support.coinbase.com/customer/portal/articles/1963534-payment-methods-for-uk-customers).
