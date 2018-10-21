=== Ether and ERC20 tokens WooCommerce Payment Gateway ===
Contributors: ethereumicoio
Tags: woocommerce, ethereum, erc20, erc223, token, e-commerce, payment, crypto, blockchain
Requires at least: 4.7
Tested up to: 4.9.5
Stable tag: 2.3.3
Donate link: https://etherscan.io/address/0x476Bb28Bc6D0e9De04dB5E19912C392F9a76535d
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html
Requires PHP: 7.0

Ether and ERC20 tokens WooCommerce Payment Gateway enables customers to pay with Ether
or any ERC20 or ERC223 tokens on your WooCommerce store.

== Description ==

Ether and ERC20 tokens WooCommerce Payment Gateway is the only one true decentralized ether and ERC20/ERC223 token payment plugin. It enables customers to pay with Ether or any ERC20 or ERC223 token on your WooCommerce store. Your customers will be offered the option of paying with Ether or some ERC20/ERC223 token at checkout. If they choose that option then they will be quoted a price in Ether or ERC20/ERC223 token for their order automatically.

After submitting their order they will be given the details of the Ether or ERC20/ERC223 token transaction they should make.

Features:

* Accept payment in Ether or any ERC20 or ERC223 token of your choice
* Mobile ready with QR codes
* Free to use. Fixed fee per purchase
* User friendly payment wizard
* Automatically convert order value to Ether or ERC20/ERC223 token at checkout
* Option for adding a percentage mark-up to the converted price of Ether and/or ERC20 tokens to help cover currency fluctuations.
* "Pay with Metamask" button to allow easy payment via MetaMask client. If customer do not want to use MetaMask, she can just copy and paste Value, Address, and Data fields in her favorite wallet software.
* The `Disallow customer to pay with Ether` option is useful to accept only some token
* Automatic transaction tracking / reconciliation and order updates
* The only one true decentralized ether and ERC20/ERC223 token payment plugin. There are no service other that Ethereum blockchain is used in this plugin. You do not need to trust us or any other party. This plugin uses a public smart contract in the Ethereum blockchain to record and confirm orders
* The Payment Gateway smart contract: [0x3E0371bcb61283c036A48274AbDe0Ab3DA107a50](https://etherscan.io/address/0x3E0371bcb61283c036A48274AbDe0Ab3DA107a50#code)

> Combined with the [Cryptocurrency Product for WooCommerce](https://wordpress.org/plugins/cryptocurrency-product-for-woocommerce/) plugin it can allow you to sell ERC20/ERC223 tokens for Ether or Ether for ERC20/ERC223 tokens.

= Ether payment =

The payment with Ether is a simple one step process. Customer have to send one transactions to the Ethereum blockchain.

= ERC20/ERC223 token payment =

The ERC20/ERC223 token payment consists of two steps: 

* Deposit funds to the payment gateway smart contract in the Ethereum blockchain, and 
* Use this deposit to pay for your order

Customer have to send two transactions to the Ethereum blockchain: 

* first for deposit and 
* second for the real payment

 > There are no need to refund the deposit to cancel the first step, since it is actually a `Token.approve` call that doesn't transfer any tokens.

== Screenshots ==

1. The payment method choice
2. The Ether payment page
3. The Ether payment page advanced toggled
4. The Ether payment page advanced and QR-code toggled
5. The Ether payment page in mobile phone
6. The Ether payment page in mobile phone advanced toggled
7. The ERC20 payment page
8. The ERC20 payment page advanced toggled
9. The ERC20 payment page advanced toggled continues and second step
10. The ERC20 payment page in mobile phone
11. The ERC20 payment page in mobile phone advanced toggled
12. The basic plugin settings
13. The infura API credentials and blockchain network settings
14. The plugin payment details settings

== Installation ==

* Install and activate it as you would any other plugin
* Head over to WooCommerce » Settings » Checkout » Ether and ERC20 tokens WooCommerce Payment Gateway
* Enter your Ethereum address to receive payments and confirm markup %
* Register for an infura.io API key and put it in admin settings. It is required to interact with Ethereum blockchain. After register you'll get a mail with links like that: https://mainnet.infura.io/1234567890. The 1234567890 part is the API Key required.
* Tune other options if you need to

== Troubleshooting ==

= WooCommerce session broken =

If you are getting this message: `ETH price quote has been updated, please check and confirm before proceeding` it means that your server installation settings broke the WooCommerse session somehow. Install the [WordPress Native PHP Sessions](https://wordpress.org/plugins/wp-native-php-sessions/) in this case.

= COPY buttons L&F =

It is very likely that COPY buttons would look not perfect in your theme. Most problems with them can be solved by adding your custom styles to this CSS class:

`
.epg-payment-instructions button.button.epg-copy-button {
    padding: 0.618em 1em;
}
.epg-payment-instructions button {
    background-color: #ffd600;
    color: #ffffff;
}
.epg-payment-instructions button:hover {
    background-color: #aad600;
    color: #dddddd;
}
`

Tune the padding, color and background values to met your theme expectations.

Add this code to your `Additional CSS` section in the theme customizing.


== Testing ==

You can test this plugin in some test network for free.

= Testing in ropsten =

* Set the `Blockchain` setting to `ropsten`
* Buy some `0x6Fe928d427b0E339DB6FF1c7a852dc31b651bD3a` TSX token by sending some Ropsten Ether amount to it's Crowdsale contract: `0x773F803b0393DFb7dc77e3f7a012B79CCd8A8aB9`
* You can "buy" some Ropsten Ether for free using MetaMask
* Set the Supported ERC20 tokens list setting to the `TSX:0x6Fe928d427b0E339DB6FF1c7a852dc31b651bD3a:0.001`
* Create a cheap test product in your store
* Buy this product with Ropsten Ether and/or this TSX token
* Check that proper amount of Ropsten Ether and/or TSX token has been sent to your payment address

= Testing in rinkeby =

* Set the `Blockchain` setting to `rinkeby`
* Buy some `0x194c35B62fF011507D6aCB55B95Ad010193d303E` TSX token by sending some Rinkeby Ether amount to it's Crowdsale contract: `0x669519e1e150dfdfcf0d747d530f2abde2ab3f0e`
* You can "buy" some Rinkeby Ether for free here: [rinkeby.io](https://www.rinkeby.io/#faucet)
* Set the `Supported ERC20 tokens list` setting to the `TSX:0x194c35B62fF011507D6aCB55B95Ad010193d303E:0.001`
* Create a cheap test product in your store
* Buy this product with Rinkeby Ether and/or this TSX token
* Check that proper amount of Rinkeby Ether and/or TSX token has been sent to your payment address

== Fees ==

The fee is published in a blockchain and is limited by a maxFee property in smart contract.
This guaranties your safety as a plugin customer. The feePercent and maxFee values a saved as % * 10^6:

* The maxFee is 3% which is saved as 3000000 and can not be changed. 
* The feePercent is 1,5% which is saved as 1500000 and can be changed in a 0% to 3% range.

> We reserve the right to change the fee in the 0% to 3% range to reflect the market changes.

== Changelog ==

= 2.3.4 =

* Add stable price feature, fixed your ERC20 tokens' rate to 1:1 USD. So you can receive USDT, TUSD. 


= 2.3.3 =

* Fix QR-codes for black backgrounds
* Show/hide Amount field for Ether payment if advanced fields are hidden/shown
* Show the Amount field as a simple text to distinguish it from the Value field to enhance user's experience

= 2.3.2 =

* Cancel process order task if order is cancelled or removed
* `epg-payment-received.php does not exist` error fix

= 2.3.1 =

* Order would be confirmed even if user closed the payment page before transaction was confirmed
* Copy buttons fix if clicked on icon

= 2.3.0 =

* `Mark ERC20 token price up by %` option is added. To help cover currency fluctuations the plugin can automatically mark up converted rates for you. These are applied as percentage markup, so a 1 ERC20 Token value with a 1.00% markup will be presented to the customer as 1.01 Token.
* email content fix
