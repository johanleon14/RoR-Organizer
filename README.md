# README

## This project works with:

* Ruby version: 3.1.2

* Database: PostgreSQL

* Deployment instructions: So just run
```
rails server
```

To run db migrations use:
```
rails db:migrate
```

To install the gems that are located in the gem file, run:
```
bundle install
```

## Internationalization: I18n
This project use i18n and i18n-tasks gems for translating the application to providing multi-language support.

All translation files located in the locales dir are loaded automatically with the corresponding language code obtained from the file name, e.g. locales/es.yml.

How to use it?

Put the texts in the original language inside the function of i18n, for example:

```
<%= t('Hello World') %>
```

Manually extracting the texts from the files is a complex task, we are often lazy to do so or we forget to add them, therefore we lose the sync between the translations files and the source code, that's why we use i18n-tasks, a handy tool that runs static analysis of the source code files and extracts the translation texts from the source code and add them to the translations files like es.yml, en.yml, etc.

To extract the keys/original text into the translations files, run:

```
i18n-tasks add-missing
```