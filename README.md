# Custom-Products_Price-Rule-Fix
Fix - Rules don´t work in custom products 
"version": "3.4.5",



# Fix for Shopware 6 Ticket
- https://issues.shopware.com/issues/CUS-517
- https://issues.shopware.com/issues/CUS-518

# Copy&Paste the content of files into: 
- /swagcustomizedproducts/src/Resources/views/storefront/component/customized-products/_include/price-label.html.twig
- /swagcustomizedproducts/src/Resources/views/storefront/component/customized-products/option-type/select/checkboxes.html.twig

## If you use another type then checkboxes please search for class "label__surcharge-info" in twig file path  
- /swagcustomizedproducts/src/Resources/views/storefront/component/customized-products/option-type/<your type>
there you must pass the context
```
     {% sw_include '@SwagCustomizedProducts/storefront/component/customized-products/_include/price-label.html.twig' with {
        value: optionValue, context: context
     } %}
```
