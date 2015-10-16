# Kent State Campus Locations Data
This dataset contains the addresses and latitudes/longitudes of the eight Kent State campuses, circa October 2015.

## Codebook
`Campus` - (String) The name of the campus.

`Address` - (String) The postal address of the campus.

`Latitude` - (Numeric) The latitude corresponding to the postal address.

`Longitude` - (Numeric) The longitude corresponding to the postal address.

`LatLongSourceURL` - (String) The latlong.net URL for the given latitude/longitude.

## Data Source
I transcribed the addresses for Kent State campus locations from [Campus Locations at Kent State](http://www.kent.edu/campus-locations) on October 16, 2015.

I retrieved the longitudes and latitudes of the campuses using the Address to Longitude and Latitude converter at [LatLong.net](http://www.latlong.net/convert-address-to-lat-long.html).

### Motivation
When the [kent.edu homepage](http://kent.edu)  was rebranded in 2014, one of the new features was a stylized map of the campus locations in Kent State colors. I wanted to try to recreate that map using the `maps` package in R, which required knowing the longitudes and latitudes of the points I wanted to map.

## For Future Updates
For future updates:
- Add other U.S. academic locations (NYC, Cleveland, etc.)
- Add global campus locations

