# Introduction #

Add your content here.


# Details #

Add your content here.  Format your content with:
  * Text in **bold** or _italic_
  * Headings, paragraphs, and lists
  * Automatic links to other wiki pages

```

var filename;
var filesize;
var filedata;

var upload = flash.getObjectById('fileUpload');

if (upload.isUploaded()) {
    filename = upload.getName();
    filedata = upload.getByteArray();
    filesize = filedata.length;
} else {
    document.write('please upload a file.');
}

```