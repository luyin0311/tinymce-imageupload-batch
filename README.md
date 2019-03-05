## Introduce
tinymce图片上传插件，暂不支持图片拖拽排序

## Source
源码地址：

## Installing

Using npm:

```bash
$ npm i tinymce-imageupload-batch
```
## Example

Performing a `GET` request

```js
import tinymce from "tinymce";
import "tinymce-imageupload-batch";

tinymce.init({
    selector: "#tinymceEditer",
    height: 500,
    branding: false,
    elementpath: false,
    language_url: "/static/tinymce/langs/zh_CN.js", // 具体路径视项目结构而定
    skin_url: "/static/tinymce/skins/lightgray", // 具体路径视项目结构而定
    theme_url: "/static/tinymce/themes/modern/theme.js", // 具体路径视项目结构而定
    menubar: "edit insert view format table tools",
    convert_urls: false,
    plugins: "imageupload", // 注意引入的组件时~需要去掉前面的tinymce-前缀
    toolbar: "imageupload", // 注意引入的组件时~需要去掉前面的tinymce-前缀
    autosave_interval: "20s",
    image_advtab: true,
    images_upload_batch_handler: (res) => {
        //上传方法
    },
    table_default_styles: {
        width: "100%",
        borderCollapse: "collapse"
    }
});
```