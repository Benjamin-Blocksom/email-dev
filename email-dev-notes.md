# Email Development Notes

## Getting started

It helps to have a good production when starting out to ease the workflow and using the property tools sets you up for success. As for IDEs, a simple text editor like [Atom](https://atom.io/) will work fine. [Litmus](litmus.com)($99/mo.) is also a recommended second text-editor which helps preview a campaign over 70 platforms. You will also need a modern webkit browser like Chrome, Safari, or Opera. Litmus For working with graphics, the following are also recommended:
* [Affinity Designer](https://affinity.serif.com/en-us/)($49) + [Photo] (https://affinity.serif.com/en-us/)($49)
* [Sketch](www.sketch.com)($99)
* [Adobe Creative Clous](adobe.com/creativecloud)($52/mo.)
* [Pixelmator](pixelmator.com)($39)

Finally, a graphics compressor is recommended to size-down graphics for uploading to servers. Here are some options:

* [TinyPNG](tinyPNG.com)($25/year)
* [JPEGmini](https://www.jpegmini.com/developers)($99)

## Building Blocks

At a high level, expect that in email development you will use:
* Embedded and inline CSS
* Align attribute and table cells
* Longhand CSS properties
* Table layouts
* CSS animations
* Checkbox hacks
* Chaos

### A basic header

```HTML
<!DOCTYPE html>
<html lang="en"
<title></title>

<meta http-equiv="Content-Type" content="text/html;
charset=utf-8" />
<meta name="viewport" content="width=device-width, initial-
scale=1">
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta http-equiv="Content-Type" content="text/html;
charset=utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta http-equiv="X-UA-Compatible" content="IE=edge" />

<style type="text/css">
/* CLIENT-SPECIFIC STYLES */
body, table, td, a { -webkit-text-size-adjust: 100%; -ms-text-
size-adjust: 100%; }
table, td { mso-table-lspace: 0pt; mso-table-rspace: 0pt; }
img { -ms-interpolation-mode: bicubic; }
/* RESET STYLES */
img { border: 0; height: auto; line-height: 100%; outline: none;
text-decoration: none; }
table { border-collapse: collapse !important; }
body { height: 100% !important; margin: 0 !important; padding: 0
!important; width: 100% !important; }
</style>
```
