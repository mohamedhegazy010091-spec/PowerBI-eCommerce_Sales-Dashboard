| Measure Name             | DAX Formula |
|--------------------------|-------------|
| Profit color             | `IF([YOY Profit] > 0, "Green", "Red")` |
| Profit Icon              | `VAR positive_icon = UNICHAR(9650) VAR negative_icon = UNICHAR(9660) VAR result = IF([YOY Profit] > 0, positive_icon, negative_icon) RETURN result` |
| Profit margin            | `SUM(ecommerce_data[profit_per_order]) / SUM(ecommerce_data[sales_per_order])` |
| Profit margin color      | `IF([YOY Profit margin] > 0, "Green", "Red")` |
| Profit margin Icon       | `VAR positive_icon = UNICHAR(9650) VAR negative_icon = UNICHAR(9660) VAR result = IF([YOY Profit margin] > 0, positive_icon, negative_icon) RETURN result` |
| PYTD Profit              | `CALCULATE(SUM(ecommerce_data[profit_per_order]), DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))` |
| PYTD Profit margin       | `CALCULATE([Profit margin], DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))` |
| PYTD Quantity            | `CALCULATE(SUM(ecommerce_data[order_quantity]), DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))` |
| PYTD Sales               | `CALCULATE(SUM(ecommerce_data[sales_per_order]), DATESYTD(SAMEPERIODLASTYEAR('Calendar'[Date])))` |
| Quantity color           | `IF([YOY Quantity] > 0, "Green", "Red")` |
| Quantity Icon            | `VAR positive_icon = UNICHAR(9650) VAR negative_icon = UNICHAR(9660) VAR result = IF([YOY Quantity] > 0, positive_icon, negative_icon) RETURN result` |
| Sales color              | `IF([YOY Sales] > 0, "Green", "Red")` |
| Sales icon color         | `IF([YOY Sales] > 0, "Green", "Red")` |
| Trend                    | `VAR positive_icon = UNICHAR(9650) VAR negative_icon = UNICHAR(9660) VAR result = IF([YOY Sales] > 0, positive_icon, negative_icon) RETURN result` |
| Selected month           | `SELECTEDVALUE('Calendar'[Month])` |
| Selected year            | `SELECTEDVALUE('Calendar'[Year])` |
| YTD Profit               | `TOTALYTD(SUM(ecommerce_data[profit_per_order]), 'Calendar'[Date])` |
| YTD Profit margin        | `TOTALYTD([Profit margin], 'Calendar'[Date])` |
| YTD Quantity             | `TOTALYTD(SUM(ecommerce_data[order_quantity]), 'Calendar'[Date])` |
| YTD Sales                | `TOTALYTD(SUM(ecommerce_data[sales_per_order]), 'Calendar'[Date])` |
| YOY Profit               | `([YTD Profit] - [PYTD Profit]) / [PYTD Profit]` |
| YOY Profit margin        | `([YTD Profit margin] - [PYTD Profit margin]) / [PYTD Profit margin]` |
| YOY Quantity             | `([YTD Quantity] - [PYTD Quantity]) / [PYTD Quantity]` |
| YOY Sales                | `([YTD Sales] - [PYTD Sales]) / [PYTD Sales]` |
| YTD Concatenate Qty      | `CONCATENATE("#", FORMAT([YTD Quantity] / 1000, "0.0 K"))` |

