# jpg_payload

The algorithm of injecting the payload into the JPG image, which will keep unchanged after transformations caused by PHP functions imagecopyresized() and imagecopyresampled().

It is necessary that the size and quality of the initial image are the same as those of the processed image.

1) Upload an arbitrary image via secured files upload script
2) Save the processed image and launch:
php jpg_payload.php <jpg_name.jpg>

In case of successful injection you will get a specially crafted image, which should be uploaded again.

Since the most straightforward injection method is used, the following problems can occur:
1) After the second processing the injected data may become partially corrupted.
2) The jpg_payload.php script outputs "Something's wrong".

If this happens, try to change the payload (e.g. add some symbols at the beginning) or try another initial image.

See also:
[https://www.idontplaydarts.com/2012/06/encoding-web-shells-in-png-idat-chunks/](https://www.idontplaydarts.com/2012/06/encoding-web-shells-in-png-idat-chunks/)
