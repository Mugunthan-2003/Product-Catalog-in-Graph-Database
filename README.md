# Product-Catalog-in-Graph-Database

Metadata is taken from Bigcommerce platform

**Product:**
id : integer
name: string
type: string
sku: string
description: string
weight: decimal
width: decimal
depth: decimal
height: decimal
price: decimal(10,2)
cost_price: decimal(10,2)
retail_price: decimal(10,2)
sale_price: decimal(10,2)
category_id: integer (FK : Category -> id)
brand_id: integer (FK : Brand -> id)
fixed_cost_shipping_price: decimal(10,2)
is_free_shipping: boolean
upc: string
search_keywords: string
availability: string
sort_order: integer
order_quantity_minimum: integer
order_quantity_maximum: integer
gtin: string
mpn: string
reviews_rating_sum: integer
reviews_count: integer
total_sold: integer
date_created: datetime
date_modified: datetime

**Brand:**
id: integer (PK)
name: string
description: string

**Category Tree:**
id: integer (PK)
name: string

**Category:**
category_id: integer (PK)
tree_id: integer (FK : Category Tree -> id)
parent_id: integer (nullable)
name: string
description: string
search_keywords: string

**Product Variant:**
id: integer (PK)
product_id: integer (FK : Product -> id)
sku: string
sku_id: integer
cost_price: decimal(10,2)
price: decimal(10,2)
sale_price: decimal(10,2)
retail_price: decimal(10,2)
weight: decimal
width: decimal
height: decimal
depth: decimal
is_free_shipping: boolean
upc: string
mpn: string
gtin: string
