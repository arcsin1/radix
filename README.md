![Radix Logo](./radix.png)

# Preface
 We spend most of our time at work - so why not make it the most out of it?

 So I make this  to do something...


# Radix
A concise tool to generate projects in an easy way.

# Installation
```
npm install radix1993-cli -g
```
or
```
git clone https://github.com/arcsin1/radix.git

cd radix && npm install

npm link
```

# Usage
Open your terminal and type `radix` or `radix -h` , you'll see the help information:
```
  Usage: radix <command>


  Commands:

    add|a      Add a new template
    list|l     List all the templates
    init|i     Create a new project
    delete|d   Delete a template

  Options:

    -h, --help     output usage information
    -V, --version  output the version number
```


# Commands
### add | a
This command would help you to add a new template to the `templates.json`, which will be used by `radix` to generate projects.
```
$ radix add

? Set the custom name of the template: myApp
? Owner/name of the template: Expendo/react-antd-webpack （your github project name）
? Branch of the template: master
┌───────────────────┬────────────────┬────────┐
│ Template Name     │ Owner/Name     │ Branch │
├───────────────────┼────────────────┼────────┤
│ myApp             │your template   │ master │
└───────────────────┴────────────────┴────────┘
✔ New template has been added successfully!
```
`radix` use [download-git-repo](https://github.com/flipxfx/download-git-repo) to down load git repos.

### list | l
It will show you list of all templates.
```
$ radix list

┌────────────────────┬────────────────┬────────┐
│ Template Name      │ Owner/Name     │ Branch │
├────────────────────┼────────────────┼────────┤
│ myApp              │ your template  │ new    │
├────────────────────┼────────────────┼────────┤
│ myApp2             │ your template  │ master │
└────────────────────┴────────────────┴────────┘
```

### init | i
After adding new templates, you can use this command to create your  project by choosing template on that list.
```
$ radix init

? Template name: myApp
? Project name: myProject
? Where to init the project? ../
⠹ Downloading template...

New project has been initialized successfully!
```

It's easy, right?

### delete | d
To delete a template, you can use this command:
```
$ radix delete

? Which template you want to delete? myApp
┌───────────────────┬────────────────┬────────┐
│ Template Name     │ Owner/Name     │ Branch │
├───────────────────┼────────────────┼────────┤
│ MyApp2            │ your template  │ master  │
└───────────────────┴────────────────┴────────┘
✔ Template has been deleted successfully
```

# Template
The most important part of radix is `template`. All templates' information were list in the `templates.json`.


# License
MIT.
