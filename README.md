# AnuIC

[![CI Status](http://img.shields.io/travis/boopathy.rajkumar@gmail.com/AnuIC.svg?style=flat)](https://travis-ci.org/boopathy.rajkumar@gmail.com/AnuIC)
[![Version](https://img.shields.io/cocoapods/v/AnuIC.svg?style=flat)](http://cocoapods.org/pods/AnuIC)
[![License](https://img.shields.io/cocoapods/l/AnuIC.svg?style=flat)](http://cocoapods.org/pods/AnuIC)
[![Platform](https://img.shields.io/cocoapods/p/AnuIC.svg?style=flat)](http://cocoapods.org/pods/AnuIC)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Anu Intelligent Compression(AnuIC)

Anu Intelligent Compression is a lossy compression technique that uses JPEG Compression to shrink high resolution images to lower sizes.

We use an unique compression algorithm to iteratively compress images such that the quality of the image is not compramised visibly. With this, an image of size around MB can finally be bought to less than 50KB, with an invisible loss of quality. 

## How it works

Get original image and calculate the image size.
If image size is < 1MB, the compressed image size should be less than 50kb.
If image size is > 1MB and < 3MB, the compressed image size should be less than 100kb.
If image size is > 3MB and < 4MB, the compressed image size should be less than 150kb.
If image size is > 4MB, the compressed image size should be less than 200kb.
Do image scaling (fitting the image to desired frame size) - If scaled image size is under target size (obtained in Step 1), then return the image.
Reduce image quality with JPEG Compression until the image size reaches the target size range or the quality compression factor reaches a desirable value.
Return the image.

This compression algorithm is best suit for applications that involve massive image processing, transmitting heavy images across servers that consume heavy bandwidth. 

## Nomenclature

The word "Anu" translates to Atom (in Tamil) that forms the smallest unit particle of anything. 

## Requirements

## Installation

AnuIC is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "AnuIC"
```

## Author

boopathy.rajkumar@gmail.com

## License

AnuIC is available under the MIT license. See the LICENSE file for more info.
