# Customer Segmentation and Targeted Marketing Strategy ML Project

## Project Overview:
This project performs an end-to-end unsupervised machine learning analysis on grocery store customer data. The goal was to identify distinct customer segments to allow the business to transition from a "one-size-fits-all" marketing approach to a targeted, high-ROI strategy.

Using Python, I cleaned raw data, engineered new features, reduced dimensionality using PCA, found the optimal number of clusters using the Elbow method, and applied Agglomerative Clustering to uncover 4 distinct customer profiles.

## Business Recommendations:
### Cluster 1 (The "Deal Hunter" families)
Who are they: 
* Deal lovers: The NumDealsPurchases graph shows this group has the highest usage of discounts (some buying 13+ deals)
* Parents of teens: The Teenhome graph has a massive density peak at 1.0, indicating these families have older children
* Moderate to high spenders: They spend significantly more than the budget groups, likely due to the food volume needed for teenagers
  
Marketing Strategy: 
* Gamified loyalty: Since they love deals, use a points-based system where they "unlock" coupons
* Bulk promotions: Teenagers consume high volumes of food. Push "Family Size" products, "Buy 2 Get 1 Free" offers, and bulk snacks/beverages
* Channel: They are active shoppers. Push notifications or app-based coupons will have a high conversion rate here

### Cluster 2 (The "Low Engagement" customers)
Who are they: 
* Lowest spenders: The Spent density plots show this group is clustered tightly at the bottom (spending nearly 0-500)
* Mixed demographics: They appear across various education levels and ages, but consistently have low interaction
* Low deal usage: Despite having low income/spend, they interestingly do not engage heavily with deals (NumDealsPurchases is low)

Marketing Strategy:
* Don't over-invest: Do not spend high ad dollars here. The ROI will be low
* Activation campaigns: Send "We miss you" emails with a strong single-use incentive (e.g., "$10 off your next purchase of $50") to try to migrate them into Cluster 1 or 4
* Analyze churn: Survey this group to find out why they don't spend. Are they buying only loss-leaders? Do they prefer a competitor?

### Cluster 3 (The "VIPs")
Who are they: 
* Top spenders: This is the most valuable customer segment as they are top spenders (up to 2500+)
* Child-free: This group is child-free as the Kidhome, Teenhome, and Is_Parent graphs show strictly 0 children
* Not deal sensitive: The NumDealsPurchases boxplot shows they rarely use coupons (Median near 0-1)
  
Marketing Strategy: 
* Do not discount: Since they don't use deals, offering discounts is throwing away margin
* Premium upsell: Promote high-margin categories like imported wines and organic produce
* Campaigns: Focus on "Quality," "Origin," and "Taste" rather than price. Send exclusive invitations to wine tasting events or early access to new products

### Cluster 4 (The "Young Families")
Who are they:
* Parents of small kids: The Kidhome graph shows a massive peak at 1.0, while Teenhome is lower
* Moderate spenders: They spend less than Cluster 0 and 2
* Deal sensitive: They use deals (median around 2-3), but less aggressively than the parents of teens (Cluster 1)
* Younger demographic: The Age vs Spent graph suggests a slight skew toward the 30-45 age range

Makreting Strategy:
* Bundle essentials: Create "Mom & Dad Saver Packs" bundling diapers, baby food, and quick-meal solutions (frozen foods, pasta)
* Smart suggestions: Use their purchase history to predict when they run out of recurring items (milk, cereal) and send reminders.
* Tone: Marketing should emphasize "Time-saving" and "Healthy options for kids" rather than just pure bulk
  
