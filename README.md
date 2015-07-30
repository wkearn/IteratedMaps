# IteratedMaps

A package providing performant iterated maps such as the chaotic logistic map.

The maps are structured as infinite iterators. As a usage example, consider the logistic map with parameter 3.57

```julia

lm = LogisticMap(3.57) # Instantiates an IteratedMap
lm(0.5) # Creates an Iterator which starts at 0.5

for i in take(lm(0.5),10)) # Print the first ten values of the map
	println(i)
end

collect(take(lm(0.5),10)) # Collect the first ten values in an array

```

## To-Do

- Refine the interface. It might be nice (for dispatch reasons) to have types for each map rather than constructing a generic `IteratedMap` type for each map
- Come up with a better way to handle multidimensional and non-real maps
- Needs tests




