# 🏠 SIMPLE CLI 👥

A CLI tool for working with dummy property and tenant data taken from CSV. 

```
npm i 
```

### Check the status of a given property
```
rep status <property_id>
```
Returns:
- "PROPERTY_VACANT": No tenants
- "PARTIALLY_VACANT": Tenant/s, but fewer than the capacity, and end of tenancy date hasn't passed
- "PROPERTY_ACTIVE": Tenants at full capacity, and end of tenancy date hasn't passed
- "PROPERTY_OVERDUE": Tenant/s, and end of tenancy date has passed  



### Check if your properties have valid UK postcodes
```
rep checkPostcodes
```

returns:
- List of property IDs where the property postcode is not valid for the UK

(Postcode validation uses British Standards document BS 7666.)



### Calculate average rent per tenant for a given property
```
rep propertyRentPerTenant <property_id>
```
Flags:
- -p -pennies to return amount in pennies

Returns:
- Average rent each tenant is paying per month in the property in pounds



### Calculate the average monthly rent per property in a given region
```
rep rentPerRegion <region>

```

Returns:
- Average rent per month you are getting from properties in that region
