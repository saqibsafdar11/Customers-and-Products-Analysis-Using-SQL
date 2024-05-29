# Customers and Products Analysis Using SQL
 
Customers: customer data
Employees: all employee information
Offices: sales office information
Orders: customers' sales orders
OrderDetails: sales order line for each sales order
Payments: customers' payment records
Products: a list of scale model cars
ProductLines: a list of product line categories 

![EDR](path/to/EDR.png)


## Questions
1. Which product should we order more of or less of?

- Identify products with low stock levels (should order more of these):
- Identify products with high performance (should order more of these)

High performaning and frequently sold products, with low stock should be prioritised for restocking

| productCode | productName             | prod_perf  |
|-------------|-------------------------|------------|
| S12_1099    | 1968 Ford Mustang       | 161531.48  |
| S18_2795    | 1928 Mercedes-Benz SSK  | 132275.98  |
| S32_1374    | 1997 BMW F650 ST        | 89364.89   |
| S700_3167   | F/A 18 Hornet 1/72      | 76618.40   |
| S50_4713    | 2002 Yamaha YZR M1      | 73670.64   |
| S700_1938   | The Mayflower           | 69531.61   |
| S24_2000    | 1960 BSA Gold Star DBD34| 67193.49   |
| S32_4289    | 1928 Ford Phaeton Deluxe| 60493.33   |
| S72_3212    | Pont Yacht              | 47550.40   |
| S18_2248    | 1911 Ford Town Car      | 45306.77   |

Question 2: How should we match marketing and communication strategies to customer behaviors?



### Marketing and Communication Strategies for Customer Segments

#### 1. VIP Customers
These are customers who have made the most purchases and generated the highest profit.

| Last Name  | First Name | City         | Country   | Profit     |
|------------|------------|--------------|-----------|------------|
| Freyre     | Diego      | Madrid       | Spain     | 326,519.66 |
| Nelson     | Susan      | San Rafael   | USA       | 236,769.39 |
| Young      | Jeff       | NYC          | USA       | 72,370.09  |
| Ferguson   | Peter      | Melbourne    | Australia | 70,311.07  |
| Labrune    | Janine     | Nantes       | France    | 60,875.30  |

**Strategies:**
- **Exclusive Offers**: Provide VIP customers with exclusive discounts, early access to sales, and special promotions.
- **Personalized Communication**: Send personalized emails and messages that recognize their loyalty and highlight products based on their purchase history.
- **Loyalty Programs**: Develop a VIP loyalty program offering points for every purchase, which can be redeemed for future discounts or gifts.
- **Private Events**: Invite them to exclusive events, such as product launches, private sales, or special meet-and-greet sessions.
- **Premium Support**: Offer dedicated customer service lines or personal account managers to handle their inquiries and issues promptly.
- **Recognition**: Feature VIP customers in newsletters or on social media (with their consent) to acknowledge their importance to your brand.

#### 2. Least Engaged Customers
These customers have the lowest engagement and have generated the least profit.

| Last Name  | First Name | City       | Country | Profit  |
|------------|------------|------------|---------|---------|
| Young      | Mary       | Glendale   | USA     | 2,610.87|
| Taylor     | Leslie     | Brickhaven | USA     | 6,586.02|
| Ricotti    | Franco     | Milan      | Italy   | 9,532.93|
| Schmitt    | Carine     | Nantes     | France  | 10,063.80|
| Smith      | Thomas     | London     | UK      | 10,868.04|

**Strategies:**
- **Re-engagement Campaigns**: Send targeted email campaigns with special offers or discounts to encourage them to make another purchase.
- **Surveys and Feedback**: Reach out with surveys to understand why they are less engaged and what improvements they would like to see.
- **Content Marketing**: Share engaging content that might interest them, such as how-to guides, product stories, and customer testimonials.
- **Personalized Recommendations**: Use purchase history data to recommend products that match their preferences and past purchases.
- **Incentives for Activity**: Offer incentives such as discounts on their next purchase or free shipping if they make a purchase within a certain time frame.
- **Reminder Emails**: Send reminder emails about items left in their cart or notify them about new arrivals and upcoming sales.

### Implementation Plan
1. **Data Analysis**: Continuously analyze customer data to identify trends, preferences, and engagement levels.
2. **Customer Segmentation**: Regularly update customer segments to reflect changes in buying behavior and engagement.
3. **Personalization Tools**: Utilize CRM and marketing automation tools to deliver personalized content and offers.
4. **Feedback Loop**: Implement mechanisms to collect and act on customer feedback to improve products and services.
5. **Monitor and Adjust**: Track the performance of marketing campaigns and adjust strategies based on what works best for each segment.

By tailoring marketing and communication strategies to match the behaviors and preferences of different customer segments, businesses can improve customer satisfaction, loyalty, and ultimately, profitability.

Question 3: How much can we spend on acquiring new customers?

ltv = total lifetime value
 = 39039.594388

LTV tells us how much profit an average customer generates during their lifetime with our store. We can use it to predict our future profit. So, if we get ten new customers next month, we'll earn 390,395 dollars, and we can decide based on this prediction how much we can spend on acquiring new customers.

### Determining Customer Acquisition Cost (CAC) Based on Lifetime Value (LTV)

Given the Lifetime Value (LTV) of a customer is $39,039.59, we can calculate how much can be spent on acquiring new customers by considering several factors, including desired profitability, marketing budget, and company growth goals.

#### Key Considerations:

1. **Customer Acquisition Cost (CAC)**: The cost incurred to acquire a new customer. This includes marketing expenses, sales expenses, and any other costs associated with attracting and converting leads into customers.
2. **Desired Profit Margin**: The percentage of LTV that a company wants to retain as profit after deducting CAC.
3. **Marketing Budget**: The total budget allocated for marketing and customer acquisition activities.

#### Steps to Determine CAC:

1. **Set a Desired Profit Margin**: Decide on the percentage of LTV you want to keep as profit. For instance, if we want to retain 50% of LTV as profit, then the maximum allowable CAC would be 50% of LTV.
2. **Calculate Maximum Allowable CAC**:
   - Maximum CAC = LTV * (1 - Desired Profit Margin)
3. **Evaluate Marketing Budget**: Ensure the calculated CAC fits within the overall marketing budget.

#### Example Calculation:

1. **Desired Profit Margin**: Let's assume we want to retain 40% of LTV as profit.
2. **Maximum Allowable CAC**:
   - LTV = $39,039.59
   - Desired Profit Margin = 40% (so, we want to retain 60% of LTV)
   - Maximum CAC = LTV * (1 - 0.40)
   - Maximum CAC = $39,039.59 * 0.60
   - Maximum CAC = $23,423.75

Thus, based on this example, we can spend up to $23,423.75 on acquiring each new customer to maintain a desired profit margin of 40%.

### Using LTV for Future Predictions

If you acquire 10 new customers in the next month, the predicted future profit can be calculated as follows:

- **Predicted Future Profit for 10 New Customers**:
  - Number of New Customers = 10
  - Total LTV for 10 Customers = 10 * LTV
  - Total LTV for 10 Customers = 10 * $39,039.59
  - Total LTV for 10 Customers = $390,395.90

Based on the above calculation, acquiring 10 new customers would generate an estimated $390,395.90 in future profit.

### Summary

- **Maximum Allowable CAC**: $23,423.75 per new customer (assuming a desired profit margin of 40%).
- **Predicted Future Profit**: $390,395.90 for acquiring 10 new customers.

### Strategic Recommendations

1. **Set Clear CAC Targets**: Based on the desired profit margins, set clear targets for maximum CAC.
2. **Optimize Marketing Spend**: Allocate the marketing budget efficiently to ensure the CAC remains within the target range.
3. **Monitor and Adjust**: Continuously monitor the actual CAC and adjust marketing strategies as needed to ensure profitability.
4. **Invest in High-ROI Channels**: Focus on marketing channels and strategies that provide the highest return on investment (ROI) and the lowest CAC.

 