---
swagger: "2.0"
info:
  title: AWS DynamoDB API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListTables&k=1:
    get:
      summary: ' List Tables '
      description: Returns an array of table names associated with the current account
        and endpoint
      operationId: listTables
      parameters:
      - in: query
        name: ExclusiveStartTableName
        description: The first table name that this operation will evaluate
        type: string
      - in: query
        name: Limit
        description: A maximum number of table names to return
        type: string
      responses:
        200:
          description: OK
      tags:
      - tables
definitions: []
x-collection-name: AWS DynamoDB
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