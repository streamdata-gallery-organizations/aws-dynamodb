---
swagger: "2.0"
x-collection-name: AWS DynamoDB
x-complete: 0
info:
  title: Amazon DynamoDB API Batch Get Item
  version: 1.0.0
  description: |-
    The BatchGetItem operation returns the attributes of one or more items from one or
          more tables.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=BatchGetItem:
    get:
      summary: Batch Get Item
      description: |-
        The BatchGetItem operation returns the attributes of one or more items from one or
              more tables.
      operationId: batchGetItem
      x-api-path-slug: actionbatchgetitem-get
      parameters:
      - in: query
        name: RequestItems
        description: A map of one or more table names and, for each table, a map that
          describes one or more items to retrieve from that table
        type: string
      - in: query
        name: ReturnConsumedCapacity
        description: 'Determines the level of detail about provisioned throughput
          consumption that is returned in the response:'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Batch Items
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