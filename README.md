# Jubaer File Picker Plugin

The Jubaer File Picker Plugin is a jQuery plugin that provides an easy-to-use interface for selecting and previewing image, video and audio files. It allows users to add multiple file input fields dynamically and provides image previews for image files and video players for video files also audio players for audio files.

## Features

- Add multiple file input fields dynamically.
- Display image previews for image files.
- Load video players for video files.
- Load audio players for audio files.
- Customize placeholder images and file input fields.
- Direct upload support for files.
- Callback functions for adding/removing rows and handling errors.

## Installation

You can install the Jubaer Image Picker Plugin via npm or by downloading the source files directly.



### Direct download
You can download the source files from the GitHub repository.

## Usage
Include jQuery and the Jubaer Image Picker Plugin script files in your HTML:
HTML
```bash
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.jsdelivr.net/gh/JubaerHossain/file-picker/file-picker.min.js"></script>
```
Initialize the plugin on a container element:
html

```bash
<div id="imagePickerContainer"></div>
```
```bash
<script>
  $(document).ready(function() {
    $('#imagePickerContainer').jubaerImagePicker({
      placeholderImageTarget: 'placeholder.jpg',
      fieldName: 'file',
      allowedExt: 'jpg,jpeg,png,gif,mp4,avi,mov,mp3',
      maxFileSize: 5000, // in kilobytes
      maxCount: 5,
      directUpload: {
        status: false,
        url: '',
        additionalParam: '',
        success: function() {},
        error: function() {}
      },
      onAddRow: function(index) {},
      onRemoveRow: function(index) {},
      onRenderedPreview: function(index) {},
      onExtensionErr: function() {},
      onSizeErr: function() {}
    });
  });
</script>
```
#### Options

* **placeholderImageTarget:**  URL of the placeholder image.
* **placeholderImageWidth:** Width of the placeholder image.
* **fieldName:** Name of the file input field.
* **allowedExt:** Allowed file extensions (comma-separated).
* **maxFileSize:** Maximum file size in kilobytes.
* **maxCount:** Maximum number of file input fields.
* **directUpload:** Configuration for direct upload (optional).
* **onAddRow:** Callback function called when a new row is added.
* **onRemoveRow:** Callback function called when a row is removed.
* **onRenderedPreview:** Callback function called when a preview is rendered.
* **onExtensionErr:** Callback function called when the file extension is not allowed.
* **onSizeErr:** Callback function called when the file size exceeds the limit.






