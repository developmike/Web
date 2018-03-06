To run the web project in dotnet core:
Stand in the project folder that you want to run in bash and type:
dotnet run
Then in will say the adress where it is locally hosting the app.

To get changes in .cs files to update immidiately instead of have to stop the process and build and start again, download the nuget package Microsoft.DotNet.Watcher.Tools and type:
dotnet watch run
Then in will say the adress where it is locally hosting the app and when you save .cs files you dont need to rebuild and restart the app.
Observe that the process "dotnet" is not killed even if you type CTRL + C on windows 10. You then have to kill the process in task manager.

OBS. This line of code must be added manually to the .csproj file to get the above to work.
<DotNetCliToolReference Include="Microsoft.DotNet.Watcher.Tools" Version="2.0.0" />