# ImageUploader
.Net Core library to upload images to the server in Restful Api's


## Setup
* Available on NuGet: https://www.nuget.org/packages/AspNetCore.ImageUploader/
* Install into your .NET Core project.

## Usage

```
  var stream = new MemoryStream(byte[] ImageArray);
  var guid = Guid.NewGuid().ToString();
  var file = $"{guid}.jpg";
  var folder = "Images";
  var response = FilesHelper.UploadImage(stream, folder, file);
  if (!response)
  {
     // Bad Request...
  }
  else
  {
     // Image Uploaded...
  }       	
```
