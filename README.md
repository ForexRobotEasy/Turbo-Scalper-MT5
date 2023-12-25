# Turbo Scalper MT5 ReadMe

Turbo Scalper MT5 is an expert advisor designed to trade the EUR/USD currency pair on the MetaTrader 5 platform. It has been developed by the Forex Robot Easy Team and more information about the product can be found on their website [forexroboteasy.com](https://forexroboteasy.com).

## Input Parameters

- TakeProfit: The desired take profit value in pips.
- StopLoss: The desired stop loss value in pips.
- TrailingStop: The desired trailing stop value in pips.
- ActivateNewsFilter: Boolean parameter to activate the news filter.
- NewsFilterTime: The time to close orders before a news event, in minutes.

## Global Variables

- newsTime: Stores the time of the upcoming news event.
- newsFilterActivated: Indicator to check if the news filter is activated.

## Expert Initialization

The expert initialization function fetches the news event time from the MQL5.com calendar and sets it in the `newsTime` variable.

## Expert Deinitialization

The expert deinitialization function is responsible for performing any necessary cleanup actions.

## Expert Tick

The expert tick function is the main function that is executed on every tick of the market. It performs the following actions:

1. Checks if the news filter is activated and if the current time is greater than or equal to the news event time. If so, it calls the `CloseOrders()` function and sets the `newsFilterActivated` variable to true.
2. Checks the indicator signals (`Signal1()`, `Signal2()`, `Signal3()`, `Signal4()`) and opens an order if any of the signals are true.

## Open Order Function

The `OpenOrder()` function is responsible for placing an order based on specific criteria. It also sets the take profit, stop loss, and trailing stop levels for the order.

## Close Orders Function

The `CloseOrders()` function is responsible for closing all open orders.

## Indicator Signal Functions

The indicator signal functions (`Signal1()`, `Signal2()`, `Signal3()`, `Signal4()`) are used to check the market strength and pivot point formations. Each function should return true if the signal is valid and false otherwise.

---

For detailed reviews and trading results of Turbo Scalper MT5, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/turbo-scalper-mt5-review-precision-eurusd-trading-advisor/). Please note that ForexRobotEasy is not the official developer of this product. They only provide a sample code that can work as described in the product. To find the official developer of this product, please use MQL5.
