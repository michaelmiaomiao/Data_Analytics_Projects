Jiashu Miao 

## I would recommend to go through the html file from knitted R file. 
###  Pleae also check Tableau and Python file for more intersting fingdings.

### Here is some digest from my over-all analysis 


### Conclusion and insights

- This analysis gives me several fidings though need further study for validation:
  - The voltage has missing values
  - There are **fours** flights that their locations are weird when looking at map at launch (upper left corner, need check)
  - specific battery and body series affects the creating of missing voltage, especially body 577209618523054080 always gives missing values ever since use it. **Avoid from using 577209618523054080 to check error** 
  - The components **are not used equally frequenly** which possibly causes overuse to affects the quality of drone system. 
  - The wing series **15SPJJJ09028064** affects the launch_airspeed and need check.
  - on 2018-09-30, only battery **15SPJJJ10056048** used the whole day and causes largest average error, and it needs to be checked, the wing and body also a affect a little bit but not as serious as this battery.
  
  
- Some possible relation: 
  - the higher the air temperature, the higher the wind, and the lower the static pressue and lower humidity. 
  - I think it's better to study the distance travel in same time other than launch airspeed and have fidings that explain the distance travel , and therefore can calculate the average speed for the trip. 
 - `distance = -1.7995 * air.temperature -5.4204 * wind.magnitude  -0.0275 * static_pressure + 2.698e+03`
 - the unexplained behavior then make sense why `2018-09-23` has low lauch_airspeed but highest distance: the wind is small and it's pretty cold with high humidity and low pressure 
 - *`physics`: rainy/cloudy has lower pressure, and lower wind and colder, but lower pressure makes techinician depressed mood therefore might cause some mistake when choosing and installing the components and monitoring the positions* 
 - *`history` weather:2018-09-23 weather in Rwanda was cloudy and high humidity.*  
- **So to travel longer distance in same period, beside checking the components to used at best performance, the weather matters too, and it is preferable that to fly at lower temperature with higher humidity, which might counter my common sense.**

- And hence people at Zipline can use weahter to best perform the fast delivery and power-saving drone system.

- Please refer to tableau visualizaed plots and python for more. 

