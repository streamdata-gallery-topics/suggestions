---
swagger: "2.0"
x-collection-name: eBay
x-complete: 0
info:
  title: Ebay Get Category Tree Category Tree  Get Category Suggestions
  description: 'This call returns an array of category tree leaf nodes in the specified
    category tree that are considered by eBay to most closely correspond to the query
    string q. Returned with each suggested node is a localized name for that category
    (based on the Accept-Language header specified for the call), and details about
    each of the category''s ancestor nodes, extending from its immediate parent up
    to the root of the category tree. Note: This call can return a large payload,
    so you are advised to submit the request with the following HTTP header: &nbsp;&nbsp;Accept-Encoding:
    application/gzip With this header (in addition to the required headers described
    under HTTP Request Headers), the call returns the response with gzip compression.
    You identify the tree using the category_tree_id parameter, which was returned
    by the getDefaultCategoryTreeId call in the categoryTreeId field. Important: This
    call is not supported in the Sandbox environment. It will return a response payload
    in which the categoryName fields contain random or boilerplate text regardless
    of the query submitted.'
  contact:
    name: eBay Inc.
  version: 1.0.0
host: api.ebay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /category_tree/{category_tree_id}/get_category_suggestions:
    get:
      summary: Get Category Tree Category Tree  Get Category Suggestions
      description: 'This call returns an array of category tree leaf nodes in the
        specified category tree that are considered by eBay to most closely correspond
        to the query string q. Returned with each suggested node is a localized name
        for that category (based on the Accept-Language header specified for the call),
        and details about each of the category''s ancestor nodes, extending from its
        immediate parent up to the root of the category tree. Note: This call can
        return a large payload, so you are advised to submit the request with the
        following HTTP header: &nbsp;&nbsp;Accept-Encoding: application/gzip With
        this header (in addition to the required headers described under HTTP Request
        Headers), the call returns the response with gzip compression. You identify
        the tree using the category_tree_id parameter, which was returned by the getDefaultCategoryTreeId
        call in the categoryTreeId field. Important: This call is not supported in
        the Sandbox environment. It will return a response payload in which the categoryName
        fields contain random or boilerplate text regardless of the query submitted.'
      operationId: getCategorySuggestions
      x-api-path-slug: category-treecategory-tree-idget-category-suggestions-get
      parameters:
      - in: path
        name: category_tree_id
        description: The unique identifier of the eBay category tree for which suggested
          nodes are being requested
      - in: query
        name: q
        description: A quoted string that describes or characterizes the item being
          offered for sale
      responses:
        200:
          description: OK
      tags:
      - Auctions
      - Category
      - Tree
      - Category
      - Tree
      - ""
      - ""
      - Category
      - Suggestions
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---