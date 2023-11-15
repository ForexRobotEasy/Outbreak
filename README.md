# Outbreak

This code is for a Forex trading robot called Outbreak developed by the Forex Robot Easy Team. The developer's website is forexroboteasy.com. This robot implements a breakout strategy to identify trade opportunities in the Forex market.

## Installation

To use this code, you need to include the necessary libraries. In this case, the Trade library is required.

## Constants

The code defines the following constants:
- `INITIAL_PRICE`: The initial purchase price for the trade.
- `PRICE_INCREASE`: The amount by which the purchase price increases for each profit increase.
- `PROFIT_INCREASE`: The minimum required profit increase to trigger a price increase.

## Trade Class

An instance of the `CTrade` class is created to handle trading operations.

## IsOrderOpen Function

This function checks if there is an open order. It uses the `PositionGet` function from the `CTrade` class to retrieve information about the current position.

## CalculatePurchasePrice Function

This function calculates the new purchase price based on the current price and the profit. It calculates the number of price increases required based on the profit increase constant and adds the corresponding amount to the current price.

## OpenTrade Function

This function opens a trade if there is no open order. It first checks if there is already an open order by calling the `IsOrderOpen` function. If there is an open order, the function returns without taking any further action. If there is no open order, the function implements the breakout strategy to identify trade opportunities and opens a new trade using the `PositionOpen` function from the `CTrade` class. The trade is opened with a stop loss set 10 pips below the entry price.

## CloseTrade Function

This function closes the trade if there is an open order. It first checks if there is an open order by calling the `IsOrderOpen` function. If there is no open order, the function returns without taking any further action. If there is an open order, the function closes the trade using the `PositionClose` function from the `CTrade` class.

## HandlePricingStructure Function

This function handles the pricing structure based on the profit. It takes the current price and profit as input parameters. It calculates the new purchase price using the `CalculatePurchasePrice` function. If the new price is greater than the current price, it updates the current price. The function then outputs the current purchase price.

## OnTick Function

This is the entry point of the program. It is called on every tick of the market. The function implements the breakout strategy to identify trade opportunities. It first opens a trade if the conditions are met by calling the `OpenTrade` function. It then closes the trade if necessary by calling the `CloseTrade` function. Finally, it calculates the profit and handles the pricing structure by calling the `HandlePricingStructure` function.

---

## Product Description

Outbreak is a Forex trading robot developed by the Forex Robot Easy Team. It is a profitable breakout trading robot that uses a sophisticated strategy to identify trade opportunities in the Forex market.

With Outbreak, you can take advantage of market breakouts and make profitable trades. The robot is designed to open trades when certain breakout conditions are met, and it implements a stop loss for risk management.

The pricing structure of Outbreak is dynamic and adjusts based on the profit. As the profit increases, the purchase price increases, allowing you to maximize your profits and minimize your risks.

To use Outbreak, simply install the code and run it on your MetaTrader platform. The robot will automatically analyze the market and open trades when favorable breakout opportunities arise. It will also monitor the trades and close them if necessary.

For detailed reviews and trading results of this product, visit our website at [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/review-outbreak-forex-software-profitable-breakout-trading-robot/).
