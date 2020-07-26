# AppCenter sink for Serilog
![GitHub](https://img.shields.io/github/license/SByteDev/Net.Serilog.Sinks.AppCenter.svg)
![Nuget](https://img.shields.io/nuget/v/SByteDev.Serilog.Sinks.AppCenter.svg)
[![Build Status](https://img.shields.io/bitrise/1bc1ba2fc59d0349/develop?label=development&token=rzXR1phG35ioOKGuHzCahw&branch)](https://app.bitrise.io/app/1bc1ba2fc59d0349)
[![Build Status](https://img.shields.io/bitrise/1bc1ba2fc59d0349/master?label=production&token=rzXR1phG35ioOKGuHzCahw&branch)](https://app.bitrise.io/app/1bc1ba2fc59d0349)
[![CodeFactor](https://www.codefactor.io/repository/github/sbytedev/net.serilog.sinks.appcenter/badge)](https://www.codefactor.io/repository/github/sbytedev/net.serilog.sinks.appcenter)

[Serilog](https://github.com/serilog/serilog) sink that uses [AppCenter.Analytics](https://docs.microsoft.com/en-us/appcenter/analytics/) and [AppCenter.Crashes](https://docs.microsoft.com/en-us/appcenter/sdk/crashes/xamarin) to log events.

## Installation

Use [NuGet](https://www.nuget.org) package manager to install this library.

```bash
Install-Package SByteDev.Serilog.Sinks.AppCenter
```

## Usage
```cs
using SByteDev.Serilog.Sinks.AppCenter;

// Configure AppCenter fisrt.
AppCenter.Start("AppCenterApiKey", typeof(Analytics), typeof(Crashes));

// Create logger that logs informational (and above) events to AppCenter.
var logger = new LoggerConfiguration()
    .WriteTo.AppCenter(LogEventLevel.Information)
    .CreateLogger();
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update the tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
