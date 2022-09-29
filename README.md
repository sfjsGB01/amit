# pax11
#Mini project for the sfjbs training
import requests
BASE_URL = 'https://fakestoreapi.com'

all_products_response=requests.get(f"{BASE_URL}/products")
#print(all_products_response.json())
print(all_products_response)

for product in all_products_response:
    print(product)
    print(f"{product['title']} costs ${product['price']}")
