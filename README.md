# "Intermediate Drupal theming" Code Sample
This code sample is being provided as part of Debug Academy's "<a href="https://drupal.tv/index.php/external-video/2024-05-07/intermediate-drupal-front-end-development-render-arrays-debugging-caching" target="_blank">Intermediate Drupal Front End Development</a>" talk from DrupalCon Portland 2024.

## Authors
The talk was presented at DrupalCon by Nagat Ahmed and Ashraf Abed. This free code sample is being provided by the <a href="https://DebugAcademy.com" target="_blank">Drupal training company, Debug Academy</a>. Learn more about our <a href="https://debugacademy.com/courses" target="_blank">Drupal courses</a> to accelerate your career.

- <a href="https://debugacademy.com/course/drupal-web-development" target="_blank">Become a Drupal developer</a> (part-time, 3 month course)
- <a href="https://debugacademy.com/course/become-drupal-architect-series-5-classes" target="_blank">Drupal Architect Series</a>
- <a href="https://debugacademy.com/course/advanced-drupal-module-development-woop-php" target="_blank">Advanced module development</a>
- <a href="https://debugacademy.com/course/drupal-10-acquia-front-end-specialist-certification-training-course" target="_blank">Acquia Front End Certification Prep</a>
- All <a href="https://debugacademy.com/courses" target="_blank">Drupal training courses</a>

## What's included
This code sample includes the following files & folders:
- [README.md](#readmemd)
- [yourtheme/yourtheme.info.yml](#yourthemeinfoyml)
- [yourtheme/yourtheme.libraries.yml (and uswds/)](#yourthemelibrariesyml-and-uswds)
- [yourtheme/components/accordion/](#componentsaccordion)
- [yourtheme/templates/node--faq.html.twig](#templatesnode--faqhtmltwig)

Explanations follow:
### README.md
This is the file you're reading right now. I hope I'm helpful!

### yourtheme.info.yml
A _subset_ of a theme's .info.yml file.

Included to demonstrate adding the Single Directory Components (sdc) module as a dependency to your theme. This is because the code sample relies on the `sdc` module.

[Click here](/yourtheme/yourtheme.info.yml) to access the file.

### yourtheme.libraries.yml (and uswds/)
The USWDS CSS & JS files are located at:
- uswds/uswds.min.css
- uswds/uswds.min.js

They were downloaded from the USWDS website and saved into yourtheme/uswds/

The yourtheme.libraries.yml file 'registers' the USWDS CSS & JS files as `yourtheme/uswds`.

This makes it possible for Drupal to automatically load them whenever your component is displayed.

- [Click here](/yourtheme/yourtheme.libraries.yml) to access the libraries.yml file.
- [Click here](/yourtheme/uswds/) to access the USWDS folder.

### components/accordion/
This folder contains two files:
- accordion.component.yml
- accordion.twig

The `accordion.component.yml` file 'registers' our component in Drupal. Essentially, this makes Drupal aware of the accordion component's existence.

It also lists the `yourtheme/uswds` library as a dependency. This way the USWDS CSS & JS automatically load whenever this component displays.

The `accordion.twig` file contains the TWIG (dynamic markup) for our component. This, along with any dependencies (e.g. CSS/JS), is what loads when we display our component.

P.S. Single directory components would also automatically load accordion.css and accordion.js, if we had created those files within our components/accordion/ folder.

[Click here](/yourtheme/components/accordion/) to access the components/accordion folder.

### templates/node--faq.html.twig
In this file, we replace the default output for the site's FAQ content type with our accordion "single directory component".

We render all of the required variables (more information in the file's comments) to ensure we don't break any functionality provided by Drupal.

[Click here](/yourtheme/templates/node--faq.html.twig) to access the node--faq file.
