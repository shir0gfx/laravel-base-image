# Laravel Image Uploader and Cropper

- Upload images
- Crop image
- Creates thumbnails with various configurable sizes
- Aspect ratio option

## Installation
**/composer.json**
```
{
    "require": {
        "noonic/image": "^1.0"
    }
}
```
**/config/app.php**
```
'providers' => [
    ...
    Noonic\Image\ImageServiceProvider::class,
];

'aliases' => [
    ...
    'Image'     => Noonic\Image\ImageHelperFacade::class,
];
```

**Run:**
```
php artisan vendor:publish
```

## Usage

```blade
{!! Form::open() !!}
  @include('noonic_image::_input', [
      'name' => 'photo', option
      'folder' => 'photos', 
      'data' => '', 
      'required' => true
  ])
{!! Form::close() !!}
```

## Options

- **name**: [required] [String] Name of file input
- **ratio**: [optional] [String] [4/3, 16:9, 1/1] Image ratio to crop and resize. Default: 4/3.
- **folder**: [optional] [String] Name of folder where the image will be uploaded. Default: 'default' folder
- **data**: [optional] [String] Pass image path to prefill data
- **required**: [optional] [Boolean] [true / false] To make the image required, prompts JavaScript Alert box.

## Authors

Atul Yadav - [GitHub](https://github.com/atulmy) &bull; [Twitter](https://twitter.com/atulmy)

## License

Copyright (c) 2015 Noonic Lab http://github.com/noonic

The MIT License (http://www.opensource.org/licenses/mit-license.php)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.