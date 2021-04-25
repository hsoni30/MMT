*)Get method is implemented to test in browser.
It takes user(emailed) and customerid as parameter.
https://localhost:44330/API/Delivery?user=cat.owner@mmtdigital.co.uk&customerid=C34454
Post method also implemented.
*)
Removed default XML Formatter in WebApiConfig
Formatter can be changed at “Application_Start” as well.
*) deliveryAddress is not in Order Table, We can pass from Customer Table if required but not sure so kept blank.
*) Catch can be implemented so not to hit database every time, structure is shown in class DeliveryRepository but not used at present 
*) api key and url can be placed in web.config
*) we can use [IgnoreDataMember] or [JsonIgnore]
To hide field from sending to client but we need proper data structure for that if we have more time.
Or we need separate data class and Model class
*) Date format can also be done either in sql or in Model Data
*) If Order is null we are hiding data in json by [JsonProperty(NullValueHandling = NullValueHandling.Ignore)]
