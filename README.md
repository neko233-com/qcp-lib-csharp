# qcp-lib-csharp

C# binding for QCP protocol.

## Installation

### NuGet

```bash
dotnet add package QcpLib.CSharp
```

## Usage

```csharp
using QcpLib;

// Create QCP client
var client = new QcpClient();

// Connect to server
client.Connect("127.0.0.1", 9000);

// Send data
client.Send(Encoding.UTF8.GetBytes("hello"));

// Receive data
byte[] buffer = new byte[1024];
int n = client.Receive(buffer);

// Close
client.Close();
```

## Features

- .NET Standard 2.0+
- Async/Await support
- Thread-safe
- Unity compatible

## License

MIT License
