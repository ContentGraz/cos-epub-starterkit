# Generating and editing epub files

Three possible ways:

1. Conversion with Calibre (and editing with sigil)
2. Transformation of markdown files with pandoc
3. Typesetting with Indesign, editing with calibre/sigil

Tools:
- [calibre - E-book management](https://calibre-ebook.com/)
- Sigil: [Sigil Ebook | Sigil is a multi-platform EPUB ebook Editor](https://sigil-ebook.com/ "Sigil Ebook | Sigil is a multi-platform EPUB ebook Editor")
- [Pandoc - About pandoc](https://pandoc.org/ "Pandoc - About pandoc")
- Epub Validator [EPUB Validator (beta)](http://validator.idpf.org/ "EPUB Validator (beta)")

Material:
[ContentGraz/cos-epub-starterkit: Advice and examples to show how to deliver your master thesis as .epub file](https://github.com/ContentGraz/cos-epub-starterkit "ContentGraz/cos-epub-starterkit: Advice and examples to show how to deliver your master thesis as .epub file")

---

## Conversion with calibre

https://makrocosmos.wordpress.com/2018/06/24/how-to-epub-from-docx-with-calibre/

makrocosmosmakrocosmos | sandrinefackner
How to .epub from .docx with Calibre (it’s free!)
It’s almost done, my master’s thesis is handed in, so I thought I’d take the time to explain how I was able to hand in my thesis as an .epub and share the things to look out for.
To my fellow #cos colleagues: there are millions of ways on how to hand in your thesis as an .epub. Sebastian Häusler worked with Atom and extensions, wrote in Markdown and converted with Pandoc. Click here for his elaborate step by step guide.
I wrote my thesis on my Macbook in Microsoft Word as a .docx, used https://convertio.co/de/docx-converter/ to convert to .epub and installed Calibre (Download for Windows, Mac) to „clean up“. I managed my references with Zotero, however, you can insert your references manually and still get the same results.
Here are the steps I followed, including issues I had to fix. I provide links with explanations. However, I assume you know your way around Microsoft Word using styles and automated numbering and indexes, and that you can navigate a semi-ugly .html file.
1. Write your thesis in Microsoft Word
The basics
Format EVERYTHING with styles: here’s how you apply them, here’s how to customize them. Use them for headings, body text, quotes, tables, bulleted lists, title, footnotes, image and table descriptions, … this is the most important step!
Make use of the automated numbering of headlines, of table descriptions and image descriptions.
Apply descriptions to you images, tables, etc.
Create an automated index, table of figures and index of tables.
Use Zotero for easy literature management and referencing. You don’t have to, though.
Issues to fix beforehand that save time when editing your .epub:
Add a bookmark to every entry in your bibliography. Select your reference in the text and add a link to the bookmark. This will link all references to the corresponding bibliography entry.
Do not copy-paste diagrams from Microsoft Excel into your .docx. The converter does not recognize them as images and will not display them in the .epub. (If copy-pasted directly from Excel, diagrams stay connected to your .xslx file and update when you data changes. I kept mine connected, and in the last moment I saved them as images and reinserted them before converting)
Do not insert a .pdf in your .docx, the converter will not recognize it and will not display it in the .epub. I re-inserted them as .png and it worked.
When you want to move imges/tables/etc with a description, always select the object and the descriptions (holding shift), and then move them. If not, descriptions might show up twice in the .epub.
Add metadata to your .docx – this will help you save time in Calibre.
2. Convert your .docx in .epub
My colleague Julia Scheiblbrandner introduced me to  and I found it worked pretty well.
Click on the link and upload your .docx (be sure to update your indexes one last time &#128521; )
Click on the little arrow near „JPG“ and select „ebook“ – „.epub“
Download the resulting file.
3. Use Calibre to edit your .epub
Thanks to Melanie Mitter for introducing me to Calibre.
First steps:
Go to your new .epub file and: right click „open with“ and select Calibre
Calibre is going to import you book to your empty catalogue.
Select your newly added book. Then, in the top navigation bar it says „Metadaten bearbeiten“ (Edit metadata). Click it.
Add a title, an author (if you haven’t already in Word) and click on the green arrows next to the text fields to add this information to give the app information about cataloguing or sorting. (E.g. author name: Sandrine Fackner. Cataloguing information: Fackner, Sandrine)
Add a cover image: I created a boring cover image using Photoshop (1200x1600px). Have fun. You can also create a title image with calibre itself. Isn’t going to look good, though &#128521; Click ok.
Now to the „good“ stuff:
Have your „book“ selected. On the top right, click „Buch bearbeiten“ (edit book). Tip: if you can’t find that button, try clicking on the tiny arrow on the right to expand the navigation bar. Or you can simply make your calibre window bigger, the button will pop right up.
All sections of your thesis are now displayed as files on the left navigation bar. Double click them and see the source code and how they look like as an .epub. On top, small windows will show you how many files you have open.
All styles can be edited in the .css section. If you find your headlines to look ridiculous, look in the .css files and play around.
Check if all images are displayed correctly. As mentioned: I had difficulties with copy-pasted diagrams from Excel and with inserted .pdfs. I re-inserted all of them as .png and it was fine.
Check all image descriptions. Look at how descriptions are displayed, I found that most of the time, they were there twice, and the paragraph that should follow them was in between. Take a close look and delete the second description. If necessary, copy paste the following paragraph including the html code and re-insert them in the right position
Save your ebook as a copy. Trust me on this. Maybe you f****** something up. Keep your original unedited .epub as safe measure.  Click on „file – save a copy“ and select a folder.
Close everything. Then, re-open your edited .epub to check if everything looks right. You can use Calibre itself (select newly added book, click „Bücher öffnen“ or „open book“) or another viewer. I used iBooks.
Additional remarks:
Added links of references to bibliography entries will need no editing, they work just fine in the .epub.
I have a Macbook, so if you work on Windows, you may not have the same experience as me.
My tables looked okay, so I didn’t bother. If you have elaborate tables, check how they look.
I had many names in my thesis, which I always formatted in italics. If you don’t want to go over your document three times, create a character style with priority „2“ in word and format every name with it. That way, when you change styles, your formatting does not go away and will adapt.
Copy-pasting a table from Excel did work just fine. Only copy-pasting diagrams caused issues.
When copy-pasting ANY text, erase it from all formatting by inserting with cmd shift v instead of cmd v (Windows: ctrl shift v / cmd shift v).
I hope you find this helpful. Good luck with your theses!
Show less


## Pandoc

Der für mich bevorzugte Weg: Markdown als Format für den Text und Konversion mit pandoc. Sebastian Häusler hat ihn genau beschrieben: [How to .epub from markdown - Sebastian Häusler - Medium](https://medium.com/@sebahaeusler/how-to-epub-from-markdown-188fef880fbb "How to .epub from markdown - Sebastian Häusler - Medium")

## Indesign Export

Genaue Beschreibung der Epub-Exportmöglichkeiten von Indesign:
[Exportieren von InDesign-Dokumenten in ein EPUB-Format](https://helpx.adobe.com/at/indesign/using/export-content-epub-cc.html "Exportieren von InDesign-Dokumenten in ein EPUB-Format").
Tutorial dazu: [In InDesign E-Books (EPUBs mit festem Layout) ohne Coden erstellen | Adobe InDesign-Tutorials](https://helpx.adobe.com/at/indesign/how-to/ebook-fixed-layout.html "In InDesign E-Books (EPUBs mit festem Layout) ohne Coden erstellen | Adobe InDesign-Tutorials").

[4 Ways to Create an ePub eBook by David Kudler](https://www.thebookdesigner.com/2015/07/4-ways-to-create-an-epub-ebook/ "4 Ways to Create an ePub eBook by David Kudler")


---

---

Validierung: [EPUB Validator (beta)](http://validator.idpf.org/ "EPUB Validator (beta)")

Leas Regeln für die Konversion von Word in Markdown für pandoc

---

epub starter pack von Lea: https://contentgraz.slack.com/files/U03HMMMB4/FB1QT66TA/cos_epub_starter_pack.zip

---


Word und Calibre:

https://contentgraz.slack.com/archives/G054V4GUX/p1535446916000100





----

(Work in Progress)

Quellformat: Pandoc Markdown

Dokumentation: Pandoc - Pandoc User’s Guide oder Pandoc Markdown

Bitte dieses Format endweder selbst erzeugen (optimal!) oder eine Vorlage erzeugen, aus der es leicht generiert werden kann, nämlich:

Andere Markdown-Version (z.B. Mulitimarkdown mit Scrivener)
Wordvorlage ohne individuelle Formatvorlagen (Formatierung entsprechend einfachem HTML).

Die Markdown-Version der Arbeiten möchten wir intern archivierem und gegebenenfalls für Publikationen nutzen.



Bibliographie:

Zotero-Export im BetterBibteX-Format

Keys für die Bibliographie im Format [auth:lower][year]

Referenzierungen im Text entweder mit Bibliographie-Manager oder (bevorzugt) mit [@key] bzw. [-@key], wenn nur die Jahreszahl im Text angezeigt werden soll.

[object Object]
Markdown, Pandoc und Zotero unter Windows

Pandoc:

Download: https://github.com/jgm/pandoc/releases/tag/1.19.2.1

Erste Schritte: Pandoc - Getting started with pandoc


MiKTeX:

Download: Download MiKTeX - MiKTeXorg

BetterBibTeX

Release 1.6.93 · retorquere/zotero-better-bibtex · GitHub

Citation Keys · retorquere/zotero-better-bibtex Wiki · GitHub

Einstellen: A common pattern is [auth:lower][year]`, which means


Command prompt:

10 Ways to Open the Command Prompt in Windows 10

Zotero Bibliographie exportieren, Format Better Bibtex auswählen


APA CSL downloaden:

Zotero Style Repository

Epub Reader:

Herunterladen | Adobe Digital Editions

Im Test zitieren: Pandoc - Pandoc User’s Guide
