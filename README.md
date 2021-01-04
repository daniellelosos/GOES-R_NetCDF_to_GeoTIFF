# GOES-R NetCDF to GeoTIFF

These scripts convert GOES-R Series products from their native netCDF format to GeoTIFFs. Each script in this repository executes a distinct tasks. The GOES-R Level 
1b (L1b) Radiance product contains 16 files for each of the 16 Advanced Baseline Imager (ABI) spectral channels. The L1b script loops through the 16 netCDF files 
and converts each to a GeoTIFF. The L2 script converts a single GOES-R Level 2 (L2) ABI product image, such as Cloud Top Height, from a netCDF file to a GeoTIFF. 
The third script clips a netCDF file image down to a shapefile boundary, and saves the region of interest as a GeoTiff. This sample shapefile uses the United States 
Census Bureau’s state borders to clip a L2 Cloud and Moisture Imagery (CMI) file to the geographic extent of Michigan. However, any georeferenced polygonal 
shapefile may be swapped in.

For all of these scripts, the file(s) of intrest are pulled from the Amazon Web Service S3 Buckets which store GOES-16 and GOES-17 data. Adjust the scripts by 
selecting the satellite, product, date, and time, to pick a particular image. Adjust the directory to a local path. The scripts download the netCDF file(s) and 
the converted GeoTIFFs to the local path.
