# fineuploader-server-php
Upload image in chunks in php using fineuploader - handles the image large in size and optimise the image.

## Image stored locally inside the location of files using php server side scripting
It uses fineuploader.js which can also be downloaded using the link https://fineuploader.com/ from the browser

### This has capacity to optimize the large scale images (both in resolution and sizes) and optimise to its minimum size image.
It handles the images captures from Iphone and Android phones as it has the capacity to upload the image in chunks.

- Download the copy of the zip file and upload into your local server
- Run the file fine-uploader-server-php/templates/default.html
- Upload the Image from your local device
- The files are now uploaded insides the files [fineuploader-server-php/php-traditional-server/files/]

### For the customisation of the images
```
 var uploader = new qq.FineUploader({
            debug: true,
            element: document.getElementById('fine-uploader'),
            request: {
                endpoint: "/fineuploader/php-traditional-server/endpoint.php"
            },
            deleteFile: {
                enabled: true,
                endpoint: '/fineuploader/php-traditional-server/endpoint.php'
            },
             chunking: {
            enabled: true,
            concurrent: {
                enabled: true
            },
            success: {
                endpoint: "/fineuploader/php-traditional-server/endpoint.php?done"
            }
        },
        scaling: {
        sendOriginal: false,
        sizes: [
            {name: "duplicate", maxSize: 600},
            // {name: "medium", maxSize: 300}
        ]
        },
            retry: {
               enableAuto: false
            }
        });
```
