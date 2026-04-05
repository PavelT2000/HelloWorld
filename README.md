# HelloWorld

## 📖 Description
A minimal, production-ready C# console application targeting the **.NET Framework 4.7.2**. Designed as a foundational template for developers exploring traditional .NET workflows, this project demonstrates standard Visual Studio solution architecture, MSBuild configuration, assembly metadata management, and basic console I/O. 

When executed, the application initializes the runtime, loads the `Main` entry point, and outputs a classic `"Hello, World!"` message to the standard output stream.

## 🛠️ Prerequisites
- **Operating System:** Windows (required for .NET Framework 4.7.2)
- **IDE:** Visual Studio 2019 or 2022 (with the `.NET desktop development` workload installed)
- **Framework:** .NET Framework 4.7.2 SDK/Runtime (automatically included with modern Visual Studio installations)
- **Build Tool:** MSBuild 15.0+ (bundled with Visual Studio)

## 📦 Installation
1. **Clone the repository:**
   ```bash
   git clone <your-repository-url>
   cd <repository-root>/Day1/HelloWorld
   ```

2. **Open the solution in Visual Studio:**
   ```bash
   start HelloWorld.sln
   ```
   *Visual Studio will automatically detect the target framework, configure build paths, and prepare the project environment. No NuGet package restoration is required.*

3. **Alternative: Command-Line Setup**
   If you prefer working outside the IDE, ensure `msbuild` is available in your system `PATH` (via Developer Command Prompt for VS):
   ```bash
   msbuild HelloWorld.sln /t:Restore /p:Configuration=Debug
   ```

## 🚀 Usage
### ▶️ Via Visual Studio
1. Open `HelloWorld.sln`
2. Press `F5` to run with debugging, or `Ctrl + F5` to run without debugging.
3. The console window will appear and display:
   ```
   Hello, World!
   ```

### 💻 Via Command Line
Build and execute the compiled binary directly:
```bash
# Build the project (Release configuration)
msbuild HelloWorld.sln /p:Configuration=Release /t:Build

# Run the executable
.\HelloWorld\bin\Release\HelloWorld.exe
```

### 📝 Expected Behavior
- The application launches, initializes the .NET Framework runtime, and executes `Program.Main()`.
- `Console.WriteLine()` writes the string to `stdout`.
- The process terminates gracefully with exit code `0`.

## 📁 Project Structure
```
Day1/HelloWorld/
├── HelloWorld.sln                 # Visual Studio solution file
├── HelloWorld/
│   ├── HelloWorld.csproj          # MSBuild project configuration (.NET Framework 4.7.2)
│   ├── App.config                 # Application runtime configuration
│   ├── Program.cs                 # Entry point & console logic
│   └── Properties/
│       └── AssemblyInfo.cs        # Assembly metadata, versioning & COM settings
├── .gitattributes                 # Line-ending normalization rules
└── .gitignore                     # Standard Visual Studio & .NET ignore patterns
```

## 📄 License
This project is provided as-is for educational and reference purposes. Modify and distribute freely according to your organization's standards.