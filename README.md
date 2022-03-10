## **ASP.NET Core Web App project**

#### Building and publishing the web application


In this project i built a web application app using Visual studio and microsoft IIS.

I started off by downloading visual studio, the community version will do just fine.

Once downloaded, i opened visual studio and selected "New Project".

In the new project window i selected "ASP.NET Core Web App", in the framework selection i chose the latest long term support .NET framework and pressed create.

Currently in the .csprof file in the directory of the project appears only "PropertyGroup".

Next i installed "Newtonsoft.Json" from the NuGet library.

After the last step i found a new text in the .csproj including the Newtonsoft.Json package in our project.

and if i rebuild the project new files in the /bin/debug/net6.0 path can be found, among them are the .dll files including the Newtonsoft.Json dll.

At this point i published my web application to a folder.



#### Making the application accesible


To make my web app accesible, i did the following steps:

I installed IIS via the server manager features, Also downloaded and installed ASP.NET core runtime bundle.

In IIS i created a new application pool, selected "No managed code" in the .NET CLR version since we are using .NET Core.

In the sites folder i added a new site, assigned it to the previously created application pool and gave it port 5100.

Copied the "publish" folder we created from the build to the folder of the IIS site we created earlier.

And fianlly restarted the site, at this point i was able to reach my web application by going to: “http://localhost:5100/”.




