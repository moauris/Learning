# Introduction

https://learning.oreilly.com/library/view/mastering-windows-presentation/9781838643416/2188e214-9a4a-4b2f-923f-9d9d2c7b551c.xhtml

# New Knowledge: WPF can output debug trace to a file

This has to do with the `app.config` file. We need to modify it so that it outputs instead of output window in Visual Studio, it outputs to a file.

Normally, WPF uses a `DefaultTraceListener` object much like the console app debug listener. This refers to the output window.

It can be overridden.

There are three options to choose from: Output window (default), text file, or xml file.

## How to do it

Modify the config file by adding a new tag called `<system.diagnostics>`

```xml
<?xml version="1.0" encoding="utf-8"?> 
<configuration> 
  <startup>  
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.6.1" /> 
  </startup> 
  <system.diagnostics> 
    <sources> 
      <source name="System.Windows.Data" switchName="Switch"> 
        <listeners> 
          <add name="TextListener" /> 
        </listeners> 
      </source> 
    </sources> 
    <switches> 
      <add name="Switch" value="All" /> 
    </switches> 
    <sharedListeners> 
      <add name="TextListener"  
        type="System.Diagnostics.TextWriterTraceListener"  
        initializeData="Trace.txt" /> 
    </sharedListeners> 
    <trace indentsize="4" autoflush="true"></trace> 
  </system.diagnostics> 
</configuration> 
```

