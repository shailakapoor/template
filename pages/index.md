```sql first10customers
select "Customer Id" as customerid,
"First Name" as firstname,
"Last Name" as lastname,
"Phone 1" as phone1,
"Phone 2" as phone2,
* exclude ("Customer Id","First Name","Last Name","Phone 2","Phone 1") from customers.customers_10000 
```

<DataTable data={first10customers}/>

```sql top10customersbycountry
select Country, count(*) as numberofcustomers from customers.customers_10000 group by Country
```

<BarChart
  data={top10customersbycountry}
  x=Country
  y=numberofcustomers
  title = "Customers by Country"
  swapXY=true
  yGridlines=false
  />

<DimensionGrid data={first10customers} />











  