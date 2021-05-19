# trading-tools
Tools I use to help me trade

## FTX ShortKeys Shortcuts

Use the chrome extension ShortKeys found here: https://chrome.google.com/webstore/detail/shortkeys-custom-keyboard/logpjaacgmcbpdkdchjiaagddngobkck. Then copy the the contents of the file `ftx_shortkeys`. Open the chrome extension ShortKeys (it should open to the settings page). First, delete the first row which includes a dummy starter shortcut (this messes with importing shortcuts for some reason). Then go to "import" and paste the settings copied from the `ftx_shortkeys` file. Scroll down to the bottom and click "save". Then refresh FTX.com.

Note the FTX is also built on React and therefore uses a virtual router, so the shortcuts won't work unless you refresh the page after navigating to a market such that "*ftx.com/trade/*" matches your url. Also, the default shortcuts conflict with typing when attempting to search for markets, so if you have to type you may need to navigate to the FTX landing page and refresh to temporarily stop the shortcuts, search for the market you want, and then refresh again.


### FTX Custom Theme

You must install TamperMonkey chrome extension: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en. 

The script to install can be found here: https://openuserjs.org/scripts/TraderSamwise/FTX_Custom_Theme

All settings, colors, etc are stored in vars at the top of the file. You can easily customize them by changing their values.



### FTX PNL Hider

Upon requet I wrote a superscript to hide position PNL on FTX. 

You must install TamperMonkey chrome extension: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en. 

The script to install can be found here: https://openuserjs.org/scripts/TraderSamwise/FTX_pnl_hider.

You will have to refresh the '.../trade/' page on FTX or make it the first page that loads for the script to activate, as FTX uses React and the virtual router and page URLs are only registered on first visiting the site.
