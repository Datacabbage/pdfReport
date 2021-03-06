pdfReport
==============

Use question text to create a pdf report : send it by email, save in survey.

## Installation

### Via GIT
- Go to your LimeSurvey Directory
- Clone in plugins/pdfReport directory `git https://gitlab.com/SondagesPro/ExportAndStats/pdfReport.git pdfReport`

### Via ZIP dowload
- Download <https://extensions.sondages.pro/IMG/auto/pdfReport.zip>
- Extract : `unzip pdfReport.zip`
- Move the directory to  plugins/ directory inside LimeSurvey

## Documentation
- Create a upload question type
- Activate pdfReport : _Use this question as pdf report._ to _Yes_
- The pdf generated take the text of this question
- Remind the default system of this question are totally deactivated
- Pdf report are saved as files uploaded in survey
- Pdf is done and saved only when survey is activated, and when user submit the survey
- See other setting

### Style and css usage

The plugin use [tcpdf](https://tcpdf.org/) and [WriteHTML function](https://tcpdf.org/docs/srcdoc/TCPDF/source-class-TCPDF/#17080). The plugin include a basic css file by default. You can replace the css included in the template used by the survey with a `pdfreport.css` in the files directory of the template.

You can use inline style in the content of the question text. For example, you can use `<strong style='color:red;font-size:18pt'>A big and red sentence</strong>`. See more example on tcdpf website : [inline style](https://tcpdf.org/examples/example_006/) or usage of a [css file](https://tcpdf.org/examples/example_061/). Remind PDF is not web, usage of position:abolute or float didn't work exactly as excpected.

### New page

Tcpdf can use `<br pagebreak="true" />` or `<page> content </page>` for page broke, you can use it in the content of the question text. HTML is filtered leaving this part.

### Image inclusion

You can include image with `<img src="/upload/files/picture.png" />` or with [Data URI](https://en.wikipedia.org/wiki/Data_URI_scheme). All image are validated before included in the pdf and replaced by a white 1px size picture if not available. It's better to use local image (or DATA uri) for speedest generation of the pdf.


## Home page & Copyright
- HomePage <http://extensions.sondages.pro/>
- Copyright © 2015-2018 Denis Chenu <https://sondages.pro>
- Copyright © 2017 Réseau en scène Languedoc-Roussillon <https://www.reseauenscene.fr/>
- Copyright © 2015 Ingeus <http://www.ingeus.fr/>

Distributed under [GNU AFFERO GENERAL PUBLIC LICENSE Version 3](http://www.gnu.org/licenses/agpl.txt) licence
