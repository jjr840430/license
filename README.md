# [license](https://github.com/nishanths/license) 

[![wercker status](https://app.wercker.com/status/1407b8c71c720358bf15eeb5815f99bd/s "wercker status")](https://app.wercker.com/project/bykey/1407b8c71c720358bf15eeb5815f99bd)

Create licenses for your open-source projects from the command-line. *Hello, productivity!*

# What is license?

`license` is a license generator that works from the command-line. 

#### Features

* Supports all the licenses available on GitHub
* Does not need network access (except on first run)
* Always up-to-date with the licenses in GitHub's API
* Easy to customize the name, year, and output filename when needed


# Demo

<img src="https://zippy.gfycat.com/JoyfulBlandGermanshorthairedpointer.gif" width="700px"/>

# Install

#### Using go

````
$ go get github.com/nishanths/license
````

[More info](https://github.com/nishanths/license/wiki/Install-using-go)

#### Download

Alternatively, download the [binary](https://github.com/nishanths/license/wiki/Install-binaries) for your platform.

# Usage

#### Generating a license

To generate a license, simply run `license` followed by the license name. The following command generates the MIT license:

````bash
$ license mit
````

#### Creating a license file

Use the `-o` option to save the license to a file. For example, the following command creates the file `LICENSE.txt` with the contents of the ISC license:

````
$ license -o LICENSE.txt isc
```` 

More options and commands are described below.

# Options

#### Customize name and year on the license

By default, license uses the current year for the year on the generated license. To determine the name, license uses the following algorithm:

* First, it looks at provided command-line arguments
* If command-line args are absent, it looks at the environment variable `LICENSE_FULL_NAME`
* Finally, it uses the name from git config and mercurial config

You can explicitly specify the name and year to use:

````
$ license --name Alice --year 2013 mit
````


#### List available licenses

View the list of locally avaialable licenses by running:

````
$ license ls
````

The equivalent command to list remote licenses is:

````
$ license ls-remote
````

[Currently available list of licenses](https://github.com/nishanths/license/wiki/List-of-current-licenses)

#### Help

Help text is available by running `license --help`. [View help command output](https://github.com/nishanths/license/wiki/Help-output)

# Contributing

Pull requests for new features, bug fixes, and suggestions are welcome!

# License

Licensed under the [MIT License](https://github.com/nishanths/license/blob/master/LICENSE).

The license file in this repo was generated by this program :).
