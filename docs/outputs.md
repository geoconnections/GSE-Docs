## Status

> **Name:** `status`

> **Type:** String

> **Description:** Indicates whether a request was successfully fulfilled or has errors

> **Possible Values:**
>> - success
>> - error

## Errors

> **Name:** `errors`

> **Type:** Array

> **Description:** An array of the errors associated with a request. If the response status is 'error' the only additional information provided will be the list of errors. Each value in the list is a dictionary.

> This documentation describes a single dict contained in the list as all of them should be identical regardless of error.

>> ### Fields

>>> **Name:** `fields`

>>> **Type:** Array

>>> **Description:** A list of the input field names that triggered error detection.

>> ### Message

>>> **Name:** `message`

>>> **Type:** String

>>> **Description:** A description of what triggered the error.

>> ### Type

>>> **Name:** `type`

>>> **Type:** String

>>> **Description:** A general error type that may be useful for styling or handling errors that are not field specific.

## Warnings

> **Name:** `warnings`

> **Type:** Array

> **Description:** An array of the warnings associated with a request. Successful requests may contain warnings for values submitted that have been automatically modified on the server side to avoid bumping into an error.  Such warnings include clamping values to within range and replacing invalid inputs with the field defaults.

> This documentation describes a single dict contained in the list as all of them should be identical regardless of error.

>> ### Fields

>>> **Name:** `fields`

>>> **Type:** Array

>>> **Description:** A list of the input field names that triggered the warning.

>> ### Message

>>> **Name:** `message`

>>> **Type:** String

>>> **Description:** A description of what triggered the warning.

>> ### Type

>>> **Name:** `type`

>>> **Type:** String

>>> **Description:** A general warning type that may be useful for styling or handling warnings that are not field specific.

## Place

> **Name:** `place`

> **Type:** Dict

> **Description:** Contains information about the location returned from search.

> ### GeoCoder

>> **Name:** `geocoder`

>> **Type:** String

>> **Description:** The name of geocoding service used to search for the location.


> ### Attribution

>> **Name:** `attribution`

>> **Type:** Dict

>> **Description:** Contains link, name and copyright html for properly crediting the GeoCoding service used on the backed. As long the attribution name field is not set to Cached Search, you must display the attribution details along with the results of your search.

>> #### Name

>>> **Name:** `name`

>>> **Type:** String

>>> **Description:** The name of the geocoding service used to resolve the searched location.

>> #### Link

>>> **Name:** `link`

>>> **Type:** String

>>> **Description:** A link to the geocoding service site

>> ### Copyright HTML

>>> **Name:** `copyright_html`

>>> **Type:** String

>>> **Description:** When provided, the geocoder has a specific attribution that it prefers.If present you should insert this HTML into your results display directly.

> ### City

>> **Name:** `city`

>> **Type:** String

>> **Description:** Text string indicating the city or town for the location address.

>> **Accepts:**
>>> * Name of city, town village, hamlet, borough etc.

> ### Region

>> **Name:** `region`

>> **Type:** String

>> **Description:** Text string indicating the region typically a state or province for the searched location. Regions are the first area division under a country.

> ### Region Type

>> **Name:** `region_type`

>> **Type:** String

>> **Description:** Text string describing the region.

> ### Sub-Region

>> **Name:** `subregion`

>> **Type:** String

>> **Description:** Text string indicating the sub-region typically a county for the searched location. Sub-Regions are the first area division under a region.

> ### Sub-Region Type

>> **Name:** `subregion_type`

>> **Type:** String

>> **Description:** Text string describing the subregion.

> ### Locality

>> **Name:** `locality`

>> **Type:** String

>> **Description:** Text string indicating the locality (city, town, etc.)

> ### Locality Type

>> **Name:** `locality_type`

>> **Type:** String

>> **Description:** Text string describing the type of locality.

> ### ZIP/Postal Code

>> **Name:** `postal_code`

>> **Type:** String

>> **Description:** Text string indicating the postal code for the searched location.

> ### Country

>> **Name:** `country`

>> **Type:** String

>> **Description:** Lowercase ISO Alpha-2 countyr code for the searched location.

> ### Latitude

>> **Name:** `lat`

>> **Type:** String or Float

>> **Description:** Signed latitude in degrees format

> ### Longitude

>> **Name:** `lon`

>> **Type:** String or Float

>> **Description:** Signed longitude in degrees format

## Hot Water Generation

> **Name:** `hwg`

> **Type:** Dict

> **Description:** Contains information specifically related to hot water generation calculation.

>> ### Hot Water Set Point

>>> **Name:** `set_point_hwg`

>>> **Type:** String (This is a string value. The number is formatted server side to a reasonable number of decimals)

>>> **Description:** The temperature to which hot water is heated.

>> ### Hot Water Supply Temperature

>>> **Name:** `supply_temp_hwg`

>>> **Type:** String (This is a string value. The number is formatted server side to a reasonable number of decimals)

>>> **Description:** The temperature at which supply water enters the hot water system.

>> ### Annual Percentage Generated by Geothermal

>>> **Name:** `annual_percent_geo_hwg`

>>> **Type:** String (This is a string value. The number is formatted server side to a reasonable number of decimals)

>>> **Description:** The percentage of the total volume of hot water that the geothermal system is responsible for. The remaining hot water is assumed to be heated by a supplemental system using the same technology as the hot water generation comparative technology.

>> ### Age of Hot Water System

>>> **Name:** `age_hwg`

>>> **Type:** String

>>> **Description:** Describes the age of the comparative hot water generation system and is used to adjust efficiency.


>> ### Standing Losses

>>> **Name:** `standing_losses_hwg`

>>> **Type:** String (This is a string value. The number is formatted server side to a reasonable number of decimals)

>>> **Description:** The percentage of energy that is lost from the heated hot water through the tank wall and piping system.


>> ### Daily Volume Per Resident

>>> **Name:** `vol_per_res_hwg`

>>> **Type:** String (This is a string value. The number is formatted server side to a reasonable number of decimals)

>>> **Description:** The average amount of hot water used by each resident in a typical day.


>> ### Units

>>> **Name:** `units`

>>> **Type:** Dict

>>> **Description:** Contains a map of units associated with each of the fields in the Hot Water Generation Dict.

## Weather

> **Name:** `weather`

> **Type:** Dict

> **Description:** Contains information specifically related to local weather.

>> ### Cooling Degree Days

>>> **Name:** `cdd`

>>> **Type:** String

>>> **Description:** The number of degrees that a day's average temperature is above 65&deg;F (18&deg;C) which is typically when people start to cool their buildings.

>> ### Heating Degree Days

>>> **Name:** `hdd`

>>> **Type:** String

>>> **Description:** The number of degrees that a day's average temperature is below 65&deg;F (18&deg;C) which is typically when people start to heat their buildings.

>> ### Minimum Outdoor Air Temperature

>>> **Name:** `oat_min`

>>> **Type:** String

>>> **Description:** The lowest outdoor air temperature recorded for the weather location.

>> ### Maximum Outdoor Air Temperature

>>> **Name:** `oat_max`

>>> **Type:** String

>>> **Description:** The highest outdoor air temperature recorded for the weather location.

>> ### Average Outdoor Air Temperature

>>> **Name:** `oat_avg`

>>> **Type:** String

>>> **Description:** The average outdoor air temperature recorded for the weather location.

>> ### Units

>>> **Name:** `units`

>>> **Type:** Dict

>>> **Description:** Contains a map of units associated with each of the fields in the Weather Dict.

## Carbon

> **Name:** `carbon`

> **Type:** Dict

> **Description:** Contains information specifically related to the estimated carbon dioxide output due to the operation of an heating/cooling system. The dictionary is split into `comp` and `gshp` with comp indicating that the values are attributed to the comparitive technology and gshp indicating that the contained values are attributed to the operation of a geothermal system.

> The values include 'upstream' carbon from generation in the case of electricity but only consider point of use carbon from fossil fuels.

> The documentation does not detail `comp` and `gshp` dicts separately as it would be redundant.

>> ### Carbon From Hot Water Generation

>>> **Name:** `hwg`, `total_hwg`, `gshp_hwg`, `supp_hwg`

>>> **Type:** Integer

>>> **Description:** The number of pounds (kilograms) of carbon dioxide output in a year just from hot water generation. Note that the geothermal system may be modeled with only a fraction of the total annual hot water volume being generated by geothermal hence, the number is broken out into its component parts (gshp, supplemental and total).

>> ### Carbon From Heating

>>> **Name:** `heating`

>>> **Type:** Integer

>>> **Description:** The number of pounds (kilograms) of carbon dioxide output in a year just from heating the space.

>> ### Carbon From Cooling

>>> **Name:** `cooling`

>>> **Type:** Integer

>>> **Description:** The number of pounds (kilograms) of carbon dioxide output in a year just from cooling the space.

>> ### Total Carbon Emmisions

>>> **Name:** `carbon`

>>> **Type:** Integer

>>> **Description:** The number of pounds (kilograms) of carbon dioxide output in a year from heating and cooling the space as well as hotwater generation.

>> ### Units

>>> **Name:** `units`

>>> **Type:** String

>>> **Description:** The unit associated with the carbon emissions figures.

>> ### Reduction

>>> **Name:** `reduction`

>>> **Type:** Dict

>>> **Description:** The difference in carbon emmissions between comparison system and GSHP. Calculated as (comp_value - gshp_value)

## Heat Pump Sizing

> **Name:** `sizing`

> **Type:** Dict

> **Description:** Contains information specifically related to the nominal capacity of the geothermal equipment required to condition the space (ignorant of hot water).

>> ### Based On

>>> **Name:** `based_on`

>>> **Type:** String

>>> **Description:** The operational mode that requires the most capacity to meet the building demands.

>> ### High Estimate

>>> **Name:** `high`

>>> **Type:** Float

>>> **Description:** An oversized nominal capacity of equipment that would reasonably service the space.

>> ### Closest Estimate

>>> **Name:** `closest`

>>> **Type:** Float

>>> **Description:** The nominal capacity it is estimated the space requires.

>> ### Low Estimate

>>> **Name:** `low`

>>> **Type:** Float

>>> **Description:** An undersized nominal capacity of equipment that would reasonably service the space.

>> ### Units

>>> **Name:** `units`

>>> **Type:** String

>>> **Description:** The unit associated with the nominal capacity values.

## Annual Savings

> **Name:** `savings`

> **Type:** Dict

> **Description:** Contains information specifically related to the amount of money the homeonwer would save if they used a geothermal heating and cooling system for their home. Note that the currency is dependent on the rates the user defines.

>> ### Savings From Hot Water Generation

>>> **Name:** `hwg`

>>> **Type:** String

>>> **Description:** The estimated amount saved from using geothermal for domestic hot water generation.

>> ### Savings From Heating

>>> **Name:** `heating`

>>> **Type:** String

>>> **Description:** The estimated amount saved from using geothermal for space heating.

>> ### Savings From Cooling

>>> **Name:** `cooling`

>>> **Type:** String

>>> **Description:** The estimated amount saved from using geothermal for space cooling.

>> ### Total Savings

>>> **Name:** `total`

>>> **Type:** String

>>> **Description:** The total estimated amount saved from using geothermal for space heating/cooling and domestic hot water generation.

## Annual Operating Costs

> **Name:** `costs`

> **Type:** Dict

> **Description:** Contains information specifically related to the estimated annual operating costs for the heating/cooling and domestic hot water systems. The dictionary is split into `comp` and `gshp` with comp indicating that the values are attributed to the comparitive technology and gshp indicating that the contained values are attributed to the operation of a geothermal system.

> Note that the currency is dependent on the rates the user defines.

> The documentation does not detail the contained `comp` and `gshp` dicts separately as it would be redundant.

>> ### Annual Cost of Hot Water Generation

>>> **Name:** `hwg`, `total_hwg`, `gshp_hwg`, `supp_hwg`

>>> **Type:** String

>>> **Description:** The cost of domestic hot water generation for the technology. Note that the geothermal system may be modeled with only a fraction of the total annual hotwater volume being generated by geothermal hence, the number is broken out into its component parts (gshp, supplemental and total).

>> ### Annual Cost of Heating

>>> **Name:** `heating`

>>> **Type:** String

>>> **Description:** The annual cost to heat the space.

>> ### Annual Cost of Cooling

>>> **Name:** `cooling`

>>> **Type:** String

>>> **Description:** The annual cost to cool the space.

>> ### Total Annual Cost

>>> **Name:** `total`

>>> **Type:** String

>>> **Description:** The annual cost to heat and cool the space as well as generate domestic hot water.

## Utility Rates

> **Name:** `rates`

> **Type:** Dict

> **Description:** Contains the rates used for calcuating operating costs organized by utility.

>> ### Standard Electric Rate

>>> **Name:** `rate_electric_standard`

>>> **Type:** String

>>> **Description:** The standard cost per unit of electricity. Applied to electric resistance, air source heat pumps and if not defined will be applied the geothermal electric rate.

>> ### Geothermal Electric Rate

>>> **Name:** `rate_electric_geo`

>>> **Type:** String

>>> **Description:** The cost per unit of electricity for the geothermal system. This allows for users in locations where their local utility offers reduced rates for geothermal installations.

>> ### Natural Gas Rate

>>> **Name:** `rate_natural_gas`

>>> **Type:** String

>>> **Description:** The cost per unit of natural gas.

>> ### Propane Rate

>>> **Name:** `rate_propane`

>>> **Type:** String

>>> **Description:** The cost per unit of propane.

>> ### Fuel Oil Rate

>>> **Name:** `rate_fuel_oil`

>>> **Type:** String

>>> **Description:** The cost per unit of fuel oil.

>> ### Units

>>> **Name:** `units`

>>> **Type:** String

>>> **Description:** Describes what unit of volume or energy the to which a given rate is applied.

## Operating Details

> **Name:** `operating_details`

> **Type:** Dict

> **Description:** Contains information that directly relates to the estimated size and performance of the geothermal and conventional system not detailed elsewhere in the response. Many of the values contained in the operating_details Dict are reporting back the inputs from the user and are provided mainly for SI implementations as their may be some floating point issues associated with the conversion of all inputs to IP for calculation and then returned to SI for the response.

>> ### Age Of Home

>>> **Name:** `age_home`

>>> **Type:** String

>>> **Description:** The age of the home is used in calculating unspecified building construction details as well as estimating degradation of equipment performance over time. This value will be applied to the `age_cooling_comp` and/or `age_heating_comp` if they are not defined.

>> ### Age Of Comparative Cooling Technology

>>> **Name:** `age_cooling_comp`

>>> **Type:** String

>>> **Description:** The age of the comparative cooling technology. If not independently defined as an input, this value will defaulted to the age_home.

>> ### Age Of Comparative Heating Technology

>>> **Name:** `age_heating_comp`

>>> **Type:** String

>>> **Description:** The age of the comparative heating technology. If not independently defined as an input, this value will defaulted to the age_home.

>> ### Insulation Level

>>> **Name:** `insulation_level`

>>> **Type:** String

>>> **Description:** A general description of how well the building is insualted. If not defined as an input, this value will be determined based on the age of the home.

>> ### Building Tightness

>>> **Name:** `building_tightness`

>>> **Type:** String

>>> **Description:** A general description of the building's resistance to infiltration. If not defined as an input, this value will be determined based on the age of the home.

>> ### Duct Insulation

>>> **Name:** `duct_insulation`

>>> **Type:** String

>>> **Description:** A general description of how well the building's duct work is insulated. If not defined as an input, this value will be determined based on the age of the home.

>> ### Duct Placement

>>> **Name:** `duct_placement`

>>> **Type:** String

>>> **Description:** Where in the space the duct work is placed. If not defined as an input, this value will typically default to conditioned space. If there is no below grade space this value will default to unconditioned attic. If there is below grade space but the basement is defined to be unconditioned, this value will default to unconditioned basement.

>> ### Duct Seal

>>> **Name:** `duct_seal`

>>> **Type:** String

>>> **Description:** A general description of the 'leakiness' of a building's duct work. If not defined as an input, this value will default to average.

>> ### Basement Construction

>>> **Name:** `basement`

>>> **Type:** String

>>> **Description:** Describes whether the basement is conditioned or unconditioned space. Additionally may return slab indicating that there is no below grade area.

>> ### Above Grade Area

>>> **Name:** `above_grade_area`

>>> **Type:** String

>>> **Description:** Area of conditioned space above grade.

>> ### Below Grade Area

>>> **Name:** `below_grade_area`

>>> **Type:** String

>>> **Description:** Area of conditioned space below grade.

>> ### Heating Set Point Temperature

>>> **Name:** `set_point_heating`

>>> **Type:** String

>>> **Description:** The temperature to which the space will be heated.

>> ### Cooling Set Point Temperature

>>> **Name:** `set_point_cooling`

>>> **Type:** String

>>> **Description:** The temperature to which the space will be cooled.

>> ### Number of Residents

>>> **Name:** `num_residents`

>>> **Type:** String

>>> **Description:** The number of people that will typically occupy the house.  If undefined as an input, the value will be defaulted to 4.

>> ### Units

>>> **Name:** `units`

>>> **Type:** Dict

>>> **Description:** Contains a map of units associated with each of the fields in the Operating Details Dict.

## Units of Energy

> **Name:** `units_of_energy`

> **Type:** Dict

> **Description:** Contains the total number of units of energy of a specific 'fuel' that are consumed in each mode of operation by the GSHP and comparative system.

>> ### Units

>>> **Name:** `units`

>>> **Type:** Dict

>>> **Description:** Contains a map of units associated with each of the fields in the GSHP and COMP Dicts.

>> ### GSHP

>>> **Name:** `gshp`

>>> **Type:** Dict

>>> **Description:** The units of energy consumed by each operating mode of the GSHP.

>> ### COMP

>>> **Name:** `comp`

>>> **Type:** Dict

>>> **Description:** The units of energy consumed by each operating mode of the comparative system.

## Monthly
> **Name:** `monthly`

> **Type:** Dict

> **Description:** Monthly is a dictionary of all months in the year.  Each month is a dict of dicts `month`,`carbon`,`savings` and `units_of_energy` dict. With the exception of `month`, these dicts are structurally identical to the annual counterpart. 

> **Keys:** `['jan','feb','mar','apr','may','jun','jul','aug','sep','oct','nov','dec']`

>> ## Month

>>> **Name:** `month`

>>> **Type:** Dict

>>> **Description:** The `month` dict contains useful information for displaying and organizing monthly data.

>>>> ### Index

>>>> **Name:** `index`

>>>> **Type:** Integer

>>>> **Description:** Ordinal for the month.

>>>> ### Abbreviation

>>>> **Name:** `abbr`

>>>> **Type:** String

>>>> **Description:** 3 character lower case abbreviation for month. These match the monthly dict keys.

>>>> #### Name

>>>> **Name:** `name`

>>>> **Type:** String

>>>> **Description:** Full month name for display.
