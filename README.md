# W10-SampleSplitView
Copyright: Tuan Tran Van
Windows 10 SplitView Sample with MVVMLight and utilities codes

# Introduction

This sample provide you all the code needed when starting a new project that use splitview and MVVM. It uses MVVMLight to implement MVVM, Json.NET to save app settings.

# Building the Sample

Unzip the downloaded file and double click ".sln" file. Or you can open Visual Studio > File > Open Project > choose the .sln file

# Description

## Sample provide you

- Ready to use MVVMLight ViewModel and Model
- A Start page that already have SplitView control
- SplitView have Hamburger Button, list of function with Icon and name, bind to a ViewModel
- Sample page that represent a real page in your app
- Setting page
- Storage helper: load and save file to local storage
- Settings helper: Get or Set settings for your app
- Every logos and images in assets folder
- Modified App.xaml to add 2 colors as resource to use in the whole app
- A lot of convenient codes
- Every class and method have it's own description. Be sure to read them before use

## Settings Helper Explaination

From the begining of Windows Store App development, when developer want to set a setting, or get a setting, they use an API that provided by Windows Store App SDK, which use a plaintext as setting key to retrive it later.

This class help you avoid using plaintext for setting key. You can use KeyName1 to represent the text "YourSettingKey1". This will reduce the bugs and errors because of mistyping plaintext setting key

```C#
public sealed class SettingKey 
{ 
     public static readonly SettingKey KeyName1 = new SettingKey("YourSettingKey1"); 
     public static readonly SettingKey KeyName2 = new SettingKey("YourSettingKey2"); 
     public static readonly SettingKey KeyName3 = new SettingKey("YourSettingKey3"); 
     public static readonly SettingKey KeyName4 = new SettingKey("YourSettingKey4"); 
 
     private SettingKey(string value) 
     { 
          Value = value; 
     } 
     public string Value { get; } 
}
```
