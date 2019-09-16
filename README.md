# gitApiWrapper
Java cli wrapper for github API
CLI returns 
* Top-N repos by number of stars.
* Top-N repos by number of forks.

##Initial setup
* In eclipse import the project as new java project by using the .projects file
* Add the simple-jsonn and jcommander jar to your build path
* Entry point is CLI.java

##Using the executable binary
* Executable is at the path /executable and is named gitApiWrapperCli.jar
* Download the executable on to a JVM enabled machine. 
* Run java -jar gitApiWrapperCli.jar -h to see all the options
* ```C02VQ20ZHV2Q:executable abhinavsi$ java -jar gitApiWrapperCli.jar -h
Usage: gitPopSearch [options]
  Options:
    -h, --help
      Displays help information
  * -c, --count
      Number of results
      Default: 0
  * -o, --organization
      Git Organization for searching
  * -s, --sortFactor
      Sorting factor should be  stars || fork || PullReq || contrib_per  where
       Contibution percentage = forks/PR ```

* Valid eg: ```java -jar gitApiWrapperCli.jar -s forks -c 10 -o yahoo
Running gitpopsearch with ...

help=false
organization=yahoo
count=10
sortFactor=forks
-------------------------------------------------------------------------------
                  Result sorted on number of Forks
-------------------------------------------------------------------------------
RepoName = kafka-manager                            Count = 1931
RepoName = open_nsfw                                Count = 961
RepoName = TensorFlowOnSpark                        Count = 842
RepoName = CaffeOnSpark                             Count = 378
RepoName = gifshot                                  Count = 328
RepoName = egads                                    Count = 278
RepoName = streaming-benchmarks                     Count = 249
RepoName = gryffin                                  Count = 245
RepoName = fluxible                                 Count = 227
RepoName = mysql_perf_analyzer                      Count = 197```
