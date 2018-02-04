# Quill-image-resize-module Integration
This is a simple experiment to display how to use React Quill Editor with the quill-image-resize-module library.

With React-Quill, you can save the value of the editor either as a HTML string or Delta (object).
To integrate quill-image-module, it is important to do the following to make it work.

```
import ImageResize from 'quill-image-resize-module'
Quill.register('modules/imageResize', ImageResize);
```

In webpack config file, add the plugin.
```
plugins: [
    new webpack.ProvidePlugin({
      'window.Quill': 'quill'
      }),
    ... ]
```
Also, add 'width' to Editor.formats.

Check App.js for the example.


This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).