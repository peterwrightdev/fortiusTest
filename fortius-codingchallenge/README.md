# Fortius code challenge



The code challenge consists in the implementation of a simple search engine for shirts.




## Procedure and what we expect

More detail is below, but at a high level you'll need to build a search engine that returns shirts by colour and size with counts (as per examples below). We've provided enough code to bootstrap the solution and included a couple of basic test cases to get you started. We ask that you understand the problem, implement the engine and be happy that the engine works. Treat this like real life - you are picking up the start of the implementation from another developer, so don't expect it to be bug free and add more code and coverage to ensure you are happy it works - you own the implementation now.



There isn't a time limit on how long you spend on this challenge, but our across our team a few hours is average.  Please be happy that your search engine implementation works and later in the interview process we'll ask you questions such as "why that way" or "how could you improve it". In addition to the implementation working, we'll look at your coding style. Have fun and enjoy the challenge.



We would like you to zip the final solution and return the test to us.



## What to do?

Shirts are in different sizes and colors. As described in the Size.cs class, there are three sizes: small, medium and large, and five different colors listed in Color.cs class.



The search specifies a range of sizes and colors in SearchOptions.cs. For example, for small, medium and red the search engine should return shirts that are either small or medium in size and are red in color. In this case, the SearchOptions should look like:



```

{

    Sizes = List<Size> {Size.Small, Size.Medium},

    Colors = List<Color> {Color.Red}

}

```



The results should include, as well as the shirts matching the search options, the total count for each search option taking into account the options that have been selected. For example, if there are two shirts, one small and red and another medium and blue, if the search options are small size AND red color, the results (captured in SearchResults.cs) with total count for each option should be:

```

{

    Shirts = List<Shirt> { SmallRedShirt },

    SizeCounts = List<SizeCount> { Small(1), Medium(0), Large(0)},

    ColorCounts = List<ColorCount> { Red(1), Blue(0), Yellow(0), White(0), Black(0)}

}

```



The search engine logic sits in SearchEngine.cs and should be implemented by the candidate. Feel free to use any additional data structures, tests, classes or libraries to prepare the data before the actual search.



There are two tests in the test project; one simple search for red shirts out of a total of three, and another one which tests the performance of the search algorithm through 50.000 random shirts of all sizes and colors which measures how long it takes to perform the search algorithm. A reasonable implementation should not take more than 100 ms to return the results.