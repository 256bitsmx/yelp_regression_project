# Danielle's Delicious Delicacies, yelp_regression_project
codeacademy project
```html
<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>yelp_regression</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box 
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this 
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+ 
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for 
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  } 
  div.output_wrapper { 
    display: block;
    page-break-inside: avoid; 
  }
  div.output { 
    display: block;
    page-break-inside: avoid; 
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Project:-Yelp-Rating-Regression-Predictor">Project: Yelp Rating Regression Predictor<a class="anchor-link" href="#Project:-Yelp-Rating-Regression-Predictor">&#182;</a></h1><p>The restaurant industry is tougher than ever, with restaurant reviews blazing across the Internet from day one of a restaurant's opening. But as a lover of food, you and your friend decide to break into the industry and open up your own restaurant, Danielle's Delicious Delicacies. Since a restaurant's success is highly correlated with its reputation, you want to make sure Danielle's Delicious Delicacies has the best reviews on the most queried restaurant review site: Yelp! While you know your food will be delicious, you think there are other factors that play into a Yelp rating and will ultimately determine your business's success. With a dataset of different restaurant features and their Yelp ratings, you decide to use a Multiple Linear Regression model to investigate what factors most affect a restaurant's Yelp rating and predict the Yelp rating for your restaurant!</p>
<p>In this project we'll be working with a real dataset provided by Yelp. We have provided six files, listed below with a brief description:</p>
<ul>
<li><code>yelp_business.json</code>: establishment data regarding location and attributes for all businesses in the dataset</li>
<li><code>yelp_review.json</code>: Yelp review metadata by business</li>
<li><code>yelp_user.json</code>: user profile metadata by business</li>
<li><code>yelp_checkin.json</code>: online checkin metadata by business</li>
<li><code>yelp_tip.json</code>: tip metadata by business</li>
<li><code>yelp_photo.json</code>: photo metadata by business</li>
</ul>
<p>For a more detailed explanation of the features in each <code>.json</code> file, see the accompanying <a href="https://docs.google.com/document/d/1V6FjJpKspVBOOBs4E7fBfp_yzHn0--XJkC2uUtWuRgM/edit">explanatory feature document</a>.</p>
<p>Let's get started by exploring the data in each of these files to see what we are working with.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Load-the-Data-and-Take-a-Peek">Load the Data and Take a Peek<a class="anchor-link" href="#Load-the-Data-and-Take-a-Peek">&#182;</a></h2><p>To get a better understanding of the dataset we can use Pandas to explore the data in DataFrame form. In the code block below we have imported Pandas for you. The <code>read_json()</code> method reads data from a json file into a DataFrame, as shown below:</p>
<div class="highlight"><pre><span></span><span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;file_name.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>
<p>Load the data from each of the json files with the following naming conventions:</p>
<ul>
<li><code>yelp_business.json</code> into a DataFrame named <code>businesses</code></li>
<li><code>yelp_review.json</code> into a DataFrame named <code>reviews</code></li>
<li><code>yelp_user.json</code> into a DataFrame named <code>users</code></li>
<li><code>yelp_checkin.json</code> into a DataFrame named <code>checkins</code></li>
<li><code>yelp_tip.json</code> into a DataFrame named <code>tips</code></li>
<li><code>yelp_photo.json</code> into a DataFrame named <code>photos</code></li>
</ul>
<p>Importing that data could take 10 to 20 seconds to run depending on your computer, but don't worry, once it's loaded in you're ready to go!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[284]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="n">businesses</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;yelp_business.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">reviews</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;yelp_review.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">users</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;yelp_user.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">checkins</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;yelp_checkin.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">tips</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;yelp_tip.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">photos</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_json</span><span class="p">(</span><span class="s1">&#39;yelp_photo.json&#39;</span><span class="p">,</span> <span class="n">lines</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>In order to more clearly see the information in our DataFrame, we can adjust the number of columns shown (<code>max_columns</code>) and the number of characters shown in a column (<code>max_colwidth</code>) with the below code:</p>
<div class="highlight"><pre><span></span><span class="n">pd</span><span class="o">.</span><span class="n">options</span><span class="o">.</span><span class="n">display</span><span class="o">.</span><span class="n">max_columns</span> <span class="o">=</span> <span class="n">number_of_columns_to_display</span>
<span class="n">pd</span><span class="o">.</span><span class="n">options</span><span class="o">.</span><span class="n">display</span><span class="o">.</span><span class="n">max_colwidth</span> <span class="o">=</span> <span class="n">number_of_characters_to_display</span>
</pre></div>
<p>Set <code>max_columns</code> to <code>60</code> and <code>max_colwidth</code> to <code>500</code>. We are working with some BIG data here!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[285]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pd</span><span class="o">.</span><span class="n">options</span><span class="o">.</span><span class="n">display</span><span class="o">.</span><span class="n">max_columns</span> <span class="o">=</span> <span class="mi">60</span>
<span class="n">pd</span><span class="o">.</span><span class="n">options</span><span class="o">.</span><span class="n">display</span><span class="o">.</span><span class="n">max_colwidth</span> <span class="o">=</span> <span class="mi">500</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Inspect the first five rows of each DataFrame using the <code>.head()</code> method to get an overview of the data (make sure to check each DataFrame in a separate cell in order to view it properly).</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[286]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">businesses</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[286]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>address</th>
      <th>alcohol?</th>
      <th>attributes</th>
      <th>business_id</th>
      <th>categories</th>
      <th>city</th>
      <th>good_for_kids</th>
      <th>has_bike_parking</th>
      <th>has_wifi</th>
      <th>hours</th>
      <th>is_open</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>name</th>
      <th>neighborhood</th>
      <th>postal_code</th>
      <th>price_range</th>
      <th>review_count</th>
      <th>stars</th>
      <th>state</th>
      <th>take_reservations</th>
      <th>takes_credit_cards</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1314 44 Avenue NE</td>
      <td>0</td>
      <td>{'BikeParking': 'False', 'BusinessAcceptsCreditCards': 'True', 'BusinessParking': '{'garage': False, 'street': True, 'validated': False, 'lot': False, 'valet': False}', 'GoodForKids': 'True', 'HasTV': 'True', 'NoiseLevel': 'average', 'OutdoorSeating': 'False', 'RestaurantsAttire': 'casual', 'RestaurantsDelivery': 'False', 'RestaurantsGoodForGroups': 'True', 'RestaurantsPriceRange2': '2', 'RestaurantsReservations': 'True', 'RestaurantsTakeOut': 'True'}</td>
      <td>Apn5Q_b6Nz61Tq4XzPdf9A</td>
      <td>Tours, Breweries, Pizza, Restaurants, Food, Hotels &amp; Travel</td>
      <td>Calgary</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>{'Monday': '8:30-17:0', 'Tuesday': '11:0-21:0', 'Wednesday': '11:0-21:0', 'Thursday': '11:0-21:0', 'Friday': '11:0-21:0', 'Saturday': '11:0-21:0'}</td>
      <td>1</td>
      <td>51.091813</td>
      <td>-114.031675</td>
      <td>Minhas Micro Brewery</td>
      <td></td>
      <td>T2E 6L6</td>
      <td>2</td>
      <td>24</td>
      <td>4.0</td>
      <td>AB</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td></td>
      <td>0</td>
      <td>{'Alcohol': 'none', 'BikeParking': 'False', 'BusinessAcceptsCreditCards': 'True', 'BusinessParking': '{'garage': False, 'street': True, 'validated': False, 'lot': True, 'valet': False}', 'Caters': 'True', 'DogsAllowed': 'True', 'DriveThru': 'False', 'GoodForKids': 'True', 'GoodForMeal': '{'dessert': False, 'latenight': False, 'lunch': False, 'dinner': False, 'breakfast': False, 'brunch': False}', 'HasTV': 'False', 'OutdoorSeating': 'True', 'RestaurantsAttire': 'casual', 'RestaurantsDelivery'...</td>
      <td>AjEbIBw6ZFfln7ePHha9PA</td>
      <td>Chicken Wings, Burgers, Caterers, Street Vendors, Barbeque, Food Trucks, Food, Restaurants, Event Planning &amp; Services</td>
      <td>Henderson</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>{'Friday': '17:0-23:0', 'Saturday': '17:0-23:0', 'Sunday': '17:0-23:0'}</td>
      <td>0</td>
      <td>35.960734</td>
      <td>-114.939821</td>
      <td>CK'S BBQ &amp; Catering</td>
      <td></td>
      <td>89002</td>
      <td>2</td>
      <td>3</td>
      <td>4.5</td>
      <td>NV</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1335 rue Beaubien E</td>
      <td>1</td>
      <td>{'Alcohol': 'beer_and_wine', 'Ambience': '{'romantic': False, 'intimate': False, 'classy': False, 'hipster': False, 'touristy': False, 'trendy': False, 'upscale': False, 'casual': False}', 'BikeParking': 'True', 'BusinessAcceptsCreditCards': 'False', 'BusinessParking': '{'garage': False, 'street': False, 'validated': False, 'lot': False, 'valet': False}', 'Caters': 'False', 'GoodForKids': 'True', 'GoodForMeal': '{'dessert': False, 'latenight': False, 'lunch': False, 'dinner': False, 'breakfa...</td>
      <td>O8S5hYJ1SMc8fA4QBtVujA</td>
      <td>Breakfast &amp; Brunch, Restaurants, French, Sandwiches, Cafes</td>
      <td>Montréal</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>{'Monday': '10:0-22:0', 'Tuesday': '10:0-22:0', 'Wednesday': '10:0-22:0', 'Thursday': '10:0-22:0', 'Friday': '10:0-22:0', 'Saturday': '10:0-22:0', 'Sunday': '10:0-22:0'}</td>
      <td>0</td>
      <td>45.540503</td>
      <td>-73.599300</td>
      <td>La Bastringue</td>
      <td>Rosemont-La Petite-Patrie</td>
      <td>H2G 1K7</td>
      <td>2</td>
      <td>5</td>
      <td>4.0</td>
      <td>QC</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>211 W Monroe St</td>
      <td>0</td>
      <td>None</td>
      <td>bFzdJJ3wp3PZssNEsyU23g</td>
      <td>Insurance, Financial Services</td>
      <td>Phoenix</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>None</td>
      <td>1</td>
      <td>33.449999</td>
      <td>-112.076979</td>
      <td>Geico Insurance</td>
      <td></td>
      <td>85003</td>
      <td>0</td>
      <td>8</td>
      <td>1.5</td>
      <td>AZ</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2005 Alyth Place SE</td>
      <td>0</td>
      <td>{'BusinessAcceptsCreditCards': 'True'}</td>
      <td>8USyCYqpScwiNEb58Bt6CA</td>
      <td>Home &amp; Garden, Nurseries &amp; Gardening, Shopping, Local Services, Automotive, Electronics Repair</td>
      <td>Calgary</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>{'Monday': '8:0-17:0', 'Tuesday': '8:0-17:0', 'Wednesday': '8:0-17:0', 'Thursday': '8:0-17:0', 'Friday': '8:0-17:0'}</td>
      <td>1</td>
      <td>51.035591</td>
      <td>-114.027366</td>
      <td>Action Engine</td>
      <td></td>
      <td>T2H 0N5</td>
      <td>0</td>
      <td>4</td>
      <td>2.0</td>
      <td>AB</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[287]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">reviews</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[287]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>business_id</th>
      <th>average_review_age</th>
      <th>average_review_length</th>
      <th>average_review_sentiment</th>
      <th>number_funny_votes</th>
      <th>number_cool_votes</th>
      <th>number_useful_votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>--1UhMGODdWsrMastO9DZw</td>
      <td>524.458333</td>
      <td>466.208333</td>
      <td>0.808638</td>
      <td>1</td>
      <td>16</td>
      <td>15</td>
    </tr>
    <tr>
      <th>1</th>
      <td>--6MefnULPED_I942VcFNA</td>
      <td>1199.589744</td>
      <td>785.205128</td>
      <td>0.669126</td>
      <td>27</td>
      <td>32</td>
      <td>53</td>
    </tr>
    <tr>
      <th>2</th>
      <td>--7zmmkVg-IMGaXbuVd0SQ</td>
      <td>717.851852</td>
      <td>536.592593</td>
      <td>0.820837</td>
      <td>29</td>
      <td>52</td>
      <td>81</td>
    </tr>
    <tr>
      <th>3</th>
      <td>--8LPVSo5i0Oo61X01sV9A</td>
      <td>751.750000</td>
      <td>478.250000</td>
      <td>0.170925</td>
      <td>0</td>
      <td>0</td>
      <td>9</td>
    </tr>
    <tr>
      <th>4</th>
      <td>--9QQLMTbFzLJ_oT-ON3Xw</td>
      <td>978.727273</td>
      <td>436.181818</td>
      <td>0.562264</td>
      <td>3</td>
      <td>4</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[288]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">users</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[288]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>business_id</th>
      <th>average_number_friends</th>
      <th>average_days_on_yelp</th>
      <th>average_number_fans</th>
      <th>average_review_count</th>
      <th>average_number_years_elite</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>--1UhMGODdWsrMastO9DZw</td>
      <td>18.791667</td>
      <td>1789.750000</td>
      <td>1.833333</td>
      <td>57.541667</td>
      <td>0.833333</td>
    </tr>
    <tr>
      <th>1</th>
      <td>--6MefnULPED_I942VcFNA</td>
      <td>214.564103</td>
      <td>2039.948718</td>
      <td>49.256410</td>
      <td>332.743590</td>
      <td>1.769231</td>
    </tr>
    <tr>
      <th>2</th>
      <td>--7zmmkVg-IMGaXbuVd0SQ</td>
      <td>126.185185</td>
      <td>1992.796296</td>
      <td>19.222222</td>
      <td>208.962963</td>
      <td>1.814815</td>
    </tr>
    <tr>
      <th>3</th>
      <td>--8LPVSo5i0Oo61X01sV9A</td>
      <td>25.250000</td>
      <td>2095.750000</td>
      <td>0.500000</td>
      <td>7.500000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>--9QQLMTbFzLJ_oT-ON3Xw</td>
      <td>52.454545</td>
      <td>1804.636364</td>
      <td>1.000000</td>
      <td>34.636364</td>
      <td>0.090909</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[289]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">checkins</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[289]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>business_id</th>
      <th>time</th>
      <th>weekday_checkins</th>
      <th>weekend_checkins</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7KPBkxAOEtb3QeIL9PEErg</td>
      <td>{'Fri-0': 2, 'Sat-0': 1, 'Sun-0': 1, 'Wed-0': 2, 'Fri-1': 1, 'Sat-1': 3, 'Thu-1': 1, 'Wed-1': 1, 'Sat-2': 1, 'Sun-2': 2, 'Thu-2': 1, 'Wed-2': 1, 'Fri-3': 1, 'Sun-3': 3, 'Mon-4': 1, 'Thu-4': 1, 'Tue-4': 2, 'Wed-4': 2, 'Sun-6': 1, 'Wed-6': 1, 'Thu-7': 1, 'Fri-10': 3, 'Mon-10': 1, 'Sat-10': 3, 'Sun-10': 3, 'Tue-10': 2, 'Mon-11': 1, 'Thu-11': 1, 'Wed-11': 2, 'Mon-12': 1, 'Sat-12': 1, 'Tue-12': 1, 'Sat-13': 3, 'Thu-13': 1, 'Tue-13': 2, 'Wed-13': 3, 'Fri-14': 2, 'Mon-14': 1, 'Sat-14': 1, 'Sun-14':...</td>
      <td>76</td>
      <td>75</td>
    </tr>
    <tr>
      <th>1</th>
      <td>kREVIrSBbtqBhIYkTccQUg</td>
      <td>{'Mon-13': 1, 'Thu-13': 1, 'Sat-16': 1, 'Wed-17': 1, 'Sun-19': 1, 'Thu-20': 1, 'Sat-21': 1}</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tJRDll5yqpZwehenzE2cSg</td>
      <td>{'Thu-0': 1, 'Mon-1': 1, 'Mon-12': 1, 'Sat-16': 1, 'Sun-22': 1, 'Fri-23': 1}</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tZccfdl6JNw-j5BKnCTIQQ</td>
      <td>{'Sun-14': 1, 'Fri-18': 1, 'Mon-20': 1}</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>r1p7RAMzCV_6NPF0dNoR3g</td>
      <td>{'Sat-3': 1, 'Sun-18': 1, 'Sat-21': 1, 'Sat-23': 1, 'Thu-23': 1}</td>
      <td>1</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[290]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">tips</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[290]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>business_id</th>
      <th>average_tip_length</th>
      <th>number_tips</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>--1UhMGODdWsrMastO9DZw</td>
      <td>79.000000</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>--6MefnULPED_I942VcFNA</td>
      <td>49.857143</td>
      <td>14</td>
    </tr>
    <tr>
      <th>2</th>
      <td>--7zmmkVg-IMGaXbuVd0SQ</td>
      <td>52.500000</td>
      <td>10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>--9QQLMTbFzLJ_oT-ON3Xw</td>
      <td>136.500000</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>--9e1ONYQuAa-CB_Rrw7Tw</td>
      <td>68.064935</td>
      <td>154</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[291]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">photos</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[291]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>business_id</th>
      <th>average_caption_length</th>
      <th>number_pics</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>--1UhMGODdWsrMastO9DZw</td>
      <td>0.000000</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>--6MefnULPED_I942VcFNA</td>
      <td>67.500000</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>--9e1ONYQuAa-CB_Rrw7Tw</td>
      <td>30.426471</td>
      <td>136</td>
    </tr>
    <tr>
      <th>3</th>
      <td>--DaPTJW3-tB1vP-PfdTEg</td>
      <td>0.000000</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>--FBCX-N37CMYDfs790Bnw</td>
      <td>5.500000</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>How many different businesses are in the dataset? What are the different features in the review DataFrame?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[292]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">businesses</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[292]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(188593, 22)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>yelp_review.json: contains Yelp review metadata by business
average_review_age: float, average age of reviews, in days, on business' Yelp page
average_review_length: float, average length of review, in characters, on business' Yelp page
average_review_sentiment: float, from -1 to 1, representing the average sentiment of reviews on business' Yelp page, with -1 being most negative, 0 being neutral, and 1 being positive
business_id: string, 22 character unique string business id
number_cool_votes: integer, total number of cool votes given to reviews on business' Yelp page
number_funny_votes: integer, total number of funny votes given to reviews on business' Yelp page
number_useful_votes: integer, total number of useful votes given to reviews on business' Yelp page</p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What is the range of values for the features in the user DataFrame?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[293]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">users</span><span class="o">.</span><span class="n">shape</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[293]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>(188593, 6)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What is the Yelp rating, or <code>stars</code>, of the establishment with <code>business_id</code> = <code>5EvUIR4IzCWUOm0PsUZXjA</code>. Use Pandas boolean indexing to find the Yelp rating, using the syntax below:</p>
<div class="highlight"><pre><span></span><span class="n">df</span><span class="p">[</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;column_we_know&#39;</span><span class="p">]</span> <span class="o">==</span> <span class="p">[</span><span class="s1">&#39;value_we_know&#39;</span><span class="p">][</span><span class="s1">&#39;column_we_want&#39;</span><span class="p">]</span>
</pre></div>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[294]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">businesses</span><span class="p">[(</span><span class="n">businesses</span><span class="o">.</span><span class="n">business_id</span> <span class="o">==</span> <span class="s1">&#39;5EvUIR4IzCWUOm0PsUZXjA&#39;</span><span class="p">)]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[294]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>address</th>
      <th>alcohol?</th>
      <th>attributes</th>
      <th>business_id</th>
      <th>categories</th>
      <th>city</th>
      <th>good_for_kids</th>
      <th>has_bike_parking</th>
      <th>has_wifi</th>
      <th>hours</th>
      <th>is_open</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>name</th>
      <th>neighborhood</th>
      <th>postal_code</th>
      <th>price_range</th>
      <th>review_count</th>
      <th>stars</th>
      <th>state</th>
      <th>take_reservations</th>
      <th>takes_credit_cards</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>30781</th>
      <td>1194 Bloor Street W</td>
      <td>0</td>
      <td>{'RestaurantsPriceRange2': '1'}</td>
      <td>5EvUIR4IzCWUOm0PsUZXjA</td>
      <td>Restaurants, Burmese</td>
      <td>Toronto</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>None</td>
      <td>0</td>
      <td>43.659419</td>
      <td>-79.438004</td>
      <td>Motherhome Myanmar Cuisine</td>
      <td>Bloordale Village</td>
      <td>M6H 1N2</td>
      <td>1</td>
      <td>4</td>
      <td>3.0</td>
      <td>ON</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[295]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">businesses</span><span class="p">[(</span><span class="n">businesses</span><span class="o">.</span><span class="n">business_id</span> <span class="o">==</span> <span class="s1">&#39;5EvUIR4IzCWUOm0PsUZXjA&#39;</span><span class="p">)][</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[295]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>30781    3.0
Name: stars, dtype: float64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>What feature, or column, do the DataFrames have in common? <strong>business_id</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Merge-the-Data">Merge the Data<a class="anchor-link" href="#Merge-the-Data">&#182;</a></h2><p>Since we are working with data from several files, we need to combine the data into a single DataFrame that allows us to analyze the different features with respect to our target variable, the Yelp rating. We can do this by merging the multiple DataFrames we have together, joining them on the columns they have in common. In our case, this unique identifying column is the <code>business_id</code>. We can merge two DataFrames together with the following syntax:</p>
<div class="highlight"><pre><span></span><span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">left</span><span class="p">,</span> <span class="n">right</span><span class="p">,</span> <span class="n">how</span><span class="o">=</span><span class="s1">&#39;inner/outer/left/right&#39;</span><span class="p">,</span> <span class="n">on</span><span class="o">=</span><span class="s1">&#39;column(s)_to_merge_on&#39;</span><span class="p">)</span>
</pre></div>
<ul>
<li><code>left</code> is the DataFrame on the left side of our merge</li>
<li><code>right</code> is the DataFrame on the right side of our merge</li>
<li><code>how</code> describes the style of merge we want to complete (similar to inner/outer/left/right joins in SQL)</li>
<li><code>on</code> is the column or columns to perform the merge on (the column connecting the two tables)</li>
</ul>
<p>Given our six DataFrames, we will need to perform 5 merges to combine all the data into one DataFrame. In the cell below we merged the business table and the review table into a new DataFrame, <code>df</code>, for you. After the merge we've added all the rows from <code>businesses</code> and <code>reviews</code> together, but kept the same total number of rows! Run the cell to perform the merge and confirm the number of rows in <code>df</code>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[296]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">businesses</span><span class="p">,</span> <span class="n">reviews</span><span class="p">,</span> <span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">on</span><span class="o">=</span><span class="s1">&#39;business_id&#39;</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">df</span><span class="p">))</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>188593
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Merge each of the other 4 DataFrames into our new DataFrame <code>df</code> to combine all the data together. Make sure that <code>df</code> is the left DataFrame in each merge and <code>how=left</code> since not every DataFrame includes every business in the dataset (this way we won't lose any data during the merges). Once combined, print out the columns of <code>df</code>. What features are in this new DataFrame?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[297]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">users</span><span class="p">,</span> <span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">on</span><span class="o">=</span><span class="s1">&#39;business_id&#39;</span><span class="p">)</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">checkins</span><span class="p">,</span> <span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">on</span><span class="o">=</span><span class="s1">&#39;business_id&#39;</span><span class="p">)</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">tips</span><span class="p">,</span> <span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">on</span><span class="o">=</span><span class="s1">&#39;business_id&#39;</span><span class="p">)</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">merge</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">photos</span><span class="p">,</span> <span class="n">how</span><span class="o">=</span><span class="s1">&#39;left&#39;</span><span class="p">,</span> <span class="n">on</span><span class="o">=</span><span class="s1">&#39;business_id&#39;</span><span class="p">)</span>

<span class="n">df</span><span class="o">.</span><span class="n">columns</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[297]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index([&#39;address&#39;, &#39;alcohol?&#39;, &#39;attributes&#39;, &#39;business_id&#39;, &#39;categories&#39;,
       &#39;city&#39;, &#39;good_for_kids&#39;, &#39;has_bike_parking&#39;, &#39;has_wifi&#39;, &#39;hours&#39;,
       &#39;is_open&#39;, &#39;latitude&#39;, &#39;longitude&#39;, &#39;name&#39;, &#39;neighborhood&#39;,
       &#39;postal_code&#39;, &#39;price_range&#39;, &#39;review_count&#39;, &#39;stars&#39;, &#39;state&#39;,
       &#39;take_reservations&#39;, &#39;takes_credit_cards&#39;, &#39;average_review_age&#39;,
       &#39;average_review_length&#39;, &#39;average_review_sentiment&#39;,
       &#39;number_funny_votes&#39;, &#39;number_cool_votes&#39;, &#39;number_useful_votes&#39;,
       &#39;average_number_friends&#39;, &#39;average_days_on_yelp&#39;, &#39;average_number_fans&#39;,
       &#39;average_review_count&#39;, &#39;average_number_years_elite&#39;, &#39;time&#39;,
       &#39;weekday_checkins&#39;, &#39;weekend_checkins&#39;, &#39;average_tip_length&#39;,
       &#39;number_tips&#39;, &#39;average_caption_length&#39;, &#39;number_pics&#39;],
      dtype=&#39;object&#39;)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Clean-the-Data">Clean the Data<a class="anchor-link" href="#Clean-the-Data">&#182;</a></h2><p>We are getting really close to the fun analysis part! We just have to clean our data a bit so we can focus on the features that might have predictive power for determining an establishment's Yelp rating.</p>
<p>In a Linear Regression model, our features will ideally be continuous variables that have an affect on our dependent variable, the Yelp rating. For this project with will also be working with some features that are binary, on the scale [0,1]. With this information, we can remove any columns in the dataset that are not continuous or binary, and that we do not want to make predictions on. The cell below contains a list of these unnecessary features. Drop them from <code>df</code> with Pandas' drop syntax, provided below:</p>
<div class="highlight"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">list_of_features_to_remove</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>
<ul>
<li><code>list_of_features_to_remove</code> is, you guessed it, the list of features we want to remove!</li>
<li><code>axis=1</code> lets Pandas know we want to drop columns, not rows, from our DataFrame (axis=0 is used for computations along rows!) </li>
<li><code>inplace=True</code> lets us drop the columns right here in our DataFrame, instead of returning a new DataFrame that we could store in a new variable</li>
</ul>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[298]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">features_to_remove</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;address&#39;</span><span class="p">,</span><span class="s1">&#39;attributes&#39;</span><span class="p">,</span><span class="s1">&#39;business_id&#39;</span><span class="p">,</span><span class="s1">&#39;categories&#39;</span><span class="p">,</span><span class="s1">&#39;city&#39;</span><span class="p">,</span><span class="s1">&#39;hours&#39;</span><span class="p">,</span><span class="s1">&#39;is_open&#39;</span><span class="p">,</span><span class="s1">&#39;latitude&#39;</span><span class="p">,</span><span class="s1">&#39;longitude&#39;</span><span class="p">,</span><span class="s1">&#39;name&#39;</span><span class="p">,</span><span class="s1">&#39;neighborhood&#39;</span><span class="p">,</span><span class="s1">&#39;postal_code&#39;</span><span class="p">,</span><span class="s1">&#39;state&#39;</span><span class="p">,</span><span class="s1">&#39;time&#39;</span><span class="p">]</span>
<span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">features_to_remove</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">columns</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[298]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>Index([&#39;alcohol?&#39;, &#39;good_for_kids&#39;, &#39;has_bike_parking&#39;, &#39;has_wifi&#39;,
       &#39;price_range&#39;, &#39;review_count&#39;, &#39;stars&#39;, &#39;take_reservations&#39;,
       &#39;takes_credit_cards&#39;, &#39;average_review_age&#39;, &#39;average_review_length&#39;,
       &#39;average_review_sentiment&#39;, &#39;number_funny_votes&#39;, &#39;number_cool_votes&#39;,
       &#39;number_useful_votes&#39;, &#39;average_number_friends&#39;, &#39;average_days_on_yelp&#39;,
       &#39;average_number_fans&#39;, &#39;average_review_count&#39;,
       &#39;average_number_years_elite&#39;, &#39;weekday_checkins&#39;, &#39;weekend_checkins&#39;,
       &#39;average_tip_length&#39;, &#39;number_tips&#39;, &#39;average_caption_length&#39;,
       &#39;number_pics&#39;],
      dtype=&#39;object&#39;)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Now we just have to check our data to make sure we don't have any missing values, or <code>NaN</code>s, which will prevent the Linear Regression model from running correctly. To do this we can use the statement <code>df.isna().any()</code>. This will check all of our columns and return <code>True</code> if there are any missing values or <code>NaN</code>s, or <code>False</code> if there are no missing values. Check if <code>df</code> is missing any values.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[299]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">isna</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[299]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>alcohol?                      False
good_for_kids                 False
has_bike_parking              False
has_wifi                      False
price_range                   False
review_count                  False
stars                         False
take_reservations             False
takes_credit_cards            False
average_review_age            False
average_review_length         False
average_review_sentiment      False
number_funny_votes            False
number_cool_votes             False
number_useful_votes           False
average_number_friends        False
average_days_on_yelp          False
average_number_fans           False
average_review_count          False
average_number_years_elite    False
weekday_checkins               True
weekend_checkins               True
average_tip_length             True
number_tips                    True
average_caption_length         True
number_pics                    True
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>As you can see, there are a few columns with missing values. Since our dataset has no information recorded for some businesses in these columns, we will assume the Yelp pages did not display these features. For example, if there is a <code>NaN</code> value for <code>number_pics</code>, it means that the associated business did not have any pictures posted on its Yelp page. Thus we can replace all of our <code>NaN</code>s with <code>0</code>s. To do this we can use the <code>.fillna()</code> method, which takes a dictionary as shown below:</p>
<div class="highlight"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">fillna</span><span class="p">({</span><span class="s1">&#39;column_1&#39;</span><span class="p">:</span><span class="n">val_to_replace_na</span><span class="p">,</span>
           <span class="s1">&#39;column_2&#39;</span><span class="p">:</span><span class="n">val_to_replace_na</span><span class="p">,</span>
           <span class="s1">&#39;column_3&#39;</span><span class="p">:</span><span class="n">val_to_replace_na</span><span class="p">},</span>
          <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>
<ul>
<li><code>column_1</code>, <code>column_2</code>, and <code>column_3</code> are the columns with missing values that we want to fill. We can include as many columns as we like in the dictionary that is passed to <code>.fill_na()</code></li>
<li><code>val_to_replace_na</code> is the value that will replace the missing values, or <code>NaN</code>s</li>
<li><code>inplace=True</code> since we want to perform our changes in place and not return a new DataFrame</li>
</ul>
<p>Fill the missing values in <code>df</code> with <code>0</code>. Afterwards, confirm the missing values have been filled with <code>df.isna().any()</code>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[300]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span>
    <span class="p">{</span><span class="s1">&#39;number_pics&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
    <span class="s1">&#39;weekday_checkins&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
    <span class="s1">&#39;weekend_checkins&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
    <span class="s1">&#39;average_tip_length&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
    <span class="s1">&#39;average_caption_length&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
    <span class="s1">&#39;number_pics&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
     <span class="s1">&#39;number_tips&#39;</span><span class="p">:</span><span class="mi">0</span><span class="p">,</span>
    <span class="p">},</span>
    <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span>
<span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">isna</span><span class="p">()</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[300]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>alcohol?                      False
good_for_kids                 False
has_bike_parking              False
has_wifi                      False
price_range                   False
review_count                  False
stars                         False
take_reservations             False
takes_credit_cards            False
average_review_age            False
average_review_length         False
average_review_sentiment      False
number_funny_votes            False
number_cool_votes             False
number_useful_votes           False
average_number_friends        False
average_days_on_yelp          False
average_number_fans           False
average_review_count          False
average_number_years_elite    False
weekday_checkins              False
weekend_checkins              False
average_tip_length            False
number_tips                   False
average_caption_length        False
number_pics                   False
dtype: bool</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Exploratory-Analysis">Exploratory Analysis<a class="anchor-link" href="#Exploratory-Analysis">&#182;</a></h2><p>Now that our data is all together, let's investigate some of the different features to see what might correlate most with our dependent variable, the Yelp rating (called <code>stars</code> in our DataFrame). The features with the best correlations could prove to be the most helpful for our Linear Regression model! Pandas DataFrames have a really helpful method, <code>.corr()</code>, that allows us to see the correlation coefficients for each pair of our different features. Remember, a correlation of <code>0</code> indicates that two features have no linear relationship, a correlation coefficient of <code>1</code> indicates two features have a perfect positive linear relationship, and a correlation coefficient of <code>-1</code> indicates two features have a perfect negative linear relationship. Call <code>.corr()</code> on <code>df</code>. You'll see that <code>number_funny_votes</code> has a correlation coefficient of <code>0.001320</code> with respect to <code>stars</code>, our Yelp rating. This is a very weak correlation. What features best correlate, both positively and negatively, with Yelp rating?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[301]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">corr</span><span class="p">()[</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">sort_values</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[301]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>average_review_length        -0.277081
average_review_age           -0.125645
average_review_count         -0.066572
average_number_years_elite   -0.064419
average_tip_length           -0.052899
price_range                  -0.052565
alcohol?                     -0.043332
has_wifi                     -0.039857
average_days_on_yelp         -0.038061
average_number_fans          -0.031141
good_for_kids                -0.030382
take_reservations            -0.024486
average_number_friends       -0.007629
number_useful_votes          -0.000066
average_caption_length        0.000040
number_funny_votes            0.001320
number_pics                   0.001727
weekday_checkins              0.004130
weekend_checkins              0.007863
number_tips                   0.014038
review_count                  0.032413
takes_credit_cards            0.037748
number_cool_votes             0.043375
has_bike_parking              0.068084
average_review_sentiment      0.782187
stars                         1.000000
Name: stars, dtype: float64</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>To further visualize these relationships, we can plot certain features against our dependent variable, the Yelp rating. In the cell below we have provided the code to import Matplotlib. We can use Matplotlib's <code>.scatter()</code> method with the below syntax to plot what these correlations look like:</p>
<div class="highlight"><pre><span></span><span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">x_values_to_plot</span><span class="p">,</span> <span class="n">y_values_to_plot</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="n">blending_val</span><span class="p">)</span>
</pre></div>
<ul>
<li><code>x_values_to_plot</code> are the values to be plotted along the x-axis</li>
<li><code>y_values_to_plot</code> are the values to be plotted along the y-axis</li>
<li><code>alpha=blending_val</code> is the blending value, or how transparent (0) or opaque (1) a plotted point is. This will help us distinguish areas of the plot with high point densities and low point densities</li>
</ul>
<p>Plot the three features that correlate most with Yelp rating (<code>average_review_sentiment</code>, <code>average_review_length</code>, <code>average_review_age</code>) against <code>stars</code>, our Yelp rating. Then plot a lowly correlating feature, such as <code>number_funny_votes</code>, against <code>stars</code>.</p>
<blockquote><p>What is <code>average_review_sentiment</code>, you ask? <code>average_review_sentiment</code> is the average sentiment score for all reviews on a business' Yelp page. The sentiment score for a review was calculated using the sentiment analysis tool <a href="https://github.com/cjhutto/vaderSentiment">VADER</a>. VADER uses a labeled set of positive and negative words, along with codified rules of grammar, to estimate how positive or negative a statement is. Scores range from <code>-1</code>, most negative, to <code>+1</code>, most positive, with a score of <code>0</code> indicating a neutral statement. While not perfect, VADER does a good job at guessing the sentiment of text data!</p>
</blockquote>
<p>What kind of relationships do you see from the plots? Do you think these variables are good or bad features for our Yelp rating prediction model?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[302]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">matplotlib</span> <span class="kn">import</span> <span class="n">pyplot</span> <span class="k">as</span> <span class="n">plt</span>

<span class="c1"># plot average_review_sentiment against stars here</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;average_review_sentiment&#39;</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">X</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.01</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[302]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x3c34cd970&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[303]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># plot average_review_length against stars here</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;average_review_length&#39;</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">X</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.01</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[303]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x3d2509940&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[304]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># plot average_review_age against stars here</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;average_review_age&#39;</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">X</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.01</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[304]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x2b8373fa0&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[305]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># plot number_funny_votes against stars here</span>
<span class="n">X</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;number_funny_votes&#39;</span><span class="p">]</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">X</span><span class="p">,</span><span class="n">y</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.01</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[305]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x3dcabd8e0&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Why do you think <code>average_review_sentiment</code> correlates so well with Yelp rating? <strong>YES</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Data-Selection">Data Selection<a class="anchor-link" href="#Data-Selection">&#182;</a></h2><p>In order to put our data into a Linear Regression model, we need to separate out our features to model on and the Yelp ratings. From our correlation analysis we saw that the three features with the strongest correlations to Yelp rating are <code>average_review_sentiment</code>, <code>average_review_length</code>, and <code>average_review_age</code>. Since we want to dig a little deeper than <code>average_review_sentiment</code>, which understandably has a very high correlation with Yelp rating, let's choose to create our first model with <code>average_review_length</code> and <code>average_review_age</code> as features.</p>
<p>Pandas lets us select one column of a DataFrame with the following syntax:</p>
<div class="highlight"><pre><span></span><span class="n">subset_of_data</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;feature_to_select&#39;</span><span class="p">]</span>
</pre></div>
<p>Pandas also lets us select multiple columns from a DataFrame with this syntax:</p>
<div class="highlight"><pre><span></span><span class="n">subset_of_data</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="n">list_of_features_to_select</span><span class="p">]</span>
</pre></div>
<p>Create a new DataFrame <code>features</code> that contains the columns we want to model on: <code>average_review_length</code> and <code>average_review_age</code>. Then create another DataFrame <code>ratings</code> that stores the value we want to predict, Yelp rating, or <code>stars</code> in <code>df</code>.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[306]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">features</span> <span class="o">=</span> <span class="n">df</span><span class="p">[[</span><span class="s1">&#39;average_review_length&#39;</span><span class="p">,</span><span class="s1">&#39;average_review_age&#39;</span><span class="p">]]</span>
<span class="n">ratings</span> <span class="o">=</span> <span class="n">df</span><span class="p">[[</span><span class="s1">&#39;stars&#39;</span><span class="p">,]]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[307]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">features</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[307]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>average_review_length</th>
      <th>average_review_age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>532.916667</td>
      <td>618.250000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>481.333333</td>
      <td>371.666667</td>
    </tr>
    <tr>
      <th>2</th>
      <td>252.000000</td>
      <td>1106.200000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>672.625000</td>
      <td>398.500000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1015.500000</td>
      <td>1412.750000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[308]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">ratings</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[308]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>stars</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2.0</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Split-the-Data-into-Training-and-Testing-Sets">Split the Data into Training and Testing Sets<a class="anchor-link" href="#Split-the-Data-into-Training-and-Testing-Sets">&#182;</a></h2><p>We are just about ready to model! But first, we need to break our data into a training set and a test set so we can evaluate how well our model performs. We'll use scikit-learn's <code>train_test_split</code> function to do this split, which is provided in the cell below. This function takes two required parameters: the data, or our features, followed by our dependent variable, in our case the Yelp rating. Set the optional parameter <code>test_size</code> to be <code>0.2</code>. Finally, set the optional parameter <code>random_state</code> to <code>1</code>. This will make it so your data is split in the same way as the data in our solution code.</p>
<p>Remember, this function returns 4 items in this order:</p>
<ol>
<li>The training data (features), which we can assign to <code>X_train</code></li>
<li>The testing data (features), which we can assign to <code>X_test</code></li>
<li>The training dependent variable (Yelp rating), which we can assign to <code>y_train</code></li>
<li>The testing dependent variable (Yelp rating), which we can assign to <code>y_test</code></li>
</ol>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[309]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">features</span><span class="p">,</span><span class="n">ratings</span><span class="p">,</span><span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span><span class="n">random_state</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Create-and-Train-the-Model">Create and Train the Model<a class="anchor-link" href="#Create-and-Train-the-Model">&#182;</a></h2><p>Now that our data is split into training and testing sets, we can finally model! In the cell below we have provided the code to import <code>LinearRegression</code> from scikit-learn's <code>linear_model</code> module. Create a new <code>LinearRegression</code> object named <code>model</code>. The <code>.fit()</code> method will fit our Linear Regression model to our training data and calculate the coefficients for our features. Call the <code>.fit()</code> method on <code>model</code> with <code>X_train</code> and <code>y_train</code> as parameters. Just like that our model has now been trained on our training data!</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[310]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.linear_model</span> <span class="kn">import</span> <span class="n">LinearRegression</span>
<span class="n">lr</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>
<span class="n">model</span> <span class="o">=</span> <span class="n">lr</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Evaluate-and-Understand-the-Model">Evaluate and Understand the Model<a class="anchor-link" href="#Evaluate-and-Understand-the-Model">&#182;</a></h2><p>Now we can evaluate our model in a variety of ways. The first way will be by using the <code>.score()</code> method, which provides the R^2 value for our model. Remember, R^2 is the coefficient of determination, or a measure of how much of the variance in our dependent variable, the predicted Yelp rating, is explained by our independent variables, our feature data. R^2 values range from <code>0</code> to <code>1</code>, with <code>0</code> indicating that the created model does not fit our data at all, and with <code>1</code> indicating the model perfectly fits our feature data. Call <code>.score()</code> on our model with <code>X_train</code> and <code>y_train</code> as parameters to calculate our training R^2 score. Then call <code>.score()</code> again on model with <code>X_test</code> and <code>y_test</code> as parameters to calculate R^2 for our testing data. What do these R^2 values say about our model? Do you think these features alone are able to effectively predict Yelp ratings? <strong>no</strong></p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[311]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[311]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.08250309566544889</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[312]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span> <span class="n">y_test</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[312]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>0.08083081210060561</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>After all that hard work, we can finally take a look at the coefficients on our different features! The model has an attribute <code>.coef_</code> which is an array of the feature coefficients determined by fitting our model to the training data. To make it easier for you to see which feature corresponds to which coefficient, we have provided some code in the cell that <code>zip</code>s together a list of our features with the coefficients and sorts them in descending order from most predictive to least predictive.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[313]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">coef_</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[313]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([[-0.00099772, -0.00011622]])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[314]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="nb">sorted</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="nb">zip</span><span class="p">([</span><span class="s1">&#39;average_review_length&#39;</span><span class="p">,</span><span class="s1">&#39;average_review_age&#39;</span><span class="p">],</span><span class="n">model</span><span class="o">.</span><span class="n">coef_</span><span class="p">)),</span><span class="n">key</span> <span class="o">=</span> <span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="nb">abs</span><span class="p">(</span><span class="n">x</span><span class="p">[</span><span class="mi">1</span><span class="p">]),</span><span class="n">reverse</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[314]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>[(&#39;average_review_length&#39;, array([-0.00099772, -0.00011622]))]</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Lastly we can calculate the predicted Yelp ratings for our testing data and compare them to their actual Yelp ratings! Our model has a <code>.predict()</code> method which uses the model's coefficients to calculate the predicted Yelp rating. Call <code>.predict()</code> on <code>X_test</code> and assign the values to <code>y_predicted</code>. Use Matplotlib to plot <code>y_test</code> vs <code>y_predicted</code>. For a perfect linear regression model we would expect to see the data plotted along the line <code>y = x</code>, indicating homoscedasticity. Is this the case? If not, why not? Would you call this model heteroscedastic or homoscedastic?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[315]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">y_predicted</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y_predicted</span><span class="p">,</span><span class="n">y_test</span><span class="p">,</span><span class="n">alpha</span><span class="o">=</span><span class="mf">0.01</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[315]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>&lt;matplotlib.collections.PathCollection at 0x363446040&gt;</pre>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Define-Different-Subsets-of-Data">Define Different Subsets of Data<a class="anchor-link" href="#Define-Different-Subsets-of-Data">&#182;</a></h2><p>After evaluating the first model, you can see that <code>average_review_length</code> and <code>average_review_age</code> alone are not the best predictors for Yelp rating. Let's go do some more modeling with different subsets of features and see if we can achieve a more accurate model! In the cells below we have provided different lists of subsets of features that we will model with and evaluate. What other subsets of features would you want to test? Why do you think those feature sets are more predictive of Yelp rating than others? Create at least one more subset of features that you want to predict Yelp ratings from.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[316]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># subset of only average review sentiment</span>
<span class="n">sentiment</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;average_review_sentiment&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[317]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># subset of all features that have a response range [0,1]</span>
<span class="n">binary_features</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;alcohol?&#39;</span><span class="p">,</span><span class="s1">&#39;has_bike_parking&#39;</span><span class="p">,</span><span class="s1">&#39;takes_credit_cards&#39;</span><span class="p">,</span><span class="s1">&#39;good_for_kids&#39;</span><span class="p">,</span><span class="s1">&#39;take_reservations&#39;</span><span class="p">,</span><span class="s1">&#39;has_wifi&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[318]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># subset of all features that vary on a greater range than [0,1]</span>
<span class="n">numeric_features</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;review_count&#39;</span><span class="p">,</span><span class="s1">&#39;price_range&#39;</span><span class="p">,</span><span class="s1">&#39;average_caption_length&#39;</span><span class="p">,</span><span class="s1">&#39;number_pics&#39;</span><span class="p">,</span><span class="s1">&#39;average_review_age&#39;</span><span class="p">,</span><span class="s1">&#39;average_review_length&#39;</span><span class="p">,</span><span class="s1">&#39;average_review_sentiment&#39;</span><span class="p">,</span><span class="s1">&#39;number_funny_votes&#39;</span><span class="p">,</span><span class="s1">&#39;number_cool_votes&#39;</span><span class="p">,</span><span class="s1">&#39;number_useful_votes&#39;</span><span class="p">,</span><span class="s1">&#39;average_tip_length&#39;</span><span class="p">,</span><span class="s1">&#39;number_tips&#39;</span><span class="p">,</span><span class="s1">&#39;average_number_friends&#39;</span><span class="p">,</span><span class="s1">&#39;average_days_on_yelp&#39;</span><span class="p">,</span><span class="s1">&#39;average_number_fans&#39;</span><span class="p">,</span><span class="s1">&#39;average_review_count&#39;</span><span class="p">,</span><span class="s1">&#39;average_number_years_elite&#39;</span><span class="p">,</span><span class="s1">&#39;weekday_checkins&#39;</span><span class="p">,</span><span class="s1">&#39;weekend_checkins&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[320]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># all features</span>
<span class="n">all_features</span> <span class="o">=</span> <span class="n">binary_features</span> <span class="o">+</span> <span class="n">numeric_features</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[321]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># add your own feature subset here</span>
<span class="n">feature_subset</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;price_range&#39;</span><span class="p">]</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Further-Modeling">Further Modeling<a class="anchor-link" href="#Further-Modeling">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Now that we have lists of different feature subsets, we can create new models from them. In order to more easily compare the performance of these new models, we have created a function for you below called <code>model_these_features()</code>. This function replicates the model building process you just completed with our first model! Take some time to review how the function works, analyzing it line by line. Fill in the empty comments with an explanation of the task the code beneath it is performing.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[324]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>

<span class="c1"># take a list of features to model as a parameter</span>
<span class="k">def</span> <span class="nf">model_these_features</span><span class="p">(</span><span class="n">feature_list</span><span class="p">):</span>
    
    <span class="c1"># sets</span>
    <span class="n">ratings</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
    <span class="n">features</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="n">feature_list</span><span class="p">]</span>
    
    <span class="c1"># split train set and test set</span>
    <span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">features</span><span class="p">,</span> <span class="n">ratings</span><span class="p">,</span> <span class="n">test_size</span> <span class="o">=</span> <span class="mf">0.2</span><span class="p">,</span> <span class="n">random_state</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
    
    <span class="c1"># don&#39;t worry too much about these lines, just know that they allow the model to work when</span>
    <span class="c1"># we model on just one feature instead of multiple features. Trust us on this one :)</span>
    <span class="k">if</span> <span class="nb">len</span><span class="p">(</span><span class="n">X_train</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span> <span class="o">&lt;</span> <span class="mi">2</span><span class="p">:</span>
        <span class="n">X_train</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span>
        <span class="n">X_test</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="o">-</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span>
    
    <span class="c1"># create model scikit learn and train</span>
    <span class="n">model</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>
    <span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
    
    <span class="c1"># check score R2</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Train Score:&#39;</span><span class="p">,</span> <span class="n">model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">))</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">&#39;Test Score:&#39;</span><span class="p">,</span> <span class="n">model</span><span class="o">.</span><span class="n">score</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span><span class="n">y_test</span><span class="p">))</span>
    
    <span class="c1"># print the model features and their corresponding coefficients, from most predictive to least predictive</span>
    <span class="nb">print</span><span class="p">(</span><span class="nb">sorted</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="nb">zip</span><span class="p">(</span><span class="n">feature_list</span><span class="p">,</span><span class="n">model</span><span class="o">.</span><span class="n">coef_</span><span class="p">)),</span><span class="n">key</span> <span class="o">=</span> <span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="nb">abs</span><span class="p">(</span><span class="n">x</span><span class="p">[</span><span class="mi">1</span><span class="p">]),</span><span class="n">reverse</span><span class="o">=</span><span class="kc">True</span><span class="p">))</span>
    
    <span class="c1"># list of score predict use X_test set</span>
    <span class="n">y_predicted</span> <span class="o">=</span> <span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
    
    <span class="c1"># create graph</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">scatter</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span><span class="n">y_predicted</span><span class="p">,</span> <span class="n">alpha</span><span class="o">=</span><span class="mf">0.01</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">&#39;Yelp Rating&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">&#39;Predicted Yelp Rating&#39;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">ylim</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">5</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Once you feel comfortable with the steps of the function, run models on the following subsets of data using <code>model_these_features()</code>:</p>
<ul>
<li><code>sentiment</code>: only <code>average_review_sentiment</code></li>
<li><code>binary_features</code>: all features that have a response range [0,1]</li>
<li><code>numeric_features</code>: all features that vary on a greater range than [0,1]</li>
<li><code>all_features</code>: all features</li>
<li><code>feature_subset</code>: your own feature subset</li>
</ul>
<p>How does changing the feature sets affect the model's R^2 value? Which features are most important to predicting Yelp rating in the different models? Which models appear more or less homoscedastic?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[326]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># create a model on sentiment here</span>
<span class="n">model_these_features</span><span class="p">(</span><span class="n">sentiment</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Train Score: 0.6118980950438655
Test Score: 0.6114021046919492
[(&#39;average_review_sentiment&#39;, 2.303390843374967)]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYIAAAEKCAYAAAAfGVI8AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjMsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+AADFEAAAgAElEQVR4nOy9e5Bl21nY9/vWWnvvc04/pu9jJK50EZIMBlwEBLoIYnCKR0gwKCKxoSBVdoxNrBiHSDZ24Sixha2qxAWB8BIPK6JcwtgVsAJYIoZCNlYUxwi4EiAJBLIsBLr36ureO3dmus9jP9ZaX/5Yu2d65k7PdM89Pat7Zv2quvbZ33ns1d1nr2+t7ymqSqFQKBTuXUzuARQKhUIhL0URFAqFwj1OUQSFQqFwj1MUQaFQKNzjFEVQKBQK9zhFERQKhcI9zokqAhH5uIh8UER+W0QevcHzIiI/LCIfFZEPiMgXneR4CoVCofBc3B24xleq6jOHPPdngc8af74E+PHxWCgUCoU7RG7T0DcAP6WJ9wI7IvJQ5jEVCoXCPcVJ7wgU+BURUeAfqepbrnv+xcAnDpw/Nso+efBFIvJa4LUAGxsbr/ycz/mckxtxoVAo3IW8733ve0ZVz9/ouZNWBF+uqo+LyAuAd4nI76vqe477IaMCeQvAI488oo8++hx3Q6FQKBRugoj80WHPnahpSFUfH49PAT8PvOq6lzwOfPqB84dHWaFQKBTuECemCERkQ0S29h8D/xnwoete9g7gvxmjh74UuKyqn6RQKBQKd4yTNA29EPh5Edm/zj9T1V8Wkb8GoKo/AfxL4OuAjwJL4C+f4HgKhUKhcANOTBGo6seAL7iB/CcOPFbgvz+pMRQKhULh1uQOHy0UCoVCZooiKBQKhXucoggKhULhHqcogkKhULjHKYqgUCgU7nGKIigUCoV7nKIICoVC4R6nKIJCoVC4xymKoFAoFO5xiiIoFAqFe5yiCAqFQuEe5060qiwUChkIIdD3gQBYoK4t1trcwzq141qtVjw7X7HqYVrD/ZtTptNp7mHx1FNP8aFPPsXuLmxvw+c99AJe8IIXrPUaRREUzhSqSoyKAgIYI4wVbrNy2ia3EALPXF6wt2oZgqWyga3phAfPbWQf1yefvsSn9vZoW8tkEnjh1hYPnd/JOq7VasWvvv/3+O0/fJJWYSLwipd9Gl/1RX8qqzJ46qmn+K4f+k3eHa7KvsL+Ed/7+i9eqzIoiqBwZlBVBh9RVRABVSQKlTNZlUEIgUvzjiF4FIsQqHrHzmaTbXLbnS/4yGMXWPUt6ASkZVpPqC3cd247y5gALjx7if/vI3/M5fkuzm3h/R7nNrf5SgsvOP9AtnG97/d+j+9/55N8jLTAUODlH3qScxP48le+Mtu4vvfHr1UCAO8OSf593/31a7tOUQSFM0MIkcEHoiqKIChGBCPgXL7V5HLVcXHRjgpKQT0intrC1uYsy5j++FMX+N1PPMbu3pxYbWCGBdtbm2xP8iqCD378j/nX732CTz4LyBwUHrp/zoNT+OqMiuBH/3lSApCUAMDHRvmX59MDvH11uPz71nidoggKZ4bBBzofEUCMoFFRNLsiuLxsuTRv6UNAo0OMp7aWicunCD708T/ivR9cMJ9DvblHP4fNzV22qj/iC/7ky7KMCeCX3/MEv/LseDLOuB98Fs695wm++ou/MNu4fu2Y8ruNEjVUODMMPtD3A4u25/KiY9H29P3A4MOt33yCXNpb8KmLCy7Pe5Zt4PK851MXF1zaW2Qb0/s+sOC3LsFjHnYX6fhbl5I8J//86ePJC3eGsiMo3JAYI95HImm14JzBmLzrhsF7Li4GrAVrK7rgCQGqzAEne6sVz+ztIWJwdoIPLaqR+zf01m8+If7gGbjM+DPA6oC8ULieE1cEImKBR4HHVfXV1z33rcD/Bjw+it6sqm896TEVbk6MkbaPGAPGmCvnk5qsyqD3niEM+GBQAdGAEul93qih5arjqb091HvcZAvf7iHO8fC5OtuYPnng8eoQeaGwz53YEbwe+DBwmIfqZ1T1O+7AOApHxPurSgD2j2mHUNf5FMHgI50fnbFG0OhBhMHHbGMCmLcLLs4XWAO1aej7jtB2zNtJtjE9e0x54d7mRO9qEXkY+HqgrPLPEJHnrvyNMeSdblOY5jB4IhCiEoFh8ISQ10ewu2hZtbDsYDEMLDtYtUleKJwFTnpH8IPAdwFbN3nNnxeR/wT4CPA3VfUTJzymU8VpTJAyJPPQQWUQY8wfWSAQfCSEOO4IBq784TKy7Hv6JfQBbLcirKC2SV4onAVO7N4WkVcDT6nq+27ysncCL1XVzwfeBbztkM96rYg8KiKPPv307YUXqCohRHxIE4lqPkfewTH5MCoBERTSeeaxOWeIMU3+kI4xJnlWFIJG/OAZeo8fPEHj1cDvTAztwDOXYbVKQ1mt4JnLSV4onAVO8s7+MuA1IvJx4P8EvkpEfvrgC1T1gqp24+lbgRumbqjqW1T1EVV95Pz588ceyGmdcGNURLiyAxARRJI8J8YYJrW5ujOAdJ45aijqqMTTHw0VIYRI1LxGq3YA3ydz0GKRjr5P8kLhLHBid7aqvkFVH1bVlwLfAvyqqv6Fg68RkYcOnL6G5FReO6d1wt2/+sGdykF54VpCVKKCj5EYNR01yXMyeAjAECDE8TjKC4WzwB3PIxCRNwGPquo7gNeJyGsATwpo+NaTuOb+TuC6cWTfEaDKEPSKX2C/lk5l8xq9Y4ysugAoYgwhRoagTJu84aMhRmL0DHG/wISnMkKIeXcE0UPvU7G54EEj9DHJC4WzwB1RBKr6buDd4+M3HpC/AXjDSV9f0rWuUQaqmtvHeGoZhlTPx9qxmJsxqc7PEGiajIogBC6tetBI7Sy970AMLw75wjQhrf7npGiruExJXGaUFwpngeyBIHcCYwRVruwAVBXVJM+KCM4Kcb+YWog4m+zfOfEx7VJiVHxIZhhjBJ/ZBNMNA37MHVAAEXz0dENeY/zQXQ1c2t9kyigvFM4C90SJCRHB2eQT2N8JWJs/TJPRiW2swY6mIR80e8mEfZPV/o5AVfE+UmVeNnQ+0tiKyjqscVipGYKny5xQFsbJ30EqgEcyR4bi7CmcEe4JRQBJGdjMtvezgjVCFyJmNKepajIVZY4aMhisKF3ox1l2oBLBZN7Y9iE5uQA6D8MBeaFwFrhnFMFpTNxChMrJNTuVKnesPmCdpdFU7dOHiEFpnMVmLPUMMKmFC8sVaKSpN+n6JYjhZS/IU+p5HwnJLyAkW+suY4BCUQSFM8I9oQj2TS77IaT7584+N5roTrLfCcnaq5P/aXBi7zvXrwxQTse4UCXEAOMOJcQ4NoLJa4NpV9CSdgUVsEe6sdpDmooUCqeNe0IRpBV3xHu9UlbZWiFGk9VcZIyMrRfj1daLItl3BTFGlr1PmcViQQPGGGpnSEGSeVj2kQ1XsVLP4D3GGabiWPZ5fQSrPkUINcBkPPajvFA4C9wTiiDESDfoNWWV/aA0VbxmNV5IdIOnH2LaQZkUF+9DpBs8dV3lG1fXM4iwUc2o3ZTeWzo/0HV5Z9zep9K628AGSVXujvJC4SxwbygCHwFF1eBDHE0ckeAl7eUzsR+WKXKtaShGzbpTaTtPiIEQU20fK4o10HawtZFtWKhRurbDu0jvhMF3BD+g9+Wr+w+wOYXpXsojCKTjdJQXCmeBe2I5rAIhCnE0vST7sqC5o0c5JOM5z3CuMETP5VXAR3DO4SNcXgWGzKmyjXEMqiyXC9phYLlcMKjSmLzrmZ0HrioB4aoy2MnXi71QOBb3xI5AFKxRRAyqihFBTEQya4LTmvGsUTEEQhR8NyBEDAGNmUdmFacRqSsM0NQVGiPYvKrz/LhLWpD8AwvSjuB8xt1ToXAc7okdgXUGMIiAs2ZM3DWjPB/GpOqZXTfQ9p6uGwghZs94ttYiJqVFOWtINYcc1uYNH41BwFn66IkoffTgbJJnpNM08Q+kUhMD6bzLvbUrFI7IPbEjsMbQVJEQ9EpZ5aqS7AlS+2GscG1Ya+U0a1hrZQ2N6emi0q4idaU0RqhsRocKEKJn6HuCRloZ0BAgKiGzyerZp+ECUJM6MA2k82dvr3VGoXDHuScUgTFCVENVXZ1wT0OtIe8j1grGjCttO0Y0Ze4NbI2wCIZalHObE7quZRGEBzP/vdq2Zxlhp9lgNttmuRQudSvaNm/U0JMX005ASBFDeyT/z5MXsw6rUDgy94QiOK21hg7tDZy7rLLCA1NLxOBjZGNSs0Wq/Z8TtZb7JxOoDD4MmNpwv0zQzCari+OGRIGLN5AXCqede0IRwOmsNXR6ewMbqroBlImYlPCGJK97RqZVTe36VKnVBCQGKmeYVnnDR589prxQOG1kn3PuZZwzhKAMg8eHyDB4QtDsvYErI/ihY7Fqubi3YrFq8UNHldk0tD1zLLxHgFkzQYCF92zP8q5nDqskUSpMFM4K98yO4DQiYz+CEE6XycqI8sxiwGqkqics25Y9MezM8q6866rm/skET0Q00jSODQx15h3BYS70vK71QuHoFEWQkZRBbHAHqnqeisziIdCY1Ht31Q1YgcYkec7QeMXx4NYW874DdSATNusGzfw1vh/41CHyQuEsUBRBRk5rL+VFN4BYmrq6UmwoxsiiG8iZLCsSWLYtUccafVFZti0ieXcEh91E5eYqnBVO/LsqIhZ4FHhcVV993XMN8FPAK0mh19+sqh8/6TGdFoTUhzeEa6ui5s5vCCEwX3nEGlQtIgENkcbmndrUBz45X6DRM2vOsewuI8bxcp83hffyMeWFwmnjTsw4rwc+fMhz3wZcVNXPBH4A+J47MJ5ThLLsAr0PRIXeB5ZdgMzVhgzK5WXHfN7S9YH5vOXyssNkHtdu2xF9T9v3XFouaPue6Ht227zNgZ84prxQOG2cqCIQkYeBrwfeeshLvgF42/j47cBXywl5SlWVECI+REKI2c0vkBLK0IiPkbb3+DieZ+7BqwJ2bALTdwMhBqxq9iJ9z+4t2Ot6uhDoNdKFwF7X8+zeIuu4DksXKGkEhbPCSe8IfhD4LlLu1I14MfAJAFX1pN30c8zQIvJaEXlURB59+unj5+2rKoMflUDUFKrp8yuD3ge8psziunIYY/Eq9D5vj0M/KMaZK0X5RAXjDH7IvCNYznlmt2XlIxHDykee2W3ZXc6zjqtQOOucmCIQkVcDT6nq+57vZ6nqW1T1EVV95Pz588d+fxgVADKGZooQYtoh5CTEiKBXEsqMMQhjC8ac45JA2w70MTCESB/TecjchLfvPSFA1w7stSu6diCEJC8UCrfPSXr/vgx4jYh8HamD37aI/LSq/oUDr3kc+HTgMRFxwDmS03ithCsNYMYVrgjGJHlO96c1hmFICWViDBojqlBXmZ3FfWAVAo1YXGUZBmg1EPq8isBYy9DBag5uWODn4KokLxQKt88t50ERed0NxJeB96nqhw57n6q+AXjD+BlfAfzt65QAwDuAvwT8GvCNwK9qbnvNHaSyhm5Iq9n0a6eksirzxBYMzGyFqx1GDMbW2N4TMuehG42sVuAjTAZoe3A+yQuFwu1zlAXxnwa+GPjF8fzrgA8ArxeRf6qq33+cC4rIm4BHVfUdwE8C/0REPkoqzfItx/mso2KN0O87YMcm8cDYjD0fKZnMoFHBCERBrGTvo+xwzKaKj0oMAWOV2dThMkfG+xhoA0iqPk3w4G2SFwqF2+cod/ZDwCtUdQ9ARP4uSSl8OSk/4JaKQFXfDbx7fPzGA/IW+KbjDvq4GCPj3K8HErYkexlqRKidJcSIIogxKYcgc4mJ2dTy2IUlSsTKhCH09BgefnCSdVzLvqd2IA1YB/UMNCR5oVC4fY6iCF7ItfWzOuCFqroUkbwB3EdEFSonpD4mqVWltfvKIeO4Rt+Fc1er0sQY0w4hIw4hohgEYw3Rp3OXuYlm24HRFOGwX/s/apIXCoXb5yiK4GeAXxORXxjPXwP8jIhsAH9wYiNbI1GVqIKxgh13BFFBVMlpjRcjaFC8D1dMViLJPJSTQYWdzSlDDGgQqrqmMpYhcyJBpbBcpljkqYHVblIK1T3jVSoUToZbKgJV/W4R+SVSFBDA61X1vePjE7Hpr5v9FbaIGY+CaiS3j1FIO4ComkxDpN2KZHYW+xAxkv5eEZLDWJI8J6aGtgWJYBoYlqAmyQuFwu1zVO/frwMf23+9iLxIVc9MBv1pXXnvJ7opeqW4myDZndhC4MJex6Ry1E1D363YGzz3b2Qe11iQaT/NIpL+bFKChgqF58VRwkf/OvAmUnx/IC1kFfhTJzu09SHwnCziVP8/c8/iENNkhoy7FCGO8iprMXvBEemGjr5XVPrRP5D377W3gukEpIZmmgKttE/yQuFupAZuFAqx7k3wUXYE3wl8rqoev7bDKSIlkcmVqKGYuwEvacK3RrD2avP6EEJ2E0xQMMYSwtVmvMZaQm7nukI7jDsCB4sWTCC7079QOCnuB548RL5OjqIIHuOst18VoXJyTfP6KrP5JQ1L0Mg1JitIpqycBO/pg6cSh1iHhkgfPMHnLeVQOVh0MAe6FnYjbI7yQuFu5EFurAgeXPN1jnILfRT4VRH5RVLoKACq+sNrHsuJsW/LOpiota8QcuKMsOz60URkMEScNUymeb2fCgw+0tPhouBDN7qy8+L7ZJ/c/9IG0rkvaQSFu5SdY8pvl6Mogk+OP9trvvYdwxjBh7GEw2gaUiVrO8iEshoiBsU6Q/CBIUa2p3mn3BgUJaZEN/VEDVhjiJltQ8/OU9GqJbCIyXY6G+WFwt2IM9ywdvO6DRpHCR/9e+u95J0nNYnnGtPQaWgS3/tIbaAPSt8NOKPUNpXDyJnDGwgMPlI5izWOED2DDwTylnK4fAn2SIlk+/+5vVFeKNyN9AeUgONqj4t+zW7EQxWBiHy/qv4tEfl5btAyS1X/3HqHcu/R9Z4uCJWraKwlhEDnIy5zWeUYwFhzxQmrms5zl/TpWtgl+QUEGLjqLygU7kb2A+IcqVHLBZIyWHeg3M12BD8zHt+85mveca7E66tezSOIQuVM1l1BJBJDxItjCIqgxOCJmctQixVsjHRE+gDIQIPJn3chaZe8O57vHpAXCncjs/EYDvwclK+LQ2ccVf2N8eHnquq/PvgDfO6ax3GinNbGNFYMvULXD4SodP1Ar0meExOVi0PPsu0ICsu24+LQY3LXQDqQcL17iLxQuJs4t3k12KUbjzLK18lRZpy/cgPZt613GCfLjRvTJGWQE2uESiIYpR88GKWSlFuQkyGmUFGVMeRWhOA9Q8xrsuoPFJebHSIvFO4mpjOoSBP1ZDxWo3yd3MxH8M2kWkIvE5GfO/DUFnDm3HP7SWT7GlUkd55syheIWKwodVMRwkBUyZ5HsOojToTW9wzBoNozsRWrdXuojsnBL93yEHmhcDscdMReL89JbaEhKYEJyT+mo3yd3Oz3/A2Sb+Jh4EcPyPeA31rvME4WI2lys1YwxhBjJHhlWuc1wWiEiYMhQD94nEnnuYvhdX3HXtdTO0tlKwbfs9f1dJmX3s8cU14oHJUXkvrm3kiek4VPWcQemJJ8ZG6Ur5NDFYGq/iHwh8C/Wu8l7zwpfDStsvfDR90pCB9VlD4Izhrq2hGCpw+aitBlxEfPqu+IsSaIZ+g9ne/xcZp1XJ88prxQOCqHlfbKWvJrvH4k7QQ2N0HmaTe87nHdckksIl8sIu8Vkcsi0opIJyK7t3rfqUKEurI4a7BmnHgrm70TGAqGiPeBVTfgfcAQbxCse4eJBhHH4D0hRAbvEXEQ85flKBROgsNWxLlNQ9ONNOkHYOjSsRrl6+Qod/aPkRrMf4zkH/gO4JblJURkIiK/ISK/IyK/KyL/4Aav+VYReVpEfnv8+W+P+wschcOrj2ZGIGJwzjJtKpyzREx254UYmBrDbLrBxFXMphtMjSFzMFOhcGIcNq+ueb49Nuc2U6VRIbVnFdL5uqOGjqLwjKr+gYg4VR2A/0NEfgv4u7d4Xwd8larORaQC/q2I/NKBpjb7/IyqfsdtjP3IiEDfR0ARY9CYij9Pm7xxhyLCpBrLT8eIFcFVZDdZzeoGU/dYjVTWEn2EumZWN1nHNQFulDuWt5Ny4W7g4HfIcjVeP/d3q7awXYNxMNmGRiD6O+ss3mchIjXwOyLyv5JMsrcchqYl+H4VmGr8yWL0iFFHK9DV8NF9ucm4yrXGkOofKc4YNAZgbGCfkdm0Zmojq6Fn3glGO6auZpa5GN4ON67EuO4CXIV7j82KlKpO2gXsHpRnZLrhmG14Vn3K8FeB2UaSr5OjzDjfOr7uO0iK8rOAbzzKh4uIFZHfBp4C3qWqv36Dl/15EfmAiLxdRD79kM95rYg8KiKPPv308dsihKhYm0wwbjxaa05FHoERHZOd09GIZs8jsAKrEIlRqW1FjMoqRHLX6DuskkSpMFF4vsw20oJiRgrXnDGeZ7YNWRGigg2gIR2jJvk6uaUiUNWPqWqrqpdU9e+p6us44iJMVYOqvoIUgvoqEfm8617yTuClqvr5wLuAtx3yOW9R1UdU9ZHz588f5dJnAhFBjMGMDmxj0nlu09CqG4g+MBBp/cBAJI4O7ZxcPqa8UDgqk9HquQO80F6d4CZ5raEMfsAHaLbg3ANCswU+JPk6OVQRiIgRkW8Skb8hIp87yr5WRN4D/ORxLqKql4B/A3ztdfILqrofnP5W4JXHGv0RsUbwPtB1A23v6cYIndwrb1WwotdEDVnR7B23Li1WdCFCsICBYOlC5NIib0/Iw/4suYOsCmef/R2BkPJ6hNOxI/BR2JqCUeiWilHYmib5OrmZoemtwMuB3wR+XEQ+DnwZ8AZVffutPlhEzgODql4SkSnwNcD3XPeah1R1Pwz8NcCHj/8r3BoR6IZAiAHEggassUzW7XE5JiEGFl3EGUNTO4L3LLpI4/KW+Vx0LaveM20mNK5i8JZV17IoZT4Ldyl1BVtjk8CN+6C6mOaNOrOPQABTwUTATJJZKOr6Awtvpgi+BPh8VQ3jRP4k8CdU9aiJnA8BbxORcVnJz6rqL4rIm4BHVfUdwOtE5DWkxLlnSf6ItTMMAQWcdWPUkBBVGYZwtV9wBnyICIoiV/oUC5q9Z7EG6PsVi3aFWXXEfkllQMO6ax4WCqeDjSlsNBAltT6djavwjbw5lDSNoesCdQ3OWYYY6PskXyc3UwSdqgYAVV2JyH84hhJAVT8AfOEN5G888PgNwBuOMd7bog8RI2niDT45PZ0V+pC3AUxUsNaOBfFS/X8ZnUM5qSu4uEx9CRoZ6BZgbP7VUaFwUmxMLOoCdGAN4EGbJM/J1E2ZNHNihOgDaPJbTN16NdTNFMHniMj7x8cCfPZ4PuZn6RetdSQnSAiBeadUzmDHBjBtG9hsMkfnGEEIxHGHYiT1JLAm75dv1fdEP1rRVBGTYpdXfWkOXLg7ESds1BAn0DQg58DEJM9JVVdsTWHZgyhUFczqJF8nN1ME/9Far5QTVWJME64S0ZjO0bwTbmUNXfAYjVhX4b0ninDO5s0jaPuI3f9miGAEcEleKNyNiFqamQcPrgbTAy7J8xLpBTZmMNncpp3v0oUkXyc3Kzr3H9Z6pYwYa6kqSRnFKqhGqsphMk+4IkJFZBU8QxeoXGTqXPbw0d4PhBa6ADIMaA+NTfJC4W5ELJhkeSH4sVT9GFuSdVwIFTBECO2KGFNmrqzZXXxPVI+xItRGsXYs5WDH88wT7uADiz7SDxFF6IfIoo8MPm/UUOh6nngaLl2EwafjE08neaFwN6IhrbyrCZzb2aSaQC9JnndgQjTJTGWNxcSx9uOa+7PeG4rACm0QBGE2qRHSuc2cKrtsO1ofcLamqSucrWl9YNnmrfu/HKDrYdnBfDcduz7JC4W7kco1bFXQD7C3O6cfYKtK8pwEAkbBNlBXDtukaKbAeheLRypYMRaN+yzSzunfq2renoXHRYWZU1ZDYNl5agezymbvet6FSGXsFROVsYYqpuStnMznyQJp4EoEUxzlhcLdSO0MvaTvuzHp2EuS58Rg0w7AQ4yR6NOOwNy63NuxuKUiEJGvBd4C/DHJdPawiPxVVf2VtY7kBAkaaYOhcobpxOG9pw1QZ24FZjFAYNV2BDVYiTgr2DX/k4/LpUVK7NjfgXqSIri0yDqswl3Aaa0gqwz0PUwm0GxM6GJL2yZ5TionNAI+1adELDSa5OvkKDuCHwT+U1X9CICI/EngXwCfu9aRnCAhRCyBGA2rbsAKWCIhrymeSSP88TMrMIqRhqgdROH8i7eyjsvG1Ae4AmSVepMOo7xQeD5scmNFsOby+semD4bNMV9SY8QZ2JwleU4UIRiYGLCVwwboYpKvk6Mogvm+EgBQ1Y+IyJlaGyrQegCPMQ4f0nq3yZ0gFWEgoq3HOkfwA1K7dUeGHRtXXxkewtXhuLxVqAt3AYfZlPPbmg1bU4MaS1VPGYwiY1n4nFTG0ojgvWKi4j00VqjWnGt0FEXwGyLyDuBnSXPqNwG/PpaGYCwVcarRGNGxvhCAEUOIAV1z4abjshg8tSq7MRBWK6wNbKtlMeS9LaxJregipExG0u2QOdq2cBdw2PSVO1p/c1YRnlJm1tFUDd3QswyezVne1WIUEFU0Qjf0EEGMsu6p6yiKYItU6fc/H8/3gG2SQlDg1CuClBSVSjkYY4hRUc3fs3h3b8nFNrJRzWi2pnSrFRfbns29ZarUlIm6himk7fEDML8AY5OyQuF5cR9w4RB5Th6cbVFVl7g0X+FixC87NjYMD87ymmklRlYIs4lhc/Mcc7nA0kck3qGEsn1U9S+u9YoZMGKobGDVDwxBqKwyrR0mcxPeLnpcjFhnUwlqZ3FdpIt5dwTTWdoBzCO0T6dt+2yUFwrPhxcCHz1EnhPXGDabho06UjXbDM0uIga35uJuxyUKnJ9WSNUgRDZnMzaG7s7tCETkB7hJqXdV/c71DuXkECLzLjKpKmbTimEYmHeBjTqvMb6xDfU04ocB64TgB+ppQ5PZBlNHWI6Pt7bh4m46z/znKtwF7GyRbApc2xt4J+/Cm2GAnc1NnDPLmE0AACAASURBVLEYOyFOLD4Ghsy5M8402HqGEKiqiqHv0HqGM+vNb7jZjuBDa71SRlSEaWVQlH7wCJrOM5uGdjZrdpcLtDZoiLgaJAR2NvMG081j+mL0wN5u8hXUo7xQeD64Kn2XetIuc4907jIHbhhj2ZzMQMBKTXAKmuQ52Z45qmcjlW2oXIWLDUPo2Z6tt2fxzWoNXdOFTESaA93EzhSqgjPC8oBpaFZXaOaEsu3ZBNN4nEaajSldu8S7iu1ZXkXQLdJKzQLbO3DxUjrvzlSsWOE0EkOa+LeB8xaeDimcNGYO5Z42Fg0LVCwqHtWAaGDa5L0XtzZmbDQ9YpRpXbOip44VWxvrtdPe0gYhIq8SkQ8C/348/wIR+ZG1juKE0eh5Zt7SDRHE0A2RZ+YtmtkW72zNZ57f4IFzE5xEHjg34TPPb+BsXq/sykNH+rlw6erjVf4Yv8IZxzTJMTwl9d6dks7XbOk4NptNzXxQ5qslUWG+WjIflM0m7704baY8vLPB1sQCnq2J5eGdDabNnetHsM8PA68GfgFAVX9HRL5yraM4YYYQ6L0yqQzGGEIQeh8ZMmeUiRGsdUyq1CjHGcVah+TupdzBLunL8UIHl1N1Xs7mfrBwmphVySRUA5v3wfziaCbKbBqKwAOTikErRIRzsw0qyZ7SQ2UgGsvOxjmsaQixw4dAtWY34lEUgVHVP7quNHLmjdzx6D3cv1HjFXwI1JVlVlv63CvcGHhm3uEEXFXT9j3zLvDwTl5FEOTqP/iZUQmEUV4oPB/OPwCTx9MEu1/hZTLKc9J7mE43mQHW1ITYo6M8J9ZanLEQY+pMEyPO2LW32D2KIviEiLwK0LH/8P8AfOQW70FEJsB7gGa8zttV9buve00D/BTwSlJ48Ter6seP9RscAWOg7yNIagkZY6RXpZ7kjc7pfcAariS6WWvRGOgzl6Hu27Rii8AO8BSjg6/0ri88T+7brtjcHpAIG+fABVCT5DkxBgwRsRaNirGChoDJnESpCJuzCh+UGIWqqnFW1l5i4ii/5rcD3wm8BPgU8KWj7FZ0wFep6hcArwC+VkS+9LrXfBtwUVU/E/gB4HuOOvDj0Fjh8qqn7QaiQtsNXF71NJnLUPcRKiPsrVY8fWnB3mpFZYTcjcBMdXUXsDse/SgvFJ4PmxubvOg87NwHzqXji84neU6mlWWIYMUwnTVYMQwxyXMiAlENdVUxmzXUVUVUs/Zc2JvlEXypqr5XVZ8CvuW4H6yqCuwXLq7Gn+vzEr4B+Pvj47cDbxYRGd+7Noy1bDWOECMhpFX4lnOYNW+vjosfOh67sMIag7E1i7ZndznnpQ9OSQndebBmzBsg/dMCyY5bSkwUni9NVVE1aYKzs4aw7HB1kudkOp1w/1ZkGDy+73Emcv9Ww3SaN2rIGUMMA/PWE2OFMQN15e5oHsGPichvAn9HVS/dzoePpqT3AZ8J/Kiq/vp1L3kx8AkAVfUichl4AHjmus95LfBagJe85CXHHkeMwvasYYiREAVrLJUxxMy1hvphYG/ZM6vTzTH0gWU/0A/rjRE+LjLuSBYk89CKsRJpbs9Z4cxjUXy/vyIUFPB9kuekto5zmxNCUCIWQ506Gdq896LGyLIPiCrWWkLoWfYhtd1dIzdb4z0CfJhUdO62ykyoalDVVwAPA68Skc+7zc95i6o+oqqPnD9//tjvF1GGGFOpCWcxYhhiRCTvl68dYKMS5u2Cpy9cZN4u2KiENnM2496cK1XY99cdwygvFJ4PnY/UU8POVsP57XPsbDXUU0Pn864yamcxCMaANTL6DITa5bUatN5jUFQMIURUDAal9ev1Yt8soSwCPygivwL8moj8GEmRS3pat496EVW9JCL/Bvhars1Yfhz4dOAxEXHAOW5ck+p5YY3QDgHBY0xFjAOKsDPNq+1733Fh0aVSs/UE71suLDq2NzI7sQ+0Jl4eIi8Ubgc1lofObWGsIyJMtzeJwaOZM3iNEcQaqigY54heUSOYzKHcbR8IAaIGRCyqARVD2683oOSmM46IfBupCc3/DGyr6raqbh1FCYjIeRHZGR9Pga8Bfv+6l70D+Evj428EfnXd/gEA1eSUNSKoKkaEygjrv9LxCMEz7zv6GAhR6WNg3neEkDdm7eKBx/0h8kLhdthuGhCD1xQG6TUleW43eTPKosJGbWlqhxFoasdGba+0as2FDwPLvidiELFEDMu+x4f1mg1u5iz+d8DHgT+jqk/exmc/BLxt9BMY4GdV9RdF5E3Ao2Mfg58E/omIfBR4lttwSh+FoIqGSBs8gw9ULjK1jpBZE0S1TMSwu5wjZkBjx0bVEDXv6uiwhX/ZEBSeL/dtNSwfewYlopOKtl0iGO7byptIoJpKrfsQ0NS/EMVmXywKsh86hOw3ERdJ8jVyM9vIG1X1X93uB6vqB4AvvIH8jQcet6S+BifK0A88veyQoNiqoV965jawkbvErHraEKhtQ11P6XtoQyBq3h3BYZvOM5VFWDiVVK6icZa9ZQumY+h7tmYbVJmrzqkG5qtuzOoXIND2nq0mr2moqiqmrmcVOrouImZg6iqqNUdZ3cxHcNtK4LSx8j2+CzSTGmMM6hxd27Pymde4UQmqVNZgjcUYQ+89ufejh1WSKBUmCs+XvWXPtJkyqSZU9YyhqRAj7C3z3ovex5TXAzhn8B6GmOQ5qQQGFTbrWWqh2a9ovadas366JyLD+w6aSYVGZfABjUozqegzz2zGVpybTrBGidFjjXJuOsHYvKuj5THlhdPHi44pv1PM+47KCBuzGU1VsTGbURlhnvlmHFSZOUFRlm2Pks6HzLYhVzs2KotKpO96VCIblcXVd6gM9d2ErSEsA6ayKe7JQBgCdiPvr187Q+Mcm80UkQrViiEM1C6vfj7sr3JPfFnuEj4NeOIQeU6MCvPB44Y5Vb3J0M9T1rrmdRZriCwGpbGWjWmFHwYWQ/7mVQZLPa0x3QDWggZcU2HW3OX5Zs7im3YgU9X/fa0jOUGmxtKGFhcCtpoQhh6PMs1c+3Zz2uCsBw0YUxFiwFnL5jTvuA7LpcybY1k4DtsH239dL89IXQl+6MBUSAz4EPFxoK7ylpiwVlCffHY6REQ9aKoGnBMxERNhe3sTYxwx1rSrDjF3rmfxfo2Dzwa+mKtN6v8L4DfWOooTxlWOaeXw0RNDQKwyNQ5X5f0nT+uaab1i1Xb0Q48Rz7RpmGbuEn/Y1Uvv+rODGtgISXnvd4dsR3lO6qqmqhs0+FQvRyJV3VBXeb9dRgxYQ/QBsRBjxIzJpzlxpmI6FQQlpTQo02mDM3euQ9k/ABCR9wBfpKp74/nfB/7vtY7ihIkRzm00qE6IGAw1Isqas7SPjyhBwVYOpxUqkaBJnpPDIpQzJzwXjsHWDJrLKf6lIh2bUZ4Tg+H+6QQVQGqoNxFN8pwoSmMNtqlIvfkMwQc0d+mL2rEzgyEoPoJzjsoKdQYfwQu5NoS8H2VnBjFCCJF28PhocSYwqfI3gGk7z2K14tJiCdKAduxszGi7vHfrYR0pS6fKs8MLHgB3OUV6DeNPM8pzYitD7Soq5xBpUDUM3mPX3WnlmAiGpqkwCGIsGiFag2RWUBNnWRhls7Y45/De0/nAZM2lL46iCH6KVG/o58fz/xJ421pHcdLEwLOLnsoIVe0Yes+y73kgs7P4wu4uj++umDrHrJmx7AKP7654we4uL8+oaw/LYsjdx6dwdDY2UhvI/fVsTTrf2Mg3JoCpqzG2Ywg9xlhi7DHWMXV5TUNVZWkCqKTkMnGCqFBlLkPdNDXbAdphoO0iViLbTUWz5haat5wJVfV/EZFfAv7MKPrLqvpbax3FCTOESOMMVeUQEUxTYQbPEPLahi7sLXAo03qKNYZpPWXwe1zYK2vvwvPDD8k/0ADntqDeS+Yhn9m+V9cGJwKuxuCIpgZV6jrvyrtxlqWJGDmwI1ClyVx0zojQ1I7KWVQEUcWM5XLWyVGXxDNgV1X/8VhD6GWq+odrHckJEtSwNWvoQyCEiLWwNWsImtc0FNXgjGF3uZfspdqn+uOZPXqHxSxl7i9eOAYrnxSBAnF8LKM8J0Ysk2aCqOJcg/eKimAk74RbVY7aBbphIAbFSEi9EzIHlACICNaOpSZOKK/hlr+liHw3qST1ZwP/mOR7+mngy05kRCeAs8pq0WOsRSQVm1t1PVtr3l4dl4mDJ559OpXIrjaJw5zKGB7eeSjruEoewdkn+hQ9KgYmWympMsYkz4lYw86sJiCEaJg0EyyKZO56pFExCE1VkR4ZDIJmzvJXGOesq+MQkbW7sI9yb/9XpJpB7wdQ1SdEJF/7rNugtialsMeAdVOCX4GxPHxf5u5DEnly12MDbN2v7F2OBBtxmTvAHHb13EFWhaPj6vT/mtVjxFANyzbJc1IbS9CBoAEwhBhADHXmMtQ+RFQEKwYxBo1CVMVnNh8nRaRXJn8RARRd87COogh6VVUZu7iISGZ30/HxUbECfYz4bkAkUluLz6ztL64GdqbQeeiGnnoCjUvynJTqo2efnRlsTyH0gAcZ0vlO5vDRygmd9xBj6kkQPN4YKpfXTBvG8vQy2t5FUrxQ7grFCPR9JI7lutHUYGva3PmooZ8VkX8E7IjIXwX+CvDWtY7ihFm0PWIsGxsNYhwaa7z3LNq8U9ulvRVVVVNNHdZMCNGC91zaW2UdV6k1dPapZoITxRvwISWSOUnynISoNJXDWjOWVYEQIiHzokzGlltpXMkU40PIndJDDBEf4xUlpSr4GIlBkpF+TRwlauj7RORrgF2Sn+CNqvqu9Q3h5BlCRBm1flSipjSR3FFDkYFndns2ZoHpbMKq7VgsAy/aymsvLYrg7OO80gvUDWzuwDxAr0meEx+EcxsTgioxGoypsCL4kLvcs2XoAt77KytvQajqvCarEBVrzFUFNeZErVtxHsVZ/D2q+neAd91AdiZwRhi8x4Q4Ot4HokZc5lpDs7oixJbVMqC2o10GQkzyQuH5MIiw1WgqNxShrlMewbDmsMPjYi3ELmKtxViDADEE7JpNHcfFWYMxqVOgqqaSDkZwmZ3YiFC5FOCSxgWVM2uPHjrKb/k1N5D92bWO4oRpnB3LSSjWGiCVl8gdIzyppzywaWgmqZVmM4EHNg2Tepp1XIXjcdjUmnPKjQGaDdg8B7NNy+a5dB4zdxeaVJZ5N7A7X7Jo03HeDUwyJ25BqjdUV45J7agrl73OEKRFbAjxStSQqhJCxK25KsLNqo9+O/DXgT8hIh848NQW8O/WOooTxjnHRmNY9gPDssU4z0ZT4VzegMhJXbMzG713bnrF5jfJXHSucDwmwI28Ojlj0iZThzAwcVA3U3o/T7kF08zVNBE0eOZ9iy484no268naWy8el6hQV4YQkunYINhKcveIwjnDaoiIRoy1xBhRBLfmUvU3+1b8M+CXgH8I/I8H5Huq+uytPlhEPp1UnuKFpHDYt6jqD133mq8A/gWwn5z2c6r6piOP/oioKn1UNGjqUBbG88wRAZtNjXUOUaWpGzrtURE2M+c3FI5HxY0VQU4D332zLSbVs/QLGJijC5hMkjwni7ZjUMPWdIuqahiGjt4HFm1HzjJIqkqIYKzBjs7iEBUxmTUBwqyxSUEBztmUXHanehar6mXgsoj8EPDsgeqj2yLyJar667f4bA/8LVV9/5h38D4ReZeq/t51r/t/VfXVz+eXuBXd0NO1gUnTYF1D8NC2A92QN2qomVTUAss4EPqWqAMzU9NMio/gLHEay3ZvTBushd6Bc8LgFGuTPCeLwTOrHVVdoyq4SYPrexZD3kw3IZWeVr2awauqiMldFRWstdjrLGfrXsQe5bf8cWB+4Hw+ym6Kqn5SVfeT0PaADwMvvp1BPl+6Xpk0VUoUGf+5k6ai6/Nq++iVAcaUdkMM43nmyI7C8TispUrWVisasBU8sGM4v73DAzsGWyV5TowaEEMcI/ZiSPHxJnNZlf2m9Qdt8SDZKxQLz530953G6+QoBkPRAyNR1SgixzI0ishLSdnJN9pF/Mci8jukznp/W1V/9wbvfy3wWoCXvOQlx7l0er9LdslV5wnBYm1g4hyS2Uew6Fv6EJnUU+q6weDpgmfRt1nHVTgeh7n2c7r8u0F48NwmAlhX0ZgZOspzsjVzXLrQ4eoKa4QQFe89W+cyV7JSxqQ2kzJ4jU3CzGsyY4TBR1TjlZ2KiKTIoXVe5wiv+ZiIvE5EqvHn9cDHjnoBEdkE/i/gb6jq7nVPvx/4DFX9AuBHgF+40Weo6ltU9RFVfeT8+fNHvfQVnAae2J2zt+qIGPZWHU/sznGZV0fL1mNV6cPAou/ow4BVZdmWgs9niYMTvhwiv9OoFaoYCRrofE/QQBUjajMrgumU7c2GyijOQGWU7c2GrWneSDkxgoi5EjJqxvPcOwK4GinkQ7wmgmidHEUR/DXgTwOPA48BX8K4Or8VIlKRlMA/VdWfu/55Vd1V1fn4+F8ClYg8eMSxH5khRFBliJHee4Y4nmdOKAvBc2mx4MLeHheXSy7s7XFpsSCEogjOEgc9OuYQ+Z1mauBTiyVt2+NsTdv2fGqxZJq7VWVd8/B9M+7fnjCrDfdvT3j4vhl15kg5I4I1V00xAljD2ss9H5cryWP75S8k7aLCmueuo2QWPwV8y3E/WFLRjp8EPnxYo3sR+TTgU2Mto1eR7qMLx73WrVj0kZ3JlAEFNTg3oUJY9HkVQe87nroUcQJ2syXMwWukf6jLOq7C8dhsoOpSrfb9/sDLUZ4Lay2VGEIfWLQtoQ9U1mCv9zre6XEZwbmK++r6SimHGBWbeeVtjBD8GEl4pdqnYDLvoPzBLOKkpa7I3RrzoG6WR/Bdqvq9IvIj3MBSpqqvu8VnfxnwF4EPishvj7L/CXjJ+P6fAL4R+HYR8aQIvG/RE9j3xBjoY8CZKhW6ikofB2LMXMph1ROG1EZw4iNtnzThclXKu50lzt0Hm09e7ekcSI7ic/flG5OPwoPnzhGiUlVThtpgjeBj7sxiQ9Rk3lAATUrA5s7g5aoJZr8BzGkYU9oRHKiBNMrMmp0XN9sRfHg8Pno7H6yq/5ZbBLuq6puBN9/O5x+HSWVSX2CUutqgHxaA8BkPZrxTgXnXUdXgGjB1hd3q8F2SF84OO7PU7nxJipkeSMlkOSt9qqSyCdNJjTMNvoJh6Mnci+mKozPGpAgEGe3x+U0wUcE6e81OJax55X1auVkewTvH49nqT3wDDAJWqEg3h0ZhQJI8IyJCH6BfQq0d/eqqPCcb3LhR/ZmrP36HMDY5hjeB+6YwWaVdQc4S+9uTmhAXMLRIXTEMLSEmeW6udNw6RYSo1ygkEcGYJM8ZW2itIWgk+HBNq8p171ZuZhp6JzcJnlLV16x1JCfIADzQTAiplBR1M8OiZG7fysQaFnuBEJJ9eXkpFeWaZN6SNtxYEZRWlTdGgQcrsAr1BOwAQfJGHk4nNY0zhOAJwSMaaZxjegoUQYwR7yORZAp1zmAyJ24BV3YBY0VqRPLWi4LkU1EFY1MUk2pEI2v3qdxM2X3fePxzwKeR2lMC/NfAp9Y6ipMmCEOMLH1Hms46Zq5Jd2tGIkoMUFVgXTr6Iclzclj9kFvWFTlhtkm10G8kz4ltYGsDxKbHlUl5Wzaj5hQMm9MpRMXaKSEIGEGOFCh4csQYWXUBSImdIUaGoEwbsioDI7DqI9YKxhhijASvTOvMiW4HcwZEUmMJs36rwc1MQ//POJDvV9VHDjz1ThG5Lb9BPnqe3Nujto5Z41h2K3ZXe7zkwbyroxBhcwOWS2iXqZ/s5kaSF57LjBsrgsxNt9huoPfQCExnMF+l8+2MikBFmLmGKIKTGu/AaGoUn5NhCMTRESsiYAwhRIYh0DT5Jl0RwY3mqv3wUWfz+y4Qoa7sc3wq6+Yo5q8NEXm5qn4sjUtexhkzF3dDJMTIyrcMavF9C8bQDXln3Lb1tB5mm1BvQm+h7ZO88FwOq+aZt/M03H9ug4lb0LbALnQtTJokz4UTg6sczjqcqfFR8MHjMpdW9mMP3rYbCApWUn19HzObHu/QhHvsYbFfb+jq/y1XiYm/CbxbRD42juszgP9uzeM4UZatxxpD6wPqAz4qE2eyZ/D6CP0qtRKcOlitIPZJXnguh00UuX0XTVVz7tyCegluBo2mnUFT5dtxzmY1s2XqbmWspQqWYIXZLO8uOIbAbhtGE4ylD4FVH9ie5I3MuVMT7nExRvDhQAN7VVRZu7P9KAllvywinwV8zij6fVU9U/GNq37FavA8uL1DU83ohoZn9i6z6vP2Bq4sBIVuDqaG1RxcleSF53KYYyq3w2o1DLgJvOico5ps8f+3d+4xlmR3ff/8zqOq7r3d0zP78lr22kbYQoEAxvGLgIgT8sAEgRAkOIiHQYkDQeKVCBSkgIhIFKGEOMQCy8K8X0a85Dg2AgQKQQIb27FZYwNyhCVsDN5dZqe7b99bVeecX/441TM9szO73Zvue2rn1kdq1a3Tt7t+ffrW+dU55/f7/vr1AQdtYNWXC0fYqRv2FkoX8lKM80LlKnbqsvOnlBJ9jIBF0Sy0GCOpcH7Dpgbcs5KXrMgzleOM5wtYsjpNqco58O1kTaB/ISIvEpFPUdW3naslF0jlK+Y+0ocWxRJCy9x7qoJPbJCfQAxZJ95IPqZYXOdqtDx+xvZN4a1jr7bD+nseSPZqi7flAg9ntaf2PcaA4hAUbx2zuqzEeRLBGWHdd8TWYE2OZkqF1+I3NeA+Xdsu2iGdZsHwx4AO+Ozh/GPA912YRRfAzmzG3Bn6rmW5PqLvWuZuiKooiMAgDQy+ykfry4esjVFff8zUvsox3pJrYovk7NSSS0Nm2Px0JmcUO2NwVopr56QQaWPCO8+8qfDO08ZECoVraHI84BqcvVEsfls4jSP4ZFX9foYMelU9ovxYdSZ2G8th35NUqX1FUuWw79ktvC6pBlwCGZLKJObzwtLsPHDG9k1x+Yztm+LS3OONMKtqdpuGWVXjjXBpXu7pu48JMZbKeWa1p3IeMba40CIGRAVrhgHXGETldCPRxIVxmu7vRGTGsGIhIp8MPKP2CJQ8xQsx0PU9IYZBt6Ow7orCsoW2zZ3btvnclq6Tesb2TfHQGds3xayac3lnB9FE7HPy1uWdHWZVucDWLkSMKhghxARGMJr3DEpijWN37jEoMUYMyu7cY03pT9d2c5re/x7g14CHRORnyGJyr71Io86b/aOOxlpSVeXIgKqisZb9o7Libm0PfT/IEfSw1pyV2hZOeb52xvZN8dAOPDzUynNkXZ/j9pKIFXabmnldY0xNSg4rub0UKSaWIUfH1ZWn73uWITErPCOorCGmSOVtfkBDQZVqBAJv28yTOoJBSvqPydnFryQvCX2Lqj66AdvOjf2jI/a7yE49o6kXrFvDfrtm/+ioqF1Ha8DCYg7zXRDNiWVHhQuU3enypeumPetekMM8e6rIjkCG9pJYEVQcM+9o/Jx1L7QhYAuuMRsrVJKjYLo+ICiVaHFZ5aqyHHYRYsQ4RwwRjKGqplC5kjypIxjqBLxdVT8d+J8bsunc0ZRIsWPdQa9C7Nek2KGpcEw14FzOI2jbfHQut5fkTitTpaOZkoH7GLT+yU5gPrSXxDvPzMJhu2TVBVRbdqoa78rtEXjrcBVoSBgraFRc5YpGMmWEeWUJSUgKrrI4Y3iGbTtulE1oM53mU/FeEXmZqv7BuV55g3jnCAqpX+PEE/o1CYMvXLPYOwgd2CqHj2qE2OX2kozVEVw7yDOBXWBRw6LNm1XXDsraJSTapMyrGu8X9D20SZGCLt07g0uJziT6PuBcwifOvdbtWcn1ERzVidmSqhZX+Rwrm9JmOk3fvwL4KhH5CFmUcqjmpp9xblZcMN4bLIq1Dm8MWEeMEe/L3hSNhVYhtMAh7Lf5H1I4mGm0jiCkvJ+yAlybj0r5TOyoSm0djfNY5/E0rENPvIDasqdFgHXKy42Vd8TQsR6BmibkwS1Gvf6Ea0cQ1jpWNqXNdBpH8I/O7WqFqJyndhUhhPwXR6V2FVXBqTtkyWlHjsuNfR7U3NBekjttoZeum2Y1zwBqskaNDuelo6wQx27tOOzXhFXA2cBuXYOUe8btU8IbpQtK1/Y4o1Q21+0uiaActRFnBWstMUbaNhUP5R4rIelNOQ3HuQ4hpXOVVnmyegQNuXD9C4GHgTer6jNTDU2zlKtgMQLeWZwzlC7XtFznDU8PYPIxDO0TT6SegbmaN62Xmo92aC+JlcijRy3eGJpqRtstebRvefY95VSQ2i6w6nQYOLKY2qpT5l3ZW1gV/JCxq6oYEby9Xop34haEPIPKLvR4RqfnnnbxZL/vJ4CXkp3Aq4H/cpZfLCIPichvi8gHReSPRORbbvMeEZEfFJEPi8gfishLzmT9KVGTsuaKATGGZHKctZqyT0fXljc2hpthMEtD+8QTOa6pEsj9FG5pL4ciArXz1NZRO09+gCs3uvUhcLTuWHWBozbk47qjD4UdgQh15YZkMsFZQ1254vLYY8VZua6eLCLElGj7dF0y+9yu8yTf+9QhWggReTPwrjP+7gD8a1V9r4jsAu8Rkd9Q1Q+eeM+rgRcNX68Afng4niupTRz1HX3b4WohtIf4uiK1ZR2BhhwB4wDZz0+4YWifeCKrdZ417QKXKnBd7rNV4RmUUvHgpV2Ouo4+dFgLD8520YKiHDEl2phwmosexZAIKQ8oJTFwfc37mJTSlFh8B4wxNF5JqrmfJNdgP++ooSf7bdfTmp7OkpCqflxV3zu8PgA+BDznlrd9CfCTmvl94LKIPPus13oqDvs1XdsjzuG8Q5yja3sO+7IjSCR38hoQk4/90F6SZ52xfVMYybWBIxBCPs6G9pJ4C0YMVy5d4t4rl7hy6RJGTFEVWQWckRw6qjl/wBkpvuHvnCGl4+WOfEwpt0/cGQGtnQAAH6dJREFUhqFOwknNqMpb2KD66GeKyHFBKAFmw/lx1NCpKwSKyAuAzwLeecu3ngP8+Ynzjw5tH7/l518HvA7gec973mkve52jdU9E0aSEmIhJSShH67IpvEbzDMAA65gHtjS0l+SF3F7a+YWbNuQWjB9mAOQqbkcMjqDsnj+7s4q/2s+SDr6y9G2PirA7KzcjsGLw3mLFIMaiSYlGsIUL0xhjaCpyXPwwE6iqcdQsHiWq9ENY3PG+Sh8S1Tk7zicrVXkuzzMisgP8EvCtqnq7SoNPiaq+CXgTwEtf+tIzD5NKIsUEStY+j5GUElo4dcvYHAFTAQuXS1V2Q3tJHnoQ+Ms7tBcktXBArlH8wAI+scylK1Nh5avFbM4De4nHD49YHkScCzywN2cxK6c1VFeOapVuzPkt2JTX40tjjKEqXAv4mYKqEqJeD7FNqsSo+HMOlbvQT4WIeLIT+BlV/eXbvOVj3KwZ9tyh7VxRgaMugUl4aem7AKl40BBKrvkp5KWhirwGXnr6XjXZQbXA/cAjDA6rcE3IaHNmcQQOlzli6L6hvSTWgBhhMWuI6rASECOUlM+praOuIqqaP1xqECfUxTOLN5Mpe7eQFCpvUOV6lJX1OSv7PLmw3h90it4MfEhVf+AOb3sr8DVD9NArgWuq+vE7vPdpUyXJmcURnHWkCEFze0kWTf4H5BJ5NwrVLAoPuEdHWcLhMtlJXSafF5ZmQoYQ2waY+3z0Q3tJQowcriNdSChCFxKH60iI5XZ7nLfMvKN2lsoZapfPXeHydykl1t3gBIwhQT4vvIkNQ4ZzTHn5OKbsREfAJuokXOTjwecAXw08LCLvG9q+C3gegKq+EXg78IXAh8lLvl93EYYkJ1xusja7eM9sp6ELPcmVdQQ7TR78EzmhLEcL5/aS7C/zU7cAe8Cj5PP9wmGtzbChPifPTto+f2iawo5guepBlaQQ+4gIGJTlque+K2VsEskzkj6mrGFlEpUpX2wlhIQxN+QR8jHPEEouFx0vweTCQnL93FmK9pk1Qh8VY27YlZLiN12z+Omiqr/LU2S0a3a533RRNhzjTMW8qWlDj0mRRGTe1DhTWHTODFXKgGoG64MhgaT0E26fJafzLQqHwzEUlsdeNHkWEMmRQpF8XnwG1Xf0UfHWY7wjBaGPPUd9uVzsGCPLNmFtlqGOsWfZJnaasjFpxzOBkxhjis8IUrrhBOD4mAfdknWLrTUkzbMTBVDFGrkp/PY8KL9guAFmLssCe+uZN3OOVj1tCMwKzwhChN0q71XUFezWWRumeNW+vK9OJG/MXjvRXpJ6Fx5oYN1lsb49k5PJ6t2ydqkqoYtQCUaFlAKhi2jBTaguRKwFO0Qe5GMsXpjGMOQNnHAGY8gjUJ745H/8BF4SkayKkJIOmcWCMQWK198NVI2ncQ5rBNVEZQUrjqopXMhb80aj8VBVkCpIPee+EXRmHPhBlmlJDtEMQ3tJKgNSw94cmiuwvgpdzO1l7bKo6YkxkJJBNaBGqQqGf8UEzjmMCCJ5s1GMEAt/uJwzrLsEpOszgZQoHkV0LOWgynUpBxFGIYa3ieL1W+EIrFY03vCXVw8JZo1LkQev7GC17NJQ7WDVga4hWTg6yBufdeH/irdwL3kt/soluLqf1+IL7zNSVZbGR4zPN6mrc2W30kVN6tpR+TzoGutIMeX62AX/kc7kTWtxFtVh2SOm4olbY80jEIG+1+v7FyklUoSmKu8INsFWOIKj/oC/ePyQeV2xWFxhubzKXzx+yIueVVbIvnKDcqbNS0OdBVJuL8l998PuMmc57+/nFaHdob0klWmo/ZKDI+gSpDXsznN7Ubuc58pO1tRPajCVxxopqm7bVI79tsP0Aes8oQ8khKb0h4tx5hGogndyc5im2x4xvPKfig2wv2wRgYjSxUAcRML2l2UzkdTCYjEsBSnMmqFATeEn7+degfd8JE+R77kEj+3nDe3nFoqAOcaYyP4yh7EuKlgu841qTNl178o7Zl6JJFRtnspjqApWGHLWslNZQkwkck1gZw2utMb5SFFuX+il9B7BptgKR7AOyryuCSmy6juEfL4OZf/Jlry80ffgfE6Mcj63l6S5VLFnO45ijhSaAXOb20tycLRm/zBvEFufy3ruH+b2knhrsFawanNa+BAH7EtmlInQ1D5vMoogqhgj565Rc7cw5j2CTbAVjkAkcHW/zYNsHYltIPSB518pu1kcEywPoRrWvBnOY+ncmiTsPQt2W6j2oLsGps7tJbl6ADs7WU3TOajn4KrcXhJjDN7aHAJpBBCMGcO697DJKLI9axxPk2mPYAuYGcvj+0CCnfs6Dh8FTG4viRkG/4NDoMrH2pdX01z1PU7A7QIuH0Of20vSh7ynYk22xw5p2X1h2e7jYis9QhzivL2VomPvTU+4w4xABGRaGrotY94jOE4iO56pXET46Lh2bC6ITpWZzwPHehWwBmY+t5ek7XIOQTV84CqXz9vCNSHtMD02DuaLBcYNMhiFb4rGwWMH8Oij0PX5+NhBbi9J0kQbFZG8LyBiaKOStODUTnIt50SuUpbQXNt5Ox5wz8wd8wjKmHOdY7XRY9XkEBN9OH/5i62YEazagGvyeryd10TbguT2koRBdauaw+ISoNCtyxdjn80bnDkirmAlS9IKnMntJdmd3aibXK2y3MRxe0lS0iwxAYPK7XBeMGY/Rc0lIDG5EIwxCEqKpYe2kaI6SDncKKPZh3TuUg5nJQ4O4LpdkM9jwrnzm91thSMIoadd5w3G1HeklLV9QmnNBPJTdncISD6OYeY+r2p8dUTswToDNmF9bi9JNHClyjMmQ85zqKvcXpIcuWSGmzUnb6WkRZcVVHKGesqCHEQSBsM5jh0TG+CkE4A8SzEmt5/n4L0VjsBaZbmCqoXKKt1hjkO3hdc6qkFxdDaDZhdsyINc4fwoKmuRBF0A3yf6kKOGqsJeatWC2OwsrctHsbm9JMYIzoCxhmEVl0TKUTqF0JjoUxwK0wiahF4jdWn5krEigncyOHBFAL9FVdO24i9NQag8BMlS1EFypE4KZad9VZPt0JiXhDTm89K6/+u+p9MckeNrh6ug09xeknYNB6ss0HfpSj4erHJ7SbyzGCNoGsTBUnYCvuDjtwoYzE3yxQZTvAbHWDnulpP9dbK9FNbccE5wY+PYnvNDxlY4giiKc7CzgHrm2Fnk8MMopfMILGqzXg6Sj2pze0lWocOa7JSMtVTDRvsqlN3Fdm7Y5F/B8iAfZ0M+QVG7rBlupOMbVnPBlYJ5BCKGWW1viLwBs9oipYs3jBRjbkQMQT7mJb+yrsDaXKsYHT5bk/ro06fxDiGwWoOTQFjn5ZemYOYngBKRIZnMmHyUPreXpFtHxOQB1ltP71qS5vaSNDNYzHKeReWBWXZQTeHNYsh7BHkZxgwzg7L2OCO0Ic9MzJBHkJJSb9Fyx1kQEZzlpqUha88/TPPp2DWpj54TqrBaD6u3s6zwOdQSKUoIoBXUBuYLoM17F6FwXLyvLPSwThBMS2jBxKG9ILuNoZondubQ7C1YX1tyeJTbS5IU6sreyEo1FpGyKrLOGVZ9QjRhhmQ3RYqLzo2ZTah8Ph02YddWfCqUhDPDBqPLiSLOULx4vbqsmSMG1st8XFS5vSQ7vqLVXBReNZFaaDW3l+SBe+7lgXvyJnHo1lgLD9yT2yduRZjXlspZjEDlLPPaUn7Ve2KMbMWMICRD1YB2EHvNdW6b3F6SSmDZ5qL11Q60R1n/v3RWu60sjYVOIIaIulwO0haeEezNFzzr8oo+9IhboGGJd569+aKoXUZg1SWslevyBDEos5KlFwFr7RPCkbdFRO1u4hmdWSwiPyoinxCRD9zh+68SkWsi8r7h67svzJYU0QR2Ds2iws5BU24vikBcw7VDONjPx7im+ENbDIqphj2CyuEcmCq3l2R3UTFzFXvzXe7b2WVvvsvMVewuys5U8vqyIHB9fdkVXl8+tuUkx7ZNPHM4rp18nPmskM+fQZnFPw68AfjJJ3nP/1bVL7pAG4C8XtpH0B5sTIQ+J9uUXi/te6CCeZ0ziyVA0KG9IKvYkUKumlZXDW08JHS5vSS1a7i0WLBqV1m51cBstqB2heNthw29EHJBGsPw2SroCIwRQswRTMeZsqqMYg18E0+4dwubqqV8kcXrf0dEXnBRv/8sNHXNrGrpegh9QCPMqtxekqi57KKvAQuXL0Pf5vaSaABxOZLJGoMx+VxLi7uJsusttdshJcei3qGS3F7WsPzUZqzBDoNuGCQeSjHWKJjjvjke3I7PnX2i1s/E5mopl94s/mwReb+IvENEPu2iLpKi4jzs7cHlSwv29nKoZmndFWMEV4N4aBYN4ofyi4Vjl+va4zQXiD9at4QOnOb2kmhSVmqprGdvvkNlPSu1aPEiz+MkR5vcSJAaw0B7uydcEYrqMo2ZTS3xlXQE7wWer6qfCfx34Ffv9EYReZ2IvFtE3v3II4+c+UJV5WhqqJ1l5itqZ2nq3F6S+/YWebquIKpZ9VNze0lqa3NmqkDtXa6aJrm9KFbYdbnKVkgBZy27zkDp5Y5hjyDFRB8iKSbccR2AiZsYq8rnWNlUolsxR6Cq+6p6OLx+O+BF5L47vPdNqvpSVX3p/fefvXBu7Woaa+hDZP9oSR8ijTXUruzS0IOX9rj/CswrmDvHvIL7r+T2knjnmNWW3YXn8nzO7sIzqy2+cAqvx9HMZuwuZlzeW7C7mNHMZvjSwW+qdH0kpEEqOCW6PpZPVBkhx3USYhyklWMuYj+5zNuzqUCEYneQiDwI/JWqqoi8nOyUHruIa3kLXUo4C7P5gtWyo0up6BouQLOY89zL93AUW4yZk+YwtzXNYl7ULu8rnnP5EnnP2tDs7uCH9pLs7NQs+3UeQPoeK4lFbdjZKevQU0qsuoiRLMmRYiINxWrKFx4dF9teCezpsImEsgtzBCLyc8CrgPtE5KPA9wAeQFXfCHw58I0iEoAV8Bq9qCBnGUoHJiWlhEVII6jfWlnLvPHYaBGpUYXamuIqn01VoQh96HDWE2KPcxVNVdgR1BWPuEDtEtbWxNiiGHbqsnb1IeXlMyDE/HRrJLeX7LIxRueMuRLYWNnE//Eio4b+2VN8/w3k8NILJ0ZYeMey72j7DjHKwnti4TQCK8JBm4h9R9M0rNcdna+whW/WmYfDvqMxlkUzY3nUcth3zMruFeOt48rc08VITFA7R2Ut3pZdGgoxoSK5+MsQ0RFTXvooxXFhFVW9XrNYUg5zLekMrsfDnxj5pz2CO7OpKKutyCxuQ8t+F1jUcxbzPZZHwn67pg1lhezb2FN7w3y2h/MzQiUchZY2lk0kSFjumS1IgBGhqRvmQ3tJ1AizusKF4zIrFu8sWjjKSgQ06k07bpoUKdhdm6psdWZGWglsrDzj8whGhQjeQtJIGzqSxrw/UPjJO0TDldkCJd8Uxntq7wiFS24ltdy7mHPQtiQSjbPs1jVJyzqCNAxu1lmywLIQk+bykAXxzhJSQlOCQX3UDElmpdhUZauJi2VTeQRb8ZmoTAVRubrfEn2L7WF3Ibm9pF3OYiVhjcVYT4pKTJGqcD1BawJXVy279Yy6mtN2R1xdrXjwSmHZblXaLpBQFIsQMQiLgpo+kB1BOi5PKSBGihemGS1bXgnsrFyPFjrhDC4ij2ArHEFKLVf3s0ZwtajpVvk8pbJLQ5d3Kv780QOSKPQNsMaocHmncB6B84hRlu2SXqHrlogRald2kyBqYh0SoopxlhTy2nzUsjMCaw0uKZFsj+hQUKRgYRprhC4M/TLsEQBUhQfdvLDBTX0zFg2kMW6ub0oqZCscwcG6o9dcxAQRksnFTQ7WhbVzrOcoJpbLa1TVHl13jcVij9qWHXDFOi43Dcu+RTXhvGHha6TwpmzfR6wBZ33W7DaeEAN9X74Q73EW7/WN2REMIHns1xNLCVI8a32sGkhjlb7YlFTIVjiCdR/ZnUMfIYYe73Mx9nXhAeTa6ghLYrG7h9UaX+9hU+La6qioXZoiCWWnmiNSoWqJGtDCaq05MsflqlsmV22y6orX4U3X1+Nvfso97w29s6AKlTdPKJZTOkxzrBpIm9qUfTo8o/MIxkSMPYdrmNXg64Y+Ljlc5/aSPHZtTcTjkqGqarouEUg8dq1sNXYRoUtCJZHKG7o+0mn5m9UbgzOBlIQuKlYUZxRvSpcc3cyG3llQcsLWE9pLewLGWQnsuFdiTDctDZXvrc2wFY6g8Y71MnC0hFlYstrPkX6laxa3oSN0HeoqQteiKRJDR1tY9x+EvcpxHP84q2pmGildKKGuLH+9ingDs8rT9x1dEurCBXM2taF3Fo6lHK7PCMirVmbSP7o9qk/cU4nl91Q2xVb8lVYMKUFsoVvnY0q5vSRO4Grb0nYdYGi7jqttiyt8r3rn8L6mqj3zWT56XxfXGrJiuVQLqpHDozWqkUu1YEsG7LM5YbCzIAJ9UNLgoJIqfdDSEdNA7p+TWkNjmKVsqgDMWNmKGcE69jQz8JfALSpC1dH3ub0k86Zm5o/opcfEjl56Zt4yb8pq58xrT11HZJAgtWJQp8wLy1AnlD4ZrLXMnUM10CdDKjyBH+O691ilHMaa8ZxO7qkc95cXtkUdeyscQQhC04D1uY6raYYC6KGw1lBV8cDODmoE0QoVgySlKqzpM68r5nUcblYLmhAR5qU1ffpATBFrLIggWGKK9H35x9yxrXuPdY9gtBnPW85WOIKm9tS+Y940zOa7rI6UI9Y0hZ9w53XNoo5EjQgeJWHFMi9cOa3ynt1ZpO17kgpGDLX3VL5sf4WkKOb6sktKoBjCtjy2nYEx7lvAeDOejcBRGxEDIgbVhCaY19vhnLbCETxw5RIfe7zDK0hKNAq29jxw5VJRu+aVQzXSxYDBkgg0NreXRCQX8am9QzEIfoiNL2pWti1FWlVCG3BW8SJsycf4TIw1Xn/0HO+sb9mzxVbcQQ/uXeHevZbDgwOMJDCRe3d3eXDvSlG7RKDXvAZfuYou9PQqIxhwBWNtHvyNyaUgTdb2KYlB2W8jtTPUQ9TQfojsNtvx1HYWxrhvAePNeE6ao9JuzbvYlsnmVjiCeePYmzXszmqsmRFTjUGYN2X//FWI7NaeqBWowdUzrCirUD5T1gmkIdrEGBlHeJkRGpufbrs+IKo0dqipOfEExrZvAePNeB4zz+h6BKNCLDv1jD72iHFo8njrKaoTDHRdwvmaeeWx1hFjoOt6uq6sdo4AQXO9BO8sKUbCCNaXNQmzZtiwFgODGqqm0paNU6dmjIw149kIrLqEtcdZ64kYlFlhQcOpHsE50seEkOhiQGOHEKispS8sX1zXFtcmnMnLQWKEJLm9JGIEJwJyvOEIDkEKP7VZK7gE1lmG4ZYYYvGn3rHq1IyRsUYzHdcGPrZFuJjawGdlU9IXo5jxXzTrdsUjyxbnGnZnuzjX8MiyZd2uitp1eTajahyWXJjDkqgax+XZrKhdgmBt1v/vQyTFhLW5vSR581pZr1tWbc963aIodeEM8dvdrCK5feJmjqOZTjKGaCZEqLzFWYM1grOGytviNUvuKF9yztfZCkfQdkrlc/GQLvSElKi8pe3K3qiXFjMu10KXVjx+7ZAurbhcC5cWZR0BKKsuEVUxxhA1n5cOpbDD+rKx+UY1Np/bwjOVTd2sdwM57FcJIRJiIoR4XbSvJMdXt9ZkZzDIZJd2UJtynBfmCETkR0XkEyLygTt8X0TkB0XkwyLyhyLykguzxRnmzmFEiDFiRJg7h5TWZhdllQxz33D/PbvMfcMqGUTKJ/0YyVITzhq8cxjJ7WXtUhpvmfmKejg23hJj4WUFxvmUO0Yph7EyRpmQTdp1kSPhjwNf8CTffzXwouHrdcAPX5QhM2vYb9es2jUhJVbtmv12zaxg4RCA5bqnEUXEsGp7RAyNKMt16ZrFQuUsSYelIU35vPDQFmGYoQyDm6Z8XtSqcQ4iY9XOGesy2vEewfVEPMaxR7Apuy5sJFTV3wH++kne8iXAT2rm94HLIvLsi7Cl8oaj9Zpry2s8vlpybXmNo/Waypd1BAdHHYfBoGKZNTUqlsNgODgqWzBHUPqYB1nvLMaYYcO97M2qKXLU9qjmyA5VyeeF6ySMcRAZ64CbBgcVBqmJEBMhZnG8iXKU3GV7DvDnJ84/OrR9/NY3isjryLMGgEMR+ZMzXclYK67OC+8pXMG4qwAa2hUplhtFxBiMsSCQ4r0Y+xgopBRzJfSCiBlCl/RekMfyy8Ijbs50O1YGuxeRx/LoFstvYNzgPuDR0kbcwshsOvaQeh/IYNeoPMHI+us6/792Pf9O33hGhI+q6puAN53H7xKRd6u2Lz2P33WeiMi7NcRx2qVpnHalkdqlOiq7xmgTjPyzNdr+uhi7Sq6NfAx46MT5c4e2iYmJiYkNUtIRvBX4miF66JXANVV9wrLQxMTExMTFcmFLQyLyc8CrgPtE5KPA9wAeQFXfCLwd+ELgw8AR8HUXZcstnMsS0wUw2XU2JrtOzxhtgsmus3JhdknpcLKJiYmJibJsRWbxxMTExMSdmRzBxMTExJZzVzqCMclbnNGuV4nINRF53/D13Ruy6yER+W0R+aCI/JGIfMtt3rPRPjulTRvvLxFpRORdIvL+wa7vvc17ahF5y9BX7xSRF4zErteKyCMn+uufX7RdJ65tReT/iMjbbvO9jffXKe0q0l8i8hEReXi45rtv8/3zvxdzOvzd9QV8HvAS4AN3+P4XAu8gy8S8EnjnSOx6FfC2Av31bOAlw+td4E+BTy3ZZ6e0aeP9Nfz9O8NrD7wTeOUt7/lXwBuH168B3jISu14LvGHTn6/h2t8O/Ozt/l8l+uuUdhXpL+AjwH1P8v1zvxfvyhmBjkje4ox2FUFVP66q7x1eHwAfImd5n2SjfXZKmzbO8PcfDqd++Lo14uJLgJ8YXv8i8PlywXoTp7SrCCLyXOAfAz9yh7dsvL9OaddYOfd78a50BKfgTvIWY+Czh+n9O0Tk0zZ98WFa/lnkJ8qTFOuzJ7EJCvTXsJzwPuATwG+o6h37SlUDcA24dwR2AXzZsJzwiyLy0G2+fxG8HvgO4E6yKUX66xR2QZn+UuDXReQ9kuV1buXc78VtdQRj5b3A81X1M4H/DvzqJi8uIjvALwHfqqr7m7z2nXgKm4r0l6pGVX0xORv+5SLyNzdx3afiFHb9D+AFqvoZwG9w4yn8whCRLwI+oarvuehrnYVT2rXx/hr4XFV9CVmh+ZtE5PMu+oLb6ghGKW+hqvvH03tVfTvgReS+TVxbRDx5wP0ZVf3l27xl4332VDaV7K/hmo8Dv80T5dav95WIOGAPeKy0Xar6mKq2w+mPAH9rA+Z8DvDFIvIR4OeBvyciP33Le0r011PaVai/UNWPDcdPAL8CvPyWt5z7vbitjmCU8hYi8uDx2qiIvJz8/7nwAWS45puBD6nqD9zhbRvts9PYVKK/ROR+Ebk8vJ4B/wD441ve9lbga4fXXw78lg67fCXtumUd+YvJ+y4Xiqr+W1V9rqq+gLwR/Fuq+lW3vG3j/XUau0r0l4gsRGT3+DXwD4FbowzP/V58RqiPnhUZqbzFKez6cuAbRSQAK+A1F31DDHwO8NXAw8MaM8B3Ac87Ydum++w0NpXor2cDPyEilux4fkFV3yYi/x54t6q+lezAfkpEPkwODnjNBdt0Wru+WUS+GAiDXa/dgF23ZQT9dRq7SvTXs4BfGZ5vHPCzqvprIvINcHH34iQxMTExMbHlbOvS0MTExMTEwOQIJiYmJracyRFMTExMbDmTI5iYmJjYciZHMDExMbHlTI5g4q5liLP+XRF59Ym2fyIiv/YkP/PR43j8U17jp0XkzwalyPeLyN89xc98vYg8eOL8x0TkU057zYmJ82ZyBBN3LUNOwTcAPyBZpnkH+I/AN53zpb5tkHb4N8APneL9Xw9cdwSq+nWq+ifnbNPExKmZHMHEXY2qfoCsGfOdwHeTVRv/r4h8rWT9/veJyA+JyE33goi8ULKu/8+LyIdE5BeGjN0n4/c4If4lIt8rIn8gIh8QkTcOM5SvAF4MvGW4djXMWl4sIk5EHheR/zTMLn5PRB4YfteLJGv1Pywi/0FEHj/PfprYbiZHMLENfC/wlWQRr++XLMb2pcDfHp7kHbfPZv1U4PWq+jeANfAvn+I6X8DNwnf/TVVfBnw6WT/nC1T1LcD7gK9Q1ReranfL79gD/tcgpPd75NkDZFG9/6yqnw4Ul0OZuLuYHMHEXY+qLoG3AD81iIj9feBlwLsH+Yq/A3zybX70zwa9d4CfBj73Dpf4ryLyp2R1yu8/0f75IvIu4P3DNU4jk71S1XcMr98DvGB4/QqyAB/kQioTE+fGXak1NDFxGxI3dOcF+FFV/XdP8TO36q/cSY/l21T1V0Xk28i6Oa8QkTnwBnKVtY+JyPcBzSnsPDlDiEz36MQGmGYEE9vIbwL/VAbJahG5V0Sed5v3fZKIvGx4/ZXA7z7F7309MBeRzwdmZMfz6KAm+WUn3ndALr95Ft5FXs6CgqJsE3cnkyOY2DpU9WHyvsFvisgfAr9OVn28lQ8B3y4iHwLmwJue4vcq8H3Ad6jqY+Slog+S68uerBb2Y8CPHG8Wn9Lsbwa+c7D3k8hVvCYmzoVJfXRi4jaIyAuBXxw2k4szaNMfqaqKyFcBX6qqX/ZUPzcxcRqm9ceJiWcGLwNeP4S5XmVDNTQmtoNpRjAxMTGx5Ux7BBMTExNbzuQIJiYmJracyRFMTExMbDmTI5iYmJjYciZHMDExMbHl/D+pFajMuqMsngAAAABJRU5ErkJggg==
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[327]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># create a model on all binary features here</span>
<span class="n">model_these_features</span><span class="p">(</span><span class="n">binary_features</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Train Score: 0.012223180709591164
Test Score: 0.010119542202269072
[(&#39;has_bike_parking&#39;, 0.1900300820804082), (&#39;alcohol?&#39;, -0.14549670708138862), (&#39;has_wifi&#39;, -0.13187397577762405), (&#39;good_for_kids&#39;, -0.08632485990337223), (&#39;takes_credit_cards&#39;, 0.07175536492195503), (&#39;take_reservations&#39;, 0.04526558530451638)]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[328]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># create a model on all numeric features here</span>
<span class="n">model_these_features</span><span class="p">(</span><span class="n">numeric_features</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Train Score: 0.6734992593766658
Test Score: 0.6713318798120134
[(&#39;average_review_sentiment&#39;, 2.272107664209677), (&#39;price_range&#39;, -0.08046080962701445), (&#39;average_number_years_elite&#39;, -0.07190366288054284), (&#39;average_caption_length&#39;, -0.0033470660077835218), (&#39;number_pics&#39;, -0.00295650281289204), (&#39;number_tips&#39;, -0.0015953050789030726), (&#39;number_cool_votes&#39;, 0.0011468839227092916), (&#39;average_number_fans&#39;, 0.0010510602097447742), (&#39;average_review_length&#39;, -0.0005813655692094734), (&#39;average_tip_length&#39;, -0.0005322032063457423), (&#39;number_useful_votes&#39;, -0.00023203784758712564), (&#39;average_review_count&#39;, -0.0002243170289508221), (&#39;average_review_age&#39;, -0.00016930608165089726), (&#39;average_days_on_yelp&#39;, 0.00012878025876724556), (&#39;weekday_checkins&#39;, 5.91858075446039e-05), (&#39;weekend_checkins&#39;, -5.518176206974201e-05), (&#39;average_number_friends&#39;, 4.826992111583864e-05), (&#39;review_count&#39;, -3.483483763867104e-05), (&#39;number_funny_votes&#39;, -7.884395674567053e-06)]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[329]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># create a model on all features here</span>
<span class="n">model_these_features</span><span class="p">(</span><span class="n">all_features</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Train Score: 0.6807828861895335
Test Score: 0.6782129045869245
[(&#39;average_review_sentiment&#39;, 2.2808456996623683), (&#39;alcohol?&#39;, -0.1499149859346954), (&#39;has_wifi&#39;, -0.12155382629262958), (&#39;good_for_kids&#39;, -0.11807814422012454), (&#39;price_range&#39;, -0.06486730150041427), (&#39;average_number_years_elite&#39;, -0.06278939713895423), (&#39;has_bike_parking&#39;, 0.027296969912258707), (&#39;takes_credit_cards&#39;, 0.024451837853625796), (&#39;take_reservations&#39;, 0.014134559172965556), (&#39;number_pics&#39;, -0.0013133612300810522), (&#39;average_number_fans&#39;, 0.001026798682265563), (&#39;number_cool_votes&#39;, 0.0009723722734413303), (&#39;number_tips&#39;, -0.0008546563320881045), (&#39;average_caption_length&#39;, -0.0006472749798193465), (&#39;average_review_length&#39;, -0.0005896257920272468), (&#39;average_tip_length&#39;, -0.0004205217503405806), (&#39;number_useful_votes&#39;, -0.0002715064125617315), (&#39;average_review_count&#39;, -0.00023398356902508714), (&#39;average_review_age&#39;, -0.00015776544111326633), (&#39;average_days_on_yelp&#39;, 0.00012326147662885568), (&#39;review_count&#39;, 0.00010112259377390332), (&#39;weekend_checkins&#39;, -9.239617469646022e-05), (&#39;weekday_checkins&#39;, 6.15390912314705e-05), (&#39;number_funny_votes&#39;, 4.847935102518744e-05), (&#39;average_number_friends&#39;, 2.069584037376758e-05)]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[330]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># create a model on your feature subset here</span>
<span class="n">model_these_features</span><span class="p">(</span><span class="n">feature_subset</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Train Score: 0.00273518518581628
Test Score: 0.0026676219581159843
[(&#39;price_range&#39;, -0.05120519606891803)]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYIAAAEKCAYAAAAfGVI8AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjMsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+AADFEAAAb/klEQVR4nO3de5gdVZnv8e/PJNxCmqBpEg5JCJBwl0toQiCOgygIiEEHHBkHFNTJiCBBnIOD5wwMPM5FHi8IHMEcUEFwDA8ChusQBkYGB5LTCQm3AEbAgQySkJB0AgiGvOePqiabZl+qO11Vna7f53n2s6tWrb3qpcLeb69aVasUEZiZWXW9p+wAzMysXE4EZmYV50RgZlZxTgRmZhXnRGBmVnFOBGZmFZdrIpD0nKRHJS2S1FlnuyRdKmmppEckTc4zHjMze7ehBezjQxHxcoNtxwCT0tchwBXpu5mZFaTsU0PHA9dG4iFgpKQdS47JzKxS8u4RBHC3pAB+GBGzemzfCXi+Zv2FtOzF2kqSZgAzAIYPH37QnnvumV/EZmaD0IIFC16OiPZ62/JOBB+IiGWSdgDmSnoyIu7vbSNpApkF0NHREZ2d7xpuMDOzJiT9rtG2XE8NRcSy9H05cDMwpUeVZcC4mvWxaZmZmRUkt0QgabikEd3LwFHAYz2qzQE+m149NBVYExEvYmZmhcnz1NBo4GZJ3fv5WUTcJelLABFxJXAHcCywFHgNOC3HeMzMrI7cEkFEPAPsX6f8yprlAM7IKwYzM2ut7MtHzcysZE4EZmYV50RgZlZxTgRmZhXnRGBmVnFOBGZmFedEYGZWcU4EZmYV50RgZlZxTgRmZhXnRGBmVnFOBGZmFedEYGZWcU4EZmYV50RgZlZxTgRmZhXnRGBmVnFOBGZmFZd7IpA0RNLDkm6rs+1USSskLUpfX8w7HjMze6c8H17fbSawBGhrsH12RJxZQBxmZlZHrj0CSWOBjwFX5bkfMzPru7xPDV0CnAtsaFLnBEmPSLpR0ric4zEzsx5ySwSSjgOWR8SCJtVuBSZExH7AXOCaBm3NkNQpqXPFihU5RGtmVl159gimAdMlPQf8HDhC0nW1FSJiZUS8ka5eBRxUr6GImBURHRHR0d7enmPIZmbVk1siiIjzImJsREwATgLujYiTa+tI2rFmdTrJoLKZmRWoiKuG3kHSRUBnRMwBzpI0HVgPrAJOLToeM7OqU0SUHUOvdHR0RGdnZ9lhmJltViQtiIiOett8Z7GZWcU5EZiZVZwTgZlZxTkRmJlVnBOBmVnFORGYmVWcE4GZWcU5EZiZVZwTgZlZxTkRmJlVnBOBmVnFORGYmVWcE4GZWcU5EZiZVZwTgZlZxTkRmJlVnBOBmVnFORGYmVWcE4GZWcXlnggkDZH0sKTb6mzbUtJsSUslzZM0Ie94zMzsnYroEcwEljTY9gXglYiYCHwP+FYB8ZiZWY1cE4GkscDHgKsaVDkeuCZdvhH4sCTlGZOZmb1T3j2CS4BzgQ0Ntu8EPA8QEeuBNcD7elaSNENSp6TOFStW5BWrmVkl5ZYIJB0HLI+IBZvaVkTMioiOiOhob2/vh+jMzKxbnj2CacB0Sc8BPweOkHRdjzrLgHEAkoYC2wErc4zJzMx6GNqqgqSz6hSvARZExGONPhcR5wHnpW0cDvxNRJzco9oc4HPAg8CJwL0REdlCNzOz/tAyEQCHAQcD3Zd/Hgs8AsyUdH1EfKc3O5R0EdAZEXOAq4GfSloKrAJO6k1bZma26dTqD3BJvwKOi4i16foIkqRwDMkP+t65R1mjo6MjOjs7i9ylmdlmT9KCiOioty3LGMFo4PWa9TeA0RHxWrpsZmabsSynhmYDD0q6JV2fDsyWNBx4KrfIzMysEC0TQURcIOlOkquAAGZGxEPpss/pm5lt5rL0CADmAc9015f0PyLiv3OLyszMCpPl8tEvAxeRXN//FiAggEIHic3MLB9ZegTnAHtFhOd2MDMbhLJcNfQCyTX+ZmY2CGXpESwF7k2fJ/D25aIRcWluUZmZWWGyJIIX01dbzrHkasLf3v6usuf++WMlRPJOjqt3HFd2AzEmcFy9VURcLe8sHmj6cmdxvQPZrcx/aMfVO44ru4EYEziu3urPuJrdWdywRyDpOxHxNUk3k1wl9A4R8We9isLMzAakZqeGZqfvlxcRiJmZlaNhIoiI+eniXhHxjmQg6Uzg3/IMzMzMipHl8tHP1yn7Qn8HYmZm5Wg2RvBpkrmEdpF0U82mEcDqvAPrT5MFC+uMiU9W8bGYmQ00zcYI5pNMKzEW+D815WuBh/MMqr89W5MEdgCW1yk3M6uqZmMEzwLPAvcUF04+1tcsL29QbmZWVS3HCCQdLOkhSWsk/UHSG5K6igiuvzTKdlmnXjUzG8yyDBb/gOQB88+QjA+cCbScXkLSVpLmS1os6XFJF9apc6qkFZIWpa8v9vY/IIu16ftBIze+asvNzKosyx/F74mIpyQNjYg/Av9X0sPA/27xuTeAIyJinaRhwAOS7qx5qE232RFxZh9iz+wD74F/3wALVsO2wLqacjOzqsvyU/iqpC2AxZL+UdJXgCGtPhSJ7t/cYemrlOHZgw6E4elyd0DD0/IyHbtt78rNzPKQJRGcmtY7k+TBNJOAE7M0LmmIpEUkY7RzI2JenWonSHpE0o2SxjVoZ4akTkmdK1b0/rEII7YR+7XB8bvCjMNGc/yusF9bUl6mAyZCO7APcNxeW7APyfoBE0sNizG9LDezzVvLRBARz0TEHyJidUT8XUScBYzM0nhEvBURB5BcgjpF0r49qtwKTIiI/YC5wDUN2pkVER0R0dHe3p5l1+8wsm08n5g6mhFbwksvvcSILeETU0czsm18r9vqT5Mm7cWZh23Be4fBs0ve5L3D4MzDtmDSpL1KjWv6/kPo+Q+1b1peplP36V15URrdj1LmfSqNpgouewrhbXpZXpTDt+tdeVFOafBT0Ki8r5rdUPYe4ARgJ+BfI2KJpKOBbwDbA+/PupOIWC3pPuBo4LGa8pU11a4CLu5d+Nm0tUFX11YcddDBb5etemU5bSV/K9raYDy7cfa+279d1vXKK6XH9d42OGz/IXxmp41dk+eWLeW9Jcc1qi350d913KS3y555/jeMKjmuMW0wuQt2n7zx76OnF65mTIlxdffepuyysWz+s+X36sYAvwem7ryx7KHfDYC42uBwYPd9Rr9d9vTjL5X6bwjQ3pb86O82fuN38bf/tZT2fo6rWY/gKuAMkkRwhaSfAJcBl0ZEyyQgqV3SyHR5a+BI4MkedXasWZ0OLOlV9Bntu+MOrNyQ/PhD8r5yQ1Jepl1HbU/XhuTHH5L3rg1JeZk+ssdEVm1IfvwheV+1ISkv01F7TWL1huTHH5L31RuS8jL95QdHsi6SH39I3tdFUl6Wr0xLxsPmP5usz382Wf/KtNJCAmDmofAayY8/6ftraXmZTjxkNOs2JD/+kLyv25CUl+mje09kzYbkxx+S9zUbkvL+1PB5BJIeB/aLiLfSH/LfA7tFxMuZGpb2IznVM4Qk4dwQERdJugjojIg5kv6JJAGsJ3kc5ukR8WTDRunb8wgAli9fzmMvLqerK/lLfN8dd2CHHcpNBACvvPIKz7z8yttx7Tpqe7bfvtxEALB06VLueWopq7qSHsJH9pjIxIklD14ATz/9NHcv+Q0vdyU9hKP2msTuu+9edlj8+te/5vr7V/P7ruSvy7/84EimTSv3V/fWW2/nsl8nX9wxJEng4x8v/0Erv/zl7Xz/wY1xzTwUjj++/Lg6Ozu5cd5Lb/8bnnjIaDo66k7fX6innnqKf31iKSu6kh7CR/eeyB577NHrdpo9j6BZIlgYEZMbrZelr4nAzKzK+vRgGmBPSQu72wD2SNdFcnVo6UnBzMw2XbNEkHkw2MzMNl/NJp37bZGBmJlZOTzJgplZxTkRmJlVXKaZmNNJ4yaRzBX0m4jwVP5mZoNEy0SQ3k08C/gvkiuGxkr6q4i4O+/gzMwsf1l6BJcAH4mIpwEk7Q78Eih3QhwzM+sXWcYI1nUnAYB0+dX8QjIzsyJl6RHMlzQHuIFkjOBTwDxJ0wEiYk6O8ZmZWc6yJIIRwBrgo+n6WpLZbD9FkhicCMzMNmMtE0FEnFJEIGZmVo5mzyP4Hk0eLRkR5+QSkZmZFapZj+CxJtvMzGyQaDbX0NW165K2jIg38g/JzMyK1PLyUUlTJD0K/CZd31/SZblHZmZmhchyH8GlwHHASoCIWAx8KM+gzMysOFkSwXsi4nc9yt7KIxgzMytelkTwvKQpQEgaIuls4OlWH5K0laT5khZLelzShXXqbClptqSlkuZJmtDr/wIzM9skWRLB6cA5wHjgJWBqWtbKG8AREbE/cABwtKSpPep8AXglIiYC3wO+lTVwMzPrH83uI5gaEQ9FxHLgpN42HBEBrEtXh6WvnvclHA/8fbp8I3C5JKWfNTOzAjTrEfxA0g8ljexr4+mppEXAcmBuRMzrUWUn4HmA9BkHa4D31WlnhqROSZ0rVqzoazhmZlZHs0TQASwhmXSuT9NMRMRbEXEAMBaYImnfPrYzKyI6IqKjvb29L02YmVkDDRNBRGyIiEuAT5Ccslkrqav7vTc7iYjVwH3A0T02LQPGAUgaCmxHepmqmZkVo+lgsaQvkDyE5n8BbRHRFhEjIqKtVcOS2rtPK0naGjgSeLJHtTnA59LlE4F7PT5gZlasZoPF/wk8B/xJRPy+D23vCFwjaQhJwrkhIm6TdBHQmT7H4Grgp5KWAqvow6C0mZltmmaTzp0fEff0teGIeAQ4sE75+TXLfyB5roGZmZWk2RhBn5OAmZltPrLcUGZmZoOYE4GZWcU1Gyxu+gSyiPhu/4djZmZFazZYPCJ93wM4mI0Pqf84MD/PoMzMrDjNnlB2IYCk+4HJEbE2Xf974PZCojMzs9xlGSMYDbxZs/5mWmZmZoNAs1ND3a4lmW/o5nT9E8A1+YVkZmZFapkIIuIfJN0J/EladFpEPJxvWGZmVpSsl49uA3RFxPeBFyTtkmNMZmZWoJaJQNIFwNeB89KiYcB1eQZlZmbFydIj+CQwHXgVICL+m42XlpqZ2WYuSyJ4M50aOgAkDc83JDMzK1KWRHCDpB8CIyX9FXAPcFW+YZmZWVGyXDX0bUlHAl0kdxmfHxFzc4/MzMwK0TIRSPpWRHwdmFunzMzMNnNZTg0dWafsmP4OxMzMytFs9tHTgS8Du0l6pGbTCOA/8w7MzMyK0ezU0M+AO4F/Av62pnxtRKxq1bCkcSTTU4wmueJoVnpDWm2dw4FfAs+mRTdFxEWZozczs03WbPbRNcAaSd8HVtXMPtom6ZCImNei7fXA1yJioaQRwAJJcyPiiR71/iMijtuU/wgzM+u7LGMEVwDratbXpWVNRcSLEbEwXV4LLAF26kuQZmaWnyyJQOkNZQBExAayzVq6sQFpAnAgUK8XcaikxZLulLRPg8/PkNQpqXPFihW92bWZmbWQJRE8I+ksScPS10zgmaw7kLQt8Avg7Ijo6rF5IbBzROwPXAbcUq+NiJgVER0R0dHe3p5112ZmlkGWRPAl4DBgGfACcAgwI0vjkoaRJIHrI+Kmntsjoisi1qXLdwDDJI3KGLuZmfWDLHcWLwdO6m3DkgRcDSxp9KB7SWOAlyIiJE0hSUwre7svMzPru2b3EZwbERdLuox0wrlaEXFWi7anAacAj0palJZ9Axiffv5K4ETgdEnrgdeBk2rHI8zMLH/NegRL0vfOvjQcEQ8AalHncuDyvrRvZmb9o9l9BLem734+sZnZINbs1NCt1Dkl1C0ipucSkZmZFarZqaFvp+9/Boxh4+Mp/wJ4Kc+gzMysOM1ODf0KQNJ3IqKjZtOtkvo0bmBmZgNPlvsIhkvatXtF0i6AH1dpZjZIZJkq4qvAv0t6huQqoJ2Bv841KjMzK0yWG8rukjQJ2DMtejIi3sg3LDMzK0rLU0OStgH+J3BmRCwGxkvytNFmZoNEljGCHwNvAoem68uAb+YWkZmZFSpLItgtIi4G/ggQEa/R4o5hMzPbfGRJBG9K2pr05jJJuwEeIzAzGySyXDV0AXAXME7S9SSTyZ2aZ1BmZlacpokgnUr6SZK7i6eSnBKaGREvFxCbmZkVoGkiSJ8TcEdEvB+4vaCYzMysQFnGCBZKOjj3SMzMrBRZxggOAU6W9BzwKsnpoYiI/fIMzMzMipElEXw09yjMzKw0zZ5HsBXJg+snAo8CV0fE+qICMzOzYjQbI7gG6CBJAscA3+lNw5LGSbpP0hOSHpc0s04dSbpU0lJJj0ia3KvozcxskzU7NbR3erUQkq4G5vey7fXA1yJioaQRwAJJcyPiiZo6xwCT0tchwBXpu5mZFaRZj+CP3Qt9OSUUES9GxMJ0eS2wBNipR7XjgWsj8RAwUtKOvd2XmZn1XbMewf6SutJlAVun691XDbVl3YmkCcCBwLwem3YCnq9ZfyEte7HH52cAMwDGjx+fdbdmZpZBs0dVDumPHUjaFvgFcHZEdLWq3yCWWcAsgI6OjuiPuMzMLJHlhrI+kzSMJAlcHxE31amyDBhXsz42LTMzs4LklgjSeYquBpZExHcbVJsDfDa9emgqsCYiXmxQ18zMcpDlhrK+mgacAjwqaVFa9g1gPEBEXAncARwLLAVeA07LMR4zM6sjt0QQEQ/Q4gE2ERHAGXnFYGZmreU6RmBmZgOfE4GZWcU5EZiZVZwTgZlZxTkRmJlVnBOBmVnFORGYmVWcE4GZWcU5EZiZVZwTgZlZxTkRmJlVnBOBmVnFORGYmVWcE4GZWcU5EZiZVZwTgZlZxTkRmJlVnBOBmVnF5fnw+h9JWi7psQbbD5e0RtKi9HV+XrGYmVljeT68/ifA5cC1Ter8R0Qcl2MMZmbWQm49goi4H1iVV/tmZtY/yh4jOFTSYkl3Stqn5FjMzCopz1NDrSwEdo6IdZKOBW4BJtWrKGkGMANg/PjxxUVoZlYBpfUIIqIrItaly3cAwySNalB3VkR0RERHe3t7oXGamQ12pSUCSWMkKV2eksaysqx4zMyqKrdTQ5L+BTgcGCXpBeACYBhARFwJnAicLmk98DpwUkREXvGYmVl9uSWCiPiLFtsvJ7m81MzMSlT2VUNmZlYyJwIzs4pzIjAzqzgnAjOzinMiMDOrOCcCM7OKcyIwM6s4JwIzs4pzIjAzqzgnAjOzinMiMDOrOCcCM7OKcyIwM6s4JwIzs4pzIjAzqzgnAjOzinMiMDOrOCcCM7OKcyIwM6u43BKBpB9JWi7psQbbJelSSUslPSJpcl6xmJlZY3n2CH4CHN1k+zHApPQ1A7gix1jMzKyB3BJBRNwPrGpS5Xjg2kg8BIyUtGNe8ZiZWX1DS9z3TsDzNesvpGUv9qwoaQZJrwFgnaSnNmG/o4CXN+HzeXFcveO4shuIMYHj6q1NjWvnRhvKTASZRcQsYFZ/tCWpMyI6+qOt/uS4esdxZTcQYwLH1Vt5xlXmVUPLgHE162PTMjMzK1CZiWAO8Nn06qGpwJqIeNdpITMzy1dup4Yk/QtwODBK0gvABcAwgIi4ErgDOBZYCrwGnJZXLD30yymmHDiu3nFc2Q3EmMBx9VZucSki8mrbzMw2A76z2Mys4pwIzMwqblAmgoE6vUWGuA6XtEbSovR1fkFxjZN0n6QnJD0uaWadOoUes4wxFX68JG0lab6kxWlcF9aps6Wk2emxmidpwgCJ61RJK2qO1xfzjqtm30MkPSzptjrbCj9eGeMq5XhJek7So+k+O+ts7//vYkQMuhfwQWAy8FiD7ccCdwICpgLzBkhchwO3lXC8dgQmp8sjgKeBvcs8ZhljKvx4pf/926bLw4B5wNQedb4MXJkunwTMHiBxnQpcXvT/X+m+zwF+Vu/fq4zjlTGuUo4X8Bwwqsn2fv8uDsoeQQzQ6S0yxFWKiHgxIhamy2uBJSR3edcq9JhljKlw6X//unR1WPrqecXF8cA16fKNwIclaQDEVQpJY4GPAVc1qFL48coY10DV79/FQZkIMmg0vcVAcGjavb9T0j5F7zztlh9I8hdlrdKOWZOYoITjlZ5OWAQsB+ZGRMNjFRHrgTXA+wZAXAAnpKcTbpQ0rs72PFwCnAtsaLC9lOOVIS4o53gFcLekBUqm1+mp37+LVU0EA9VCYOeI2B+4DLilyJ1L2hb4BXB2RHQVue9GWsRUyvGKiLci4gCSu+GnSNq3iP22kiGuW4EJEbEfMJeNf4XnRtJxwPKIWJD3vnojY1yFH6/UByJiMskMzWdI+mDeO6xqIhiQ01tERFd39z4i7gCGSRpVxL4lDSP5wb0+Im6qU6XwY9YqpjKPV7rP1cB9vHu69bePlaShwHbAyrLjioiVEfFGunoVcFAB4UwDpkt6Dvg5cISk63rUKeN4tYyrpONFRCxL35cDNwNTelTp9+9iVRPBgJzeQtKY7nOjkqaQ/Pvk/gOS7vNqYElEfLdBtUKPWZaYyjhektoljUyXtwaOBJ7sUW0O8Ll0+UTg3khH+cqMq8d55Okk4y65iojzImJsREwgGQi+NyJO7lGt8OOVJa4yjpek4ZJGdC8DRwE9rzLs9+/iZjH7aG9pgE5vkSGuE4HTJa0HXgdOyvsLkZoGnAI8mp5jBvgGML4mtqKPWZaYyjheOwLXSBpCknhuiIjbJF0EdEbEHJIE9lNJS0kuDjgp55iyxnWWpOnA+jSuUwuIq64BcLyyxFXG8RoN3Jz+fTMU+FlE3CXpS5Dfd9FTTJiZVVxVTw2ZmVnKicDMrOKcCMzMKs6JwMys4pwIzMwqzonABq30OusHJB1TU/YpSXc1+cwL3dfjZ9zHdZKeTWeKXCzpQxk+83lJY2rWfyxpj6z7NOtvTgQ2aKX3FHwJ+K6SaZq3Bf4ROKOfd/XVdGqHvwF+kKH+54G3E0FEnBYRT/VzTGaZORHYoBYRj5HMGfN14HySWRt/K+lzSubvXyTpB5Le8V2QNFHJvP4/l7RE0g3pHbvNPEjN5F+SLpT0/yQ9JunKtIfyaeAAYHa67y3SXssBkoZKWi3pn9PexYOSdkjbmqRkrv5HJf2DpNX9eZys2pwIrAouBD5DMonXxUomY/skcFj6l/xQ6t/NujdwSUTsBfwB+OsW+zmad0589/2IOBh4P8n8OUdHxGxgEfDpiDggIt7s0cZ2wK/SifQeJOk9QDKp3rcj4v1A6dOh2ODiRGCDXkS8CswGfppOIvYR4GCgM52+4k+B3ep89Nl0vneA64APNNjF9yQ9TTI75cU15R+WNB9YnO4jyzTZr0fEnenyAmBCunwIyQR8kDxIxazfDMq5hszq2MDGeecF/Cgi/q7FZ3rOv9JoPpavRsQtkr5KMm/OIZK2AS4necraMknfBLbKEGdtD+Et/B21ArhHYFV0D/DnSqeslvQ+SePr1NtF0sHp8meAB1q0ewmwjaQPA1uTJJ6X09kkT6ipt5bk8Zu9MZ/kdBaUOCmbDU5OBFY5EfEoybjBPZIeAe4mmfWxpyXAOZKWANsAs1q0G8A3gXMjYiXJqaInSJ4vW/u0sB8DV3UPFmcM+yzg62m8u5A8xcusX3j2UbM6JE0EbkwHk0uXzk3/WkSEpJOBT0bECa0+Z5aFzz+abR4OBi5JL3N9hYKeoWHV4B6BmVnFeYzAzKzinAjMzCrOicDMrOKcCMzMKs6JwMys4v4/hA9Hnvg1ovIAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Danielle's-Delicious-Delicacies'-Debut">Danielle's Delicious Delicacies' Debut<a class="anchor-link" href="#Danielle's-Delicious-Delicacies'-Debut">&#182;</a></h2><p>You've loaded the data, cleaned it, modeled it, and evaluated it. You're tired, but glowing with pride after all the hard work. You close your eyes and can clearly see opening day of Danielle's Delicious Delicacies with a line out the door. But what will your Yelp rating be? Let's use our model to make a prediction.</p>
<p>Our best model was the model using all features, so we'll work with this model again. In the cell below print <code>all_features</code> to get a reminder of what features we are working with.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[331]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model_these_features</span><span class="p">(</span><span class="n">all_features</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Train Score: 0.6807828861895335
Test Score: 0.6782129045869245
[(&#39;average_review_sentiment&#39;, 2.2808456996623683), (&#39;alcohol?&#39;, -0.1499149859346954), (&#39;has_wifi&#39;, -0.12155382629262958), (&#39;good_for_kids&#39;, -0.11807814422012454), (&#39;price_range&#39;, -0.06486730150041427), (&#39;average_number_years_elite&#39;, -0.06278939713895423), (&#39;has_bike_parking&#39;, 0.027296969912258707), (&#39;takes_credit_cards&#39;, 0.024451837853625796), (&#39;take_reservations&#39;, 0.014134559172965556), (&#39;number_pics&#39;, -0.0013133612300810522), (&#39;average_number_fans&#39;, 0.001026798682265563), (&#39;number_cool_votes&#39;, 0.0009723722734413303), (&#39;number_tips&#39;, -0.0008546563320881045), (&#39;average_caption_length&#39;, -0.0006472749798193465), (&#39;average_review_length&#39;, -0.0005896257920272468), (&#39;average_tip_length&#39;, -0.0004205217503405806), (&#39;number_useful_votes&#39;, -0.0002715064125617315), (&#39;average_review_count&#39;, -0.00023398356902508714), (&#39;average_review_age&#39;, -0.00015776544111326633), (&#39;average_days_on_yelp&#39;, 0.00012326147662885568), (&#39;review_count&#39;, 0.00010112259377390332), (&#39;weekend_checkins&#39;, -9.239617469646022e-05), (&#39;weekday_checkins&#39;, 6.15390912314705e-05), (&#39;number_funny_votes&#39;, 4.847935102518744e-05), (&#39;average_number_friends&#39;, 2.069584037376758e-05)]
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYIAAAEKCAYAAAAfGVI8AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjMsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy+AADFEAAAgAElEQVR4nOy9f5Bl21Xf91l773POvbe7Z+bN0+ihnxbG5ofL4eezIMauskmwsSHCiaFQVewYG1tlHCxc4CJWYgubqqRCKo4JEAMKlEuEuCJKMVjIJmU5QBGXjcgTCAEWJrIkEOL9mDcz/eP+OOfsHyt/7NMzPfO6Z7pnbvfunjmfqq5zz+o7967pvn3W2Xut9V2iqoyMjIyMPLmY0g6MjIyMjJRlDAQjIyMjTzhjIBgZGRl5whkDwcjIyMgTzhgIRkZGRp5wxkAwMjIy8oRzqoFARD4pIr8qIh8WkecO+b6IyPeKyMdE5CMi8sWn6c/IyMjIyCtxZ/Aef1xVXz7ie38K+P3D15cCPzAcR0ZGRkbOiNJbQ18L/KhmfgG4IiKvKezTyMjIyBPFaa8IFPgXIqLAD6nqu+75/uuATx04/53B9vzBJ4nI24C3AWxsbHzJ537u556exyMjjwmqgICQ/xBRECnrU0qDksFBRwZ1A2PKOZeSkvSAb/s+iRT16zc/vUN3iL0BPvt1l0/0Wh/60IdeVtVrh33vtAPBH1HVT4vIq4EPiMhvqOrPn/RFhgDyLoBnn31Wn3vuFemGkZGRA8SYSKqo5iAg5OubEcHachsBq84TE6jq7QuuiGANTJuqmF+78xWLztOHREiCM0rtDBtNxaXNaTG/3vS3/tmR33vuv//qE72WiPzWUd871UCgqp8eji+JyE8AbwYOBoJPA284cP76wTYyMvIIJFViytdaEUFVSQkwii3olwH6GHOAEkFUEYHKlPQKYoy8uLNktepQqRHtmU4bfs/Tm0X9OitO7dZARDZEZGv/MfAngF+752nvA/6LoXroy4AdVX2ekZGRR0KTAvluGxiOOtjLIQIhgRihchYxks8Lb1nNV0tevLHH3qpntQrsrXpevLHHfLUs69gZcZorgmeAnxg+iA74x6r6f4nIXwVQ1R8E/jnwp4GPAUvgL56iPyMjTwxiBIYtmP0VAQhSuDxEEaa1wYdE7wNWYFoblLKR4OXtJfOuR1GsCFE7BOHl7SVv+Iyirp0JpxYIVPXjwBccYv/BA48V+C9Py4eRkScVIwJmyBFovswaM9gLoqqEmP3aD1AhKkbKrlRuLBbM2x7nKiqr+Agh9NxYFHXrzDiLPoKRkZEzxhghxXzx37/gqpatzAHQlFh2AWsFYywpJaJXKlP2UtT3PYtuRR2VVFu6vqcPLX1f1K0zYwwEIyOPISKCkUTfRyJggbq2SOG9oZhycjiXa6ahaijbS1Jbw/PXb/HyNmgF4uFVV+Czr20U9eusGAPByMhjSEqJxcrTh0DCYEj46NicCcaUCwZRFU2JLsTbZZqNs0QtG6B297b5xPOQIly6Bju3YG8FX/SG7aJ+nRVjIBgZeQxp257tZZ/zAsaQUmLZ9zgDs9mkmF/RB67vrUgxgakgeYw1vM6Uq9UH+MSLc3Z28sopCnRziIP9SWAMBCMjjyHzticBzrhhBeAIKTBv+6KBoA0912/u0QWP0KB0NK7i6Y2yfQSffglWwB5waQ92ga3B/iQwBoKRC0VKiRASidwE45wputVxXulj3hAKMZFCwsh+M1cq6tfNnQW3lh1WoaoF3yeWfcfNnQWvvfZ0Mb9eeiHXsAvQA9vAi8BnvFDMpTNlDAQjF4aUEm2f7truaPvEpGYMBvfgBF7YXRJSIqnDSMAZw2dcLrcagFymuVotCWKgj6Aep4kbi7LVTPtVogrcOsT+uDMGgpELQwh3ggDsH/MKoa7HQHAQI4kXbuzSxZ7KzPBpSWNrXnulLurXYm/FJ29toyFQTS/hV7uIc1ydlv39ffSE9seNMRCMXBgSr7zz318ZjNzN7qJl4XtCCEQX8CEQXLa/utwODLvdHi+82CEO6jinn0c0RHaf3ivnFNCe0P64Md5GjVwYDLziop9SGj/Eh/DCzhzfR4KarKipBt9HXtgpWwWzs7uiixA8xJQIHrqY7SPlGFcEIxcG5wxtn4B0eyWQEuO20CHs7S64Pl8gGGw1JfoVSuJyXXb11IaIX8FuDzKPqIdpne0j5RgDwciFwRhDUyl9H+ljwgJNbc9FojjLPOtt7X9j5LbyZwmWYcWnbu4waxyzqWW52mPZBV57qezPajGH396BGrjcwM4Krq/gs5+Mcv1zyxgIRi4MqkpSoaod9b7GvoJRLXrR3RdOO6j9H6LiLMX8Cj5ihtFkKnk6jZFsL8l8qNEXIGzDTnaRedkUwRPPGAhGLgwp3bnYwh2N/ZQUa8uOOTxvfql1zKwhxsDuYoGLgZk1qC37J7+3zI1bLTn5vw1MBvtIOcZAMHJhUPLdt/fxroay0lNNzqNfE4TdLuE7cBuesICqSUwK6/7f3L5Tm79DlnFYDPaRcoyBYORQztueN+xLGEfEgIghaqJvE7PGQsE5vJoSe6seH+JtgbfKWbamdTG/kgncvAHJQ0OkuzVI+3xWKOLPPgebtcIR9pGzZwwEI6/gPO55Qx7IHlLCqCAmj11MqsQoVOXmntN7z829DjGKMRUpeXQVaJxQVWX+xLb3Vvn358DafBTJ9pLcPKF95GwoX24xcu44bM97X0O+JCEp1pi7/LLGEAr7NV/2BE2ESK7ZjxA0MV+Wm2qys9djBZoGUshHK9lekqOke54QSZ9zy6kHAhGxIvLLIvL+Q773jSJyXUQ+PHz95dP2Z+TB7F9WY0yEmIiDUFnZy20eyB5joO0881VP23liDMUHsi+DJ0QlISSFhBCisgy+mE+th+vb8OJLsDvPx+vb2T4yci9nsW79VrJkx6Ujvv8eVf2WM/Bj5Lio4qPezguoKj4kqoKVOQBI4uV5j0VxVU3reyLCa680Rd3SkNhb9oCgOIQAKDNbTtcndPBbHjxw9WbeeqkifHFXzKWRc8yprghE5PXAVwM/fJrvM7J+VPWuFYFq6fUAeB8RTWCEEPNRNOEL18Ybo9zYmfP8jZu8fGuP52/c5MbOHGPK/cy2d2EOLMmyykvy+fZuMZdGzjGnvTX0PcB3kEuGj+LPishHROS9IvKGU/Zn5Bgor0wKi0jxraE+KnVd4azFWYOzlrqu6GNZz9quZxkCBoOzDoNhGQJtV24//uUbOQAIOQjs6+y/fKOYSyPnmFMLBCLyNcBLqvqh+zztp4A3qernAx8A3n3Ea71NRJ4TkeeuX7/+UP6cxzvc84oOyWLnhguus4hQfC8elBQjKWoeuBLzeensxW7naSRvCC36jgA0Iux25Tbkbw23XpEs5xDvsY+MHOQ0VwRfDrxFRD4J/B/AV4jIjx18gqreUNX9XcsfBr7ksBdS1Xep6rOq+uy1a9dO7Mh++eP+na5CPh+DwaGIEVQhhEiIiRAiqtleksoK8y7iY8QYg4+ReReL5y761rPnI71PiFh6n/J5wczs/oVfuSPjcNA+MnKQUwsEqvoOVX29qr4JeCvwM6r65w4+R0Rec+D0LZzSHIjzWg55XhF4RZBU1cI9qWCNZaPOw2i63gOJjdpgTdl5t4nAfL7Hqm9Z9C2rvmU+3yNRrnnrYJq6P8I+MrLPmXe7iMh3Ac+p6vuAt4vIW8hNhjeBbzyN9zxyz3tcEVwsRGgqh41p6OAVnC0vMWEwtEDbLZlKxapbgsm5glIc1V9XsO9u5BxzJoFAVX8O+Lnh8TsP2N8BvOO033//DvdgMDgPd7jnlYN9BCqCqGKtKZ4szmWtCQSEvMXnY4LCAT1ookmRZVTmqxUkZUYkaLkN+aN+IsV/hyPnkidCYsKY3OADensloEpRxcp9zqOmTxqS6nkLLfsSYsIK4Mptw6gqXR+Imm7X61sx6LTsx9j3gW2fqAWm9YTVqmPbJ3xfbmvoKCGJcQ7YyGE8EYFARHA25wT2VwLWlr/gnldNn3TbL0WMQVNCFSpb9n7Sp8iy9/R9QCUh6qlrh09lNzz6GNCuZa6wSpbYtVSS7aV4+YT2kSebJyIQwKBLcw5WAAc5jzr2D/KrJMtlx3zlscZgjCEmYb7yLJcdPFXOr84HYlVxuW6YzS6zXAp7fUfnywWCo+a8jPNfRg7jiQkE55HznMROmogh6+cY9gNT2eqcpfeoCtZVOOcIooSuZ+nLCug4Z7lUGaJEdldzjEQuVbn/ohTtCe0jTzZjICjI+U1ia9b9RzHWEWJEgzBxZcVqVYXaCTFGQlBEErUTVMv+xKa2Yrf3hN5jJ5vEdo6rK6Z2rNEZuRiMgaAgxgg+JFRTLoEcgkJV+IIbUxqCQPbDWEOKiZjKtqVOa8uL2z0iYG1DjD2q8MzlaVG/jI3sbHtaD01a0e3BpPKYzyzXvnXUO48NZSOHMc4jGHkFMYF19k6toebzWFieYOIsSgIdJEI0oSQmBbdgAHbmHcFAXcGknlBXEEy2j4xcBMZAUJDz2/GskPQurSFSLr8tirFsTmuMgxQjxsHmtIbCncW3+pYqQdvByzcXtB1UKdtHRi4CYyAoSFIlJu7SQIop20vijEERctuAybkMBGfKflx8iCjgrBuClMtNZaHshsfy1pLnd6CLMN10dBGe38n2kZGLwJgjKIgOfQ2qgrKfJFY0FRZ3qxwzDfQh0sWEFWVW22Lzd/fx0bNYBiZNRdXURK8slh6/WbZqqEuwdwNWk9w7sNyD0EL3uqJujYwcmzEQlEQghDzYxBhDSomUoHSxiTWCiGFSm7saymxh9dE8i0ZZtR20CfBYI8VzFzFksax5C0Fh3sFksI+MXATGQFAS3VdsyL0DRgRjtfhWvIhgROljJHrBGqW2tnwndspaQ0kVI0rSRFIpPidhscwKnzNgMoXU5Xr9xbgzNHJBGHMEBcn6/ncayPJRiuv+x5ToIwiGunIIhj5SvHwUEl3wpGGFklI+v/8AvDPwKuayzCXQtfkYB/vIyEXgiVkRnEdxt6N1/8v65X0EjUQV+hiwAkYS3kNTl9u32r/x9ymQNBA1YMRQvMjK5Iv/LrDbwgK4NNhHRi4CT0QgUNWhcUvvNG6l3LhVOhicR0JKzLtcr2+so4sBxBTPEYSYCN4zDx7RhErPpqvyIPuCLOfwElnrvyYHhJcG+8jIReCJuGe5Pas46e2v/dnFJTmvQ+JDCIQQMCbnBYyxt20l6bqOG53HqmNzuoFVx43O03VlG7e29/LmVMewPUQ+3x4V3kYuCE/EimA/CAD7+zG37SWFwTQdmJHAHZXPgvNMsl8IxtrbJa2KDudlVwStRuoU8Sg7yzmop06JVstuxm8fmAXpj7CPjJxnnohAkFcEg7jbEAhUFVNa3k3AewXS7TJNEGxd1i9rDJaeZRvog1A7ZVY7rCk78VZbpdVEv2pxlRD8krqu0bbwnIQDj+0R9pGR88wTEQiUYeCLE4zI7cErVVllgqGhLKGAxiz0JuegocxI4uV5jxNwVUPvO5Z9z6XCk8B66Xjxxi2cNZjakvoVYW/B731VU9Svg+nznSPsIyPnmVPPEYiIFZFfFpH3H/K9RkTeIyIfE5EPisibTsUHBOfkjuwzDOeFR0LqoPdvDJWzuakMKS4x4UNCVAkp0faBkPK5D2X3rLqVZxkju60nCuy2+bxblb33HgfFj1x0zuIW71uBjzJU1N3DNwG3VPX3ichbge8GvmHdDlhrMCkSUiRpbpZyxmBtaX19qOydXoLcUFZ8FjsrH5lUFRghb6AZSMrKl92L32l7KrIsdtv2NNaQNLHTlt2MPypVPWqPjlwUTvVKKCKvB74a+OEjnvK1wLuHx+8F/iM5hXpOI9CH3JEqw9ZQHxKFqyExQ0OZMZK3Ow6clySlREh5RkLOqwghJVLhhrIYQ95Gc4amqVFnslBfYS2Hg+uRyRH2kZHzzGmvCL4H+A5g64jvvw74FICqBhHZAZ7mnhnbIvI24G0Ab3zjG0/sRErD3bbZ187JttJyz264o0VzoxuqGMn2ktTOsPAtpvcYW5NiTxJ4enPy4H98ilgr7CwBAm66Q1il2/aSHPwjao+wj4w8DBMOHy+67r/EU7viiMjXAC+p6oce9bVU9V2q+qyqPnvt2rUT//uoMGkclbNYI1TOMmkcsfAWjLVDk9ZQxYQq1kjxLStnDJKUpJEQIkkjkrS4DHUt4D2EPm+fhT6fFy6yOnKSc+FahJHHgKMu+OsOBKd50/LlwFtE5E+T/b4kIj+mqn/uwHM+DbwB+B0RccBl4Ma6Hcm18Nx1gU0plS4eBXLvgLXmrlGVpUkKk8qRUBSLUGGQ4lIObciVXjFCigmRLNrXhvNTPnoc+8jIeeOBgUBE3n6IeQf4kKr+2lH/TlXfAbxjeI0/BvzNe4IAwPuAvwD8G+DrgJ/Re8V31kDlDKs+Aem23HOMyrQue4ebkg6aR3f82NdEKrndEdGcYFdQMYhaRLK9JF2MWAGpwVUV1B6Tsr0kL53QPjJyXDaA7SPs6+Q4V8I/TK78+azh668DbwF+VES+/aRvKCLfJSJvGU5/BHhaRD4GfBvwt076esfBOUtTGUQ1rwRUaSpTtKsYzq/EBFHxKd01Oc2nROm9NNFEHGYDz5o8GziabC/J9RPaR0aOy1HJ1aPsD8txtoZeA3yhqu4BiMjfBt4P/BHgOeDvP+gFVPXngJ8bHr/zgL0Fvv6kTp8UEaGuLMmac6k+etCP/T6HkhgnBB/p8KAJxGMxGFe2s7iZ1FSmQwVCCqhAZbK9JEeFodKi3SMXn2eA3zjCvk6OEwieAVYHzjvgGVVdisiFKZXOe/GlL7F3Y4wMqqjprhxB5Qr3NwQlaCL5hFhFY0KrbC/JlpuwtblEgGYyoaNHB/vIyOPI5avgbuYJeFeBm+SL9uWr632f4wSC9wD/RkR+cjh/C/AeEdkA/t163XnyUFViTKgIolq8YgjAayT5QfpiyBAnn/CFxd1mmxM2jaVNkRACFpgYy6xwWevIyGmxNc0d6mH4gny+NV3v+zwwEKjqd4rIT5OrgAC+VVV/YXj81vW6c3qcx8E0cV8VVe74ElMODCXzF30f8VERc2f7SlO2l2RqKnpVFotIvRnpFxGzaZiaUcxh5PHEx5zIdeRRqEvy+bqb/I9bPvpB4OP7zxeR16rq767XldNDB5G53CQrt8+dfWWy9iwJMZH0TlBSciVRaXnsLMWRcLj881FD1EAoPHuxjR2r1oPknx0Cq9bTxguzQzkyciKWbb7oTsiB4DJ5ZbA8rMvsEThO+ehfA76LXN8fuVOW/wfW68rpkdKdIAB3dP9Ll2nudzanxG3t/+xXMZeA4ecjBjGCsVkIj1R+mtut+ZJ5B34JhDwcuJpl+8jI44j3+SK9AUwMhJRHofo1N6kcZ0XwbcDnqeqFrYY7skyzsLqbCPigWMOd/oakTFzZC25tHbNGEWsAAWuprFDbsqIJL1y/xc1taGqoLfTA3na2j4w8jrgGJot8B64pHyeDfa3vc4zn/A45WX1hObdlmiKIRrwf5KjJEhNGyl5wZ9OaZhXp475aa6Rxltm0bJnmzV2Y70K8BHEFXQ+r3WwfGXkcuTyD1c18DWvIukM62NfJca44HwN+ZpgncHszVlW/d72unB7GCL2Pr6jOqUtPppG81FMUkSxAp2mYolaQxlmSSNZlso4UI0mEpnADXtfDXoAbN2G2DcuUh8V340jIkceUS5v5M74iB4AATAf7OjlOIHh++DpsnsCFYD85DHcniytXVtsnhoSIDmsBMGIAJYbhClcIVdicOJAKVTskjLX4nATf56XpDKhqSG0+92MgGHlM6fqcH3gKmG3BZC9via775uc45aN/Z71vefaEkLBWMGa4o7V5Pz6ERF1QbyiihKBEIqoGkYTFEF3ZK25EmE2avILCIGRhvFh6qZKG0jmg7/PRDPaRkceRZOG1m2BqqDdhs4LUZ/s6OTIQiMjfV9VvF5GfgFfK36jqf7ZeV06PRF4J5AvbnT6C0iMho48s+p4UFRWLaMRYobFl9+JFleA9QXOZprOKpojYsvX6yeVl8Q4gKS+XLw/2kZHHkUsz8t1OD7HPR8xgXyP3+xN6z3D8/vW+5dkjw0Qya83traHeR+rCkhM+BZZdYlo76qrCe1h2ga2m7MQtY5Tr8x6HUtUTVm1HQLg8K3zF9bmGeQps5tOsWT7qPY88pjxztUY/3qMW6iksV7l66Jmr671ZPPIvW1V/cXj4eap6VzAQkW8B/u+1enKKGCNo0NuVQzrsd5ceCRkCzGpDTIll22NFmdWGUDYO4H2iEiUmZdV5DEplsr00Pbm7UrmjuzIy8rgyqzbY3OxZLcG3eTdjczPb18lxNsj/0iG2b1qrF6eMGMO0sRjyQBoDTBuLFJ64JRZiEpyzTJsK5ywxCVK4mKkNEdUsPe19zJLUmu0l2e8bS+TqiXSPfWTkYTmqCGfNxTknJilsbcLWFdi6PBw3WfuQqPvlCL6BrCX0mSLyTw58a4vDZyWcWw5OKBtapG7bS1Ibg5iAlTywXlSIRqlN2UjQ9z0391qsNTjr6LvIInq21tzEclLm87wimJIrhzpynmA+L+rWyGPAJnDYx6h0INjrW3yAjQlIPUG1zWXU/Xo1Ju63sv5F8hbs64H/5aBvwC+v1YtTRgS8V8yBDt4UYVJ42G3T1GxEwcdAjCBENuqKpimblPUxsOhaRAxOlKAdqgkfy27E7K9HVtyti152nTLyOLAFvHCEvShJ8Qm0h8nE0Pa592jdS4L75Qg+AXwC+JdrfccCqELlhDwfXjEiWEfxunhnDNPaUqsZOngtVqT4kPjeJ0ICQ0BsRYyBhKEvnCMYZwOPnBZPndB+ZhihGi4H3vcIeRgTa85vPvCKIyJ/SER+QUR2RKQVkU5ELlRT//71PsZEiIkY0132UhiTFUf3NY9Us0x26SS2TwGJAcUQ0tBLEAM+lc1iH9VDM/aTjTwqmweKcLaOsJdgUlVgAQuVc7cfT6r17hoc59bzH5IHzH+c/DP6FuCB8hIiMhGRXxSRXxGRXxeRv3fIc75RRK6LyIeHr7980v/AcdCUWLYBP8g++5jPtbDMZxo6nMMwlyDERIhavL+BBLu+5+Z8h912lY++L964dVROeMwVjzwqk0mWTpiQm/onDOeFZx5Na4dJEFtYrVpiCyZl+zo5zqsZVf13IuJU1QP/q4j8MvC3H/DvOuArVHUuIhXwr0Tkpw8MtdnnPar6LQ/h+7GJMRFVcWboIxAhprwyWHNgPRF9H1BVKlcNoyoNMUb6PtDU5RwLybMznxOJuGAIYYnFEtJ6S9ZOyhgIRk6Lqs5SDleBK1PYXuULWFV4RRBiIpksL7G5eYW526bzwzyONXKcQLAQkRr4FRH578i6Qw8sa9G837GfiK+GryK3ulGhqexdOYKmssTCd94hKTHlQeyIAU0IQlh3bdgJWSxbupSobUVTNaTY0cXAYt3TME7IUYm74gm9kQvPtcvgXs7qnstVPlaDvSQJw6s3LUEMQmJjUnG5SaRjbeYcn+O82jcOz/sWcoHG7we+7jgvLiJWRD4MvAR8QFU/eMjT/qyIfERE3isibzjidd4mIs+JyHPXr598LMK+DPVBzoMMda7EybN+svid4GPMw+wLMu8CNimrvuPGfI9V32GTMu/K5giOql4tXNU68hiweTmvCGry3XFNPt8sHAgq69ivbNkXf8S6bF8jDwwEqvpxVW1VdVtV/46qvh24cpwXV9Woql9ILkF9s4j8wXue8lPAm1T184EPAO8+4nXeparPquqz165dO85b34WzQucTMaWsOZQSnU+4whITRoQQI8u2Y77qWbYdIUZM4Ulg3vfcXK5YtT1RYdXmc19Y5nOsGho5LazmG4qngMtX8rEZ7CWZVsKi7zAIk6rGkM+n1RlVDYmIEZGvF5G/ISKfN9i+SkR+HviRk7yJqm4DPwt81T32G6q6P+Pgh4EvOZH3x8QYw6QyGBk6i4V8XrhME3JNcCJH+4TmGuHCRA3sLWHlFZ8SK6/sLbO9JDdOaB8ZOS5tgI0NuHQZNjaH40a2l6R2NZeqBmvyDoI1cKlqqN0ZaQ2RL8y/F/h/gR8QkU8CXw68Q1Xf+6AXFpFrgFfVbRGZAl8JfPc9z3mNqj4/nL4F+OjJ/wvHQIS6soSQSIBBcM7kBG1BYkpMKkNVNeQNLIf3nli4mknVZG2hFqIsSC1ULttLclQ7+4Vqcx85l6jAbAPqGtxMqFH6PtuL+mUcl2dTFl1LipHaWjaaCWrOrmroS4HPV9U4XMhfAD5LVV8+5mu/Bni3iFjyyuPHVfX9IvJdwHOq+j7g7SLyFrJ0zE1yPmL9qOKHW+190TkfErUrrDVkLHVlSSndThbXVYUUXqhoTBgHtoJ6MqVnkRPta65UOCljH8HIabE1sVQu96jv3x9WLttLYjXQpsTmdJO62aTv5qxCj13z6vx+gaBT1QigqisR+fcnCAKo6keALzrE/s4Dj98BvOME/j4U+xd+kSxAp4OIWlU4R1AZwYeIswZF8qSylKgKaw1RQYy5dM5agxgIfbaPjDyOPPPUFvrb26xWUIvSL2DSZHtJ1BgExceO5Cti7HLxy5q3te8XCD5XRH5peCzA5wznQxGOfvFaPTlFYtK7unVFBJFsL3ltqyvLXheRFDHGEVNEVYrPUp5KTdVADLm0NUaommwvSc3hd/+FS71HHgNmTQUCKeUVQUqADPaSqGFiHW0KiCYiMLEO1rxNe79A8B+s9Z0KkoZAcDA5nFIiFa7XF2NonLDsPCElnEnMmrq4PLapDRMFrcEYi61BYraX5CqHC4NdPWtHRh47dtueqoKNWa7WNDNwVbaXxEiiV6WxDbVr6DXSp4CRM2ooU9V/v9Z3KogxQtsH+hiJSbBGqa1lsuY27ZPifcAHpa5r6jwtAR8U7wN1Vc63Cosa8B0gPXR5m6h6cB/hqXJU2C6tGTVy8bm5O8c6mGzAZHaJttnFd9leEhGDGEE1kEioBsQIsuZE4pMx4EkTu23ACbjKEbyn9YFJVfYOt/cxD4HxmvmjDRUAACAASURBVKfUaEREaLxQUswhpMCyzb0rToUQcwVRKCw6N5aPjpwW3udhTNbmmx1rLb1GvC8sci7C1OWhVc7WVHZKCHHtFY9PRCDwIeFI+KisfMIZHRK1iZKaUn0KrDqfFUhRhIgA08Kb3vNVRwLUkvdNbR4WP191D/qnp8pRYahwqffIY8CljSnm1opuEQm0xEXESLaXpHKOrWaCcw5rmixJY0NWIl0jx7olFpFKRP6AiHyeiFy44NGFSJuEmHKkjwnaJHSFRy/6LrDwkaSCtZakwsJHfGEphy6God8CnK2GTatsHxl5HHlqa4YP4D0E3+M9+JDtJdmcTrLSqAZiDKCBae3YnK73FvaBF3UR+SrgXcBvkyuGXi8if0VV/8VaPTlFfPCEPtFMcuOWdY6u7fC27NZQMlCLyXMJNCe0azGk0n0EmiCAtxCXc1IEEymugTRy8bEcPlGucME006pmaxN6D9PplFVaUVfZXpKNxpFQMIIzlpCyAsFGc/Yy1N8D/Meq+psAIvLZwD8FPm+tnpwigiEI0HucqwjBD2p+Za+4DktT56qmpAmD0tQGV/jPwmFYdOAUJlcdficQJNtHRh6F1wKfOsJeEo9wbWNKrwmxDZsuUYvBF5amNMZQGYfRiDMWwWLFrl0e5ziBYL4fBABU9TdFZLFWL04Z5wxTGwkJut7jjDK12V6SSWO5ufSAIsYQU65qmmwVThI4sAH6CH4noD1UlickozRymhxVBFF20gWkoLi6YVpVNNWMzld470mhbE1aH5TNaY0PCU2G2jVUztCv2a/j/Gn/ooi8D/hxcqXe1wMfHKQhGKQizjWVNUQsk9pQVfkX3IVEVXhryBmDtQKJoURMhiVgWb9im/CAjzC1sIqAzfaRkUfhvEqJTyeOlCK+V1QdwfckTUwnZe9+Qop4n1CRrIqA4H0ipPXmN4/zv9wCdoA/OZzvkae4fT05MJz7QOCs41KTWIXAfBmpnHKpcbg1a3qflISw2VRDfwPY2lJbSyq8HN3zHfPtHAjaBGGRVwR7vmzV0MjF5+Dl62C+oHCRJtOqxjqHqDKpKpZREHHFcwSkxNJHZlVF1VT4LrD0YWh9Xh8PvBKq6p9f6zsWQCRP+mlsxaS2aIwkpLT4KDFmsblp4xAxqObxmbGwuNt8B/Y8VAKXNuHWHFqf7SMjj8LBWpd0hL0EdVPxqukUtYLBMak2kKjUhSUmjLVsNQ6MEEPAOmHLOIxdbx7xyEAgIv+A+zRtquq3rdWTU0RTrtSXQW9IhiodLS0xIUdMTiscoRbLfLdWOehW+Zh8to+MPAqb+7XIwGXuSIhvFq5DqF3N1nRGFwLWVMSUaGq3dt3/k/tVUU8S3oe8TyBKNamo3XoD1P1WBL+21ncqyP6dRx8CSQ1GEpW1lN7xdtYiJtH1PYpFiEMHYeFiOgdNA80UZpeH4fArxmTxyCNTT2A23FDUwOyAvSSNM4jAtK4wUpE0oao0hQtKGif43qMyqH2i+N7TuDPqI1DVu6aQiUhzYJrYhSKmOIymtDhnSTGfT6qyO5NGIMW0/xvOXbwxT1AryVNb0H4S5h3s7EGI+YNSWJF35DFgaxOeXubP00YNG33uDN/aLOtXVVmss9hBZiJGQ5RsL4kYIWEwKWErS/SQBv2hdfLAcCcibxaRXwX+v+H8C0Tk+9bqxSmTopI00nrPfNXTek/SSIplt4bSMCehawOdj3RtwIdE0rJ+bVZ5ATAnKzDOyeeb4zyCkUfkqSswJVcJzSb5OB3sJREsm02F2HzjKJZ8Xrinpw/KlVnNbDbBWWE2m3BlVhcpH/1e4GuAnwRQ1V8RkT++Vi9OmYSy6hNJIyIVqh4jlq1J2Qtu5wNtH/ApkhSMBKqkdL6slMMy5EVKAhZtPspgHxl5FF79lOGZK4mUYLKVZx0Zk+0lURIxJKyxWQBS8rkW3kBOSRHj2KhygjjFSO/D2iX0jxMIjKr+1j0JzNLVXicihECMcRgDadEEvfeEUPiC23bsrnqMMcOkSmWVerYmZfeGbu7mC78FnAE77F7d3C3q1shjwKuuXuHaUzdpe3DTvCKY1NlekqSJZUhUIlS1xfc9reaO/5I0tUVbT4gBUdAUUBJNfXbJ4n0+JSJvBnSYP/zXgd98wL9BRCbAz5N/1w54r6p+5z3PaYAfBb6ErCb8Dar6yRP9D45B0qwvlBU+c8LFOkcqPJl61XtWrccYGSqIelJSVn3Zu6OdbdglN4tMZxDm+XxnnBI/8ohsNhOaCTknVgkuKM0k20sSgtJY8KrErgejNCbbSzKtKpwLpBjRZEBjVkqo1hsIjnPF+Wbg24A3Ai8CXzbYHkQHfIWqfgHwhcBXiciX3fOcbwJuqervA/4B8N3HdfwkZDE3BVV6H0CVWu4eX1mC3gf6EHKnYEh4n+hDyD4WxIecwFsBfZuPYbCPjDwKYhTvoQ9526MfFD/FFM7XofgoCIJzDkHwMQu8lcQ5y8RZnBWMgLOSz93Z9RF8mar+gqq+BLz1pC+suUB+f7xPNXzd+1P9WuDvDo/fC3y/iIjeW1z/iFRGWPhEZYW6qgihZxGUpzbKBgJF8SESjWLVElMgpYQW/vA1M4jzvETzIa8GmsE+MvIobM+XrDrQlJtjU4JVl+0lEVWQRGUqjDUYLL36bC9ISpqrHY0FY4fhIKw9R3C/FcE/FJEfEpGH3rwTESsiHwZeAj6gqh+85ymvYxAjVNVAlrJ4+pDXeZuIPCciz12/fv3EfhhrmFQml2umXJ45qQymsNaQId9xhBSJKeuHJBRTWGKiMjlB3JDrvBvyeeGBbiOPAS/d2qHvoNe8KugV+i7bS+Iqx6SqqSqDc4aqMkyqGldwZCxA1Hw9EDs0w1rBIMQ1B6j7/Wk/C3yULDr3UDITqhpV9QuB1wNvFpE/+JCv8y5VfVZVn7127dpD/HthWhlg2BpCmVYmi7wVxFihspZpVTOpKqZVTWUtxpb1qx7ePpCrAsI99pGRh2V7D17ehsUibwktFvl8e6+sX42tmDUGUqTvekiRWZNlaUqiSYmAwVA5i8EQYe2qCEcGAlVNqvo9wJ8hb9nsicju/vEkb6Kq28DPAl91z7c+DbwBYJh8dplTGEGbUmR7lSeBTZqapJLP16zgd1KccTTOEIKn7TtC8DTO4EzZu5CVZlngKblyaEo+X41T4kcekVUHfQ+rJXRdPvZ9tpekroRVn8AIzaQGk8/rqvQ8AsEZwTmDHY7OyNrzm/dd7IvIN5GH0Pw3wCVVvaSqW6p66UEvLCLX9reVRGQKfCXwG/c87X3AXxgefx3wM+vODwCEGBEdaoQBayyiiRDLBgJrYOUjQRNiDEETKx8pvGOFdrAAWvJqoCWfX8y+8ieTo1KJpSeBWfJFp3FQ1/lozoFfqlDVBmstxuTRsVVtKJwioHIOZ2DVtewuWlZdizOsfWbx/ZLF/xr4JPBHVfWFh3jt1wDvHkpODfDjqvp+Efku4LlhjsGPAP+biHwMuMlDJKWPQ8LklUBKg8ib5vPCe/F5EE3EGoOIYG4PpykboELKCWIYmsoO2EcuBpvkhNth9pJcugRPP5XznpWDjU2YTrO9JD7B5emEJJCSwRiD0WwviUFZ9hFBqCtHip5lH7k8PbuGsneq6r982BdW1Y8AX3SI/Z0HHrfkuQanihXQ6AkJfExUVqk0YqWssmDnFWcsfQy5YkgjtXV0vuxtyOLAfu3iCPvI+eaoT1Dp3b1nrm7wsRsLSFA3YDxgsr0kAogItbW5i1ITMcbCt4oQUgJNhKSkGDAkrJFsXyP3E5176CBw3nAWbiwDtUAzmdK2K3YVni48ErIPnsVqwSIGUA/Ss2EdfSiboHr5iM/YUfaR88cmd1Z199pL8pqnLrM1W+B7sM5g6kRVZ3tJJpXlxrxFfEBshUaPAq/aLNvo1vpIEosxirOOFCGJ0PrIOn9iT4SwcIxwqcmy0zFG6toyGewlaVcrfmd3wUbl2JhNWCxX3PIdr7tSdnDfUQW6Jy/cHSnFUS0fpVtBppMJzzy1QUqRyfQy7WoHYyzTSdkLbuVybiClCKooCWMs1Zobt06KDwGjUNdNFii2NX3f4de8T/tEBIKgMGtqgioxCdYYnAiFu8eZ956pNThbEWLA2YppSsx7X9SvoxJCD5MoGinDUXf+pVcEmIrPfPoqbUwkHGbqmFgDpuwqOCXYaCx9lCy7Xjtqa9Y9EfLEOGvp2ohvW6ytiNGTVNicnF1n8X0nkKnq/7RWT04Rg7LoA04MxlliCHQamRZuFtFkmE2mt+v0sYaZnWZNkZGRR+Co0RGlR0rU1mJcxdSBlYaoHTLYSxI0EdTgjBmSsoGg2V6S2hosPSlBn4YcgUC95v6G+10J9z8znwP8Ie4Mqf9PgF9cqxenjLNCjAk71ASrKDEkXOHGrWljWNxcYa3DVBUheLoYmF4tu186cvE56vJVOs2zMbG0vs/d81WF956EsjEpmyxOMSGqVHWV54cbR9/7PDiqINYabFUxMYJz+Rrhk2LXXGN+v2Tx3wMQkZ8HvlhV94bzvwv8s7V6ccoY47g0U/pBjtqIcmlWYwo3bm1Na/oQIPSI1Ky6JWDYmhaekwr0R9hHLgYH9QGfIatF3msvgbOOpq4hRipjcjONtThb9m/RWkvlsgxNzhXkWn1b+GZRjOXqLCeNfQhUVtiaOMSc0dbQAZ7h7utCP9guDCLgBNRYggpOLE6yvSyOp2ZTVn2bk2fOMq0nlE7dHJVDv1BDKJ5wDm4cLI6wlyCqcG1jg2QFjRaxFSYqsbDcS1M5YgqEpMQYsaLUldAU3j42QExCU1VMGoOmREzKustJjvO//FGy3tBPDOd/Bnj3mv04VUSVvS5RO6GpK7zv2etS8QllbQjU1iHTTYQaxVAN9pKc122FkeMzm4Brc9/AjCwlLoO9JNYYqsbl7ZfKIhjUJawpPCS+siz6RO3AOkcMgajZXhJrhKSK6DDaXJWkil2zxMQDA4Gq/rci8tPAHx1Mf1FVf3mtXpwySaG2idZH9laByiUmzrJm3aYTE31gtw/UxjJtKlZdxypFYmHh//PajDRyfCazHAgs+WtCXtFNCtePzhrH726vCH1ApEG1w9WO2VNl09jWWjbqSOsDXe9xRtmoHbZwEluMYVpbQky3lZPr2iJrDpzHXffMgF1V/UeDhtBnquon1urJKeJTZK8NdN6jWtF5j68qtqZlNztUFGLAq6J9R4gBUsz2kZFHYDaDjZs5eG+Sp0TJYC+JFei7CKI4yXLKfRcpvBVPUgWxTGqDmLwFA/luvDTGGGpjGMYYnsp7PDAQiMh3kiWpPwf4R+Rtxh8DvvxUPDoFVquWl27uEVWxkojaYaXlqYnAWvvzToZgEGtB05CvSIjNy+WRkUdhMsmDPTw5AFwm/+EW7tui9YnZLO9wi1TUesdekhgSxoDdT1pbQ4yRGFLRxMr+dtDBmfGqiqxZ/OI4K4L/lKwZ9EuDE78rIqXLkU/EznLF9qrDas4RdL0nirKzXBX1yxggBoIoKXiSRlzKH8iRi4Pj8GqckmlGJ3e28qYN+C6fu8J33l1MbE5qxFiSCkYcmiJd4TJNjCAqty+6+Wig8OpcjAB3+wUy2NfHcT6rvaqqSP6JiEjZgt+HYHvRkmLEWkcfQx71FiPbi7asY6osQ8KoMpla+j7Rn+Lyb+TJYX9ruwFm06z9Hw/YS1EZ4ZYPOKOIcYQUCCmy1RQuHxXJc0F8xEeobNYfqtY8JP7EKFROyG2xDGWjuvaE3XF++j8uIj8EXBGRvwL8JeCH1+vG6eJ9YOU9vSqVtfjoiSHgfdm/ij4mamtADUYEZyuQRF/47kg4/HNWvNr2nHJUar9kyl/IA4V6YD5MDp9S/nc4axyrl+b46BEmKC2VrZg9/dATcddE4tYyUluYNDV933NrGfmMy6WTxYIkQYTbKwJVQda8a3CcqqH/UUS+kixm+DlkeeoPrNeN08UZWAbPlKxEGkJgFTzOlN0w1ZSH5ESGZJUVLJbCXe3U5OTiYfaRi4FKDkQK1BPo58N54UigSYlJSQmcEWKCKLr20YsnpfeJzcYAhpQStXPULtH7RF3wg29EwCiq+7mBvKVs1twEdZxk8Xer6n8FfOAQ24Wgbio2qv0uwUTl8t5k3ZRd9lmBpe+xIZEmjtS2dM4Ur6A4SvKurBTeyEmIwy/r6hbMruR50zt7d+ylmPeeaV1j3BTEgTpSiMWFFoNCVVWkpBgYLri2+BRDY4QU88X/zoqAsx1VOfCVh9j+1Fq9OGUmVcPWZEplLJUYKmPZmkyZVGXlnpFE8J7gsqZIcBC8Bym7JBgbyk7GUXVnJRWj6hpe/apcLto0+fjqV1H07hag6xOudrjKYa3BVQ5XO7q+sKYPyqrtCTF37oaYWLU9tnD3jIhgTdZC8iGSYsIOQWGd3E999JuBvwZ8loh85MC3toB/vVYvTplJZamMwdkGKzVRFVFlUrhr0EehaWpiys0iQj73sfRO7shJeCPwq0fYS3H56Zqn255IThJvbeTGsstPF9axqoSbi0Bd57nAMSb6PvDUrGyyuHKG7VWkJlJVFT4E+qBcmpYt4VNVYgJjDXZYEcQEIrrWYHC//+U/JiuN/tPhuP/1Jar6nz/ohUXkDSLysyLyb0Xk10XkWw95zh8TkR0R+fDw9c7DXutRqWuHoqy6Fau+Y9WtUJS6Lvvhk6GpxmFISXHkOQkyNpRdKN701MnsZ8EbLl/GA0bh8tZGnr872Euy2dQgSvA93geC70E02wsixnJ1s6KyQhjE3a5uVmsXdzspKentRDHko0i2r5P7qY/uADsi8j8DNw+oj14SkS9V1Q8+4LUD8O2q+ktD38GHROQDqvpv73ne/6OqX/Mo/4kHEfpIFwN9ilSS8CliYiD0Zff/UkrcWiwgJdzEENo5GENKxceHjJyA2RE7jEfZz4JrVy6xaa9z/SYsw4K4hGtXs70kTVVzadKz6DtiCBibuFQ3NFX5UgTn3F3lopoztAU9ysn+e+/87/QTrI/j3BL/APDFB87nh9hegao+Dzw/PN4TkY8CrwPuDQSnzm67ovORumqoTI2YSOcDu23ZhrIQA3vLQBTYcIFFl7CastTEyIVhd+fO49cBnz7EftbM2x43hVddBTubECctbprtJVFRKue44hwYBynctpfEGsFHvSspm5JSlZahJt8w6tA6IGSliTOvGgJED4QfVU0icqI9FRF5E7k7+bBVxH8oIr8C/C7wN1X11w/5928D3gbwxjeefOd1sfKokJMtNs8kUMn2kqz6HmuzIBgJNkxevq/6sn+sIyfj1iqLcTXk/finyOW3twreZ7y4u4vFMrvUYOoZyRk63/Hi7mEj7c+OGJWqclTWYqwlRYuPkRgLBwJrSJpyVQ7AoPC57gEwJ0UEvM8Byphc2poiTOqzrxr6uIi8XUSq4etbgY8f9w1EZBP4P4G/oar3fgp/Cfg9qvoFwPcBP3nYa6jqu1T1WVV99tq1a8d969sEDfR9AAyGXCvc94GgZe+8F21AFZbDGLplyivRRTuuCC4SiZyInQJXTD5aylZZ7S07fFQighhDJN/x7i0P6xA5O0QM08piTL7TNQamlc1yDkX9EpyVO9o+5MmG667OOSk6dBabYZViRKicrH3H6jg//b8K/GHyivd3gC9luDt/ECJSkYPA/66q/+Te76vqrqrOh8f/HKhE5FXH9P3Y1GJJIhiEyjkMQhKhlrKJoJg8O7uwWkDbe1YL2NnN9pGLw9VpHv5yE9hN+bgY7KVwztCFhPc9Pga87+lCwrmyF9y6MiTAGcOkdjiTz+uqfHWOD+mu8lEf0tr34k/sF3klYK3B2Xw0xqy9qPU4ncUvAW896QtLDqU/Anz0qEH3IvIZwIuDltGbyYHpxknf60Fsbs24sutZhY7FClQ7rtQVm1tlNXmNSYSQu50hN46EmO0jF4dnroH7bWjJAaAld2E/c/LF69q4trFBXS1RIgZQInWV7SVpnKOyCdVESkODpxUaV7aCL4RI5xPWyu0tmM5n/f+q4JSy4jkCEfkOVf0fROT7OER6RlXf/oDX/nLgzwO/KiIfHmz/NUN5tar+IPB1wDeLSCAPUXqrnkII3nAV4gyVmtsDoMUZNlzZzmIfDJXL3Z7tIqABqirbRy4Opso5AkPOE0yGL1Pw43Xl0hav2piz6FZ431GZxJXplCuXCg+AcZZZUxFiRPMIe5y1WFe4pyfcCQLAcMyrgpK6c2eVI7hfqPvocHzuYV5YVf8VD9C4UtXvB77/YV7/JJgKUkgk8p5bIp+X/EPNRHwCTO747HtIKdtHLg6LVU4QW2BrCpdW+Te4KJgsbipHM51QWUfdbNF3BlO74jN4GcY/NpW7fYd7GmqaD+HWmZRpnhTVvGMQo+ayd3LuYt1u3a+P4KeG44WaT3wYq2XEVg6i4KwF8gi61bJwH0EMzBdZGlgbaDuIMdtHLg4h3EkMt20OAmmwl0KBmauRakJlJ3inqKbS11vECBp0qNwTRBVrzf/f3rnHSJbd9f3zO4/7qO6emX3hXeFdm4BFAgGMs34QEHFCHthBRgQSDOJhUGIgSIBJBApSQEQkihAQh1hgWZj3y4SXjGNbgCAQJLBjOzY2XkAOWMKWg73rnZ3p7qp77znnlz/Ore6e8fRst1VVp3b6fqRRVZ2q7nvmdt3zu+f3+P6Qwmmazgh9THkuywremKgKzyuNlcRLQ3WysniVe6jbuYZ+g9vYaVV9yQrnsVYOQo9JYGyNMRahhhQ4CGXTNIeQBa76BZgqP2bXUOnLdeI8WAOH5EZWMwNdzGnAJTMPkxp2q4aoCSMGKw4rhqSF3Y6qdH0gahpdQwkbDd6W3Z57bwkp5haVY6tKI4IvLEOTYiJEPTZQQIgpO9VW6E673T7xB8bHfwbcT25PCfAVwF+vbAYbQENikZSZESrrx1RNRUPZoGw/QDeMf08BY/PrwkKME+eksjk4XAO+gmaeXR5VwTXEmpwJ463DGEdKkRhjUeMEOSi7CBHJLYLRqAwSaYIpGpQ1xtBUSt9HYkpYoKrMUcygFKe6rFZ8nNu5hn5vPOgPqurDJ976DRH5uOIGpagqh9MFXewYEiTtcFpea2je5QXDmqwQGQ+za2heNtV7a6m5dZ+EwhqytDO4V6DX44DxnuTxUtTOZnHFFMec/UhUpS4clO1iBBVkmaNvDRqVLkYKZtvmSmIVfOWolpXFCkZXK+52XnJ9Azf0I1jWO6ySs6yEOyLyN1T1L8aJfRLwlGpX2XqPGmWI3Rh5X+BtRVu4DV3lcks8JDepQfLrwvZpaznty19aq3V3B5oWaoVqJ19UInm8FM46Kifsdx02CjF17NY1zhZO0xyyH94dpYsaAoFQuHn9rcTdIMtM2IJxAmuEfum5ONGPoFpxPchZvhWvAP6niPwF+Zp7BvANK53FmhGTAyzOVlSupg8hB1xMWV/8zs7YMS2OzcVjfl041Xtr2SPn6N9qvCR1lTt/VQ5292C/hz7m8VJEIiFCU9U5WByVEPN4SZw3LPplVfGYDpmyG6Yk25o1ZIyQkpLG2AXjeVt1Y5qzFJS9WUSeBfzNcehPVfUp5bzog7LjPUmyJaudx2geL0ntHIchICG30xyG7F4oXVyzrVwGPnLKeEl2ZjM+4a5D+gGM5GbxV3weL0XfZT0towZBEDUkSfRdWUPQOJdFFVNO5yYlnM3jJdlU4dZ5SUkxRjDGLid0Ynx1xzlLq8oZ8O1kTaB/JSLPEpFPVdU3rG4a6yVERaynEsGZmpAgqhIKC12FlNipIFb57jHNci56SGW3yZ5bt6UsXXZx2ve+dPmddxV3XToEEaTaQdsDUMW7cluCgOKNw1mLMw4juYgrFE4grSpHHTVn6JADxs7Y4vG6TRVunZeYjjOGluQUUj2TO+esnOV3/QTwduBzxtcfBP478JQxBM4BGhBToYzBnzTgSlcWL0a3QsoB49aBmDxekm01BNsaI7jU1jS1AwRbeyIOUC615cLYTgyNt1S2QoyjSkpvetwWiLtV3mKjjHUE5mMWuhIsxd2WQVkjgnXF2xFsjLN8Kz5ZVb+fcW1Q1UPKX3vnonUVgypPHF7joFvwxOE1BlXagndsALiUC8gUYhofYx4vybYuuKfZx8J2k91Zg3Ee5wyzqsI5g3Ge3VlTbE57Ow1WhEWYs+g7FmGOFWFvp9yc4NjV4ZzFWYNz9sgPXpJNpWmeFzuem2WsYtknwW46RgD0ItIyFpeJyCdz6yy+rUWMYlLEeYOq4rzBpFg8WGwFHnscTIT2Hpg/Bsnm8ZKcVsZQurzh5F3LjFzEdfN4CWpfcc+sYr8fiGHAO8tu5Yt23Zo5hwpYEayxxCSo5PGSpFHlM8Z0Q2Wxd2allbLnRnVsTCNHQeIhpOKNaTbVJ+Es34rvAd4MPCgiP0cWk3vZSmexZroh0qdENwxY44hpoPaebigbOBs6QCDanBAQx3jQUNjMnlZvXbpdzskmi4enjJdBENdy2VY01R6L/jpJxrzgUlih8ZYhAgrOWbwtf5cRQ2TexbzgGkGT0oeAweIL1zhkWQnNF+GRT6hwh7KxT0IISlI90hpatSvttoZglJL+U3J18QvIZ+VbVfXRlc5izVw/WLDfDZAUqYQhKEMauH5Q1qmwn6CpwHqwDnZ3sxLp/qRCfUvuOaWi7J7CFWWJxEwSOI9qpPEeYiAVbE3T9QlX1XhVjK1I0aIidH3ZL1eI+awYGe+8RUhk/f+SnNTyWbINriEdk1pOzi9ExctqC91uawjGPgFvVNXPAP7Hyo66Yfb7Of2ip2rbbO2to5/P2e/L9iymzxpDzkBVg3Y5H730rfcOWVf/VuMl2fEcGQLLsUbrTuEotqjhUA0672iaisWiQ7xHCur6hBSxMZCspe8GnAcbAyGVdaQlBW/z4j+EXPXsrVA4RICOBWXWJCV7JAAAIABJREFUHu9KUkpo4YnFsVHOkcuKnElkYsKtcAd1lm/FO0TkuSs7YgF0gAWJJ65f4+r8kCeuX2NBQgs7vesaFlfho1fho4/mx8XVPF6S075eZTfusAhZvsEC94yP9TheEpWIDD1iDSFGxBpk6FEp53o0wNVOGRaRqqkZFpGrnRaPpxiBPqSxkjcHQvuQWHHs89yIEUBuCMqCjOPlOGkEIO8KjBHiig3UWWIEzwe+SkTeT75RHNt66meudCZrJJnI4eEBYOilI/Y99IlkynYoqy3sA12Ce8ltDutxvCSn3WCXTh9VOS72CeOjjuMlSQGi99RiaOuGeRfojCEVNFDGCnuVosbSLzpsZdhLAVM6+DlmwQij6FxaTxbMeTEiqCRiVMYWIblRTeF0201xFkPwT9Y+izUjUVmEhDNKbRxdioSkSOGCsi7mP4AD+u7Y9VK4+HNrdwQxHHvNPNkYLMdLItZw2XsigqaEd44GRQpKfTrjsZUS44CvHCl12KrBFe7GJMbQeEMfIv2gWFEab5HCKp8iyzaxgh8LykJcqdLzx4U1MmYzHccIUtKVZzPdrh9BQ25c/ynAu4HXqupTsmPKoNAYmA+Jx/avYUOi9cJQ2C959Vr2c/dkIzAnyxlfvVZ0WqeGOEvHsE/eNF47ZbwElbNUztP4CmtqYnIshp6q4CriLHiTqFxFUoORCk2x+MKmqiQE7xzVqPufoLimz6Y6gZ2XTaWP3u63/RTwMNkIvAj4wfP8YhF5UER+V0TeKyJ/IiLfeovPiIj8sIi8T0T+WESec67Zn5F+GDgMecvXVDUJOAxKP5QNEly/Bo+TDcAw5MfHx/GSbKtryJANpSfrC/nxdenN+6WdltpZQuroY09IHbWzXNopJ6zsrEWMw4rQVPlRRsmJkujoFjpZUCbjeEnSKENtrME7i7GGpEIqbAlEBO8MzhqsEdxYc7HJ9NFPG7OFEJHXAm895+8OwL9R1XeIyB7wdhH5LVV974nPvAh41vjv+cCPjo8rJYSB6wfgBAbTEecQNI+XpFvARxnjAsB1clJMV7hU9rRYdWndfzU5LtCSdyczclVx6aZbs8pTWUMXDUaEhKGyhllVznQaY9mtLfNhoOsHnE3sVj6LlxVErMELN9zhemcp7YpfGiIZJ5LdMCnLwxdGRNYuhX07Q3C0SqpqOK8FUtUPAR8an18XkUeATwROGoIvBn5a877wj0Tkiog8MP7syhhixNjcAazyjs73mJjHSxIk39HCsb+7GsdLcpoIQVlxgqz5bxfHRmBOjls0JTuaAILgao9LFmMaUgJMVv0shiYQw917e1hriTEy73pKr2x2DMom5ahAyohiS2sgGYE0Nn85qieQ4gZqU9zOEHyWiCydFAK04+tl1tCZCzpF5JnAZwNvuemtTwT+6sTrD4xjNxgCEXk58HKAhx566KyHPWJIuW2gGnJ6n8kLbuFeGHmLTF7UKrKu/jYIOZ0m61xa7tm743OzNJwyjpdkUGVWOYakaARbebwRhoJuBescTSXEEHKqYYrZRVQ4SGCtMO/BWvCjgRoC1G35rCGM3tAJzJjyMtSb4natKlfyjRGRXeBXgG9T1Y/L+62qrwFeA/Dwww+f++pqnUVtNgZt2zJPHX3M4yVpfTYAEagF9jW/bgs747c1a2hWwX3k83V3A7LIc5oV1g6MIRHVUHuLbTwxDgwhEgv2xHbGUJlIT67mdRYqk8fLIjSVMIREPwSsQFMZSt/+GCOkyA3ZOaqsvAHMtrLWeykR8WQj8HOq+qu3+MgHgQdPvH76OLZSZrMaq9cZBgiHB+iQJVdms7Je70t3QfP48ev6xHhJTn4pTkpSl26XU1+CvQ+OtQSadygyjpfE2iyeJrJ0LTCKqRVscShwMEREFWM9IQwMolwqfJeRVFEM3puj3sA6uolK3mgsewMvlT6F8e96QXYEa7s9GHWKXgs8oqo/dMrHXg98zZg99ALgiVXHBwAa46lrofZweWdG7aGuhaZwTvVeA3fbvKBd3suPd9s8XpKTwhu7p4yX4EoFroa2hit350dX5/GS1N5T1w6jipHc8LyuHXXBnthRFRkX2BATaXwdS6dpJgX0hkpZ0OJZQ8u5WDtm6GxBj4RNss6bvM8Fvhp4t4i8cxz7LuAhAFV9NfBG4MXA+8ju8a9bx0TUCa0Ic1Hmiw4j0Iqgruwfemc3u4LmQDdq6FTjeElmjJWV5F2KJ7tjytZhQzMz7PmUi8pSFutrx/GS1N7RuoEuJkKMOKvU1lAXDF50faSuHHbZ4lA9MUW6vmyChBhBoxJCPFL5FBGktPb6BWdt31RV/QOexPE3Zgt987rmsCT1ibkKIcGsrTk8WDA3QiqsxGgU1OXOZHv3wfWPZLdH4TYJNJfh0hN5LhXZAMg4XhLvK9orC9oE9d4oxWHyeEmsCBFD5YS2roixJ6pgC95RqgEixJRQBCE34y2dajtmmtwwll0xkyEoSWm370Y4jB2HBxFV6PQ6dNBL5DCWFf7vNP8BugDXr0IIULs8XpKnXQH3RH7uOS4ke9qVUjPKeOfYbSGkfDPZtFm51ZdutgK0XuiD0g8BZ/LrkrcZHuFaCHhjsM4RQ2RIiZ3SKVYcC6edlEyYKEv5b8UGWMw79heQBmgrmO+D8Xm8JP0cDrosMdEGmMesd1JaHfvKJbhCFsSD/CXZHcdL4q0lxBwodq4idD1B83hJQkwEzb7lqnKkGHLBYkGNfe8tfhFIROIAIhEvgveFc79E8E5uCMp6VzqTaeJCGIJr80Pmc3I3sP0sJkXI4yV54ho8SvZzz0zOzrk2jpdEU44JVOQvyDLFtXSVpRVBhyzK523P0OWU4JIuGICkCWLCVPlyMtaQ+kAqKIsqJhulYQioEUQFX7ny4m5kl+NJrZylQZgox4UwBPsHMMQchN25XHGgPQf7ebwkB/Nj7RxrjoOyB4V3BFcPR3lnwFdw2OfnV8vaTYYYiQpmdA2ZBNGUrxA3YlCTGIaAGIemAKashHGKCQM0dTXGCGwWeCvcCcwYIcTjzKFl+mjJVNslSzfVUur8ZB+AO50LYQichWbULV4c9BDy69JKjNisOmrJ6ofV+Lx05dbB9ZzCpYDrs56PjONF59V1iAFf5+pdUw8EzeMlsVawku/CcxGBQQvXESiQMDgR3FjBGzHFWy+KCNYoIaQj3X+3BhG187JsASlyY0tIZyk+t01wIQxBXRusJNBc2h41F9zUddlt8l6bA42Nz4FP7bMK6V5h7Zzri9yBaLlbCeQ4xvXCYnjDMMqD7EDTtiwYiAd5vCQWQ+UdzhqMsaRkCDFhC+qiigi1U2LSowre2pVf1FSVmLL7zI4LbkwgK+7Be15SOjYCcFzfkFJZg74pLkSU5spug7G5QbwdH43N4yV52t35TvvqAPvX86OM4yXxcUxjJRsBw+gmKtwwZzar8RaGOVw/2GeYg7flK8Sdd+w1Hm9zmqa3wl7jcQUzdKyRrKUl4J0FydpapTuB3WrBFaF45tCyOfxJtqF5PeTeyX0fWPSBvg+ktHr33oXYEVxqZ+xdOkQDuLrGhw5xebwkbeu4PAv0C5jtgR2gavJ4URqYzfNuJZEvktk4XpKdqmKIh0gC3xqGkFCTx0virclN2d2yeCtnxPiCHcqMZHcVHAdjrZQXUTt1wS2t+8+x8uiSbQhip5RY9CkL4I2d0xZ9oqny61VxIQyBsRUP3DUjhoi6FqnAOouxZReQoMKVSyBXwDSwV+XMnFC4Ce+VGcjj+cthyY86jpekco6mBgzstC0H6TqkPF4S7y1D1Jw9hAFNGDFlUzVFjiubRY4ryQobgm1dcLc1iB1CQkRRFUJMudez5BhLVU2G4FxUlcUbi209lWvpg2JioqoKN+kQwY932baxxBSPxkvifZaWMMBuA8PYA6CgdA4A1lXcf2WHPgTEWOpZTeUc1pU16DkACmFIRM19eL0vGwCVMV9fdbwLJ7tgpgX31myr6FwcO6edDGKrLpNwV8eFMAQz59mfLzg8HDBtT5rPmc08M1d2ZXNWWByMi6xGhkOOeqWWZKeFuyR3casq2Fnk7m4FOy8CWUK59p6mrnGuJYTc87a0tHIIkS5kKQdjDKqJLiScjfhCcYLjpuc3VvCW/m5t64K7nFtpg/QxJEXRo85yIkJKcdV24GIYghB6uhSoGqjbhk7ndCkQQl90XlaFRYA4gG1hPs9Carawa8i3cO9dYCrwDVyaQerzeElmjSOEgBiDcxBCQFNi1pT9GndDoA8JI7mjlaZcZOZMKGcIrCGmmN2hIqMstll50/OPh61ccLcU6wxhUFJKRzECVcH6zfUsvmN49LCjdu4ouFJVNSklHj0srDUUB0zM2jmLw7yAmJjHS3K5rWl2OpwDP3MMEgg+j5ekthXOGg4P5wR1xMWc2aylLhzr6YeIqiBL6WJj0BDpC6e15tTMREIw6IVpsvLxso0FZdYYap+IcTQGgPeCXfEu+EIYgqEfiEnphoAlEruAs8LQl11wrx9Gosv9B5q7DAuTOAx5vCT3Xtlj9v86+gBxCJByF7B7r+wVndegEWsMO7MW4yqSaTHGMGjhvFYYWy7G40VXwBd0WYUQ6YNircWNd5J9UKwp567aZra1oMwYIanB+/V2TrsQ34g+9nzkamBnBg1CHyOPX4dn3FXWNTSEnJsfHCzmiUB+PYQn/dG1stvUeA8pgvWO2Ae8z+MlmS8GVCxN1dA0OywWefc0X5Q16NbAE4ddDvaLBx2wxrJzVzlf2hByyqGO4nfLHrxDSMWD/tvIthaUbSqmciEMQWMdYqHrwdSBrgexebwktYdgoTEw23Ec9IGFzeMl6UKi9iAGXOUJGqhsHi+JCjiUfujpk0DscSaPlyTGyCJEnMlb9hiFRYjEghpISZWQyFKtS6k3zbLdEx/LttY3LOexbmN0IQyB9Z6Zh/0FDNcOIOa0SFv41ujyXsVu1aMGhi5gDexWebwk86EnxrwjGGJCYxbDmw+lg+twfegRlNpWdLFDo2ALX6uLkJhVLhfgJcU5SzWOl0JU6UPCO5vdC0kZQsT78pZgG33xAmMglqN5yRYU4G2K8t+KDaAp0ins7sEDn3A3u3u5+Yumsr7lK7NLtLvgXdY98g7a3TxekoPDOdd6GBSc8wwK1/o8XhJjcyGNM47KeZxxhJAwhS1BCImskLBc0ISkebwUxpqcVjtWOaOKMwZTOGto6Xtf3oEr5NelK4sFhqC5t7MISZUhaOn6u42xzub1Py4iHxaR95zy/gtF5AkReef477vXNRcQvELs4Yn9fWIPfrxwS9LUjssNXNmDS7OWK3twucnjJZkPA2nIF0e+MHJTn/lQ1hevyXGlrYhh4PrhATEMXGkrNJU9X9YoB4sAKlTegQoHi4At2HPUGENbW7w1OXBt8+tVyhJ8PGyt1pCCd4IZ3UHmREHeRWCdV9BPAq8Cfvo2n/lfqvpFa5wDAIJBXDYEToQYwVV5vCTOOtp2B4tQt3t0RogornDsonEebwf6BUQ5JC6yuFtTuAAvSWJIhlndUlW79L0wJCVJ2dhF5Tw7NYgmYoyIJnbqvGsphTVCDDll1BzpH5Wv4N1WX7xya+2e0vPaFOtsXv/7IvLMdf3+8zDowLAAbC7ZVsmyCYOWvcN1xnPXrKHrB9BI7Qx15XGm7IIrRgiaK4mr2S491zno8nhJrChoxLgmL3DOQbfI4wWpKs9dO0I3RIKCs5baW6qqnEE3Znk3qycWWileS7Ctvvht1UDaFKVjBJ8jIu8SkTeJyKev7ShRGcj/2VnVYMhtIYllFxDnoY8R5z1tVeO8H18XnRZ7bcPde8JuU7HX1Ow2FXfvCXttWflRb2ra2Q5GRn+3KO1sB2/KprVW1oAxzJqKK7sNsywNmccLsa2ujm31xS8N53IHsK58/W2lpA/iHcAzVHVfRF4M/DrwrFt9UEReDrwc4KGHHjr3gQLCzMI8QH/tGgSYuTxeEm8sUZXQLxBT0/ULxDq8KSuGt9vucf+lyH63gBSpveGe+jK7bdmCsqq13Fc71LYktezWe0gcqNqy58s5S+MUHXcmxgleDa5gC7w0ipUZK0cNYJLmbKKSZ2tpoJaLrhHBOrbAQG2vBtImKHbLoqrXVHV/fP5GwIvIvad89jWq+rCqPnzfffed+1iSEgtg1gr333Mvs1Zy+8U1NHg4D0GV3cqz186onGWvnbFbeULhq+LSjkckF5Bdaht2mxqRPF6SvapBXYMTw14zw4lBXcNeVXanIsYwaxzemKOK4llTtlG8pmOFTzgukNLSQVmyL95agxu1j4wp30ITlvn6x/O6KEYACu4IROR+4K9VVUXkeWSj9Ng6jlU1jpnJd0PX5/sYVWYmj5ckJfDWIxZEHGodGvN4SRrriMZiU6T1NYdhTjS2eAHezqzm7mbB/jCw6OdYm7jbe3YKdyhjbLfovaM6ar+omIKxCzEC6djvvYwRSGFn8Db74rexvgE2M6+1Xdki8gvAC4F7ReQDwPeQW+Ciqq8Gvgz4JhEJwBx4qa4pRF+bmnpWIRppZzvMJUsV1IV9y9bAQd8RSTgrhDjHYrCmbAeYAeGBnZZ5jCRN7M1aWmsZCl+uzhhM3XJvO6OqG/puQZ+0uAw1jAJvUY86lGUKatSIgNEjF8xSYqJ0UHZb+xGoau54p8d/Q0mCd2V3BpvSQFpn1tBXPMn7ryKnl66dpnZcqRzJtzjjcLu7mGEonq+PJuZhwGKovaXrlJ4hy5AWZAiJKBZrBG8qUlKi5NaQJRFjuae17A+B/YM5daXcUzukcExluezHmG6QfC7p7jBGSDEv/usUKzsv2+qLjzHlXdyyfwPk1zGVjfVsSAPpQkhM7NQtVduRUqCpKhZ9h2ln7NRlBfZDgtZ5lNzm0DtDhaXwegsaeOz6AZWz1JWn63v6EHnwrsLpTKrMk6G2FTuXK0LfM09wpXBMJY2LiHX2aNGNMWFjgkKLyLYuuMu5ld4B3MxJIwB5jsbk8ZKL5KbqLi6EIWgbT2sS10PP/vwAIz07ztA2ZRe2GBRvhD7pkUCZHwuBSpKSnmhxm7+EaspXf4JCHOgR5oeKlUi+7y77NT65IzjpGip9trZxwYXt9cVvI5uKqZR3rm4ATZF5MuxUu9x/5R52ql3myRTXGkIij897NELtazTC4/MepOy8Ioa7myY3P9dE7R13Nw2x8NclJeiS0IdAUuhDoEtSPLg+cXa2VWvIjsJ8J+sIUlJsYVfapuobLsSOYBGUS9bRo8y7BSLCJetYFL7zFoTKgRolpIAapXJ5vCR+vECNsVnYLUVUE77wXduQAqIRYx1JwVqHpsiQyjZwWJ6VZcrh0jU03eN+LGlMa00JFD2qLE6pbMDYWkPSHCzOBdnZCJRu7SkiWJPFFhNjT/M1BLAvhCGIQ0KtxStYVxFDQiWPF8U6WtcwxIBGRVRoXQOltYZqyyImGgvOWGJM+XVdNigbozKoYKNinSGGQERytk5BjDU49IZFxFmD2UK3TGnSmGp7MgsmJcCULXQTyRlCxy4r2QqXlY7ny1hzVBiYz58+NbKGtgnxiasHB1hjqbyhHxbEFHnGfWV1/71A1GEsIEsETRgdWHFf6vPPy3kuN54hREIcMAKXG48vrX0BEAILTeg8Ii7gxTBmJRfDjIFZVTlaRLZBP2cbWRa0yVjQkI1BKp0odzSXbYupTFlDK8QGoU+B0C9oxTFfHOCcw4bCqXRGudZHWiPUriIOh1zrE1JQvhjyRdq4GmcjhpoEOLFHF28xNLEYlMZ73G5D6BYshlA83XZbUzW3kW0tdNtWpqyhFbIgYlL2R3Z9LosySVlQNigbAtzVViQRIFE1FY0qoXDPYhEFUWrjc8WzJqLGPF4SY5g1Nnfb6gdElFlj8wpckG1O1dw2trXQDbYzm2lTWUMXwhB0857DMKAhYepE6gODS3Tzsq0XE0Jja5IBKx6nCZPyeEkMBsGgKSGW/CgGUzhryGCovB+jsw4QUIrPC7bTrbCNbOvuaVMVvOdlU5XYF8IQHPQLru73VA6aGhYh0C/yeEkqJ3RpwCWLVIIOiY5I5coWuokVmnwF5A721ueS+8ILXeVzwKyqHMY4UhL6PlBNfXifMmzr7mlTvvjzsqnzdSEMwWIxoEASCCmS8o0ki0XZxjRN5fKdhw6YFAlpQEVoCjY0AbBicI3HGYuxnhQNIUVsYUduU1XMaiXESFRBNDKrHU1VNui/rXeT28o27p62tXPach7rPl8XwhBgBePIDg8ZHR9OofCXUbDsNjUhBIwRau9wziFFE+mgrjxtlXLucowIibbKchMl8dbS1JZhgITBYPHe4m3Z87Wtd5MTZ2ebVVE3wYUwBJWzeHIuLijGGnyIVAXFpAASSiMeZg2WioiFIZIKixPUzuZdQW0Q8Tmwl/J4SUTAiqWeeYyxpBQJIRXvbrXNd5MTZ2NbVVHhKS5DvU3sVg0qELqIdUroIuLyeEmsGMRbHAbnHCEEgqe4C8ZZS1s78lfPABZBcIXvvBHDrHaElEgpYQRmtaN07uFFv5u8E9jW2MVTXoZ6m2hqR2MNvSZUE9bmPrOlZajr2lHn9Ilc0m4Fq4a68LzE5AW3D5GYwBpD5WzRjltwvOAebZh0Oxbcbb6bnDg72xi7mArKVkhK0M5m7GFomj0WC0sgFRcra6zHV46YEhZDRLDG0tjycs8haY6nOAsKIWnxxrKCMh8SlTNU4w5qPiTawllD23w3OWUyPbWZCspWSMRwyXsGVWIMeGeYiS2upulrS+0ciCI4lAQq+MKaPqpKDOC9wVqbNX6GVNznrQiNE4YU6RcJa5TGGcrvCbbvbnJbO25NnI+poGyFVEboouKMUPmKvu/polKVlpjF0FSWEFNW05TcOLt0gZQi7DS5YEsFrLVUtvyCm1DSMvPLGdBEQooH17eRGBMhjlvevJoAihGKdtyaOB+bcjuWr8TZAJU3JI3EGBlSfkwayxciKTkf3kjubmWEqFK8o4m1ZvyiLfXZx/hFYUlejYkhRGDp4hCGENG4BYplW8by5gIZz5UISTk2DhNPCbLbUY53BpBfr3hXt7YrW0R+XEQ+LCLvOeV9EZEfFpH3icgfi8hz1jcXS1vVGGdxo9+7rWpESqePJjQGQkgMfX7UGMjK4+XwRuhCAgHvLAh0IeFLi6iNfRK6MLDoA13IhYLF80e3kFsFGbPu/7R7eqqR3Y7ZW7DsebFq1nmL95PAF97m/RcBzxr/vRz40XVNJAG1NVTeYQxU3lFbU3i5hRASi5hbVhpriUFZxDxeEmMMjTUYQ07TNIyvC+8INC9uzlicNThjR/f3tLjdzKY6W03cGaztylbV3wc+epuPfDHw05r5I+CKiDywjrkIysEQGLqAqjB0gYMhIIV9MEOK2JQQZwghIs5gU2Io3EJTRagrhxODNYITQ105dAvuvAXBmvHuyJji3dyWLLuShZiIsXxg3VmDGWMDOeV2jA8Udu9NnJ9NfLdKBos/EfirE68/MI596OYPisjLybsGgH0R+bNzHclYJ77JSm4x3IV1jwPosJiTYjnRZzFWrPOAaop3i7EfBURjGIo3VM7NBxTVexF5FMgdRApP6ig4gN4D8hhHgYyt2RbcB3yk9CRuYhvnBHAv8GjpSdyCO3VezzjtjadE1pCqvgZ4zSp+l4i8TYfFw6v4XatERN6WYtjKeWlK2zkv3dZ56VbNaxvnBNO8zss651Vyn/hB4METr58+jk1MTExMbJCShuD1wNeM2UMvAJ5Q1Y9xC01MTExMrJe1uYZE5BeAFwL3isgHgO9h7DKuqq8G3gi8GHgfcAh83brmchMrcTGtgWle52Oa19nZxjnBNK/zsrZ5SenshomJiYmJsky5ZBMTExMXnMkQTExMTFxw7khDsE3yFuec1wtF5AkReef477s3NK8HReR3ReS9IvInIvKtt/jMRs/ZGee08fMlIo2IvFVE3jXO63tv8ZlaRF43nqu3iMgzt2ReLxORj5w4X/9y3fM6cWwrIv9HRN5wi/c2fr7OOK8i50tE3i8i7x6P+bZbvL/6a1HHysM76R/w+cBzgPec8v6LgTeRdRlfALxlS+b1QuANBc7XA8Bzxud7wJ8Dn1bynJ1xThs/X+P/f3d87oG3AC+46TP/Gnj1+PylwOu2ZF4vA1616e/XeOxvB37+Vn+vEufrjPMqcr6A9wP33ub9lV+Ld+SOQLdI3uKc8yqCqn5IVd8xPr8OPEKu8j7JRs/ZGee0ccb///740o//bs64+GLgp8bnvwx8gaxDKez88yqCiDwd+KfAj53ykY2frzPOa1tZ+bV4RxqCM3CavMU28Dnj9v5NIvLpmz74uC3/bPId5UmKnbPbzAkKnK/RnfBO4MPAb6nqqedKVQPwBHDPFswL4EtHd8Ivi8iDt3h/HbwS+A44VeexyPk6w7ygzPlS4DdF5O2S5XVuZuXX4kU1BNvKO4BnqOpnAf8N+PVNHlxEdoFfAb5NVa9t8tin8SRzKnK+VDWq6rPJ1fDPE5G/vYnjPhlnmNdvAM9U1c8Efovju/C1ISJfBHxYVd++7mOdhzPOa+Pna+TzVPU5ZIXmbxaRz1/3AS+qIdhKeQtVvbbc3qvqGwEvIvdu4tgi4skL7s+p6q/e4iMbP2dPNqeS52s85lXgd/lYufWjcyUiDrgMPFZ6Xqr6mKp248sfA/7OBqbzucBLROT9wC8C/0BEfvamz5Q4X086r0LnC1X94Pj4YeDXgOfd9JGVX4sX1RBspbyFiNy/9I2KyPPIf5+1LyDjMV8LPKKqP3TKxzZ6zs4ypxLnS0TuE5Er4/MW+EfAn970sdcDXzs+/zLgd3SM8pWc101+5JeQ4y5rRVX/nao+XVWfSQ4E/46qftVNH9v4+TrLvEqcLxHZEZG95XPgHwM3Zxmu/Fp8SqiPnhfZUnmLM8zry4BvEpEAzIGxPJF9AAADgElEQVSXrvuCGPlc4KuBd48+ZoDvAh46MbdNn7OzzKnE+XoA+CnJ7e0M8Euq+gYR+Q/A21T19WQD9jMi8j5ycsBL1zyns87rW0TkJUAY5/WyDczrlmzB+TrLvEqcr6cBvzbe3zjg51X1zSLyjbC+a3GSmJiYmJi44FxU19DExMTExMhkCCYmJiYuOJMhmJiYmLjgTIZgYmJi4oIzGYKJiYmJC85kCCbuWMY86z8QkRedGPvnIvLm2/zMB5b5+Gc8xs+KyF+OSpHvEpG/f4af+XoRuf/E658QkU896zEnJlbNZAgm7ljGmoJvBH5IskzzLvCfgG9e8aFeMUo7/FvgR87w+a8HjgyBqn6dqv7Ziuc0MXFmJkMwcUejqu8ha8Z8J/DdZNXG/ysiXytZv/+dIvIjInLDtSAinyJZ1/8XReQREfmlsWL3dvwhJ8S/ROR7ReR/i8h7ROTV4w7ly4FnA68bj12Nu5Zni4gTkasi8p/H3cUfisgnjL/rWZK1+t8tIv9RRK6u8jxNXGwmQzBxEfhe4CvJIl7fL1mM7UuAvzveyTtuXc36acArVfVvAQvgG57kOF/IjcJ3/1VVnwt8Blk/5wtV9XXAO4EvV9Vnq2p/0++4DPzeKKT3h+TdA2RRvR9Q1c8AisuhTNxZTIZg4o5HVQ+A1wE/M4qI/UPgucDbRvmKvwd88i1+9C9HvXeAnwU+75RD/BcR+XOyOuX3nxj/AhF5K/Cu8Rhnkcmeq+qbxudvB545Pn8+WYAPciOViYmVcUdqDU1M3ILEse68AD+uqv/+SX7mZv2V0/RYXqGqvy4iryDr5jxfRGbAq8hd1j4oIt8HNGeY58kdQmS6Ric2wLQjmLiI/DbwL2SUrBaRe0TkoVt87pNE5Lnj868E/uBJfu8rgZmIfAHQkg3Po6Oa5Jee+Nx1cvvN8/BWsjsLCoqyTdyZTIZg4sKhqu8mxw1+W0T+GPhNsurjzTwCfLuIPALMgNc8ye9V4PuA71DVx8iuoveS+8ue7Bb2E8CPLYPFZ5z2twDfOc73k8hdvCYmVsKkPjoxcQtE5FOAXx6DycUZtekPVVVF5KuAL1HVL32yn5uYOAuT/3Fi4qnBc4FXjmmuj7OhHhoTF4NpRzAxMTFxwZliBBMTExMXnMkQTExMTFxwJkMwMTExccGZDMHExMTEBWcyBBMTExMXnP8Pmj611dp3G+sAAAAASUVORK5CYII=
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Run the cell below to grab all the features and retrain our model on them.</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[332]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">features</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="n">all_features</span><span class="p">]</span>
<span class="n">ratings</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">loc</span><span class="p">[:,</span><span class="s1">&#39;stars&#39;</span><span class="p">]</span>
<span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">features</span><span class="p">,</span> <span class="n">ratings</span><span class="p">,</span> <span class="n">test_size</span> <span class="o">=</span> <span class="mf">0.2</span><span class="p">,</span> <span class="n">random_state</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>
<span class="n">model</span> <span class="o">=</span> <span class="n">LinearRegression</span><span class="p">()</span>
<span class="n">model</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[332]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>LinearRegression(copy_X=True, fit_intercept=True, n_jobs=None, normalize=False)</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>To give you some perspective on the restaurants already out there, we have provided the mean, minimum, and maximum values for each feature below. Will Danielle's Delicious Delicacies be just another average restaurant, or will it be a 5 star behemoth amongst the masses?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[333]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="nb">zip</span><span class="p">(</span><span class="n">features</span><span class="o">.</span><span class="n">columns</span><span class="p">,</span><span class="n">features</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="s1">&#39;mean&#39;</span><span class="p">],</span><span class="n">features</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="s1">&#39;min&#39;</span><span class="p">],</span><span class="n">features</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span><span class="o">.</span><span class="n">loc</span><span class="p">[</span><span class="s1">&#39;max&#39;</span><span class="p">])),</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;Feature&#39;</span><span class="p">,</span><span class="s1">&#39;Mean&#39;</span><span class="p">,</span><span class="s1">&#39;Min&#39;</span><span class="p">,</span><span class="s1">&#39;Max&#39;</span><span class="p">])</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[333]:</div>



<div class="output_html rendered_html output_subarea output_execute_result">
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Feature</th>
      <th>Mean</th>
      <th>Min</th>
      <th>Max</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>alcohol?</td>
      <td>0.140610</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>has_bike_parking</td>
      <td>0.350692</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>takes_credit_cards</td>
      <td>0.700243</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>good_for_kids</td>
      <td>0.279029</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>take_reservations</td>
      <td>0.106086</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>has_wifi</td>
      <td>0.134968</td>
      <td>0.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>review_count</td>
      <td>31.797310</td>
      <td>3.000000</td>
      <td>7968.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>price_range</td>
      <td>1.035855</td>
      <td>0.000000</td>
      <td>4.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>average_caption_length</td>
      <td>2.831829</td>
      <td>0.000000</td>
      <td>140.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>number_pics</td>
      <td>1.489939</td>
      <td>0.000000</td>
      <td>1150.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>average_review_age</td>
      <td>1175.501021</td>
      <td>71.555556</td>
      <td>4727.333333</td>
    </tr>
    <tr>
      <th>11</th>
      <td>average_review_length</td>
      <td>596.463567</td>
      <td>62.400000</td>
      <td>4229.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>average_review_sentiment</td>
      <td>0.554935</td>
      <td>-0.995200</td>
      <td>0.996575</td>
    </tr>
    <tr>
      <th>13</th>
      <td>number_funny_votes</td>
      <td>15.617091</td>
      <td>0.000000</td>
      <td>36822.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>number_cool_votes</td>
      <td>18.495973</td>
      <td>0.000000</td>
      <td>6572.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>number_useful_votes</td>
      <td>43.515279</td>
      <td>0.000000</td>
      <td>38357.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>average_tip_length</td>
      <td>45.643426</td>
      <td>0.000000</td>
      <td>500.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>number_tips</td>
      <td>6.285217</td>
      <td>0.000000</td>
      <td>3581.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>average_number_friends</td>
      <td>105.132000</td>
      <td>1.000000</td>
      <td>4219.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>average_days_on_yelp</td>
      <td>2005.367009</td>
      <td>76.000000</td>
      <td>4860.000000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>average_number_fans</td>
      <td>11.590148</td>
      <td>0.000000</td>
      <td>1174.666667</td>
    </tr>
    <tr>
      <th>21</th>
      <td>average_review_count</td>
      <td>122.110660</td>
      <td>0.666667</td>
      <td>6335.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>average_number_years_elite</td>
      <td>0.923313</td>
      <td>0.000000</td>
      <td>10.666667</td>
    </tr>
    <tr>
      <th>23</th>
      <td>weekday_checkins</td>
      <td>45.385094</td>
      <td>0.000000</td>
      <td>73830.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>weekend_checkins</td>
      <td>49.612515</td>
      <td>0.000000</td>
      <td>64647.000000</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<p>Based on your plans for the restaurant, how you expect your customers to post on your Yelp page, and the values above, fill in the blanks in the NumPy array below with your desired values. The first blank corresponds with the feature at <code>index=0</code> in the DataFrame above, <code>alcohol?</code>, and the last blank corresponds to the feature at <code>index=24</code>, <code>weekend_checkins</code>. Make sure to enter either <code>0</code> or <code>1</code> for all binary features, and if you aren't sure of what value to put for a feature, select the mean from the DataFrame above. After you enter the values, run the prediction cell below to receive your Yelp rating! How is Danielle's Delicious Delicacies debut going to be?</p>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[334]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">danielles_delicious_delicacies</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">1</span><span class="p">,</span><span class="mi">10</span><span class="p">,</span><span class="mi">2</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">10</span><span class="p">,</span><span class="mi">10</span><span class="p">,</span><span class="mi">1200</span><span class="p">,</span><span class="mf">0.9</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">6</span><span class="p">,</span><span class="mi">5</span><span class="p">,</span><span class="mi">50</span><span class="p">,</span><span class="mi">3</span><span class="p">,</span><span class="mi">50</span><span class="p">,</span><span class="mi">1800</span><span class="p">,</span><span class="mi">12</span><span class="p">,</span><span class="mi">123</span><span class="p">,</span><span class="mf">0.5</span><span class="p">,</span><span class="mi">0</span><span class="p">,</span><span class="mi">0</span><span class="p">])</span><span class="o">.</span><span class="n">reshape</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="o">-</span><span class="mi">1</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[335]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">model</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">danielles_delicious_delicacies</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt output_prompt">Out[335]:</div>




<div class="output_text output_subarea output_execute_result">
<pre>array([4.03799004])</pre>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Next-Steps">Next Steps<a class="anchor-link" href="#Next-Steps">&#182;</a></h2><p>You have successfully built a linear regression model that predicts a restaurant's Yelp rating! As you have seen, it can be pretty hard to predict a rating like this even when we have a plethora of data. What other questions come to your mind when you see the data we have? What insights do you think could come from a different kind of analysis? Here are some ideas to ponder:</p>
<ul>
<li>Can we predict the cuisine of a restaurant based on the users that review it?</li>
<li>What restaurants are similar to each other in ways besides cuisine?</li>
<li>Are there different restaurant vibes, and what kind of restaurants fit these conceptions?</li>
<li>How does social media status affect a restaurant's credibility and visibility?</li>
</ul>
<p>As you progress further into the field of data science, you will be able to create models that address these questions and many more! But in the meantime, get back to working on that burgeoning restaurant business plan.</p>

</div>
</div>
</div>
    </div>
  </div>
</body>

 


</html>

```
