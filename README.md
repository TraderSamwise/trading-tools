# trading-tools
Tools I use to help me trade

## FTX ShortKeys Shortcuts

Please see https://github.com/TraderSamwise/tealstreet for details on installing ShortKeys / importing these settings. Note the FTX is also built on React and therefore uses a virtual router, so the shortcuts won't work unless you refresh the page after navigating to a market such that "*ftx.com/trade/*" matches your url. Also, the default shortcuts conflict with typing when attempting to search for markets, so if you have to type you may need to navigate to the FTX landing page and refresh to temporarily stop the shortcuts, search for the market you want, and then refresh again.

```
[{
		"key": "z",
		"action": "javascript",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"activeInInputs": true,
		"blacklist": "whitelist",
		"code": "document.getElementsByClassName(\"MuiTable-root\")[0].children[1].children[0].children[1].click();",
		"label": "set price to top price visible on the bid side"
	},
	{
		"key": "c",
		"action": "javascript",
		"code": "document.getElementsByClassName(\"MuiTable-root\")[1].children[1].children[0].children[0].click();",
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"activeInInputs": true,
		"label": "set price to top price visible on the ask side"
	},
	{
		"key": "a",
		"action": "javascript",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"code": "var input = document.getElementsByClassName(\"MuiInputBase-input\")[0]\ninput.stepDown();\nvar ev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "decrease price by one tick"
	},
	{
		"key": "d",
		"action": "javascript",
		"code": "var input = document.getElementsByClassName(\"MuiInputBase-input\")[0]\ninput.stepUp();\nvar ev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "increase price by one tick"
	},
	{
		"key": "alt+z",
		"action": "javascript",
		"code": "document.getElementsByClassName(\"MuiTable-root\")[1].children[1].children[0].children[0].click();\nvar input = document.getElementsByClassName(\"MuiInputBase-input\")[0]\ninput.stepDown();\nvar ev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "set price to one tick above the top visible level on the bid side"
	},
	{
		"key": "alt+c",
		"action": "javascript",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"code": "document.getElementsByClassName(\"MuiTable-root\")[0].children[1].children[0].children[1].click();\nvar input = document.getElementsByClassName(\"MuiInputBase-input\")[0]\ninput.stepUp();\nvar ev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "set price to one tick above the top visible level on the ask side"
	},
	{
		"key": "2",
		"action": "javascript",
		"code": "var input = document.getElementsByClassName(\"MuiInputBase-input\")[3]\ninput.step = 2000;\ninput.stepUp();\nev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "increase notional order size by 2k"
	},
	{
		"key": "`",
		"action": "javascript",
		"blacklist": "whitelist",
		"code": "var input = document.getElementsByClassName(\"MuiInputBase-input\")[3]\nif (input.value != \"\" && input.value != \"0\") {\ninput.step = parseFloat(input.value);\ninput.stepDown();\nev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);\n}\n",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "reset order size to 0"
	},
	{
		"key": "4",
		"action": "javascript",
		"code": "var input = document.getElementsByClassName(\"MuiInputBase-input\")[3]\ninput.step = 4000;\ninput.stepUp();\nev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "increase notional order size by 4k"
	},
	{
		"key": "5",
		"action": "javascript",
		"code": "var input = document.getElementsByClassName(\"MuiInputBase-input\")[3]\ninput.step = 5000;\ninput.stepUp();\nev = new Event('input', { bubbles: true});\ninput.dispatchEvent(ev);",
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "increase notional order size by 5k"
	},
	{
		"key": "q",
		"action": "javascript",
		"blacklist": "whitelist",
		"activeInInputs": true,
		"code": "document.getElementsByClassName(\"MuiSwitch-input\")[1].click()",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "toggle post (only on futures)"
	},
	{
		"key": "w",
		"action": "javascript",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"code": "document.getElementsByClassName(\"MuiSwitch-input\")[0].click()",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "toggle reduce (only on futures)"
	},
	{
		"key": "x",
		"action": "javascript",
		"code": "posMenu = false;\ntry {\ntableText = document.getElementsByClassName(\"MuiTableHead-root\")[3].children[0].children[0].innerText\nif (tableText == \"Market\" || tableText == \"Coin\") {\nposMenu = true;\n}\n} catch {}\ndocument.getElementsByClassName(\"MuiTab-wrapper\")[6].click();\ntry {\ndocument.getElementsByClassName(\"MuiTableBody-root\")[3].children[0].children[6].children[0].click()\n} catch {}\nposMenu && document.getElementsByClassName('MuiTab-wrapper')[5].click();\n\n\n",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "cancel resting order at top of orders list"
	},
	{
		"key": "alt+shift+a",
		"action": "javascript",
		"code": "document.getElementsByClassName(\"MuiTab-wrapper\")[1].click()\ndocument.getElementsByClassName(\"MuiButton-containedPrimary\")[0].click();",
		"blacklist": "whitelist",
		"sites": "*ftx.com/trade/*",
		"activeInInputs": true,
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "place buy order with values in order form"
	},
	{
		"key": "alt+shift+d",
		"action": "javascript",
		"activeInInputs": true,
		"blacklist": "whitelist",
		"code": "document.getElementsByClassName(\"MuiTab-wrapper\")[2].click()\ndocument.getElementsByClassName(\"MuiButton-containedPrimary\")[0].click();",
		"sites": "*ftx.com/trade/*",
		"sitesArray": [
			"*ftx.com/trade/*"
		],
		"label": "place sell order with values in order form"
	}
]
```

### FTX PNL Hider

Upon requet I wrote a superscript to hide position PNL on FTx. 

You must install TamperMonkey chrome extension: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en. 

The script to install can be found here: https://openuserjs.org/scripts/TraderSamwise/FTX_pnl_hider.

You will have to refresh the '.../trade/' page on FTX or make it the first page that loads for the script to activate, as FTX uses React and the virtual router and page URLs are only registered on first visiting the site.
