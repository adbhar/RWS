
This Visual Studio extension only supports Visual Studio 2019 and EPiServer CMS 11 on .NET Framework 4.x.


#	Configure Episerver NuGet Feed

You need to add the Episerver Nuget feed within your Visual Studio, otherwise, you will not be able to find and install the Episerver packages. To add the feed, within Visual Studio click:
Tools ➡ Options➡ NuGet Package Manager ➡ Package Sources
 
Click the + icon and at the bottom add EpiServer as the name of the feed and within package source option, use this URL:

http://nuget.episerver.com/feed/packages.svc/

Click Update and you're done . In Nuget explorer, you should now see an Episerver option within the Online section. From here you can browse all the packages within the Episerver feed.


#	Install Package 

Now In the NPM(Nuget Package Manager), Browse for RWS.Translator and install it

# Dependencies

1.RestSharp  -   104.5.0

2.Entity Framework   -   6.1.0

3.PagedList.MVC   -   4.5.0

4.Newtonsoft.Json   -   10.0.3
