# Data-projects-TripleTen-

***Shopify Analysis***

Reviewed the landscape of apps on the Shopify platform, using data scraped from publicly available Shopify websites. 

The Data:

The shopify.xlsx dataset contains public data scraped from the Shopify App Store. It includes 4 tables:

apps: Details of the apps on Shopify apps marketplace
apps_categories: Join tables to connect apps with categories
categories: Categories of the apps. Each app has multiple categories
reviews: Each review (row) contains information on user opinion about the related app (rating and comment). Also, it contains the response from the developer if present.

App Landscape:

- KPI Card (a visual with a single number) that counts the unique number of apps.
- Line Chart getting the sum of the review count on the Y-axis, and the lastmod date on the X-Axis.
- Scatterplot with the reviews_count on the X axis and the average rating on the Y axis.

Reviews:

- Created a new Column in the Reviews table named helpful_reviews using a DAX expression, which multiplies the rating by 1+helpful_count to       weigh the reviews by how helpful they’ve been found.
- KPI Card with the average value of the new helpful_reviews column.
- Created a new Column in the Reviews table named developer_answered using a DAX expression, which is 1 (or TRUE) if the developer_reply column is not blank and 0 (or FALSE) if the column row is blank. 
- Scatterplot comparing the average rating on the Y-Axis by the value of the developer_answered column on the X-Axis.

App Reviews

- Created a new relationship between the Reviews table and the Apps table. Use the app_id column from the Reviews table, the id column from the Apps table.  Made the relationship many-to-one built as many (Reviews table) to one (Apps table). Using this new table, made a bar chart with the developer on the X-Axis, and the sum of rating on the Y-Axis.
- Made a new bar chart with developer on the X-Axis against the helpful_review average on the Y-Axis.
- Made a bar chart with the developer from the apps table and the developer_answered.
- Added a Filter for this visual only which selects only the rows where reviews_count is greater than 500.

[App_Landscape](/../main/App_Landscape.png)

[Reviews](/../main/Reviews.png)

[App_Reviews](/../main/App_Reviews.png)

[Popular_Reviews](/../main/Popular_Reviews.png)
