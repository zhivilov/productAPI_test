# productAPI_test
Product API Swagger Apiary Test

Run on a local machine
1) Go to cd /Users/zhyviiva/Documents/CODE BASE/API_test/node_modules/dredd/bin
2) Run node dredd init -r apiary -j apiaryApiKey:3d76aaadb5259e8b7af8b39e0e8d7ef9 -j apiaryApiName:productdataapi
3) Configire path to swagger file: ../../../productAPI_test/swagger.yaml
4) Configure endpoint: https://www.adidas.co.uk
5) Check dredd.yaml file and run node dredd 


availability_status:
        type: string
        description: The status of the product. Possible values are "IN_STOCK". "NOT_AVAILABLE", "PREORDER", "BACKORDER"
        enum:
          - IN_STOCK
          - NOT_AVAILABLE
          - PREORDER
          - BACKORDER
      variation_list:
        type: array
        description: List of product variations
        items:
          $ref: '#/definitions/variation_list_definition'
