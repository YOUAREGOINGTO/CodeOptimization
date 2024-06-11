* Text file has Tle lines  and btain the co-ordinates for one day with time frame of one minute.(get_satellite_positions)
* Convert the co-ordinates to longitude, latitude and laltitude.(ecef2lla,convert_to_lla_single)
* Compare within a given range of latitude and longitude.(filter_positions)
* Code Optimization with Distributed Computing.(Using Dask Library)
# Distributed Computing
* Using Dask Bag as Data is Unstructured and Dak Bag has map , filter functions.
* Code can be Easily scaled By Replacing Local Cluster with Required Cloud Cluster.(Production Ready Code)
*Cluster has n_workers argument but no need to pass as Dask can automatically assign workers based on Computation resources.
* We can use Adaptive Scaling for setting max and min workers.(Cloud Clusters
# Computation Time
* Sequential Approach Takes 55 sec and where as Dask Approach takes 30 secs.(For 41 Satellites). We can Scale to Cloud Cluster for 30000 satellites
* Most of the time is wasted at function ecef2lla
# Alternative Approach
* As ecef2lla function taking time I have Updated the function and Intialized a Transformer Object Before hand.
* This step reduces the Computation time by a Margin.
# Results
* Sequential Approach is Better than Dask Approach.
* Dask seems to be infeffective to handle Pre determined Objects
* By below Task stream image, there's lot of waiting time when using Dask Because of the Transformer Object.
* Sequential Approach Takes around 95 sec for 30000 satellites.
![image](https://github.com/YOUAREGOINGTO/CodeOptimization/assets/106869151/98e6751c-bd1a-46f3-aa9d-f5e96177bf27)
