# Command-line parameter

Command-line parameters are accessible through Application Startup event. Second parameter `StartupEventArgs` contains list of passed parameters. Example taken from the Microsoft documentation.

```xaml
<Application
  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
  x:Class="SDKSample.App"
  Startup="App_Startup" />
```

```csharp
using System.Windows;

namespace SDKSample
{
    public partial class App : Application
    {
        void App_Startup(object sender, StartupEventArgs e)
        {
            // Application is running
            // Process command line args
            bool startMinimized = false;
            for (int i = 0; i != e.Args.Length; ++i)
            {
                if (e.Args[i] == "/StartMinimized")
                {
                    startMinimized = true;
                }
            }

            // Create main application window, starting minimized if specified
            MainWindow mainWindow = new MainWindow();
            if (startMinimized)
            {
                mainWindow.WindowState = WindowState.Minimized;
            }
            mainWindow.Show();
        }
    }
}
```

* [Startup documentation](https://learn.microsoft.com/en-us/dotnet/api/system.windows.application.startup?view=windowsdesktop-7.0)
* [WPF Tutorial](https://wpf-tutorial.com/wpf-application/command-line-parameters/)
