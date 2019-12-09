# Email Development Notes

## Getting started

It helps to have a good production environment when starting out to ease the workflow and using the proper tools sets you up for success. As for IDEs, a simple text editor like [Atom](https://atom.io/) will work fine. [Litmus](litmus.com) ($99/month) is also a recommended second text-editor which helps preview a campaign over 70 platforms. You will also need a modern webkit browser like Chrome, Safari, or Opera. Litmus For working with graphics, the following are also recommended:

  - [Affinity Designer](x) ($49) + [Photo](https://affinity.serif.com/en-us/) ($49)
-   [Sketch](www.sketch.com) ($99)
-   [Adobe Creative Clous](adobe.com/creativecloud) ($52/month)
-   [Pixelmator](pixelmator.com) ($39)

Finally, a graphics compressor is recommended to size-down graphics for uploading to servers. Here are some options:

-   [TinyPNG](tinyPNG.com) ($25/year)
-   [JPEGmini](https://www.jpegmini.com/developers) ($99)

## Building Blocks

At a high level, expect that in email development you will use:

-   Embedded and inline CSS
-   Align attribute and table cells
-   Longhand CSS properties
-   Table layouts
-   CSS animations
-   Checkbox hacks
-   Chaos

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


### Tables

At its most basic level, structuring e-mail layouts centers around using the `table` property of HTML. Even then, we effectively only use three `table` elements: `<table>`, `<tr>`, and `<td>`. A simplification might look like this:

```HTML
<table>
  <tr>
    <td>Content</td>
  </tr>
</table>
```

As for attributes, MDN specifies nine which can be applied to tables:

-   align
-   bgcolor
-   border
-   cellpadding
-   cellspacing
-   width
-   frame
-   rules
-   summary

The last three (`frame`, `rules`, and `summary`) don't apply to e-mail development and can be safely ignored.

### Accessibility

Since tables are used throughout e-mail layout design, improve accessibility by adding the `role="presentation"` attribute to all `table` property declarations.

Due to email client limitations, e-mail development cannot use all of semantic HTML elements as on the Web. Still, it is important to make e-mails accessible to the widest range possible by marking up copy with the following tags: `heading` (i.e. `h1`-`h6`), `p`, and `span`.

### Padding and cellpadding

Perhaps the most useful CSS property for structuring content is `padding`. Combined with the `align` attribute, it does most of the heavy-lifting for e-mail design. The best place to add `padding` is to the table cell containing the actual content.

As a quick refresher, `padding` takes on four values corresponding to each side of the cell, written in clockwise order beginning with `top`. It looks like this:

```html
padding: top right bottom left;
```

## Misc

"If an attribute exists in HTML, use that instead of CSS"

If you are having troubles with padding, don't use it at all. Just use empty cells to create space. It's safe to use padding on `<td>` tags, but not on `p` or `div`.

Images are fickle. Include crucial aspects of email as text. Use images only to supplement text.
