This project serves as a reproducible for this [VS Developer Community issue](https://developercommunity.visualstudio.com/t/Using-latest-preview-VS2022-and-Blazor-W/10481382).

In VS Community 17.8 Preview 5, Im running into the above issue as well as the RZ10012 in blazor components and I believe the problem has to do with  `UseArtifactsOutput`.

Currently this project is in a functional state, to show the issue please follow the steps below:

1. Change `UseArtifactsOutput` to `true` in _Directory.Build.props_
2. Close visual studio
3. Delete the _\bin_ and _\obj_ folders under the _Client_ project (skipping this step will only partially show the issues)
4. Open the solution

After following the steps above you should see compile errors in _Program.cs_ and RZ10012 errors in any blazor component (_Home.razor_ has an example of both first (`PageTitle`) and third (`MudText`) party blazor component usage).
