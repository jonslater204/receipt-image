## Image to ESC/POS Converter

### Convert your image files to send them to receipt printers as ESC/POS data.

I needed a way to include images in receipts on an Epson printer. But with the
Epson bundled software it takes a little bit of time to go through the whole
procedure, time that starts to add up if you are making small tweaks and
fine-tuning. There are a couple of projects out there but I couldn't get
anything running on Windows 10.

It's always nice to find a way to do things yourself though, and it turned out
to be fairly straightforward, with the browser doing all the image loading heavy
lifting. You could add a few more niceties to suit your own projects such as
specifying parameters like filenames in the URL but this was as far as I've
needed to take it.

The resulting .tlg file can be included in the string of ESC/POS commands you
send to the printer. It contains all the bytes necessary to download the image
into the first memory slot (32,32). If you need more than one image in printer
memory at one time, you can tweak values in the header variable for (33,32),
(34,32) etc.

### Quick Start Guide
1. Place your image file in the same folder as the converter
2. Set the filename variable in the converter
3. Open the converter page in a browser
4. Save the file

It should handle BMP, PNG, JPG, GIF - anything you can load in a browser. You
don't necessarily need to use 2-bit black/white images, but it's probably a good
idea so you know what to expect.