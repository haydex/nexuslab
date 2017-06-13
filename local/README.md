NEXUSlab
This is a brief description of the structure and configuration for the NEXUSlab Hugo website, please note that the theme is totally separated from the customized files.


- The config.toml file has all of the general settings for the website, here the most important ones:
  - title: website title.
  - fullTitle: full title of every page.
  - publishDir: the directory where Hugo will render the website(This is the website that can be published)
  - baseurl: hostname (and path) to the root of the website, this is very important when the website is rendered.
  - canonifyurls: if true, it makes the URLs pretty.
  - theme: the name of the theme to be used by Hugo. “hugo-bootstrap-premium” was used in our case.
  - [params.theme] name: this is the name of the subtheme that will be used to render the website. “flatly” was used.
  - [params] BrandImage: this is the path to the brand image for the website.
  - footline: this is the copyright section at the footer of every page.
  - showRightSidebar: this is for hiding or showing the sidebar. false is its current value.
  - [[Languages.en.menu.main]]: these are the menu items at the main bar. they have a name, url, and weight(that is used for ordering menu items).
- The content folder contains the .md files that have content only and written with the MarkDown language, they consist of the following:
  - _index.md: this is the content for the home page of the website. (_index.md is rendered by /layouts/index.html). Its front matter(TOML variables at the top of the _index.md file between the two +++ lines) are title, topImage, bottomImage1, bottomImage2, bottomImage3 which are located in the static/images/home folder. The _index.md file also contains topsection and bottomsection shortcodes, which are Hugo html files that are used to format the layout of the contained text inside it.
  - contact.md: just a simple .md file that is contained at the root of the content folder, because it consists of one page only. (contact.md is rendered by /layouts/contact/single.html). Front matter has these main variables: type = “contact” and [menu][menu.main] 
  - news: folder that contains .md files for the /news/ page. (Rendered by /layouts/news/list.html and single.html). Front Matter has type = “news”, link(if set it will refer to an external link), weight(if set it will reorder the headlines)
  - people: folder that contains .md files for the /people/ page. (Rendered by /layouts/people/list.html and single.html). Front Matter of each .md file has type = “current” or “faculty” or “past”, link(if set it will refer to an external link), weight(if set it will reorder the headlines), image(always set it to the image of the person located at /static/images/people/). It also contains the shortcode profile to render the about section for each person using the image variable.
  - project: folder that contains .md files for the /projects/ page. (Rendered by /layouts/project/list.html and single.html). Front Matter has type = “project”, image(is the path to the project image), weight(if set it will reorder the headlines)
  - publication: folder that contains .md files for the /publications/ page. (Rendered by /layouts/publication/list.html and single.html). Front Matter of each .md file has type = “publication”, link(if set it will refer to an external link), weight(if set it will reorder the headlines), pdf(if set it will add a [PDF] link at the end of the publication title in the list view, pdf files are located at /static/documents/). It also contains the shortcode profile to render the about section for each person using the image variable.
- The data folder contains a single Menu.toml file that sets the main menu highlight selection.
- The docs folder. This is the rendered website folder. It was set in the config.toml file with the publishDir variable.
- The layouts folder. This folder contains all of the layout files that are used by Hugo to render the .md content pages in the /content/ folder.
- the static folder. contains every static content like the css styling folder (css/style.css), the documents folder (pdf etc), the images folder that contains specific page images, and finally it contains the favicon.png for the website icon.
- the themes folder. This is the theme files being used by Hugo to render the website. they are separated from the customized files in the main NEXUSlab folder. “hugo-bootstrap-premium” theme was used in this case.
- the license and readme files. which contain general copyright and information about NEXUSlab website.


Copyright 2017, NEXUSlab, HAYDEX
