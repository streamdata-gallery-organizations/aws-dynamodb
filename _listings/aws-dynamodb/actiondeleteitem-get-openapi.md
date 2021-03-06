---
swagger: "2.0"
x-collection-name: AWS DynamoDB
x-complete: 0
info:
  title: Amazon DynamoDB API Delete Item
  version: 1.0.0
  description: Deletes a single item in a table by primary key.
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
  /?Action=BatchWriteItem:
    get:
      summary: Batch Write Item
      description: The BatchWriteItem operation puts or deletes multiple items in
        one or more tables.
      operationId: batchWriteItem
      x-api-path-slug: actionbatchwriteitem-get
      parameters:
      - in: query
        name: RequestItems
        description: A map of one or more table names and, for each table, a list
          of operations to be performed        (DeleteRequest or PutRequest)
        type: string
      - in: query
        name: ReturnConsumedCapacity
        description: 'Determines the level of detail about provisioned throughput
          consumption that is returned in the response:'
        type: string
      - in: query
        name: ReturnItemCollectionMetrics
        description: Determines whether item collection metrics are returned
        type: string
      responses:
        200:
          description: OK
      tags:
      - Batch Items
  /?Action=CreateTable:
    get:
      summary: Create Table
      description: The CreateTable operation adds a new table to your account.
      operationId: createTable
      x-api-path-slug: actioncreatetable-get
      parameters:
      - in: query
        name: AttributeDefinitions
        description: An array of attributes that describe the key schema for the table
          and indexes
        type: string
      - in: query
        name: GlobalSecondaryIndexes
        description: One or more global secondary indexes (the maximum is five) to
          be created on the table
        type: string
      - in: query
        name: KeySchema
        description: Specifies the attributes that make up the primary key for a table
          or an index
        type: string
      - in: query
        name: LocalSecondaryIndexes
        description: One or more local secondary indexes (the maximum is five) to
          be created on the table
        type: string
      - in: query
        name: ProvisionedThroughput
        description: Represents the provisioned throughput settings for a specified
          table or index
        type: string
      - in: query
        name: StreamSpecification
        description: The settings for DynamoDB Streams on the table
        type: string
      - in: query
        name: TableName
        description: The name of the table to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tables
  /?Action=DeleteItem:
    get:
      summary: Delete Item
      description: Deletes a single item in a table by primary key.
      operationId: deleteItem
      x-api-path-slug: actiondeleteitem-get
      parameters:
      - in: query
        name: ConditionalOperator
        description: This is a legacy parameter
        type: string
      - in: query
        name: ConditionExpression
        description: A condition that must be satisfied in order for a conditional
          DeleteItem to      succeed
        type: string
      - in: query
        name: Expected
        description: This is a legacy parameter
        type: string
      - in: query
        name: ExpressionAttributeNames
        description: One or more substitution tokens for attribute names in an expression
        type: string
      - in: query
        name: ExpressionAttributeValues
        description: One or more values that can be substituted in an expression
        type: string
      - in: query
        name: Key
        description: A map of attribute names to AttributeValue objects, representing
          the primary key of      the item to delete
        type: string
      - in: query
        name: ReturnConsumedCapacity
        description: 'Determines the level of detail about provisioned throughput
          consumption that is returned in the response:'
        type: string
      - in: query
        name: ReturnItemCollectionMetrics
        description: Determines whether item collection metrics are returned
        type: string
      - in: query
        name: ReturnValues
        description: Use ReturnValues if you want to get the item attributes as they
          appeared before they      were deleted
        type: string
      - in: query
        name: TableName
        description: The name of the table from which to delete the item
        type: string
      responses:
        200:
          description: OK
      tags:
      - Items
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